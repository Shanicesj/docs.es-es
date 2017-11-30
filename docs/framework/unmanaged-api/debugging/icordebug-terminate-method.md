---
title: "ICorDebug::Terminate (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebug.Terminate
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebug::Terminate
helpviewer_keywords:
- Terminate method, ICorDebug interface [.NET Framework debugging]
- ICorDebug::Terminate method [.NET Framework debugging]
ms.assetid: fffe5616-0896-4426-ab5e-21869b514883
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: b18bb6222296c5e8875f983d47118f938a54bcc2
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugterminate-method"></a><span data-ttu-id="451e9-102">ICorDebug::Terminate (Método)</span><span class="sxs-lookup"><span data-stu-id="451e9-102">ICorDebug::Terminate Method</span></span>
<span data-ttu-id="451e9-103">Finaliza el `ICorDebug` objeto.</span><span class="sxs-lookup"><span data-stu-id="451e9-103">Terminates the `ICorDebug` object.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="451e9-104">`Terminate`no debe llamarse hasta un [ICorDebugManagedCallback:: ExitProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitprocess-method.md) se ha recibido la devolución de llamada para todos los procesos que se está depurados.</span><span class="sxs-lookup"><span data-stu-id="451e9-104">`Terminate` should not be called until an [ICorDebugManagedCallback::ExitProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitprocess-method.md) callback has been received for all processes being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="451e9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="451e9-105">Syntax</span></span>  
  
```  
HRESULT Terminate ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="451e9-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="451e9-106">Remarks</span></span>  
 <span data-ttu-id="451e9-107">`Terminate`se debe llamar cuando la `ICorDebug` objeto ya no es necesario.</span><span class="sxs-lookup"><span data-stu-id="451e9-107">`Terminate` must be called when the `ICorDebug` object is no longer needed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="451e9-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="451e9-108">Requirements</span></span>  
 <span data-ttu-id="451e9-109">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="451e9-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="451e9-110">**Encabezado:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="451e9-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="451e9-111">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="451e9-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="451e9-112">**Versiones de .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="451e9-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="451e9-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="451e9-113">See Also</span></span>  
 [<span data-ttu-id="451e9-114">ICorDebug (interfaz)</span><span class="sxs-lookup"><span data-stu-id="451e9-114">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)