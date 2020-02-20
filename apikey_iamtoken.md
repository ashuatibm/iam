---

copyright:
  years: 2018, 2020
lastupdated: "2020-02-18"

keywords: IAM token, token, API key, generate token, access token, temporary credential

subcollection: iam


---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:help: data-hd-content-type='help'} 
{:support: data-reuse='support'}

# Generating an {{site.data.keyword.Bluemix_notm}} IAM token by using an API key
{: #iamtoken_from_apikey}
{: help} 
{: support}

Generate an {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) token by using either your IAM API key or a service ID's API key. {{site.data.keyword.Bluemix_notm}} APIs can be accessed only by users who are authorized by an assigned IAM role. Each user who is calling the API must pass credentials for the API to authenticate.
{:shortdesc}

You can generate an IAM token by using either your [{{site.data.keyword.Bluemix_notm}} API key](/docs/iam?topic=iam-userapikey#userapikey) or a [service ID's API key](/docs/iam?topic=iam-serviceidapikeys#serviceidapikeys). The API key is a permanent credential that can be reused if you don't lose the API key value or delete the API key in the account. This process is also used if you are developing an application that needs to work with other {{site.data.keyword.Bluemix_notm}} services. You must use a service ID API key to get an access token to be passed to each of the {{site.data.keyword.Bluemix_notm}} services.

An access token is a temporary credential that expires after one hour. After the acquired token expires, you must generate a new token to continue calling {{site.data.keyword.Bluemix_notm}} or service APIs, and you can perform only actions that are allowed by your level of assigned access within an account.
{: note}

Use the following `curl` command to generate an IAM token by using an API key.

### POST /identity/token
{: #post_id_token}

### Headers
{: #header}

  - Content-Type: application/x-www-form-urlencoded
  - Accept: application/json


### Parameters
{: #parameters}

  - grant_type=urn:ibm:params:oauth:grant-type:apikey
  - apikey=*[API key]*

```
curl -k -X POST \
  --header "Content-Type: application/x-www-form-urlencoded" \
  --header "Accept: application/json" \
  --data-urlencode "grant_type=urn:ibm:params:oauth:grant-type:apikey" \
  --data-urlencode "apikey=<apikey>" \
  "https://iam.cloud.ibm.com/identity/token"
```
{: codeblock}

The following sample is the expected response:

### Response
{: #response}

```
{
  "access_token": "eyJhbGciOiJIUz......sgrKIi8hdFs",
  "refresh_token": "SPrXw5tBE3......KBQ+luWQVY=",
  "token_type": "Bearer",
  "expires_in": 3600,
  "expiration": 1473188353
}
```
{: codeblock}

An IAM token is valid for 60 minutes, and it is subject to change. When a token expires, you must generate a new one.
{: note}
