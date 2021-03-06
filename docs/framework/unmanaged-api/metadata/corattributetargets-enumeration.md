---
title: "CorAttributeTargets 枚举"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorAttributeTargets
api_location: mscoree.dll
api_type: COM
f1_keywords: CorAttributeTargets
helpviewer_keywords: CorAttributeTargets enumeration [.NET Framework metadata]
ms.assetid: 694c0fa0-7011-41a9-9dfd-f0e16ea574b5
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 4ce701c026b4e977c376b6e6f0f342b031634e38
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="corattributetargets-enumeration"></a>CorAttributeTargets 枚举
指定可应用属性的应用程序元素。  
  
## <a name="syntax"></a>语法  
  
```  
typedef enum CorAttributeTargets  
{  
    catAssembly            = 0x0001,  
    catModule              = 0x0002,  
    catClass               = 0x0004,  
    catStruct              = 0x0008,  
    catEnum                = 0x0010,  
    catConstructor         = 0x0020,  
    catMethod              = 0x0040,  
    catProperty            = 0x0080,  
    catField               = 0x0100,  
    catEvent               = 0x0200,  
    catInterface           = 0x0400,  
    catParameter           = 0x0800,  
    catDelegate            = 0x1000,  
    catGenericParameter    = 0x4000,  
  
    catAll                 =   
        catAssembly | catModule | catClass | catStruct |   
        catEnum | catConstructor | catMethod | catProperty |   
        catField | catEvent | catInterface | catParameter |   
        catDelegate | catGenericParameter,  
  
    catClassMembers        =   
        catClass | catStruct | catEnum | catConstructor |   
        catMethod | catProperty | catField | catEvent |   
        catDelegate | catInterface  
  
} CorAttributeTargets;  
```  
  
## <a name="members"></a>成员  
  
|成员|描述|  
|------------|-----------------|  
|`catAssembly`|特性可以应用于程序集。|  
|`catModule`|特性可以应用于可移植可执行文件 （.dll 或.exe） 模块。|  
|`catClass`|特性可以应用于类。|  
|`catStruct`|特性可以应用于结构;即，类型值。|  
|`catEnum`|特性可以应用于枚举。|  
|`catConstructor`|特性可以应用于构造函数。|  
|`catMethod`|特性可以应用于方法。|  
|`catProperty`|特性可以应用于属性。|  
|`catField`|特性可以应用于字段。|  
|`catEvent`|特性可以应用于事件。|  
|`catInterface`|特性可以应用于接口。|  
|`catParameter`|特性可以应用于参数。|  
|`catDelegate`|特性可以应用于委托。|  
|`catGenericParameter`|特性可以应用于泛型参数。|  
|`catAll`|特性可以应用于任何应用程序元素。|  
|`catClassMembers`|特性可以应用于类的成员。|  
  
## <a name="remarks"></a>备注  
 `CorAttributeTargets`枚举值可以组合与按位 OR 操作来获得首选的组合。  
  
 `CorAttributeTargets`便可与托管<xref:System.AttributeTargets?displayProperty=nameWithType>枚举。  
  
## <a name="requirements"></a>惠?  
 **平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** CorHdr.h  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅  
 [Metadata 枚举](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
