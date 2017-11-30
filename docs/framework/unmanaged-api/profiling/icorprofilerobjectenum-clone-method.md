---
title: "ICorProfilerObjectEnum::Clone 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerObjectEnum.Clone
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerObjectEnum::Clone
helpviewer_keywords:
- Clone method, ICorProfilerObjectEnum interface [.NET Framework profiling]
- ICorProfilerObjectEnum::Clone method [.NET Framework profiling]
ms.assetid: b0b2facd-5991-4f4c-932d-c4937f45cef9
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: e077115863ab3371570463d0bfd9244b69888f9e
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="icorprofilerobjectenumclone-method"></a><span data-ttu-id="fafc6-102">ICorProfilerObjectEnum::Clone 方法</span><span class="sxs-lookup"><span data-stu-id="fafc6-102">ICorProfilerObjectEnum::Clone Method</span></span>
<span data-ttu-id="fafc6-103">获取对此副本的接口指针[ICorProfilerObjectEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md)接口。</span><span class="sxs-lookup"><span data-stu-id="fafc6-103">Gets an interface pointer to a copy of this [ICorProfilerObjectEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md) interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fafc6-104">语法</span><span class="sxs-lookup"><span data-stu-id="fafc6-104">Syntax</span></span>  
  
```  
HRESULT Clone (  
    [out] ICorProfilerObjectEnum   **ppEnum);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fafc6-105">参数</span><span class="sxs-lookup"><span data-stu-id="fafc6-105">Parameters</span></span>  
 `ppEnum`  
 <span data-ttu-id="fafc6-106">[out]指向反过来指向此副本的接口指针的指针`ICorProfilerObjectEnum`接口。</span><span class="sxs-lookup"><span data-stu-id="fafc6-106">[out] A pointer to the interface pointer that in turn points to the copy of this `ICorProfilerObjectEnum` interface.</span></span> <span data-ttu-id="fafc6-107">复制维护其自己的枚举状态独立于此。</span><span class="sxs-lookup"><span data-stu-id="fafc6-107">The copy maintains its own enumeration state separately from this one.</span></span> <span data-ttu-id="fafc6-108">但是，该副本的初始光标位置将与此枚举器的当前光标位置相同。</span><span class="sxs-lookup"><span data-stu-id="fafc6-108">However, the copy's initial cursor position will be the same as this enumerator's current cursor position.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fafc6-109">要求</span><span class="sxs-lookup"><span data-stu-id="fafc6-109">Requirements</span></span>  
 <span data-ttu-id="fafc6-110">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fafc6-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fafc6-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fafc6-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="fafc6-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fafc6-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fafc6-113">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fafc6-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fafc6-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fafc6-114">See Also</span></span>  
 [<span data-ttu-id="fafc6-115">ICorProfilerObjectEnum 接口</span><span class="sxs-lookup"><span data-stu-id="fafc6-115">ICorProfilerObjectEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md)