---
title: "Funciones estáticas globales para generación de perfiles"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
helpviewer_keywords:
- global static functions [.NET Framework profiling]
- profiling global static functions [.NET Framework]
- unmanaged global static functions [.NET Framework], profiling
ms.assetid: 08a13a57-dc49-488d-b937-31e3051fda97
caps.latest.revision: "14"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 4da4509a6e8b87490cee076b403f3fa525de91e0
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="profiling-global-static-functions"></a><span data-ttu-id="26b33-102">Funciones estáticas globales para generación de perfiles</span><span class="sxs-lookup"><span data-stu-id="26b33-102">Profiling Global Static Functions</span></span>
<span data-ttu-id="26b33-103">Esta sección describen las funciones de API no administradas que utiliza la API de generación de perfiles.</span><span class="sxs-lookup"><span data-stu-id="26b33-103">This section describes the unmanaged API functions that the profiling API uses.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="26b33-104">En esta sección</span><span class="sxs-lookup"><span data-stu-id="26b33-104">In This Section</span></span>  
  
## <a name="net-framework-version-1-profiling-functions"></a><span data-ttu-id="26b33-105">Funciones de generación de perfiles de .NET framework versión 1</span><span class="sxs-lookup"><span data-stu-id="26b33-105">.NET Framework version 1 Profiling Functions</span></span>  
 [<span data-ttu-id="26b33-106">FunctionEnter (función)</span><span class="sxs-lookup"><span data-stu-id="26b33-106">FunctionEnter Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter-function.md)  
 <span data-ttu-id="26b33-107">Notifica al generador de perfiles que se pasan a una función de control.</span><span class="sxs-lookup"><span data-stu-id="26b33-107">Notifies the profiler that control is being passed to a function.</span></span> <span data-ttu-id="26b33-108">En desuso en .NET Framework 2.0.</span><span class="sxs-lookup"><span data-stu-id="26b33-108">Deprecated in the .NET Framework 2.0.</span></span>  
  
 [<span data-ttu-id="26b33-109">FunctionLeave (función)</span><span class="sxs-lookup"><span data-stu-id="26b33-109">FunctionLeave Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave-function.md)  
 <span data-ttu-id="26b33-110">Notifica al generador de perfiles que una función está a punto de devolver al llamador.</span><span class="sxs-lookup"><span data-stu-id="26b33-110">Notifies the profiler that a function is about to return to the caller.</span></span> <span data-ttu-id="26b33-111">En desuso en .NET Framework 2.0.</span><span class="sxs-lookup"><span data-stu-id="26b33-111">Deprecated in the .NET Framework 2.0.</span></span>  
  
 [<span data-ttu-id="26b33-112">FunctionTailcall (función)</span><span class="sxs-lookup"><span data-stu-id="26b33-112">FunctionTailcall Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall-function.md)  
 <span data-ttu-id="26b33-113">Notifica al generador de perfiles que la función en ejecución está a punto de realizar una llamada de cola a otra función.</span><span class="sxs-lookup"><span data-stu-id="26b33-113">Notifies the profiler that the currently executing function is about to perform a tail call to another function.</span></span> <span data-ttu-id="26b33-114">En desuso en .NET Framework 2.0.</span><span class="sxs-lookup"><span data-stu-id="26b33-114">Deprecated in the .NET Framework 2.0.</span></span>  
  
## <a name="net-framework-version-2-profiling-functions"></a><span data-ttu-id="26b33-115">Funciones de generación de perfiles de .NET framework versión 2</span><span class="sxs-lookup"><span data-stu-id="26b33-115">.NET Framework version 2 Profiling Functions</span></span>  
 [<span data-ttu-id="26b33-116">FunctionIDMapper (función)</span><span class="sxs-lookup"><span data-stu-id="26b33-116">FunctionIDMapper Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionidmapper-function.md)  
 <span data-ttu-id="26b33-117">Notifica al generador de perfiles que el identificador especificado de una función puede reasignarse a otro identificador que se usará en el [FunctionEnter2](../../../../docs/framework/unmanaged-api/profiling/functionenter2-function.md), [FunctionLeave2](../../../../docs/framework/unmanaged-api/profiling/functionleave2-function.md), y [FunctionTailcall2](../../../../docs/framework/unmanaged-api/profiling/functiontailcall2-function.md) devoluciones de llamada de esa función.</span><span class="sxs-lookup"><span data-stu-id="26b33-117">Notifies the profiler that the given identifier of a function may be remapped to an alternative ID to be used in the [FunctionEnter2](../../../../docs/framework/unmanaged-api/profiling/functionenter2-function.md), [FunctionLeave2](../../../../docs/framework/unmanaged-api/profiling/functionleave2-function.md), and [FunctionTailcall2](../../../../docs/framework/unmanaged-api/profiling/functiontailcall2-function.md) callbacks for that function.</span></span> <span data-ttu-id="26b33-118">También permite al generador de perfiles indicar si desea recibir devoluciones de llamada para esa función</span><span class="sxs-lookup"><span data-stu-id="26b33-118">Also enables the profiler to indicate whether it wants to receive callbacks for that function</span></span>  
  
 [<span data-ttu-id="26b33-119">FunctionEnter2 (función)</span><span class="sxs-lookup"><span data-stu-id="26b33-119">FunctionEnter2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter2-function.md)  
 <span data-ttu-id="26b33-120">Notifica al generador de perfiles que el control se pasa a una función y proporciona información sobre la pila de argumentos de marco y la función.</span><span class="sxs-lookup"><span data-stu-id="26b33-120">Notifies the profiler that control is being passed to a function and provides information about the stack frame and function arguments.</span></span> <span data-ttu-id="26b33-121">En desuso en el [!INCLUDE[net_v40_short](../../../../includes/net-v40-short-md.md)].</span><span class="sxs-lookup"><span data-stu-id="26b33-121">Deprecated in the [!INCLUDE[net_v40_short](../../../../includes/net-v40-short-md.md)].</span></span>  
  
 [<span data-ttu-id="26b33-122">FunctionLeave2 (función)</span><span class="sxs-lookup"><span data-stu-id="26b33-122">FunctionLeave2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave2-function.md)  
 <span data-ttu-id="26b33-123">Notifica al generador de perfiles que una función se va a devolver al llamador y proporciona información sobre el valor de retorno de marco y la función de pila.</span><span class="sxs-lookup"><span data-stu-id="26b33-123">Notifies the profiler that a function is about to return to the caller and provides information about the stack frame and function return value.</span></span> <span data-ttu-id="26b33-124">En desuso en el [!INCLUDE[net_v40_short](../../../../includes/net-v40-short-md.md)].</span><span class="sxs-lookup"><span data-stu-id="26b33-124">Deprecated in the [!INCLUDE[net_v40_short](../../../../includes/net-v40-short-md.md)].</span></span>  
  
 [<span data-ttu-id="26b33-125">FunctionTailcall2 (función)</span><span class="sxs-lookup"><span data-stu-id="26b33-125">FunctionTailcall2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall2-function.md)  
 <span data-ttu-id="26b33-126">Notifica al generador de perfiles que la función en ejecución está a punto de realizar una llamada de cola a otra función y proporciona información sobre el marco de pila.</span><span class="sxs-lookup"><span data-stu-id="26b33-126">Notifies the profiler that the currently executing function is about to perform a tail call to another function and provides information about the stack frame.</span></span> <span data-ttu-id="26b33-127">En desuso en el [!INCLUDE[net_v40_short](../../../../includes/net-v40-short-md.md)].</span><span class="sxs-lookup"><span data-stu-id="26b33-127">Deprecated in the [!INCLUDE[net_v40_short](../../../../includes/net-v40-short-md.md)].</span></span>  
  
 [<span data-ttu-id="26b33-128">StackSnapshotCallback (función)</span><span class="sxs-lookup"><span data-stu-id="26b33-128">StackSnapshotCallback Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/stacksnapshotcallback-function.md)  
 <span data-ttu-id="26b33-129">Proporciona el generador de perfiles con información sobre cada marco administrado y cada ejecución de marcos no administrados en la pila durante un recorrido de pila, que se inicia mediante la [ICorProfilerInfo2:: DoStackSnapshot](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-dostacksnapshot-method.md) método.</span><span class="sxs-lookup"><span data-stu-id="26b33-129">Provides the profiler with information about each managed frame and each run of unmanaged frames on the stack during a stack walk, which is initiated by the [ICorProfilerInfo2::DoStackSnapshot](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-dostacksnapshot-method.md) method.</span></span>  
  
## <a name="net-framework-version-4-profiling-functions"></a><span data-ttu-id="26b33-130">Funciones de generación de perfiles de .NET framework versión 4</span><span class="sxs-lookup"><span data-stu-id="26b33-130">.NET Framework version 4 Profiling Functions</span></span>  
 [<span data-ttu-id="26b33-131">FunctionIDMapper2 (función)</span><span class="sxs-lookup"><span data-stu-id="26b33-131">FunctionIDMapper2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionidmapper2-function.md)  
 <span data-ttu-id="26b33-132">Notifica al generador de perfiles que el identificador especificado de una función puede reasignarse a otro identificador que se usará en el [FunctionEnter3](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md), [FunctionLeave3](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md), y [FunctionTailcall3](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md), o[FunctionEnter3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md), [FunctionLeave3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md), y [FunctionTailcall3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md) devoluciones de llamada de esa función.</span><span class="sxs-lookup"><span data-stu-id="26b33-132">Notifies the profiler that the given identifier of a function may be remapped to an alternative ID to be used in the [FunctionEnter3](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md), [FunctionLeave3](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md), and [FunctionTailcall3](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md), or[FunctionEnter3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md), [FunctionLeave3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md), and [FunctionTailcall3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md) callbacks for that function.</span></span> <span data-ttu-id="26b33-133">También permite al generador de perfiles indicar si desea recibir devoluciones de llamada para esa función.</span><span class="sxs-lookup"><span data-stu-id="26b33-133">Also enables the profiler to indicate whether it wants to receive callbacks for that function.</span></span>  
  
 <span data-ttu-id="26b33-134">`FunctionIDMapper2`extiende la [FunctionIDMapper](../../../../docs/framework/unmanaged-api/profiling/functionidmapper-function.md) funcionando con un `clientData` parámetro, que los generadores de perfiles pueden usar para eliminar la ambigüedad entre los Runtime.</span><span class="sxs-lookup"><span data-stu-id="26b33-134">`FunctionIDMapper2` extends the [FunctionIDMapper](../../../../docs/framework/unmanaged-api/profiling/functionidmapper-function.md) function with a `clientData` parameter, which profilers may use to disambiguate among runtimes.</span></span>  
  
 [<span data-ttu-id="26b33-135">FunctionEnter3 (función)</span><span class="sxs-lookup"><span data-stu-id="26b33-135">FunctionEnter3 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md)  
 <span data-ttu-id="26b33-136">Notifica al generador de perfiles que se pasan a una función de control.</span><span class="sxs-lookup"><span data-stu-id="26b33-136">Notifies the profiler that control is being passed to a function.</span></span>  
  
 [<span data-ttu-id="26b33-137">FunctionEnter3WithInfo (función)</span><span class="sxs-lookup"><span data-stu-id="26b33-137">FunctionEnter3WithInfo Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md)  
 <span data-ttu-id="26b33-138">Notifica al generador de perfiles que se pasan a una función de control y proporciona un identificador que puede pasarse a [ICorProfilerInfo3:: Getfunctionenter3info](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-getfunctionenter3info-method.md) para recuperar los argumentos de marco y la función de la pila.</span><span class="sxs-lookup"><span data-stu-id="26b33-138">Notifies the profiler that control is being passed to a function, and provides a handle that can be passed to [ICorProfilerInfo3::GetFunctionEnter3Info](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-getfunctionenter3info-method.md) to retrieve the stack frame and function arguments.</span></span>  
  
 [<span data-ttu-id="26b33-139">FunctionLeave3 (función)</span><span class="sxs-lookup"><span data-stu-id="26b33-139">FunctionLeave3 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md)  
 <span data-ttu-id="26b33-140">Notifica al generador de perfiles que se devuelve de una función de control.</span><span class="sxs-lookup"><span data-stu-id="26b33-140">Notifies the profiler that control is being returned from a function.</span></span>  
  
 [<span data-ttu-id="26b33-141">FunctionLeave3WithInfo (función)</span><span class="sxs-lookup"><span data-stu-id="26b33-141">FunctionLeave3WithInfo Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md)  
 <span data-ttu-id="26b33-142">Notifica al generador de perfiles que se devuelve de una función de control y proporciona un identificador que puede pasarse a [ICorProfilerInfo3:: Getfunctionleave3info](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-getfunctionleave3info-method.md) para recuperar el marco de pila y el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="26b33-142">Notifies the profiler that control is being returned from a function, and provides a handle that can be passed to [ICorProfilerInfo3::GetFunctionLeave3Info](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-getfunctionleave3info-method.md) to retrieve the stack frame and the return value.</span></span>  
  
 [<span data-ttu-id="26b33-143">FunctionTailcall3 (función)</span><span class="sxs-lookup"><span data-stu-id="26b33-143">FunctionTailcall3 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md)  
 <span data-ttu-id="26b33-144">Notifica al generador de perfiles que la función en ejecución está a punto de realizar una llamada de cola a otra función.</span><span class="sxs-lookup"><span data-stu-id="26b33-144">Notifies the profiler that the currently executing function is about to perform a tail call to another function.</span></span>  
  
 [<span data-ttu-id="26b33-145">FunctionTailcall3WithInfo (función)</span><span class="sxs-lookup"><span data-stu-id="26b33-145">FunctionTailcall3WithInfo Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md)  
 <span data-ttu-id="26b33-146">Notifica al generador de perfiles que la función en ejecución está a punto de realizar una llamada de cola a otra función y proporciona un identificador que puede pasarse a [ICorProfilerInfo3:: Getfunctiontailcall3info](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-getfunctiontailcall3info-method.md) para recuperar el marco de pila.</span><span class="sxs-lookup"><span data-stu-id="26b33-146">Notifies the profiler that the currently executing function is about to perform a tail call to another function, and provides a handle that can be passed to [ICorProfilerInfo3::GetFunctionTailcall3Info](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-getfunctiontailcall3info-method.md) to retrieve the stack frame.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="26b33-147">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="26b33-147">Related Sections</span></span>  
 [<span data-ttu-id="26b33-148">Información general de generación de perfiles</span><span class="sxs-lookup"><span data-stu-id="26b33-148">Profiling Overview</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-overview.md)  
  
 [<span data-ttu-id="26b33-149">Interfaces de generación de perfiles</span><span class="sxs-lookup"><span data-stu-id="26b33-149">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)  
  
 [<span data-ttu-id="26b33-150">Enumeraciones de generación de perfiles</span><span class="sxs-lookup"><span data-stu-id="26b33-150">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)  
  
 [<span data-ttu-id="26b33-151">Estructuras de generación de perfiles</span><span class="sxs-lookup"><span data-stu-id="26b33-151">Profiling Structures</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-structures.md)