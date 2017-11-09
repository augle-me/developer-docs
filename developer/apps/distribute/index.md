---
layout: 'doc'
sidebar: 'developer-apps'
id: 'distribute'
---

You can distribute models online using our web store either for free or for some cost.

To distribute your model you need to bundle you model in a `.arpk` file, To know more information about the `.arpk` file [read this](/developer#whatisarpk)

In this article we explain the following things

    1. Getting prepared for building `.arpk` file.

    2. Building `.arpk` file.

    3. Publishing `.arpk` file.

Overall aim of this this article is to make the `.arpk` file and make it ready to distribution (publish).

**\*\*Important** One `.arpk` file contains only one model. How to develop a model is not mentioned in this article, to know (Read this article)

## Preparing for .arpk file

<aside class="notice">git clone https://github.com/augle-me/augle-model-template </aside>

Once you clone the github project <https://github.com/augle-me/augle-model-template> you can jump to Build section. However, knowing more about how to prepare for building `.arpk` file will give you more flexibility while creating model. For that, you need to know few things.

    1. Directory structure and Important Files

    2. Required configuration

### Directory structure & Important files

Directory structure important, as we look for few important files identify the model. if your model does not stick to this format, you can't publish though our console.
One of the most important file is `manifest.json` in th root directory. which explains about the model.

```
model-project-folder/
 ├──assets/                 * [optional] assets files required for this model
 ├──manifest.json           * This will provide important information about the model
 ├──init.js                 * This file can be any with in the where in model-project-folder and have to refer this in manifest.json
```

Let's take a moment to explain what's is in the folder structure. `manifest.json` is the most important file without it model is unidentified while publishing. Few og the important things it will describe is Version code, Version, Main file to load, model configuration variables. To full list of properties that are available in the `manifest.json` is available here (Link to Apendiex)

{start-file}.json, this is file where the actual 3D model is programmed, this file can have any name, Examples: main.js or init.js or could be any thing. But reference to this file is exists in `manifest.json` *main* property

Example: **manifest.json** with init.js as main file

```
{
"main": "init.js"
}
```

With this 2 files, manifest.json and initial load file(init.js in out case), we are good to go to create `.arpk` file.

### Required Configuration

When you publish a model to market place you can publish numerous versions, and each version of model could differ in different ways, to identified the different version we need some configuration in the `manifest.json`.

Example basic configuration of manifest.json file.

```
{
    "main": "init.json",
    "verCode": 1,
    "version": "1.0.0"
}
```

Little explanation on the `manifest.json` properties.

`main`: tell which script to invoke to load the model. the value the property can be changed for a version

`verCode`: integer to identify the version this should be unique for each version, If you have a model, Car, you can have 1O version release to the same car with improved model. But each version must a unique `verCode` in it manifest.json

`version`: this is a string X.Y.Z for format there is no strict rules on this, but recommended is Semantic Versioning

There are more properties available in the `manifest.json` (Link to Apendiex).

Once you have a directory structure and files ready in place, you can move to the next step of building .arpk file

## Build .arpk file

>To know how to prepare for building `.arpk` file  [click here](#preparing-for-arpk-file)

At this point, you should already cloned the <https://github.com/augle-me/augle-model-seed> project, If not, execute the steps one by one

```
> git clone https://github.com/augle-me/augle-model-seed
> cd augle-model-seed
> npm install
```

```
> npm run build
```


Running above code build a `.arpk` file in the `dist` directory. This `.arpk` file is ready for publishing.

<aside class="warning"> Doing this will just create `.arpk` file, but developeing model with it is covered in another section. So, if you just cloning and running build, then it will have dummy model. Read, [How to creating model](/sad)</aside>

## Publish .arpk file

Once you have `.arpk` files build in previous step, then you are ready to publish.

For publishing you need to login into [Developer Portal](/developer/publish) and fillow the steps

    1. Create Listing

    2. Provide as much as information as you can listing.

    3. Go to Release Files Tab and upload the `.arpk` file you have generated

    4. Go to PRICING & DISTRIBUTION Tab and provide the details

    5. Publish

By doing all the above steps your model is published to the public.

If you are not happy with the model you have just published, you need to build another `.arpk` file. with new verCode and version, and do the build and then go to Release Files Tab and upload click upload new release to upload next version of the same model.

### Test you Package
### Move to production
## EARN