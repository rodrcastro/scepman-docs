# Logging

{% hint style="info" %}
Applicable to version 2.4 and above
{% endhint %}

## AppConfig:LoggingConfig:WorkspaceId

**Value:** Guid

**Description:**

The WorkspaceID of your Log Analytics Workspace (shown in the Overview of the workspace). This is a required setting if you want to use Azure Monitor, together with SharedKey.

## AppConfig:LoggingConfig:SharedKey

**Value:** String

**Description:**

Use one of the two keys for the Log Analytics Workspace. They are displayed if you access the Log Analytics Workspace on portal.azure.com and navigate to Settings/Agents, where you can unfold the "Log Analytics agent instructions" section. Use either the Primary or the Secondary key.

This is a required setting if you want to use Azure Monitor, together with WorkspaceId.

## AppConfig:LoggingConfig:AzureOfferingDomain

**Value:** String

**Description:**

If the workspace is not in the Global Azure Cloud, you can configure the offering domain here. The default is 'azure.com'.

{% hint style="danger" %}
Changes can harm your service!
{% endhint %}

## AppConfig:LoggingConfig:LogLevel

**Value:** Trace, Debug, Info, Warn, Error, Fatal

**Description:**

The minimum log level to be logged. The default is 'Info'. Only log entries with a log level equal or higher than the configured log level will be logged.

Note that if you configure this setting to 'Trace' or 'Debug', log output might contain personal data like UPNs or IP addresses of users. If you want to avoid personal data in the log output, you should configure this setting to 'Info' or higher.