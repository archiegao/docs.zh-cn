---
title: "&lt;clientCredentials&gt; 的 &lt;windows&gt; 元素"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 793e41c2-31ea-4159-abbc-2123bf097233
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 6687f93be26dedcb34f08770708c072742fdd4de
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="ltwindowsgt-of-ltclientcredentialsgt-element"></a>&lt;clientCredentials&gt; 的 &lt;windows&gt; 元素
指定用于表示客户端的 Windows 凭据的设置。  
  
 \<系统。ServiceModel >  
\<行为 >  
\<endpointBehaviors >  
\<行为 >  
\<c a t e >  
\<windows >  
  
## <a name="syntax"></a>语法  
  
```xml  
<windows   
    allowedImpersonationLevel="Identification/Impersonation/Delegation/Anonymous/None"  
        allowNtlm="Boolean"  
/>  
```  
  
## <a name="attributes-and-elements"></a>特性和元素  
 下列各节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
  
|特性|描述|  
|---------------|-----------------|  
|`allowedImpersonationLevel`|设置客户端用于与服务器进行通信的模拟首选项。 服务器上不强制使用客户端所选择的模拟模式。 包括以下有效值：<br /><br /> -Identification： 服务器可以获取的标识和权限的客户端，但不能模拟客户端。<br />-模拟： 服务器可以模拟客户端的本地系统上的安全上下文。<br />-Delegation： 服务器可以模拟在远程系统上的客户端的安全上下文。<br />-Anonymous： 服务器无法模拟或标识客户端。<br />-None： 模拟级别未分配。<br /><br /> 默认值为 Identification。 此属性的类型为 <xref:System.Security.Principal.TokenImpersonationLevel>。|  
|`allowNtlm`|如果 Kerberos 不可用，则将此属性设置为 `true` 可令身份验证降级到 NTLM。<br /><br /> 如果使用 NTLM，则将此属性设置为 `false` 将导致 [!INCLUDE[indigo1](../../../../../includes/indigo1-md.md)] 尽最大努力引发异常。 请注意，将此属性设置为 `false` 可能不阻止通过网络发送 NTLM 凭据。|  
  
### <a name="child-elements"></a>子元素  
 无。  
  
### <a name="parent-elements"></a>父元素  
  
|元素|描述|  
|-------------|-----------------|  
|[\<c a t e >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)|指定用于向服务证明客户端身份的凭据。|  
  
## <a name="see-also"></a>请参阅  
 <xref:System.ServiceModel.Configuration.WindowsClientElement>  
 <xref:System.ServiceModel.Configuration.ClientCredentialsElement>  
 <xref:System.ServiceModel.Description.ClientCredentials>  
 <xref:System.ServiceModel.Configuration.ClientCredentialsElement.Windows%2A>  
 <xref:System.ServiceModel.Description.ClientCredentials>  
 <xref:System.ServiceModel.Description.ClientCredentials.Windows%2A>  
 <xref:System.ServiceModel.Security.WindowsClientCredential>  
 [保护客户端](../../../../../docs/framework/wcf/securing-clients.md)  
 [使用证书](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)  
 [保护服务和客户端的安全](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
