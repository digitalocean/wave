This guide shows how to create a Knowledge Base (KB) and an Agent using DigitalOcean's GradientAI API via the `doctl` CLI.

## Prerequisites
- [doctl](https://github.com/digitalocean/doctl) CLI installed and authenticated
- [jq](https://stedolan.github.io/jq/) installed for JSON parsing
- DigitalOcean account
- Project ID and Embedding Model UUID

## Step-by-Step Instructions

### 1. Set Environment Variables

```sh
export PROJECT_ID="b398b02e-2bf4-45de-9175-89b92dc14794" 
export EMBEDDING_MODEL_UUID="22653204-79ed-11ef-bf8f-4e013e2ddde4"
export MODEL_ID="llama3.3-70b-instruct"
export REGION="tor1"
export KB_NAME="kb-AI"
export AGENT_NAME="Agent-AI"
export INSTRUCTION="You are an agent who has good understanding of Artificial Intelligence"
```

### 2. Create a Knowledge Base (KB)
This command creates a KB using a web crawler to ingest content from Wikipedia:
```sh
doctl genai knowledge-base create \
  --name "$KB_NAME" \
  --region "$REGION" \
  --project-id "$PROJECT_ID" \
  --embedding-model-uuid "$EMBEDDING_MODEL_UUID" \
  --data-sources '[{"web_crawler_data_source":{"base_url":"https://en.wikipedia.org/wiki/Artificial_intelligence","crawling_option":"SCOPED","embed_media": true}}]' \
  --output json | jq -r '.[0].uuid'
```
Save the output UUID for the next step (or assign it to a variable):
```sh
export KB_UUID=$(doctl genai knowledge-base create \
  --name "$KB_NAME" \
  --region "$REGION" \
  --project-id "$PROJECT_ID" \
  --embedding-model-uuid "$EMBEDDING_MODEL_UUID" \
  --data-sources '[{"web_crawler_data_source":{"base_url":"https://en.wikipedia.org/wiki/Artificial_intelligence","crawling_option":"SCOPED","embed_media": true}}]' \
  --output json | jq -r '.[0].uuid')
echo "Created KB: $KB_UUID"
```

### 3. Create an Agent and Attach the KB
This command creates an agent and attaches the KB you just created:
```sh
export AGENT_UUID=$(doctl genai agent create \
  --name "$AGENT_NAME" \
  --project-id "$PROJECT_ID" \
  --model-id "$MODEL_ID" \
  --region "$REGION" \
  --instruction "$INSTRUCTION" \
  --knowledge-base-id "$KB_UUID" \
  --output json | jq -r '.[0].uuid')
echo "Created Agent: $AGENT_UUID"
```

## Variables
- `PROJECT_ID`: DigitalOcean project UUID
- `EMBEDDING_MODEL_UUID`: The embedding model to use for the KB
- `MODEL_ID`: The LLM model for the agent (e.g., `llama3.3-70b-instruct`)
- `REGION`: DigitalOcean region (e.g., `tor1`)
- `KB_NAME`: Name for the knowledge base
- `AGENT_NAME`: Name for the agent
- `INSTRUCTION`: Instruction prompt for the agent
