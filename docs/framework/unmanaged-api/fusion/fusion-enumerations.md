---
title: "合成枚举"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
helpviewer_keywords:
- unmanaged enumerations [.NET Framework], fusion
- fusion enumerations [.NET Framework]
- enumerations [.NET Framework fusion]
ms.assetid: 5817b4bc-b0ba-4b2f-a11c-a03dd8cb8f84
caps.latest.revision: "7"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 53c346418234fd0be45242f3e7aa0212dcef477a
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="fusion-enumerations"></a><span data-ttu-id="b1f2b-102">合成枚举</span><span class="sxs-lookup"><span data-stu-id="b1f2b-102">Fusion Enumerations</span></span>
<span data-ttu-id="b1f2b-103">本部分描述合成 API 使用的非托管的枚举。</span><span class="sxs-lookup"><span data-stu-id="b1f2b-103">This section describes the unmanaged enumerations that the fusion API uses.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="b1f2b-104">本节内容</span><span class="sxs-lookup"><span data-stu-id="b1f2b-104">In This Section</span></span>  
 [<span data-ttu-id="b1f2b-105">ASM_CACHE_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="b1f2b-105">ASM_CACHE_FLAGS Enumeration</span></span>](../../../../docs/framework/unmanaged-api/fusion/asm-cache-flags-enumeration.md)  
 <span data-ttu-id="b1f2b-106">指示由程序集的源[IAssemblyCacheItem](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md)全局程序集缓存中。</span><span class="sxs-lookup"><span data-stu-id="b1f2b-106">Indicates the source of an assembly represented by [IAssemblyCacheItem](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md) in the global assembly cache.</span></span>  
  
 [<span data-ttu-id="b1f2b-107">ASM_CMP_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="b1f2b-107">ASM_CMP_FLAGS Enumeration</span></span>](../../../../docs/framework/unmanaged-api/fusion/asm-cmp-flags-enumeration.md)  
 <span data-ttu-id="b1f2b-108">指示版本、 生成、 区域性、 签名和等等，要进行比较的两个程序集的[iassemblyname:: Isequal](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-isequal-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="b1f2b-108">Indicates the version, build, culture, signature, and so on, of two assemblies to be compared by the [IAssemblyName::IsEqual](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-isequal-method.md) method.</span></span>  
  
 [<span data-ttu-id="b1f2b-109">ASM_DISPLAY_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="b1f2b-109">ASM_DISPLAY_FLAGS Enumeration</span></span>](../../../../docs/framework/unmanaged-api/fusion/asm-display-flags-enumeration.md)  
 <span data-ttu-id="b1f2b-110">指示版本、 生成、 区域性、 签名和等等，将通过检索其显示名称的程序集[iassemblyname:: Getdisplayname](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-getdisplayname-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="b1f2b-110">Indicates the version, build, culture, signature, and so on, of the assembly whose display name will be retrieved by the [IAssemblyName::GetDisplayName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-getdisplayname-method.md) method.</span></span>  
  
 [<span data-ttu-id="b1f2b-111">ASM_NAME 枚举</span><span class="sxs-lookup"><span data-stu-id="b1f2b-111">ASM_NAME Enumeration</span></span>](../../../../docs/framework/unmanaged-api/fusion/asm-name-enumeration.md)  
 <span data-ttu-id="b1f2b-112">指示版本、 生成、 区域性、 签名和等等，将检索或设置其属性的程序集[IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)方法。</span><span class="sxs-lookup"><span data-stu-id="b1f2b-112">Indicates the version, build, culture, signature, and so on, of the assembly whose properties will be retrieved or set by [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) methods.</span></span>  
  
 [<span data-ttu-id="b1f2b-113">AssemblyComparisonResult 枚举</span><span class="sxs-lookup"><span data-stu-id="b1f2b-113">AssemblyComparisonResult Enumeration</span></span>](../../../../docs/framework/unmanaged-api/fusion/assemblycomparisonresult-enumeration.md)  
 <span data-ttu-id="b1f2b-114">根据所指示的两个程序集标识，等同性[CompareAssemblyIdentity](../../../../docs/framework/unmanaged-api/fusion/compareassemblyidentity-function.md)函数。</span><span class="sxs-lookup"><span data-stu-id="b1f2b-114">Indicates the equivalence of two assembly identities, as determined by the [CompareAssemblyIdentity](../../../../docs/framework/unmanaged-api/fusion/compareassemblyidentity-function.md) function.</span></span>  
  
 [<span data-ttu-id="b1f2b-115">CREATE_ASM_NAME_OBJ_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="b1f2b-115">CREATE_ASM_NAME_OBJ_FLAGS Enumeration</span></span>](../../../../docs/framework/unmanaged-api/fusion/create-asm-name-obj-flags-enumeration.md)  
 <span data-ttu-id="b1f2b-116">指定的属性`IAssemblyName`对象时其构建方式是[CreateAssemblyNameObject](../../../../docs/framework/unmanaged-api/fusion/createassemblynameobject-function.md)函数。</span><span class="sxs-lookup"><span data-stu-id="b1f2b-116">Specifies the attributes of an `IAssemblyName` object when it is constructed by the [CreateAssemblyNameObject](../../../../docs/framework/unmanaged-api/fusion/createassemblynameobject-function.md) function.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="b1f2b-117">相关章节</span><span class="sxs-lookup"><span data-stu-id="b1f2b-117">Related Sections</span></span>  
 [<span data-ttu-id="b1f2b-118">合成接口</span><span class="sxs-lookup"><span data-stu-id="b1f2b-118">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)  
  
 [<span data-ttu-id="b1f2b-119">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="b1f2b-119">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)  
  
 [<span data-ttu-id="b1f2b-120">合成结构</span><span class="sxs-lookup"><span data-stu-id="b1f2b-120">Fusion Structures</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-structures.md)