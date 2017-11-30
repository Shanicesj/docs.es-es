---
title: "ICorProfilerCallback::ObjectAllocated (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback.ObjectAllocated
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback::ObjectAllocated
helpviewer_keywords:
- ObjectAllocated method [.NET Framework profiling]
- ICorProfilerCallback::ObjectAllocated method [.NET Framework profiling]
ms.assetid: eb412622-77cc-4abd-a2cd-c910fe8edd54
topic_type: apiref
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: a7e67e6085db4b73ca39688935767072ceadb68e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilercallbackobjectallocated-method"></a><span data-ttu-id="ab6e7-102">ICorProfilerCallback::ObjectAllocated (Método)</span><span class="sxs-lookup"><span data-stu-id="ab6e7-102">ICorProfilerCallback::ObjectAllocated Method</span></span>
<span data-ttu-id="ab6e7-103">Notifica al generador de perfiles que se ha asignado la memoria en el montón de un objeto.</span><span class="sxs-lookup"><span data-stu-id="ab6e7-103">Notifies the profiler that memory within the heap has been allocated for an object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ab6e7-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab6e7-104">Syntax</span></span>  
  
```  
HRESULT ObjectAllocated(  
    [in] ObjectID objectId,  
    [in] ClassID classId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ab6e7-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab6e7-105">Parameters</span></span>  
 `objectId`  
 <span data-ttu-id="ab6e7-106">[in] El identificador del objeto para el que se asignó la memoria.</span><span class="sxs-lookup"><span data-stu-id="ab6e7-106">[in] The ID of the object for which memory was allocated.</span></span>  
  
 `classId`  
 <span data-ttu-id="ab6e7-107">[in] El identificador de la clase de la que el objeto es una instancia.</span><span class="sxs-lookup"><span data-stu-id="ab6e7-107">[in] The ID of the class of which the object is an instance.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ab6e7-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ab6e7-108">Remarks</span></span>  
 <span data-ttu-id="ab6e7-109">El `ObjectedAllocated` no se llama el método para las asignaciones desde la pila o memoria no administrada.</span><span class="sxs-lookup"><span data-stu-id="ab6e7-109">The `ObjectedAllocated` method is not called for allocations from either the stack or unmanaged memory.</span></span> <span data-ttu-id="ab6e7-110">El `classId` parámetro puede hacer referencia a una clase en código administrado que no se han cargado todavía.</span><span class="sxs-lookup"><span data-stu-id="ab6e7-110">The `classId` parameter can refer to a class in managed code that has not been loaded yet.</span></span> <span data-ttu-id="ab6e7-111">El generador de perfiles recibirá una devolución de llamada de carga de clase para esa clase inmediatamente después de la `ObjectAllocated` devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="ab6e7-111">The profiler will receive a class load callback for that class immediately after the `ObjectAllocated` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ab6e7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab6e7-112">Requirements</span></span>  
 <span data-ttu-id="ab6e7-113">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ab6e7-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ab6e7-114">**Encabezado:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ab6e7-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ab6e7-115">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ab6e7-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ab6e7-116">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ab6e7-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab6e7-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab6e7-117">See Also</span></span>  
 [<span data-ttu-id="ab6e7-118">ICorProfilerCallback (interfaz)</span><span class="sxs-lookup"><span data-stu-id="ab6e7-118">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="ab6e7-119">ClassLoadStarted (método)</span><span class="sxs-lookup"><span data-stu-id="ab6e7-119">ClassLoadStarted Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-classloadstarted-method.md)  
 [<span data-ttu-id="ab6e7-120">ClassLoadFinished (método)</span><span class="sxs-lookup"><span data-stu-id="ab6e7-120">ClassLoadFinished Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-classloadfinished-method.md)