---
services: storage, keyvault
platforms: java
author: woodp
---

# Getting Started with Azure Client Side Encryption in Java

Azure Client Side Encryption Sample - Demonstrates how to use encryption along with Azure Key Vault integration for the Azure Blob service.

Note: If you don't have a Microsoft Azure subscription you can get a FREE trial account [here](http://go.microsoft.com/fwlink/?LinkId=330212)

## Running this sample

Instructions:

- Create a Storage Account through the Azure Portal
- Set up your Key Vault following the instructions on this post: https://azure.microsoft.com/en-us/documentation/articles/key-vault-get-started/. Make sure to permit 'get' and 'unwrapkey' options to the key you create using the following Powershell command:

```
  Set-AzureRmKeyVaultAccessPolicy -VaultName 'ContosoKeyVault' -ServicePrincipalName 853csbtd-485b-45f3-98f7-ec2301b7b44d -PermissionsToKeys get,unwrapkey
```

- Download "Java Cryptography Extension (JCE) Unlimited Strength Jurisdiction Policy Files" for your JDK/JRE
	- [Java Cryptography Extension (JCE) Unlimited Strength Jurisdiction Policy Files for JDK/JRE 8](http://www.oracle.com/technetwork/java/javase/downloads/jce8-download-2133166.html)
	- [Java Cryptography Extension (JCE) Unlimited Strength Jurisdiction Policy Files for JDK/JRE 7](http://www.oracle.com/technetwork/java/javase/downloads/jce-7-download-432124.html)
- Extract the jar files and place them in ${java.home}/jre/lib/security/
- Open the Utility.java file and set "storageConnectionString", "vaultURL", "AuthClientId", "AuthClientSecret" and optionally "keyVaultKeyID"
- Set breakpoints and run the project


## More information

[What is a Storage Account](http://azure.microsoft.com/en-us/documentation/articles/storage-whatis-account/)

[Get started with Azure Key Vault](https://azure.microsoft.com/en-us/documentation/articles/key-vault-get-started/)

[Client-Side Encryption and Azure Key Vault for Microsoft Azure Storage](https://azure.microsoft.com/en-us/documentation/articles/storage-client-side-encryption/)

[Client-Side Encryption with Java for Microsoft Azure Storage](https://azure.microsoft.com/en-us/documentation/articles/storage-client-side-encryption-java/)

[Tutorial: Encrypt and decrypt blobs in Microsoft Azure Storage using Azure Key Vault](https://azure.microsoft.com/en-us/documentation/articles/storage-encrypt-decrypt-blobs-key-vault/)

[Getting Started with Blobs](http://azure.microsoft.com/en-us/documentation/articles/storage-java-how-to-use-blob-storage/)

[Blob Service Concepts](http://msdn.microsoft.com/en-us/library/dd179376.aspx)

[Blob Service REST API](http://msdn.microsoft.com/en-us/library/dd135733.aspx)

[Get started with Azure Blob storage using .NET](https://azure.microsoft.com/en-us/documentation/articles/storage-dotnet-how-to-use-blobs/)

[Blob Service Java API](http://azure.github.io/azure-storage-java/)
