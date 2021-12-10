---
nav_title: Jebbit
article_title: Jebbit
page_order: 4
description: "Cet article décrit le partenariat entre Braze et Jebbit, un PaaS qui vous permet de passer des courriels et des attributs d'utilisateurs de vos campagnes Jebbit en tant que données utilisateur à Braze en temps réel."
alias: /fr/partners/jebbit/
page_type: partenaire
search_tag: Partenaire
---

# Jebbit

> [Jebbit](https://www.jebbit.com/) is a PaaS that allows you to build engaging experiences for users to capture first-party data.

The Braze and Jebbit integration lets you pass user emails and attributes from your Jebbit campaigns as user data to Braze in real-time. This data can then be used to drive marketing initiatives like personalized email campaigns and triggers.

## Prerequisites

| Requirement         | Description                                                                                                                                                                             |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Jebbit account      | A Jebbit account is required to take advantage of this partnership.                                                                                                                     |
| Braze REST API key  | A Braze REST API Key with all user data permissions. <br><br> This can be created within the __Braze Dashboard -> Developer Console -> REST API Key -> Create New API Key__ |
| Braze REST Endpoint | Your REST Endpoint URL. Your endpoint will depend on the Braze URL for [your instance](https://www.braze.com/docs/api/basics/#endpoints).                                               |
{: .reset-td-br-1 .reset-td-br-2}

## Integration

When requesting integrating with Jebbit, communicate if any hard deadlines need to be met. Additionally, ensure that you have the attributes mapped to your Jebbit experience(s) that you would like passed to Braze.

### Étape 1 : Fournir les identifiants API

Provide your API credentials to Jebbit in a text file via a Dropbox file request. Submit your file using the following [Dropbox URL](https://www.dropbox.com/request/RqKQHkJHXw1cFBKbXpZx).

### Étape 2 : Confirmer la soumission du test

A Jebbit engineer assigned to your integration will push through a test submission from Jebbit to Braze, so you can see how the data will look in your Braze environment. This is the final step in activating the integration. Now that your Jebbit data is set up, use it to drive your marketing initiatives.

{% alert note %}
The attribute ID you have set in Jebbit is how the attribute field name will be shown in Braze.
{% endalert %}

## Personnalisation

We currently support the [user data]({{site.baseurl}}/api/endpoints/user_data/) endpoints specifically, but requests for different endpoints can be supported. Attribute field names can also be customized to your preference.

If you want additional attributes from Jebbit in Braze, map the new attribute in your Jebbit account. The attribute will automatically show in Braze as you collect data for that attribute.