---
description: SCEPman - Certificates Simplified
---

# Welcome

{% hint style="warning" %}
Intune service discovery API endpoint will require specific permissions starting January 1st 2023. For more details, see the [Microsoft website](https://aka.ms/mem-servicediscovery-api-blog).

**SCEPman instances running versions prior to version 2.0 may have issues with this change.**&#x20;

Please ensure that you are using the [latest version of SCEPman](scepman-configuration/optional/update-strategy.md).
{% endhint %}

## Overview

SCEPman is a slim and resource-friendly solution to issue and validate certificates using SCEP. **It is an Azure Web App providing the SCEP protocol and works directly with the Microsoft Graph and Intune API.** SCEPman uses an Azure Key Vault based Root CA and certificate creation. No other component is involved, neither a database nor any other stateful storage except the Azure Key Vault itself. That said, SCEPman **will not need any backup procedures** or other operation level tasks. Only an Azure subscription is necessary to deploy it.

![SCEP flow with Microsoft Intune](.gitbook/assets/scepman-flowchart.webp)

The following documentation will show you a straightforward way to deploy certificates to modern cloud managed clients. Without any on-premises PKI your users and devices will be able to get certificates.

## SCEPman vs. Legacy PKI

If you are interested in learning more about the effort involved in installing and operating a legacy/on-premises PKI such as the Certificate Connector for Intune / Active Directory Certificate Services (ADCS) in comparison to SCEPman, please refer to below article.&#x20;

{% content-ref url="other/faqs/certificate-connector.md" %}
[certificate-connector.md](other/faqs/certificate-connector.md)
{% endcontent-ref %}

## Get more details about SCEPman

{% embed url="https://www.youtube.com/watch?v=kr8uBPlG4J8" %}
SCEPman 2.0 - What's new?
{% endembed %}

{% content-ref url="details.md" %}
[details.md](details.md)
{% endcontent-ref %}

{% content-ref url="editions.md" %}
[editions.md](editions.md)
{% endcontent-ref %}

## SCEPman Guides

We offer two guides to deploy the SCEPman environment. Please follow below link for guidance on which guide is best suited for your scenario and deployment requirements:

{% content-ref url="scepman-deployment/deployment-guides/" %}
[deployment-guides](scepman-deployment/deployment-guides/)
{% endcontent-ref %}

## Change Log

News from our development and our roadmap can be found under the **Change Log**.

{% content-ref url="changelog.md" %}
[changelog.md](changelog.md)
{% endcontent-ref %}
