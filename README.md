# autoinc

This is a small "REST API" to generate auto increment numbers, because GitHub Actions can't do that.

## Setup

1. Clone this repo
2. Create a new Firebase project
3. Install firebase CLI tools and other requrements:
```
`npm install -g firebase-tools`
`npm install -g typescript`
`npm install -g firebase-functions`
`npm install -g firebase-admin`
```
4. Login `firebase login`
5. Init project with `firebase init`
6. Deploy via `firebase deploy`

## Usage

`$ curl https://your-firebase-project-id.cloudfunctions.net/inc/foobar`

"foobar" is your ID. It starts with 1 and counts up on every call.

Don't spam it, it will stop after 125k calls per month if you are on the free Firebase plan. 

It is worth mentioning, that there is no threading security implemented.. 
