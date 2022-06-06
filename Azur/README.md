# Azure Blob Storage

## Introduction
One of the main services provided with Azure is Cloud Storage. This allows us to store different artifacts in the Cloud. These include Tables, Queues, Files, and Containers. Containers are used to store Blobs which can be any type of file including text files, image files, video files, etc.

## About Blob storage

Blob storage is designed for:

- Serving images or documents directly to a browser.
- Storing files for distributed access.
- Streaming video and audio.
- Writing to log files.
- Storing data for backup and restore, disaster recovery, and archiving.
- Storing data for analysis by an on-premises or Azure-hosted service.

## Storage accounts
A storage account provides a unique namespace in Azure for your data. Every object that you store in Azure Storage has an address that includes your unique account name. The combination of the account name and the Blob Storage endpoint forms the base address for the objects in your storage account.

## Type of storage account
 - General-purpose v2 : Standard storage account type for blobs, file shares, queues, and tables. Recommended for most scenarios using Blob Storage or one of the other Azure Storage services.

 - Block blob : Premium storage account type for block blobs and append blobs. Recommended for scenarios with high transaction rates or that use smaller objects or require consistently low storage latency.

 - Page blob : Premium storage account type for page blobs only.

 ## Setup Azure Blob Storage

 In order to setup Azure Blob Storage as a state store, you will need the following properties:

1. **accountName** : The storage account name. For example: mystorageaccount.
2. **accountKey** : Primary or secondary storage account key.
3. **containerName** : The name of the container to be used for Dapr state. The container will be created for you if it doesn’t exist.

 ## Authenticating with Azure AD

This component supports authentication with Azure AD as an alternative to use account keys. Whenever possible, it is recommended that you use Azure AD for authentication in production systems, to take advantage of better security, fine-tuned access control, and the ability to use managed identities for apps running on Azure.

## Apply the configuration

**In Kubernetes**
To apply Azure Blob Storage state store to Kubernetes, use the kubectl CLI:
```
kubectl apply -f azureblob.yaml
```

**Running locally**

To run locally, create a components dir containing the YAML file and provide the path to the dapr run command with the flag --components-path.

This state store creates a blob file in the container and puts raw state inside it.

For example, the following operation coming from service called myservice:
```
curl -X POST http://localhost:3500/v1.0/state \
  -H "Content-Type: application/json"
  -d '[
        {
          "key": "nihilus",
          "value": "darth"
        }
      ]'
```

## Azure Storage

The Azure Storage platform is Microsoft's cloud storage solution for modern data storage scenarios. Azure Storage offers highly available, massively scalable, durable, and secure storage for a variety of data objects in the cloud. Azure Storage data objects are accessible from anywhere in the world over HTTP or HTTPS via a REST API. 

## Benefits of Azure Storage

****Durable** and highly available. Redundancy ensures that your data is safe in the event of transient hardware failures. You can also opt to replicate data across data centers or geographical regions for additional protection from local catastrophe or natural disaster. Data replicated in this way remains highly available in the event of an unexpected outage.

**Secure**. All data written to an Azure storage account is encrypted by the service. Azure Storage provides you with fine-grained control over who has access to your data.

**Scalable**. Azure Storage is designed to be massively scalable to meet the data storage and performance needs of today's applications.
Managed. Azure handles hardware maintenance, updates, and critical issues for you.

**Accessible**. Data in Azure Storage is accessible from anywhere in the world over HTTP or HTTPS. Microsoft provides client libraries for Azure Storage in a variety of languages, including .NET, Java, Node.js, Python, PHP, Ruby, Go, and others, as well as a mature REST API. Azure Storage supports scripting in Azure PowerShell or Azure CLI. And the Azure portal and Azure Storage Explorer offer easy visual solutions for working with your data.

## Azure Storage data services

**Azure Blobs**: A massively scalable object store for text and binary data. Also includes support for big data analytics through Data Lake Storage Gen2.

**Azure Files**: Managed file shares for cloud or on-premises deployments.

**Azure Queues**: A messaging store for reliable messaging between application components.

**Azure Tables**: A NoSQL store for schemaless storage of structured data.

**Azure** Disks: Block-level storage volumes for Azure VMs.

