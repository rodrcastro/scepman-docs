# Azure KeyVault

## AppConfig:KeyVaultConfig:RootCertificateConfig:AddExtendedKeyUsage

{% hint style="info" %}
Applicable to version 1.8 and above
{% endhint %}

**Value:** _true_ or _false_

**Description:** This setting determines whether SCEPman generates its CA certificates with an Extended Key Usage extension. The extension is not required by the standards, but Cisco ISE sometimes requires it to make OCSP work.

**True** (default for 1.9 and above): SCEPman adds an Extended Key Usage extension to newly generated CA certificates.

**False** (default for 1.8 and before): SCEPman generates a CA certificate without Extended Key Usage extension.

## AppConfig:KeyVaultConfig:RootCertificateConfig:DaysExpiresIn

The validity of the generated Root CA certificate in days. Defaults to 3650, i.e. about ten years. We recommend to not reduce this value, as this increases availability risks, with no security advantage -- stopping the distribution of the Root CA certificate is easy and much faster than waiting for the certificate expiration.

{% hint style="danger" %}
Changes can harm your service!
{% endhint %}

## AppConfig:KeyVaultConfig:RootCertificateConfig:KeySize

The length of the Root CA key in bits. Defaults to 2048.

{% hint style="danger" %}
Changes can harm your service!
{% endhint %}

## AppConfig:KeyVaultConfig:RootCertificateConfig:KeyType

The type of key created for the Root CA. _RSA_ is a software-protected RSA key; _RSA-HSM_ is HSM-protected. If you want to use an ECC key, please contact the SCEPman support for further instructions.

{% hint style="danger" %}
Changes can harm your service!
{% endhint %}

## AppConfig:KeyVaultConfig:KeyVaultURL

The Azure Key Vault URL. This setting is automatically configured during the setup.

This setting MUST be in the configuration of your App Service. It is NOT possible to define this setting as a Secret in Azure Key Vault!

{% hint style="danger" %}
Changes can harm your service!
{% endhint %}

## AppConfig:KeyVaultConfig:RootCertificateConfig:CertificateName

The Root Certificate Name. This setting is automatically configured during the setup.

The name does not appear in the certificate itself and is only a reference to the CA certificate within Azure Key Vault. As it is part of the URL, there are name restrictions, like limitations to alphanumeric characters, numbers, and dashes.

{% hint style="danger" %}
Changes can harm your service!
{% endhint %}

## AppConfig:KeyVaultConfig:RootCertificateConfig:Subject

The Root Certificate Subject. This setting is automatically configured during the setup. It is used only as input at the time of CA certificate creation and will not be used anyomre once a CA certificate exists.

{% hint style="danger" %}
Changes can harm your service!
{% endhint %}
