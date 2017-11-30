---
title: "CreateInstallReferenceEnum (Función)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CreateInstallReferenceEnum
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type: DLLExport
f1_keywords: CreateInstallReference
helpviewer_keywords: CreateInstallReference function [.NET Framework fusion]
ms.assetid: 80dbbbf8-54fc-4894-b74a-0179d3201083
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 07c7ec72a66b37798e6e2af523bb024e9dd63d9a
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="createinstallreferenceenum-function"></a><span data-ttu-id="ffc29-102">CreateInstallReferenceEnum (Función)</span><span class="sxs-lookup"><span data-stu-id="ffc29-102">CreateInstallReferenceEnum Function</span></span>
<span data-ttu-id="ffc29-103">Obtiene un puntero a un [IInstallReferenceEnum](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md) instancia que representa una lista de referencias de una aplicación para el ensamblado especificado.</span><span class="sxs-lookup"><span data-stu-id="ffc29-103">Gets a pointer to an [IInstallReferenceEnum](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md) instance that represents a list of an application's references to the specified assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ffc29-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ffc29-104">Syntax</span></span>  
  
```  
HRESULT CreateInstallReferenceEnum (  
    [out] IInstallReferenceEnum **ppRefEnum,  
    [in]  IAssemblyName         *pName,  
    [in]  DWORD                 dwFlags,  
    [in]  LPVOID                pvReserved  
 );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ffc29-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ffc29-105">Parameters</span></span>  
 `ppRefEnum`  
 <span data-ttu-id="ffc29-106">[out] El valor devuelto `IInstallReferenceEnum` puntero.</span><span class="sxs-lookup"><span data-stu-id="ffc29-106">[out] The returned `IInstallReferenceEnum` pointer.</span></span>  
  
 `pName`  
 <span data-ttu-id="ffc29-107">[in] El [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) que identifica el ensamblado para el que se va a enumerar las referencias.</span><span class="sxs-lookup"><span data-stu-id="ffc29-107">[in] The [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) that identifies the assembly for which to enumerate references.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="ffc29-108">[in] Marcas que influyen en el comportamiento del enumerador.</span><span class="sxs-lookup"><span data-stu-id="ffc29-108">[in] Flags that influence the enumerator's behavior.</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="ffc29-109">[in] Reservado para extensibilidad futura.</span><span class="sxs-lookup"><span data-stu-id="ffc29-109">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="ffc29-110">`pvReserved`debe ser una referencia nula.</span><span class="sxs-lookup"><span data-stu-id="ffc29-110">`pvReserved` must be a null reference.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ffc29-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffc29-111">Requirements</span></span>  
 <span data-ttu-id="ffc29-112">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ffc29-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ffc29-113">**Encabezado:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="ffc29-113">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="ffc29-114">**Biblioteca:** Fusion.dll y Mscorwks.dll.</span><span class="sxs-lookup"><span data-stu-id="ffc29-114">**Library:** Fusion.dll and Mscorwks.dll.</span></span> <span data-ttu-id="ffc29-115">Use Fusion.dll en lugar de Mscorwks.dll para asegurarse de que la versión correcta de .NET Framework de destino.</span><span class="sxs-lookup"><span data-stu-id="ffc29-115">Use Fusion.dll instead of Mscorwks.dll to ensure that you target the correct version of the .NET Framework.</span></span>  
  
 <span data-ttu-id="ffc29-116">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ffc29-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ffc29-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffc29-117">See Also</span></span>  
 [<span data-ttu-id="ffc29-118">IInstallReferenceEnum (interfaz)</span><span class="sxs-lookup"><span data-stu-id="ffc29-118">IInstallReferenceEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md)  
 [<span data-ttu-id="ffc29-119">IAssemblyName (interfaz)</span><span class="sxs-lookup"><span data-stu-id="ffc29-119">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)  
 [<span data-ttu-id="ffc29-120">Funciones estáticas globales de fusión</span><span class="sxs-lookup"><span data-stu-id="ffc29-120">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)