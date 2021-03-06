---
title: Search Console integration
--- 

import useBaseUrl from '@docusaurus/useBaseUrl';

In 2012, [Google stopped including](https://webmasters.googleblog.com/2012/03/upcoming-changes-in-googles-http.html) search terms in the `Referer` header when people click through a Google search. They only send Google as the referrer source instead. This means that Plausible Analytics cannot automatically access search terms that lead users to your website.

However, you can still access your search terms by setting up your website on Google Search Console. Once you’ve done that, you can enable the Google Search Console integration in Plausible Analytics to get all of your important search results stats under one roof.

_Note that we don’t yet have an integration with Bing Webmaster Tools. You can track the status of the integration [here](https://plausible.nolt.io/26)._

Here’s how you can add your site to Google Search Console and then integrate the Search Console data into your Plausible Analytics dashboard:

## Add your site to the Google Search Console

_If your site is already set up on Google Search Console, you can skip to the "**[Allow Plausible Analytics to access your Search Console](#allow-plausible-analytics-to-access-your-search-console)**" step._

Head over to [Google Search Console](https://search.google.com/search-console/) and click on the "**Start now**" button. If you don’t have any sites set up on Google Search Console already, you will be taken straight to the form to add a new domain. Otherwise, you can open the drop down on the top left and select "**Add property**".

You can either create a domain property or a URL prefix property on Google Search Console. Check out [their documentation](https://support.google.com/webmasters/answer/34592?hl=en) to understand the difference between these options. Plausible Analytics works with both options, so it’s completely up to you.

<img alt="Plausible Analytics" src={useBaseUrl('img/select-property-type.png')} />

## Verify your ownership of the website

You should see several options to verify to Google that you do indeed own this website. You’ll either need to be able to add HTML to your site or alternatively, you can add a DNS record to verify your ownership.

Follow the provided instructions depending on which verification method you’ve chosen. Once you’ve successfully verified the site, head back to the Plausible Analytics website.

<img alt="Plausible Analytics" src={useBaseUrl('img/verify-ownership.png')} />

## Allow Plausible Analytics to access your Search Console

Open the settings for your website on [your Plausible Analytics account](https://plausible.io/sites). Scroll down to the settings section called "**Google Integration**":

Clicking on the "**Continue with Google**" button will take you through to Google’s authentication flow to get the necessary permissions.

<img alt="Continue with Google" src={useBaseUrl('img/continue-with-google.png')} />

Choose your Google account to continue with the authentication. Google will share your name, email address, language preference and profile picture with Plausible Analytics. We've set it so we get the absolutely minimum amount of information possible that Google allows us. 

We really only need and use the email address from this. Email address is useful because some Plausible Analytics users have multiple Google accounts so we can remember which one is integrated with the Plausible Analytics site.

<img alt="Choose your Google account" src={useBaseUrl('img/choose-google-account.png')} />

You also need to grant Plausible Analytics a permission to view your Search Console website data.

<img alt="Grant Plausible Analytics a permission to view your Search Console website data" src={useBaseUrl('img/grant-permission.png')} />

And you also need to confirm all these choices once again.

<img alt="Confirm all the choices once again" src={useBaseUrl('img/confirm-choices.png')} />

## Select property to pull keywords from

Next up, you are back in Plausible Analytics settings where you should see a select box where you can choose which property from Google Search Console to integrate your Plausible Analytics dashboard with. Properties that start with `sc-domain:` represent domain properties and others are URL prefix properties in Search Console.

Once you’ve selected your property, click on the "**Save**" button. At that point, the integration should be fully functional.

<img alt="Choose which property from Google Search Console to integrate with" src={useBaseUrl('img/choose-property.png')} />

## Check your search query data in Plausible Analytics

Look at your site’s "**Top Referrers**" stats in your Plausible Analytics dashboard, click on "**Google**" in the referrers list, and you should see the keywords coming through.

<img alt="Google search query data in Plausible Analytics" src={useBaseUrl('img/google-search-query-referrers.png')} />

### I don't see Google search query data in my dashboard

Search query data is not live. It is delayed by approximately 24-36 hours even on Google Search Console itself. 

So if you go back two days in your Plausible Analytics dashboard and click on Google in the referral sources you should be able to see the search queries for that day. We get the search query data directly from Google Search Console so as soon as they show up there they show up in Plausible Analytics too.

### Search query number doesn't add up to the total number of Google visitors

Google samples its keyword data heavily. The sampling is why your keyword visitor numbers don’t add up to the total number of visitors from Google. Unfortunately, there’s nothing we can do about the quality of the keyword data. We show exactly the same data that you see in your Search Console.

## Plausible Analytics will be listed in your Google account settings

You can always view your Plausible Analytics integration in your Google account within the section "**Third-party apps with account access**". Here's how it looks like.

<img alt="Third-party apps with account access" src={useBaseUrl('img/third-party-apps.png')} />

## Remove the Google Search Console integration

If you'd like to remove the Google Search Console integration, click on the "**Unlink Google account**" button in the "**Google Integration**" section of your website settings.
