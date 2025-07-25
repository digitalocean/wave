<p align="center"><a href="https://devdojo.com/wave" target="_blank"><img src="https://cdn.devdojo.com/images/october2024/wave-logo.png" width="200"></a></p>

<p align="center">
<a href="https://github.com/thedevdojo/wave/actions"><img src="https://github.com/thedevdojo/wave/actions/workflows/tests.yml/badge.svg" alt="Build Status"></a>
<a href="https://github.com/thedevdojo/wave"><img src="https://img.shields.io/github/v/release/thedevdojo/wave" alt="Latest Stable Version"></a>
<a href="https://github.com/thedevdojo/wave"><img src="https://img.shields.io/badge/license-MIT-green" alt="License"></a>
<a href="https://herd.laravel.com/new?starter-kit=devdojo/wave"><img src="https://img.shields.io/badge/Install%20with%20Herd-f55247?logo=laravel&logoColor=white"></a>
</p>

Wave is a SaaS framework, built with <a href="https://laravel.com">Laravel</a>, that will make building your SaaS application fun and easier than ever before. <a href="https://devdojo.com/wave/docs" target="_blank">View the full docs here</a>.

Wave provides you with all the essential features found in many popular SaaS platforms, allowing you to quickly transform your idea into a profitable SaaS product. Here are a handful of features that Wave Provides:

 - <a href="https://devdojo.com/wave/docs/features/auth" target="_blank">Authentication</a>
 - <a href="https://devdojo.com/wave/docs/features/user-profiles" target="_blank">User Profiles</a>
 - <a href="https://devdojo.com/wave/docs/features/user-impersonations" target="_blank">User Impersonations</a>
 - <a href="https://devdojo.com/wave/docs/features/billing" target="_blank">Billing</a>
 - <a href="https://devdojo.com/wave/docs/features/subscription-plans" target="_blank">Subscription Plans</a>
 - <a href="https://devdojo.com/wave/docs/features/roles-permissions" target="_blank">Roles & Permissions</a>
 - <a href="https://devdojo.com/wave/docs/features/notifications" target="_blank">User Notifications</a>
 - <a href="https://devdojo.com/wave/docs/features/changelog" target="_blank">Changelog</a>
 - <a href="https://devdojo.com/wave/docs/features/blog" target="_blank">Blog</a>
 - <a href="https://devdojo.com/wave/docs/features/pages" target="_blank">Pages</a>
 - <a href="https://devdojo.com/wave/docs/features/api" target="_blank">API</a>
 - <a href="https://devdojo.com/wave/docs/features/admin" target="_blank">Admin</a>
 - <a href="https://devdojo.com/wave/docs/features/themes" target="_blank">Themes</a>
 - <a href="https://devdojo.com/wave/docs/features/plugins" target="_blank">Plugins</a>

Be sure to view a list of <a href="https://devdojo.com/wave/docs/features/auth" target="_blank">all features here</a>.

## Demo

You can view a <a href="https://devdojo.com/wave/demo" target="_blank">live demo here</a>, which will also allow you to preview all the <a href="https://devdojo.com/wave/themes" target="_blank">available themes</a>.

<a href="https://devdojo.com/wave/demo" target="_blank"><img src="https://cdn.devdojo.com/images/august2024/wave-anchor-theme.jpeg"></a>

## 🚀 Deploy to DigitalOcean App Platform

You can easily deploy Wave to [DigitalOcean App Platform](https://www.digitalocean.com/products/app-platform/) with just a few clicks. All you need is a [DigitalOcean account](https://cloud.digitalocean.com/registrations/new).

### 1. Deploying the Application

Click this button to deploy the app to the DigitalOcean App Platform. If you are not logged in, you will be prompted to log in with your DigitalOcean account.

<a href="https://cloud.digitalocean.com/apps/new?repo=https://github.com/digitalocean/wave/tree/main" target="_blank"><img src="https://www.deploytodo.com/do-btn-blue.svg" width="240" alt="Deploy to DO"></a>

> Using this button disables the ability to automatically re-deploy your app when pushing to a branch or tag in your repository as you are using this repo directly. If you want to automatically re-deploy your app, fork the GitHub repository to your account so that you have a copy of it stored to the cloud. Click the Fork button in the GitHub repository and follow the on-screen instructions.

After forking the repo, you should now be viewing this README in your own GitHub org (e.g. **https://github.com/< your-org >/wave**). To deploy the new repo, visit https://cloud.digitalocean.com/apps and click Create App. Then, click GitHub, select the repository you created and select the main branch.


### 2. Configure Your App

Once you're in the DigitalOcean Control Panel:

* You can **leave all default settings as-is** if you're just testing.
* For production or heavier workloads, consider adjusting:

  * **Component size** (e.g., Basic vs. Professional)
  * **Number of containers**
  * **Environment variables and secrets**
  * **Database settings** (if you want to use a managed database)
  * **Custom domain** (optional, but recommended for production)

### 3. Initial Build and Database Setup

* The initial build will take a bit longer because it also provisions a **development PostgreSQL database**.
* This dev database is perfect for testing or staging.
* For production deployments, we recommend setting up a **Managed PostgreSQL Database** via DigitalOcean and attaching it to your app along with adjusting any necessary environment variables.

### 4. Seed the Database (First-Time Only)

After deployment is complete:

1. Open the App Platform **Console Shell** from your dashboard.
2. Run the following command:

   ```bash
   php artisan db:seed
   ```

This step is required **only on the first deploy** to populate your database with default data. Future deployments will work automatically as you push changes to the `main` branch.

## Installation

There are two ways to install Wave, you can install it via the automated installer or manually.

Click here to <a href="https://devdojo.com/wave/docs/install" target="_blank">view the full installation instructions</a>.

## Agent Setup

For step-by-step instructions on how to create a Knowledge Base (KB) and an Agent using `doctl` CLI, please refer to the [agent/README.md](agent/README.md) guide.

## Support the Project

The best way to support this project is to support us by subscribing to a <a href="https://devdojo.com/pro">DevDojo Pro</a> account. This will give you access to <a href="https://devdojo.com/wave/pro">premium content</a> to help you build your SaaS even quicker. Also, make sure to tell your friends and <a href="https://github.com/thedevdojo/wave/compare" target="_blank">submit a PR</a> if you want to contribute.

We've also got a full video series on how you can setup, build, and configure Wave. 🍿 You can watch first few videos for free, and additional videos will require a [DevDojo Pro](https://devdojo.com/wave/pro) subscription. By subscribing to a [DevDojo Pro](https://devdojo.com/pro) subscription you will also be supporting the ongoing development of this project. It's a win win! 🙌

[Click here to watch the Wave Video Course](https://devdojo.com/wave/videos).


## Documentation

Checkout the [official documentation here](https://devdojo.com/wave/docs).

## Sponsors

Wave is proudly supported by our amazing sponsors. A big thank you to:

[![DigitalOcean Referral Badge](https://web-platforms.sfo2.cdn.digitaloceanspaces.com/WWW/Badge%203.svg)](https://www.digitalocean.com/?refcode=dc19b9819d06&utm_campaign=Referral_Invite&utm_medium=Referral_Program&utm_source=badge)
