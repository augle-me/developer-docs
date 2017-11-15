---
layout: 'developer-doc'
sidebar: 'developer-apps'
id: 'develop'
title: 'Step by Step guide for integrating Admob ads'
---

#### Steps

This is in-depth step by step guide to integrate Admob ads to your Augle app. By the end of the guide
you should know how to integrate Admob Ad unit to Augle app. Depending on the knowledge you have on the Admob you can
skip few steps. For more understanding you can refer to [Video Tutorial](/developer/videos/).

There are 4 steps involved in integration.

1. Create Admob account
2. Create Ad unit which you want to prefer to display.
3. Add the ad unit to Augle Developer Console.
4. Integrate ad in your code.

#### Step 1: Create Admob account

If you already have an Admob account you can move on to next step 2. If not please proceed to
[Admob](https://www.google.co.in/admob/) website to create an Admob account.

#### Step 2: Create Ad unit for Augle usage

**This is important section.**{: .red-text} There is lot of documentation on the Admob website
on how to create the ad unit. But when you are creating an Ad unit to use with Augle Mobile app. You have to
do few thing differently then usual.

So, after creating Admob account.

![Admob, ADD APP](/assets/images/admob-add-app.jpg "Admob, ADD APP")
{: .fit-image}
Click, **ADD APP**{: .green-text}

In the search, enter Augle, and select an app name Augle(You might see two Apps with same name one for Android and
one for iOS. Please also look for Augle icon) to make sure you are selecting the Augle app. See
[things to know](#things-to-know) for more information on what app should be selected.

// Screen shots about selecting augle app

Once a app is created, click on creating ad unit. To what kind of app ad format you need please refer this

Once you create the ad unit get the ad unit id, you need this in the next step.

// Screen shot on getting the

#### Step 3: Add the ad unit to Augle Developer Console

Once you created the ad unit on Admob Website you have to use that ad unit id to create In-app ad items in the Augle
developer console.

> Prerequisites for adding the in-app ads to Augle app*
>
> 1. Go to Augle Developer Console. <br/>
   <a href="https://web.augle.me/developer/publish" class="btn">Augle Developer Console</a>
>
> 2. Create an Augle app.(We hope you already had an Augle app, If not, [Create an Augle app](/developer/apps/develop/) first.)
>
> 3. Click on the App in the list to open the app view.

Once you finished with the prerequisites. go to You app > Monetization tab > and navigate to In app ads.

You can see the form to add Admob ad unit.

![In-app ad, Adding form](/assets/images/in-app-ad-add-form.jpg "In-app ad, Adding form")
{: .fit-image}

Fill the form.

1. **In-app Ad Name:** this should be unique across your app and a alpha numeric characters with/without underscores.
No need to be same with your Admob name.**(Example: FIRST_AD)**

2. Admob ad unit Id. This the ad unit id you copied from the ad mob. **(Example: ca-app-pub-3940256099942544/6300978111)**

3. Ad Format, this should be same as Admob ad format. Augle only supports Banner and Rewarded Video formats for now.

4. Click the ADD IN-APP AD.

No the In-app Ad Name item will serve as reference to your Admob ad in Augle App you can refer it in your Augle app code
to display the ad, See the next step on to integrate an Admon ad in your code.


#### Final Step 4: Integrate ad in your code

Once you finished all the above steps, You can start using the the In-app ad you created in Step 3, go to your code Augle
app and include

```
    // This is to load add at the default position, which is TOP.

    Augle.loadAd('FIRST_AD')

    // Second argument to the `loadAd` takes the positions of the add to display

    Augle.loadAd('FIRST_AD', 'BOTTOM')
```

Now you have integrated your add mob add to your Augle app. When you deploy next version of your app throught augle
console you can see your app displaying the code.

**Alpha Release, will only display test ads that are provided in the Admob documentation. Only live apps load the your
actual Admob Ad units you have provided in Augle Developer Console.
{: .notice .important}

#### Things to know

The Augle app you develop is the Progressive Web app, So it is available in both Android and iOS version of Augle.

In Step 2, While creating the an App in Admob console, you have to create two Apps actually. One for Augle Android
App and one for Augle iOS app.

Then in Step 3 you will add the In-app Ad to Augle with different names `FIRST_AD_ANDROID` and `FIRST_AD_IOS`

Finally in Step 4, In your code you ask to display your app

```
    // This is to load add at the default position, which is TOP.
    if(Augle.getPlatform() === 'ios'){
        Augle.loadAd('FIRST_AD_IOS')
    }else if(Augle.getPlatform() === 'android'){
        Augle.loadAd('FIRST_AD_ANDROID')
    }
```

We hope this is all you need to know about the Admob - Augle Ad integration.

#### Also See

[Augle Ad display positions](augle-ad-display-positions.html)