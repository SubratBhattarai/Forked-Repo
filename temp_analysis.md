## What triggers this workflow to run?
Any changes made to on branch which in my case is main will trigger the workflow to run.
on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

## What are the four main steps this workflow performs?
1. name: Checkout code
2. name: Validate HTML
3. name: Check links
4. name: Upload artifact

## What does "Checkout code" do?
The checkout downloads the repo code into the action environment which is necessary because other workflow steps need the access to it before testing and deploying.

## What is the purpose of the environment configuration?
It sets up the required access and permissions for deployment

## How does this automated deployment improve reliability compared to manual deployment?
Because the same tests and deployments are ran again and again making human mistakes less while also making sure the website passes the required checks before deploying.
 

## What would happen if you pushed code to a different branch (not main)?

The trigger only happens in main as told from 'on:' which means that any changes to other branch will be saved but not be in effect. 