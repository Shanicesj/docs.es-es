---
title: "ICLRPolicyManager::SetActionOnTimeout (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRPolicyManager.SetActionOnTimeout
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRPolicyManager::SetActionOnTimeout
helpviewer_keywords:
- SetActionOnTimeout method [.NET Framework hosting]
- ICLRPolicyManager::SetActionOnTimeout method [.NET Framework hosting]
ms.assetid: 38439fa1-2b99-4fa8-a6ec-08afc0f83b9c
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 924a8a64fb698ec0e78397ad791f445297c0fee6
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="iclrpolicymanagersetactionontimeout-method"></a><span data-ttu-id="c2942-102">ICLRPolicyManager::SetActionOnTimeout (Método)</span><span class="sxs-lookup"><span data-stu-id="c2942-102">ICLRPolicyManager::SetActionOnTimeout Method</span></span>
<span data-ttu-id="c2942-103">Especifica la acción de directiva que common language runtime (CLR) debe realizar cuando se agota el tiempo de espera de la operación especificada.</span><span class="sxs-lookup"><span data-stu-id="c2942-103">Specifies the policy action the common language runtime (CLR) should take when the specified operation times out.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c2942-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2942-104">Syntax</span></span>  
  
```  
HRESULT SetActionOnTimeout (  
    [in] EClrOperation operation,  
    [in] EPolicyAction action  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c2942-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2942-105">Parameters</span></span>  
 `operation`  
 <span data-ttu-id="c2942-106">[in] Uno de los [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) valores, que indica la operación para el que se especifica la acción de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="c2942-106">[in] One of the [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) values, indicating the operation for which to specify the timeout action.</span></span> <span data-ttu-id="c2942-107">Se admiten los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="c2942-107">The following values are supported:</span></span>  
  
-   <span data-ttu-id="c2942-108">OPR_AppDomainUnload</span><span class="sxs-lookup"><span data-stu-id="c2942-108">OPR_AppDomainUnload</span></span>  
  
-   <span data-ttu-id="c2942-109">OPR_ProcessExit</span><span class="sxs-lookup"><span data-stu-id="c2942-109">OPR_ProcessExit</span></span>  
  
-   <span data-ttu-id="c2942-110">OPR_ThreadRudeAbortInCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="c2942-110">OPR_ThreadRudeAbortInCriticalRegion</span></span>  
  
-   <span data-ttu-id="c2942-111">OPR_ThreadRudeAbortInNonCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="c2942-111">OPR_ThreadRudeAbortInNonCriticalRegion</span></span>  
  
 `action`  
 <span data-ttu-id="c2942-112">[in] Uno de los [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) valores, que indica la acción de directiva que se realizará cuando se agota el tiempo de espera de la operación.</span><span class="sxs-lookup"><span data-stu-id="c2942-112">[in] One of the [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) values, indicating the policy action to be taken when the operation times out.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c2942-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2942-113">Return Value</span></span>  
  
|<span data-ttu-id="c2942-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c2942-114">HRESULT</span></span>|<span data-ttu-id="c2942-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2942-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c2942-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2942-116">S_OK</span></span>|<span data-ttu-id="c2942-117">`SetActionOnTimeout`se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="c2942-117">`SetActionOnTimeout` returned successfully.</span></span>|  
|<span data-ttu-id="c2942-118">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="c2942-118">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="c2942-119">El CLR no se han cargado en un proceso o el CLR está en un estado en el que no se puede ejecutar código administrado o procesar la llamada correctamente.</span><span class="sxs-lookup"><span data-stu-id="c2942-119">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="c2942-120">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c2942-120">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="c2942-121">La llamada agotó el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="c2942-121">The call timed out.</span></span>|  
|<span data-ttu-id="c2942-122">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="c2942-122">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="c2942-123">El llamador no posee el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="c2942-123">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="c2942-124">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="c2942-124">HOST_E_ABANDONED</span></span>|<span data-ttu-id="c2942-125">Se canceló un evento mientras un subproceso bloqueado o fibra esperó en él.</span><span class="sxs-lookup"><span data-stu-id="c2942-125">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="c2942-126">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="c2942-126">E_FAIL</span></span>|<span data-ttu-id="c2942-127">Se ha producido un error catastrófico desconocido.</span><span class="sxs-lookup"><span data-stu-id="c2942-127">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="c2942-128">Cuando un método devuelve E_FAIL, CLR ya no es utilizable dentro del proceso.</span><span class="sxs-lookup"><span data-stu-id="c2942-128">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="c2942-129">Las llamadas posteriores a métodos de hospedaje devuelven HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="c2942-129">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="c2942-130">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c2942-130">E_INVALIDARG</span></span>|<span data-ttu-id="c2942-131">No se puede establecer un tiempo de espera para el elemento especificado `operation`, o se ha proporcionado un valor no válido para `operation`.</span><span class="sxs-lookup"><span data-stu-id="c2942-131">A timeout cannot be set for the specified `operation`, or an invalid value was supplied for `operation`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c2942-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2942-132">Remarks</span></span>  
 <span data-ttu-id="c2942-133">El valor de tiempo de espera puede ser el tiempo de espera predeterminado establecido por CLR o un valor especificado por el host en una llamada a la [ICLRPolicyManager:: SetTimeout](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-settimeout-method.md) método.</span><span class="sxs-lookup"><span data-stu-id="c2942-133">The timeout value can be either the default timeout set by the CLR, or a value specified by the host in a call to the [ICLRPolicyManager::SetTimeout](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-settimeout-method.md) method.</span></span>  
  
 <span data-ttu-id="c2942-134">No todos los valores de acción de directiva se pueden especificar como el comportamiento de tiempo de espera para las operaciones de CLR.</span><span class="sxs-lookup"><span data-stu-id="c2942-134">Not all policy action values can be specified as the timeout behavior for CLR operations.</span></span> <span data-ttu-id="c2942-135">`SetActionOnTimeout`Normalmente se usa solo para intensificar el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="c2942-135">`SetActionOnTimeout` is typically used only to escalate behavior.</span></span> <span data-ttu-id="c2942-136">Por ejemplo, un host puede especificar que las anulaciones de subprocesos se conviertan en anulaciones anulaciones de subprocesos, pero no se especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="c2942-136">For example, a host can specify that thread aborts be turned into rude thread aborts, but cannot specify the opposite.</span></span> <span data-ttu-id="c2942-137">La siguiente tabla describe los válido `action` valores para válido `operation` valores.</span><span class="sxs-lookup"><span data-stu-id="c2942-137">The table below describes the valid `action` values for valid `operation` values.</span></span>  
  
|<span data-ttu-id="c2942-138">Valor de`operation`</span><span class="sxs-lookup"><span data-stu-id="c2942-138">Value for `operation`</span></span>|<span data-ttu-id="c2942-139">Valores válidos para`action`</span><span class="sxs-lookup"><span data-stu-id="c2942-139">Valid values for `action`</span></span>|  
|---------------------------|-------------------------------|  
|<span data-ttu-id="c2942-140">OPR_ThreadRudeAbortInNonCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="c2942-140">OPR_ThreadRudeAbortInNonCriticalRegion</span></span><br /><br /> <span data-ttu-id="c2942-141">OPR_ThreadRudeAbortInCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="c2942-141">OPR_ThreadRudeAbortInCriticalRegion</span></span>|<span data-ttu-id="c2942-142">-eRudeAbortThread</span><span class="sxs-lookup"><span data-stu-id="c2942-142">-   eRudeAbortThread</span></span><br /><span data-ttu-id="c2942-143">-eUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="c2942-143">-   eUnloadAppDomain</span></span><br /><span data-ttu-id="c2942-144">-eRudeUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="c2942-144">-   eRudeUnloadAppDomain</span></span><br /><span data-ttu-id="c2942-145">-eExitProcess</span><span class="sxs-lookup"><span data-stu-id="c2942-145">-   eExitProcess</span></span><br /><span data-ttu-id="c2942-146">-eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="c2942-146">-   eFastExitProcess</span></span><br /><span data-ttu-id="c2942-147">-eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="c2942-147">-   eRudeExitProcess</span></span><br /><span data-ttu-id="c2942-148">-eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="c2942-148">-   eDisableRuntime</span></span>|  
|<span data-ttu-id="c2942-149">OPR_AppDomainUnload</span><span class="sxs-lookup"><span data-stu-id="c2942-149">OPR_AppDomainUnload</span></span>|<span data-ttu-id="c2942-150">-eUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="c2942-150">-   eUnloadAppDomain</span></span><br /><span data-ttu-id="c2942-151">-eRudeUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="c2942-151">-   eRudeUnloadAppDomain</span></span><br /><span data-ttu-id="c2942-152">-eExitProcess</span><span class="sxs-lookup"><span data-stu-id="c2942-152">-   eExitProcess</span></span><br /><span data-ttu-id="c2942-153">-eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="c2942-153">-   eFastExitProcess</span></span><br /><span data-ttu-id="c2942-154">-eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="c2942-154">-   eRudeExitProcess</span></span><br /><span data-ttu-id="c2942-155">-eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="c2942-155">-   eDisableRuntime</span></span>|  
|<span data-ttu-id="c2942-156">OPR_ProcessExit</span><span class="sxs-lookup"><span data-stu-id="c2942-156">OPR_ProcessExit</span></span>|<span data-ttu-id="c2942-157">-eExitProcess</span><span class="sxs-lookup"><span data-stu-id="c2942-157">-   eExitProcess</span></span><br /><span data-ttu-id="c2942-158">-eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="c2942-158">-   eFastExitProcess</span></span><br /><span data-ttu-id="c2942-159">-eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="c2942-159">-   eRudeExitProcess</span></span><br /><span data-ttu-id="c2942-160">-eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="c2942-160">-   eDisableRuntime</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c2942-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2942-161">Requirements</span></span>  
 <span data-ttu-id="c2942-162">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c2942-162">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c2942-163">**Encabezado:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="c2942-163">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c2942-164">**Biblioteca:** incluye como recurso en MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c2942-164">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c2942-165">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c2942-165">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c2942-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2942-166">See Also</span></span>  
 [<span data-ttu-id="c2942-167">EClrOperation (enumeración)</span><span class="sxs-lookup"><span data-stu-id="c2942-167">EClrOperation Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md)  
 [<span data-ttu-id="c2942-168">EPolicyAction (enumeración)</span><span class="sxs-lookup"><span data-stu-id="c2942-168">EPolicyAction Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md)  
 [<span data-ttu-id="c2942-169">ICLRControl (interfaz)</span><span class="sxs-lookup"><span data-stu-id="c2942-169">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)  
 [<span data-ttu-id="c2942-170">ICLRPolicyManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="c2942-170">ICLRPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)