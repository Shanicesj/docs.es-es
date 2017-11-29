---
title: "ICorDebugInternalFrame2::GetFrameAddress (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugInternalFrame2.GetFrameAddress Method
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugInternalFrame2::GetFrameAddress
helpviewer_keywords:
- GetFrameAddress method [.NET Framework debugging]
- ICorDebugInternalFrame2::GetFrameAddress method [.NET Framework debugging]
ms.assetid: 4ee8d058-ffc8-4967-9133-a5adfef4e518
topic_type: apiref
caps.latest.revision: "6"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 9ee867afe99fc5d2f2eb27bb1e6888aef8341d71
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="icordebuginternalframe2getframeaddress-method"></a><span data-ttu-id="cd016-102">ICorDebugInternalFrame2::GetFrameAddress (Método)</span><span class="sxs-lookup"><span data-stu-id="cd016-102">ICorDebugInternalFrame2::GetFrameAddress Method</span></span>
<span data-ttu-id="cd016-103">Devuelve la dirección de la pila del marco interno.</span><span class="sxs-lookup"><span data-stu-id="cd016-103">Returns the stack address of the internal frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cd016-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd016-104">Syntax</span></span>  
  
```  
HRESULT GetFrameAddress([out] CORDB_ADDRESS *pAddress);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cd016-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd016-105">Parameters</span></span>  
 `pAddress`  
 <span data-ttu-id="cd016-106">[out] Puntero a la `CORDB_ADDRESS` para el marco interno.</span><span class="sxs-lookup"><span data-stu-id="cd016-106">[out] Pointer to the `CORDB_ADDRESS` for the internal frame.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cd016-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd016-107">Return Value</span></span>  
 <span data-ttu-id="cd016-108">Este método devuelve los siguientes HRESULT específicos así como los errores HRESULT que indican un error del método.</span><span class="sxs-lookup"><span data-stu-id="cd016-108">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="cd016-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="cd016-109">HRESULT</span></span>|<span data-ttu-id="cd016-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd016-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="cd016-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd016-111">S_OK</span></span>|<span data-ttu-id="cd016-112">La dirección del marco interno se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="cd016-112">The address of the internal frame was successfully returned.</span></span>|  
|<span data-ttu-id="cd016-113">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd016-113">E_FAIL</span></span>|<span data-ttu-id="cd016-114">No se pudo devolver la dirección del marco interno.</span><span class="sxs-lookup"><span data-stu-id="cd016-114">The address of the internal frame could not be returned.</span></span>|  
|<span data-ttu-id="cd016-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="cd016-115">E_INVALIDARG</span></span>|<span data-ttu-id="cd016-116">El valor de `pAddress` es `null`.</span><span class="sxs-lookup"><span data-stu-id="cd016-116">`pAddress` is `null`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cd016-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd016-117">Remarks</span></span>  
 <span data-ttu-id="cd016-118">El valor devuelto en `pAddress` puede utilizarse para determinar la ubicación del marco interno en relación con otros marcos de la pila.</span><span class="sxs-lookup"><span data-stu-id="cd016-118">The value returned in `pAddress` can be used to determine the location of the internal frame relative to other frames on the stack.</span></span> <span data-ttu-id="cd016-119">Incluso en equipos basados en IA-64, el marco interno se mantiene en la pila solo y no hay ningún puntero correspondiente a un almacén de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="cd016-119">Even on IA-64-based computers, the internal frame lives on the stack only, and there is no corresponding pointer to a backing store.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cd016-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd016-120">Requirements</span></span>  
 <span data-ttu-id="cd016-121">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cd016-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cd016-122">**Encabezado:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cd016-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cd016-123">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cd016-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cd016-124">**Versiones de .NET framework:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cd016-124">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cd016-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd016-125">See Also</span></span>  
 [<span data-ttu-id="cd016-126">ICorDebugInternalFrame2 (interfaz)</span><span class="sxs-lookup"><span data-stu-id="cd016-126">ICorDebugInternalFrame2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginternalframe2-interface.md)  
 [<span data-ttu-id="cd016-127">Interfaces de depuración</span><span class="sxs-lookup"><span data-stu-id="cd016-127">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="cd016-128">Depuración</span><span class="sxs-lookup"><span data-stu-id="cd016-128">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)