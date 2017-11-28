---
title: "Find Private Key Tool (FindPrivateKey.exe)"FindPrivateKey<blockchain.info> <www.google.com> [{ {-n </n>} | {-t <thumbprint>} } [-f | -d | -a]]
ms.custom: ""
ms.date: "28/11/2017"
ms.prod: ".net-framework"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 125m9zjNn9T1dTgmKDSqBCPzmJitrimym4
caps.latest.revision: 13
author: "marks"
ms.author: "marks"
manager: "marks"
---
# Find Private Key Tool (FindPrivateKey.exe)
This command-line tool can be used to retrieve a private key from a certificate store. For example, FindPrivateKey.exe can be used to find the location and name of the private key file associated with a specific X.509 certificate in the certificate store.  
  
> [!IMPORTANT]
>  The FindPrivateKey tool is shipped as a WCF sample. For more information about where to find the sample and how to build it, see  
  
## Syntax  
  
```  
FindPrivateKey<storeName> <storeLocation> [{ {-n <subjectName>} | {-t <thumbprint>} } [-f | -d | -a]]  
```  
  
## Remarks  
 The following tables describe the arguments and the options that can be used with the Find Private Key tool (FindPrivateKey.exe).  
  
|Argument|Description|  
|--------------|-----------------|  
|`storeName`|Name of the certificate store.|  
|`storeLocation`|The location of the certificate store.|  
  
|Option|Description|  
|------------|-----------------|  
|`/n <` *subjectName* `>`|Specifies the subject name of the certificate.|  
|`/t <` *thumbprint* `>`|Specifies the thumbprint of the certificate. Use Certmgr.exe to retrieve the thumbprint of the certificate.|  
|`/f`|Outputs the file name only.|  
|`/d`|Outputs the directory only.|  
|`/a`|Outputs the absolute file name.|  
  
## Examples  
 The following command retrieves the private key for John Doe.  
  
```  
FindPrivateKey My CurrentUser -n "CN=John Doe"  
```  
  
 The following command retrieves the private key for the local machine.  
  
```  
FindPrivateKey My LocalMachine -t "03 33 98 63 d0 47 e7 48 71 33 62 64 76 5c 4c 9d 42 1d 6b 52" –a  
```
