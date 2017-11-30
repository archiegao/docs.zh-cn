---
title: "ICorProfilerInfo3::SetFunctionIDMapper2 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo3.SetFunctionIDMapper2 Method
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo3::SetFunctionIDMapper2
helpviewer_keywords:
- SetFunctionIDMapper2 method [.NET Framework profiling]
- ICorProfilerInfo3::SetFunctionIDMapper2 method [.NET Framework profiling]
ms.assetid: 8cdb1188-952a-4ba8-9f05-bfebc18cdd29
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: adc23b8774737f9884ded7ec1e3a891ed8b63b2d
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerinfo3setfunctionidmapper2-method"></a><span data-ttu-id="3a00c-102">ICorProfilerInfo3::SetFunctionIDMapper2 方法</span><span class="sxs-lookup"><span data-stu-id="3a00c-102">ICorProfilerInfo3::SetFunctionIDMapper2 Method</span></span>
<span data-ttu-id="3a00c-103">指定将调用以将 `FunctionID` 值映射至替换值（传递至探查器的输入/退出挂钩）的探查器实现函数。</span><span class="sxs-lookup"><span data-stu-id="3a00c-103">Specifies the profiler-implemented function that will be called to map `FunctionID` values to alternative values, which are passed to the profiler's function entry/exit hooks.</span></span> <span data-ttu-id="3a00c-104">此方法扩展[icorprofilerinfo:: Setfunctionidmapper](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setfunctionidmapper-method.md)具有其他数据参数，探查器可能用于消除运行时之间的歧义方法。</span><span class="sxs-lookup"><span data-stu-id="3a00c-104">This method extends the [ICorProfilerInfo::SetFunctionIDMapper](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setfunctionidmapper-method.md) method with an additional data parameter, which profilers may use to disambiguate among runtimes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3a00c-105">语法</span><span class="sxs-lookup"><span data-stu-id="3a00c-105">Syntax</span></span>  
  
```  
HRESULT SetFunctionIDMapper2(  
       [in] FunctionIDMapper2 *pFunc,  
       [in] void *clientData);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3a00c-106">参数</span><span class="sxs-lookup"><span data-stu-id="3a00c-106">Parameters</span></span>  
 `pFunc`  
 <span data-ttu-id="3a00c-107">[in]指向的指针[FunctionIDMapper2](../../../../docs/framework/unmanaged-api/profiling/functionidmapper2-function.md)实现，它将调用以映射`FunctionID`至其替换值的值。</span><span class="sxs-lookup"><span data-stu-id="3a00c-107">[in] A pointer to a [FunctionIDMapper2](../../../../docs/framework/unmanaged-api/profiling/functionidmapper2-function.md) implementation that will be called to map the `FunctionID` values to their alternative values.</span></span>  
  
 `clientData`  
 <span data-ttu-id="3a00c-108">[in]一个指针，它传递到每个[FunctionIDMapper2](../../../../docs/framework/unmanaged-api/profiling/functionidmapper2-function.md)函数所做的当前运行时调用。</span><span class="sxs-lookup"><span data-stu-id="3a00c-108">[in] A pointer that is passed to every [FunctionIDMapper2](../../../../docs/framework/unmanaged-api/profiling/functionidmapper2-function.md) function call made by the current runtime.</span></span> <span data-ttu-id="3a00c-109">探查器可以使用此信息来消除运行时之间的歧义。</span><span class="sxs-lookup"><span data-stu-id="3a00c-109">The profiler can use this information to disambiguate among runtimes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3a00c-110">返回值</span><span class="sxs-lookup"><span data-stu-id="3a00c-110">Return Value</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3a00c-111">备注</span><span class="sxs-lookup"><span data-stu-id="3a00c-111">Remarks</span></span>  
 <span data-ttu-id="3a00c-112">FunctionID 值备选方法将传递给探查器的输入/退出挂钩函数 ([FunctionEnter3](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md)， [FunctionLeave3](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md)，和[FunctionTailcall3](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md);或[FunctionEnter3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md)， [FunctionLeave3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md)，和[FunctionTailcall3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md)) 指定[SetEnterLeaveFunctionHooks3](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3-method.md)或[SetEnterLeaveFunctionHooks3WithInfo](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3withinfo-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="3a00c-112">The alternatives for the FunctionID values will be passed to the profiler's function entry/exit hooks ([FunctionEnter3](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md), [FunctionLeave3](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md), and [FunctionTailcall3](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md); or [FunctionEnter3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md), [FunctionLeave3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md), and [FunctionTailcall3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md)) that are specified by the [SetEnterLeaveFunctionHooks3](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3-method.md) or [SetEnterLeaveFunctionHooks3WithInfo](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3withinfo-method.md) method.</span></span>  
  
 <span data-ttu-id="3a00c-113">`FunctionIDMapper2`方法可以只能设置一次; 我们建议将其设置[icorprofilercallback:: Initialize](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-initialize-method.md)回调。</span><span class="sxs-lookup"><span data-stu-id="3a00c-113">The `FunctionIDMapper2` method can be set only once; we recommend that you set it in the [ICorProfilerCallback::Initialize](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-initialize-method.md) callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3a00c-114">要求</span><span class="sxs-lookup"><span data-stu-id="3a00c-114">Requirements</span></span>  
 <span data-ttu-id="3a00c-115">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3a00c-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3a00c-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="3a00c-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="3a00c-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3a00c-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3a00c-118">**.NET framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3a00c-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3a00c-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3a00c-119">See Also</span></span>  
 [<span data-ttu-id="3a00c-120">SetFunctionIDMapper</span><span class="sxs-lookup"><span data-stu-id="3a00c-120">SetFunctionIDMapper</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setfunctionidmapper-method.md)  
 [<span data-ttu-id="3a00c-121">ICorProfilerInfo3 接口</span><span class="sxs-lookup"><span data-stu-id="3a00c-121">ICorProfilerInfo3 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)  
 [<span data-ttu-id="3a00c-122">分析接口</span><span class="sxs-lookup"><span data-stu-id="3a00c-122">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)  
 [<span data-ttu-id="3a00c-123">分析</span><span class="sxs-lookup"><span data-stu-id="3a00c-123">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)