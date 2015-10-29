<!--
title: "Introduction To The Contrast REST API"
description: "Overview of the REST API"
-->

There are two sets of **Contrast APIs**. The Contrast plugin uses its own set of APIs to send vulnerabilities and other application information to the Contrast site for you to view in our web interface. That set of APIs is subject to change at any time, uses *different keys*, and in general is more about writing data to your Contrast account. We call this set of APIs the **Engine APIs**.

This documentation is all about the set of APIs meant to read data by our end users - we call these the **User APIs**. You can use this set of APIs to get all the same vulnerability and application information available through the website, but delivered through a REST service instead. 

>**Note:** Unlike other REST services, we use the **PUT** method for all of our services for security purposes

## API Security

Services, like the rest of your Contrast experience, is only available over SSL. On top of that, there are two things needed by every API request: an **Authorization Token** and an **API Key**.

### Authorization Token

This value holds the *Base64-encoded* username and your user service key (**not** your password), separated by a colon.

To get your service key, click on your **Account Settings** dropdown and select **API Key**. This page will allow you to email yourself the key.

```AuthorizationToken = BASE64(<username>:<service_key>)```

This value goes into its own HTTP request header, **Authorization**.

### API Key

This value holds your organization's API key. You can get this value from the same API Key email, or from your Administrator. If you're the Administrator, you can see how to find and rotate this value in the **Admin Guide**. 

```APIKey = <org_service_key>```

This value will go into its own HTTP request header, **API Key**.

### Testing Your Credentials

Once you have your credentials and have encoded them properly, try issuing a simple *service call* with them. We suggest using **Burp**, **ZAP**, **WebScarab**, or other HTTP tools to verify your credentials before testing them. Any key mismatches or authentication issues (like locked accounts) will cause a ```401 error```.

## See Also

[Security API Keys](admin_tsconfigset.html#key)

[Get Your Monitored Applications](dev_api1.html#monitor)