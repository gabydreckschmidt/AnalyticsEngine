---

copyright:
  years: 2017
lastupdated: "2017-11-02"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Retrieving IAM access tokens

## Pre-requisites

a. You must have a valid IBM ID.

b. Download and install the [{{site.data.keyword.Bluemix_notm}} CLI](https://console.bluemix.net/docs/cli/reference/bluemix_cli/all_versions.html#bluemix-cli-installer-downloads).

### Step 1: Log into the {{site.data.keyword.Bluemix_notm}} CLI.

```
bx api https://api.ng.bluemix.net
bx login
<enter your credentials>

<If you are part of multiple {{site.data.keyword.Bluemix_notm}} accounts, you'll be asked to choose an account for the current session. Also, you'll need to choose an organization and space in {{site.data.keyword.Bluemix_notm}}.>
```

### Step 2: Fetch the IAM access token.

```
bx iam oauth-tokens
```

Two tokens will be produced: one named `IAM token` and the other one named `UAA token`. Use `IAM token` for making cluster management REST API calls and `UAA token` to programmatically provision an instance of the IBM Analytics Engine service.
