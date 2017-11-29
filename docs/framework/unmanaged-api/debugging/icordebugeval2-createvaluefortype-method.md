---
title: "ICorDebugEval2::CreateValueForType (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugEval2.CreateValueForType
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugEval2::CreateValueForType
helpviewer_keywords:
- CreateValueForType method [.NET Framework debugging]
- ICorDebugEval2::CreateValueForType method [.NET Framework debugging]
ms.assetid: ea38ae20-7e0a-427a-be77-d78fae719d82
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: cc2760b1c303141372aed824bda71ebdae8ffe0f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugeval2createvaluefortype-method"></a><span data-ttu-id="395cd-102">ICorDebugEval2::CreateValueForType (Método)</span><span class="sxs-lookup"><span data-stu-id="395cd-102">ICorDebugEval2::CreateValueForType Method</span></span>
<span data-ttu-id="395cd-103">Obtiene un puntero a un nuevo objeto ICorDebugValue del tipo especificado, con un valor inicial de cero o null.</span><span class="sxs-lookup"><span data-stu-id="395cd-103">Gets a pointer to a new ICorDebugValue of the specified type, with an initial value of zero or null.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="395cd-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="395cd-104">Syntax</span></span>  
  
```  
HRESULT CreateValueForType (  
    [in] ICorDebugType         *pType,  
    [out] ICorDebugValue       **ppValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="395cd-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="395cd-105">Parameters</span></span>  
 `pType`  
 <span data-ttu-id="395cd-106">[in] Puntero a un objeto ICorDebugType que representa el tipo.</span><span class="sxs-lookup"><span data-stu-id="395cd-106">[in] Pointer to an ICorDebugType object that represents the type.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="395cd-107">[out] Puntero a la dirección de un `ICorDebugValue` objeto que representa el valor.</span><span class="sxs-lookup"><span data-stu-id="395cd-107">[out] Pointer to the address of an `ICorDebugValue` object that represents the value.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="395cd-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="395cd-108">Remarks</span></span>  
 <span data-ttu-id="395cd-109">`CreateValueForType`generaliza [ICorDebugEval:: CreateValue](../../../../docs/framework/unmanaged-api/debugging/icordebugeval-createvalue-method.md) por lo que permite especificar un tipo de objeto arbitrario, incluidos construyen tipos como `List<int>`.</span><span class="sxs-lookup"><span data-stu-id="395cd-109">`CreateValueForType` generalizes [ICorDebugEval::CreateValue](../../../../docs/framework/unmanaged-api/debugging/icordebugeval-createvalue-method.md) by allowing you to specify an arbitrary object type, including constructed types such as `List<int>`.</span></span> <span data-ttu-id="395cd-110">El único propósito de este método consiste en generar un valor que puede pasarse a una evaluación de función.</span><span class="sxs-lookup"><span data-stu-id="395cd-110">The only purpose of this method is to generate a value that can be passed to a function evaluation.</span></span>  
  
 <span data-ttu-id="395cd-111">El tipo debe ser una clase o un tipo de valor.</span><span class="sxs-lookup"><span data-stu-id="395cd-111">The type must be a class or a value type.</span></span> <span data-ttu-id="395cd-112">No se puede usar este método para crear valores de matriz o valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="395cd-112">You cannot use this method to create array values or string values.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="395cd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="395cd-113">Requirements</span></span>  
 <span data-ttu-id="395cd-114">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="395cd-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="395cd-115">**Encabezado:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="395cd-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="395cd-116">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="395cd-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="395cd-117">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="395cd-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>