# Dreamhouse Lightning Web Components Sample Application

[![Github Workflow](<https://github.com/dreamhouseapp/dreamhouse-lwc/workflows/Salesforce%20DX%20(scratch%20org)/badge.svg?branch=master>)](https://github.com/dreamhouseapp/dreamhouse-lwc/actions?query=workflow%3A%22Salesforce+DX+%28scratch+org%29%22) [![Github Workflow](<https://github.com/dreamhouseapp/dreamhouse-lwc/workflows/Salesforce%20DX%20(packaging)/badge.svg?branch=master>)](https://github.com/dreamhouseapp/dreamhouse-lwc/actions?query=workflow%3A%22Salesforce+DX+%28packaging%29%22)

> IMPORTANT: This is the new Lightning Web Components version of the Dreamhouse sample application. If you are looking for the Aura version, click [here](https://github.com/dreamhouseapp/dreamhouse-sfdx).

![dreamhouse-logo](dreamhouse-logo.png)

DreamHouse is a sample application that demonstrates the unique value proposition of the Salesforce platform for building Employee Productivity and Customer Engagement apps.

> This sample application is designed to run on Salesforce Platform. If you want to experience Lightning Web Components on any platform, please visit https://lwc.dev, and try out our Lightning Web Components sample application [LWC Recipes OSS](https://github.com/trailheadapps/lwc-recipes-oss).

## Installation Instructions

There are two ways to install Dreamhouse:

-   [Using a Scratch Org](#installing-dreamhouse-using-a-scratch-org): This is the recommended installation option. Use this option if you are a developer who wants to experience the app and the code.
-   [Using an Unlocked Package](#installing-dreamhouse-using-an-unlocked-package): This option allows anybody to experience the sample app without installing a local development environment.

## Installing Dreamhouse using a Scratch Org

1. Set up your environment. Follow the steps in the [Quick Start: Lightning Web Components](https://trailhead.salesforce.com/content/learn/projects/quick-start-lightning-web-components/) Trailhead project. The steps include:

-   Enable Dev Hub in your Trailhead Playground
-   Install Salesforce CLI
-   Install Visual Studio Code
-   Install the Visual Studio Code Salesforce extensions, including the Lightning Web Components extension

2. If you haven't already done so, authenticate with your hub org and provide it with an alias (**myhuborg** in the command below):

```
sfdx force:auth:web:login -d -a myhuborg
```

3. Clone this repository:

```
git clone https://github.com/dreamhouseapp/dreamhouse-lwc
cd dreamhouse-lwc
```

4. Create a scratch org and provide it with an alias (**dreamhouse** in the command below):

```
sfdx force:org:create -s -f config/project-scratch-def.json -a dreamhouse
```

5. Push the app to your scratch org:

```
sfdx force:source:push
```

6. Assign the **dreamhouse** permission set to the default user:

```
sfdx force:user:permset:assign -n dreamhouse
```

7. Import sample data:

```
sfdx force:data:tree:import --plan data/sample-data.json
```

8. Open the scratch org:

```
sfdx force:org:open
```

9. In **Setup**, under **Themes and Branding**, activate the **Lightning Lite** theme.

10. In App Launcher, select the **Dreamhouse** app.

## Installing Dreamhouse using an Unlocked Package

1. [Sign up](https://developer.salesforce.com/signup) for a Developer Edition (DE) org.

2. Enable MyDomain in your DE org. Instructions to do this are [here](https://trailhead.salesforce.com/modules/identity_login/units/identity_login_my_domain).

3. Click [this link](https://login.salesforce.com/packaging/installPackage.apexp?p0=04tB0000000OE9wIAG) to install the Dreamhouse unlocked package in your DE org.

4. Select **Install for All Users**

5. In App Launcher, select the Dreamhouse app.

6. Click the **Settings** tab and click the **Import Data** button in the **Sample Data Import** component.

7. In **Setup**, under **Themes and Branding**, activate the **Lightning Lite** theme.

8. In App Launcher, select the **Dreamhouse** app.

## Sample Data Import

Properties inserted using the Salesforce CLI will appear as listed on TODAY() - 10 days. If you want to have this value randomized, perform the data import from the app Settings tab instead.

## Optional Installation Instructions

This repository contains several files that are relevant if you want to integrate modern web development tooling to your Salesforce development processes, or to your continuous integration/continuous deployment processes.
