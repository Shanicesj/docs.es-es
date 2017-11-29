---
title: "IAssemblyEnum::GetNextAssembly (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IAssemblyEnum.GetNextAssembly
api_location: fusion.dll
api_type: COM
f1_keywords: IAssemblyEnum::GetNextAssembly
helpviewer_keywords:
- GetNextAssembly method [.NET Framework fusion]
- IAssemblyEnum::GetNextAssembly method [.NET Framework fusion]
ms.assetid: 5d7a4ca2-5f46-4ef1-a9a2-257884e9dc11
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: cef1624d0432d571edfddfa772f31366e23074f5
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="iassemblyenumgetnextassembly-method"></a><span data-ttu-id="3609f-102">IAssemblyEnum::GetNextAssembly (Método)</span><span class="sxs-lookup"><span data-stu-id="3609f-102">IAssemblyEnum::GetNextAssembly Method</span></span>
<span data-ttu-id="3609f-103">Obtiene un puntero a la siguiente [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) contenida en esta instancia [IAssemblyEnum](../../../../docs/framework/unmanaged-api/fusion/iassemblyenum-interface.md) objeto.</span><span class="sxs-lookup"><span data-stu-id="3609f-103">Gets a pointer to the next [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) contained in this [IAssemblyEnum](../../../../docs/framework/unmanaged-api/fusion/iassemblyenum-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3609f-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3609f-104">Syntax</span></span>  
  
```  
HRESULT GetNextAssembly (  
    [in]  LPVOID          pvReserved,  
    [out] IAssemblyName   **ppName,  
    [in]  DWORD           dwFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3609f-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3609f-105">Parameters</span></span>  
 `pvReserved`  
 <span data-ttu-id="3609f-106">[in] Reservado para extensibilidad futura.</span><span class="sxs-lookup"><span data-stu-id="3609f-106">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="3609f-107">`pvReserved`debe ser una referencia nula.</span><span class="sxs-lookup"><span data-stu-id="3609f-107">`pvReserved` must be a null reference.</span></span>  
  
 `ppName`  
 <span data-ttu-id="3609f-108">[out] El valor devuelto `IAssemblyName` puntero.</span><span class="sxs-lookup"><span data-stu-id="3609f-108">[out] The returned `IAssemblyName` pointer.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="3609f-109">[in] Reservado para extensibilidad futura.</span><span class="sxs-lookup"><span data-stu-id="3609f-109">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="3609f-110">`dwFlags`debe ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="3609f-110">`dwFlags` must be 0 (zero).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3609f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3609f-111">Requirements</span></span>  
 <span data-ttu-id="3609f-112">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3609f-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3609f-113">**Encabezado:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="3609f-113">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="3609f-114">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3609f-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3609f-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="3609f-115">See Also</span></span>  
 [<span data-ttu-id="3609f-116">IAssemblyName (interfaz)</span><span class="sxs-lookup"><span data-stu-id="3609f-116">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)  
 [<span data-ttu-id="3609f-117">IAssemblyEnum (interfaz)</span><span class="sxs-lookup"><span data-stu-id="3609f-117">IAssemblyEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyenum-interface.md)