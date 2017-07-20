---
layout: 'doc'
sidebar: 'apps'
---

# Get started in 5 Steps using `Hello, world!` example

## Step 1 - Get the app sample template

Clone project to the your local machine `https://github.com/augle-me/augle-model-seed`

Use your favorite IDE to open and edit files

```
Please refer to app policy to know further
```
```
Know about prerequisite softwored before you want to build the app
```
<hr>
## Step 2 - Change `modelId`

Open Manifest.json file

Enter model ID
```
{
	"main": "./model/init.js",
	"verCode": 0,
	"version": "1.0.0",
	"modelId": "com.example"
}
```
Example, change `modelId: "com.example"` to what your preferred model id

<hr>
## Step 3 - Build Locally

Run
```
npm install
npm run build
```
To build a package and check for release.arpk file

<hr>
## Step 4 - Create Listing in developer console

Go to https://www.augle.me/developer/publish

Click Create listing.

Fill in all the required fields.

Then upload the `release.arpk` you have generated in Step 3.

Click Publish

<hr>
## Step 5 - Test you app through augle mobile app.

Open you Augle Mobile app. Android or iOS.

Login into with developer email account

Click, View my apps in side navigation.

You can see all you apps, along with the one you have published now.

## What's next

Go to [Develop](/developer-docs/apps/develop) Section to know more about building complex apps.