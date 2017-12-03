---
title: "EContextType 枚举"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: EContextType
api_location: mscoree.dll
api_type: COM
f1_keywords: EContextType
helpviewer_keywords: EContextType enumeration [.NET Framework hosting]
ms.assetid: 92b926a9-b87e-408a-9036-df7b752c9492
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 73e6e9a1f1118a524b86b3711c0c7a6af4777f2d
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="econtexttype-enumeration"></a><span data-ttu-id="de83b-102">EContextType 枚举</span><span class="sxs-lookup"><span data-stu-id="de83b-102">EContextType Enumeration</span></span>
<span data-ttu-id="de83b-103">描述当前正在执行的线程的安全上下文。</span><span class="sxs-lookup"><span data-stu-id="de83b-103">Describes the security context of the currently executing thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="de83b-104">语法</span><span class="sxs-lookup"><span data-stu-id="de83b-104">Syntax</span></span>  
  
```  
typedef enum {  
    eCurrentContext    = 0x00,  
    eRestrictedContext = 0x01  
} EContextType;  
```  
  
## <a name="members"></a><span data-ttu-id="de83b-105">成员</span><span class="sxs-lookup"><span data-stu-id="de83b-105">Members</span></span>  
  
|<span data-ttu-id="de83b-106">成员</span><span class="sxs-lookup"><span data-stu-id="de83b-106">Member</span></span>|<span data-ttu-id="de83b-107">描述</span><span class="sxs-lookup"><span data-stu-id="de83b-107">Description</span></span>|  
|------------|-----------------|  
|`eCurrentContext`|<span data-ttu-id="de83b-108">在公共语言运行时 (CLR) 调用时指示当前线程上的上下文[ihostsecuritymanager:: Getsecuritycontext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-getsecuritycontext-method.md)方法或请求的对的调用中 CLR 的上下文[Ihostsecuritymanager:: Setsecuritycontext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-setsecuritycontext-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="de83b-108">Indicates the context on the current thread at the time the common language runtime (CLR) calls the [IHostSecurityManager::GetSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-getsecuritycontext-method.md) method, or the context requested by the CLR in a call to the [IHostSecurityManager::SetSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-setsecuritycontext-method.md) method.</span></span>|  
|`eRestrictedContext`|<span data-ttu-id="de83b-109">指示通过该主机具有较低的权限，如垃圾回收器或类或模块的构造函数的上下文。</span><span class="sxs-lookup"><span data-stu-id="de83b-109">Indicates a context over which the host has lower privileges, such as the garbage collector, or class or module constructors.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="de83b-110">备注</span><span class="sxs-lookup"><span data-stu-id="de83b-110">Remarks</span></span>  
 <span data-ttu-id="de83b-111">CLR 提供了之一`EContextType`值对的调用中的参数值作为`IHostSecurityManager::GetSecurityContext`和`IHostSecurityManager::SetSecurityContext`方法。</span><span class="sxs-lookup"><span data-stu-id="de83b-111">The CLR supplies one of the `EContextType` values as a parameter value in calls to the `IHostSecurityManager::GetSecurityContext` and `IHostSecurityManager::SetSecurityContext` methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="de83b-112">要求</span><span class="sxs-lookup"><span data-stu-id="de83b-112">Requirements</span></span>  
 <span data-ttu-id="de83b-113">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="de83b-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="de83b-114">**标头：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="de83b-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="de83b-115">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="de83b-115">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="de83b-116">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="de83b-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="de83b-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="de83b-117">See Also</span></span>  
 [<span data-ttu-id="de83b-118">IHostSecurityContext 接口</span><span class="sxs-lookup"><span data-stu-id="de83b-118">IHostSecurityContext Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md)  
 [<span data-ttu-id="de83b-119">IHostSecurityManager 接口</span><span class="sxs-lookup"><span data-stu-id="de83b-119">IHostSecurityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-interface.md)  
 [<span data-ttu-id="de83b-120">承载枚举</span><span class="sxs-lookup"><span data-stu-id="de83b-120">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)