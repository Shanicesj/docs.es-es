---
title: "IHostCrst::SetSpinCount (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostCrst.SetSpinCount
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostCrst::SetSpinCount
helpviewer_keywords:
- IHostCrst::SetSpinCount method [.NET Framework hosting]
- SetSpinCount method [.NET Framework hosting]
ms.assetid: 863fc8ce-9b8a-477e-8dd8-75c8544bb43a
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 19172c6d498e5066c102c642105d78d10b26212c
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="ihostcrstsetspincount-method"></a><span data-ttu-id="b825f-102">IHostCrst::SetSpinCount (Método)</span><span class="sxs-lookup"><span data-stu-id="b825f-102">IHostCrst::SetSpinCount Method</span></span>
<span data-ttu-id="b825f-103">Establece el recuento circular actuales [IHostCrst](../../../../docs/framework/unmanaged-api/hosting/ihostcrst-interface.md) instancia.</span><span class="sxs-lookup"><span data-stu-id="b825f-103">Sets the spin count for the current [IHostCrst](../../../../docs/framework/unmanaged-api/hosting/ihostcrst-interface.md) instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b825f-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b825f-104">Syntax</span></span>  
  
```  
HRESULT SetSpinCount (  
    [in] DWORD dwSpinCount  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b825f-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b825f-105">Parameters</span></span>  
 `dwSpinCount`  
 <span data-ttu-id="b825f-106">[in] El nuevo recuento de número para el actual `IHostCrst` instancia.</span><span class="sxs-lookup"><span data-stu-id="b825f-106">[in] The new spin count for the current `IHostCrst` instance.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b825f-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b825f-107">Return Value</span></span>  
  
|<span data-ttu-id="b825f-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b825f-108">HRESULT</span></span>|<span data-ttu-id="b825f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b825f-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b825f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b825f-110">S_OK</span></span>|<span data-ttu-id="b825f-111">`SetSpinCount`se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="b825f-111">`SetSpinCount` returned successfully.</span></span>|  
|<span data-ttu-id="b825f-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="b825f-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="b825f-113">Common language runtime (CLR) no se han cargado en un proceso o el CLR está en un estado en el que no se puede ejecutar código administrado o procesar la llamada correctamente.</span><span class="sxs-lookup"><span data-stu-id="b825f-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="b825f-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b825f-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="b825f-115">La llamada agotó el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="b825f-115">The call timed out.</span></span>|  
|<span data-ttu-id="b825f-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="b825f-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="b825f-117">El llamador no posee el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="b825f-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="b825f-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="b825f-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="b825f-119">Se canceló un evento mientras un subproceso bloqueado o fibra esperó en él.</span><span class="sxs-lookup"><span data-stu-id="b825f-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="b825f-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="b825f-120">E_FAIL</span></span>|<span data-ttu-id="b825f-121">Se ha producido un error catastrófico desconocido.</span><span class="sxs-lookup"><span data-stu-id="b825f-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="b825f-122">Cuando un método devuelve E_FAIL, CLR ya no es utilizable dentro del proceso.</span><span class="sxs-lookup"><span data-stu-id="b825f-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="b825f-123">Las llamadas posteriores a métodos de hospedaje devuelven HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="b825f-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b825f-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b825f-124">Remarks</span></span>  
 <span data-ttu-id="b825f-125">En sistemas multiprocesador, si la sección crítica que representa el actual `IHostCrst` instancia no está disponible, un subproceso que realiza la llamada gira `dwSpinCount` veces antes de llamar a [IHostSemaphore:: wait](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-wait-method.md) en un semáforo asociado con la sección crítica.</span><span class="sxs-lookup"><span data-stu-id="b825f-125">On multi-processor systems, if the critical section represented by the current `IHostCrst` instance is unavailable, a calling thread spins `dwSpinCount` times before calling [IHostSemaphore::Wait](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-wait-method.md) on a semaphore associated with the critical section.</span></span> <span data-ttu-id="b825f-126">Si la sección crítica deja de estar disponible durante la operación circular, el subproceso que realiza la llamada evita la operación de espera.</span><span class="sxs-lookup"><span data-stu-id="b825f-126">If the critical section becomes free during the spin operation, the calling thread avoids the wait operation.</span></span>  
  
 <span data-ttu-id="b825f-127">El uso de `dwSpinCount` es idéntico al uso del parámetro del mismo nombre en Win32 `InitializeCriticalSectionAndSpinCount` función.</span><span class="sxs-lookup"><span data-stu-id="b825f-127">The usage of `dwSpinCount` is identical to the usage of the parameter of the same name in the Win32 `InitializeCriticalSectionAndSpinCount` function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b825f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b825f-128">Requirements</span></span>  
 <span data-ttu-id="b825f-129">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b825f-129">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b825f-130">**Encabezado:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="b825f-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b825f-131">**Biblioteca:** incluye como recurso en MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b825f-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b825f-132">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b825f-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b825f-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="b825f-133">See Also</span></span>  
 [<span data-ttu-id="b825f-134">ICLRSyncManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="b825f-134">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)  
 [<span data-ttu-id="b825f-135">IHostCrst (interfaz)</span><span class="sxs-lookup"><span data-stu-id="b825f-135">IHostCrst Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcrst-interface.md)  
 [<span data-ttu-id="b825f-136">IHostSyncManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="b825f-136">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)