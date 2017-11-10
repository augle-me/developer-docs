---
layout: 'developer-doc'
sidebar: 'developer-apps'
breadcrumb: Get started
id: 'getting-started'
title: Get started in 5 Steps using <strong>Hello, world!</strong> example
---
#### Step 1 - Get the app sample template

Clone project to the your local machine `https://github.com/augle/augle-app-seed`

Use your favorite IDE to open and edit files
```
Know about prerequisite softwore before you want to build the app
```
#### Step 2 - Change `modelId`

Open Manifest.json file

Enter model ID
```
{
	"main": "index.html",
	"verCode": 1,
	"version": "0.1.0",
	"modelId": "com.example.apps.sampleapp"
}
```
Example, change `modelId: "com.example.apps.sampleapp"` to what your preferred model id

#### Step 3 - Build Locally

Run
```
npm install
npm run build

or

yarn install
yarn run build

```
To build a package and check for release.arpk file
#### Step 4 - Create Listing in developer console

Go to https://www.augle.me/developer/publish

Click Create listing.

Fill in all the required fields.

Then upload the `release.arpk` you have generated in Step 3.

Click Publish

#### Step 5 - Test and distribute your app

Open you Augle Mobile app. Android or iOS.

Login into with developer email account

Click, View my apps in side navigation.

You can see all you apps, along with the one you have published now.

#### What's next

Go to [Develop](/developer/apps/develop) Section to know more about building complex apps.