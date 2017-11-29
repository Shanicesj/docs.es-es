---
title: "ICorProfilerInfo::SetILInstrumentedCodeMap (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo.SetILInstrumentedCodeMap
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo::SetILInstrumentedCodeMap
helpviewer_keywords:
- ICorProfilerInfo::SetILInstrumentedCodeMap method [.NET Framework profiling]
- SetILInstrumentedCodeMap method [.NET Framework profiling]
ms.assetid: bce1dcf8-b4ec-4e73-a917-f2df1ad49c8a
topic_type: apiref
caps.latest.revision: "15"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 35c87b98a8e0c02ab6f4bca7a4f7a16ff6839c6b
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="icorprofilerinfosetilinstrumentedcodemap-method"></a><span data-ttu-id="9dbad-102">ICorProfilerInfo::SetILInstrumentedCodeMap (Método)</span><span class="sxs-lookup"><span data-stu-id="9dbad-102">ICorProfilerInfo::SetILInstrumentedCodeMap Method</span></span>
<span data-ttu-id="9dbad-103">Establece un mapa de código para la función especificada usando las entradas de mapa de lenguaje intermedio (MSIL) de Microsoft especificadas.</span><span class="sxs-lookup"><span data-stu-id="9dbad-103">Sets a code map for the specified function using the specified Microsoft intermediate language (MSIL) map entries.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9dbad-104">En .NET Framework versión 2.0, una llamada a `SetILInstrumentedCodeMap` en un `FunctionID` que representa un tipo genérico se funcionen en un dominio de aplicación determinado afectarán a todas las instancias de esa función en el dominio de aplicación.</span><span class="sxs-lookup"><span data-stu-id="9dbad-104">In the .NET Framework version 2.0, calling `SetILInstrumentedCodeMap` on a `FunctionID` that represents a generic function in a particular application domain will affect all instances of that function in the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9dbad-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9dbad-105">Syntax</span></span>  
  
```  
HRESULT SetILInstrumentedCodeMap(  
    [in]  FunctionID functionId,  
    [in]  BOOL       fStartJit,  
    [in]  ULONG      cILMapEntries,  
    [in, size_is(cILMapEntries)] COR_IL_MAP rgILMapEntries[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9dbad-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9dbad-106">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="9dbad-107">[in] El identificador de la función para que se establecerá el mapa de código.</span><span class="sxs-lookup"><span data-stu-id="9dbad-107">[in] The ID of the function for which to set the code map.</span></span>  
  
 `fStartJit`  
 <span data-ttu-id="9dbad-108">[in] Un valor booleano que indica si la llamada a la `SetILInstrumentedCodeMap` método es la primera para una determinada `FunctionID`.</span><span class="sxs-lookup"><span data-stu-id="9dbad-108">[in] A Boolean value that indicates whether the call to the `SetILInstrumentedCodeMap` method is the first for a particular `FunctionID`.</span></span> <span data-ttu-id="9dbad-109">Establecer `fStartJit` a `true` en la primera llamada a `SetILInstrumentedCodeMap` para un determinado `FunctionID`y a `false` a partir de ahí.</span><span class="sxs-lookup"><span data-stu-id="9dbad-109">Set `fStartJit` to `true` in the first call to `SetILInstrumentedCodeMap` for a given `FunctionID`, and to `false` thereafter.</span></span>  
  
 `cILMapEntries`  
 <span data-ttu-id="9dbad-110">[in] El número de elementos de la `cILMapEntries` matriz.</span><span class="sxs-lookup"><span data-stu-id="9dbad-110">[in] The number of elements in the `cILMapEntries` array.</span></span>  
  
 `rgILMapEntries`  
 <span data-ttu-id="9dbad-111">[in] Una matriz de estructuras COR_IL_MAP, cada uno de los cuales especifica un desplazamiento MSIL.</span><span class="sxs-lookup"><span data-stu-id="9dbad-111">[in] An array of COR_IL_MAP structures, each of which specifies an MSIL offset.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9dbad-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9dbad-112">Remarks</span></span>  
 <span data-ttu-id="9dbad-113">A menudo, un generador de perfiles inserta instrucciones incluidas en el código fuente de un método para instrumentar ese método (por ejemplo, para notificar cuando se alcanza una línea de código fuente).</span><span class="sxs-lookup"><span data-stu-id="9dbad-113">A profiler often inserts statements within the source code of a method in order to instrument that method (for example, to notify when a given source line is reached).</span></span> <span data-ttu-id="9dbad-114">`SetILInstrumentedCodeMap`permite a un generador de perfiles asignar las instrucciones de MSIL originales a sus nuevas ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="9dbad-114">`SetILInstrumentedCodeMap` enables a profiler to map the original MSIL instructions to their new locations.</span></span> <span data-ttu-id="9dbad-115">Un generador de perfiles puede usar el [ICorProfilerInfo:: GetILToNativeMapping](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getiltonativemapping-method.md) método para obtener el desplazamiento MSIL original de un desplazamiento nativo dado.</span><span class="sxs-lookup"><span data-stu-id="9dbad-115">A profiler can use the [ICorProfilerInfo::GetILToNativeMapping](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getiltonativemapping-method.md) method to get the original MSIL offset for a given native offset.</span></span>  
  
 <span data-ttu-id="9dbad-116">El depurador supondrá que cada desplazamiento anterior hace referencia a un desplazamiento dentro del código MSIL original, sin modificar de MSIL, y que cada nuevo desplazamiento hace referencia al desplazamiento de MSIL dentro del nuevo código instrumentado.</span><span class="sxs-lookup"><span data-stu-id="9dbad-116">The debugger will assume that each old offset refers to an MSIL offset within the original, unmodified MSIL code, and that each new offset refers to the MSIL offset within the new, instrumented code.</span></span> <span data-ttu-id="9dbad-117">La asignación se debe ordenar en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="9dbad-117">The map should be sorted in increasing order.</span></span> <span data-ttu-id="9dbad-118">Para la ejecución paso a paso para que funcionen correctamente, siga estas instrucciones:</span><span class="sxs-lookup"><span data-stu-id="9dbad-118">For stepping to work properly, follow these guidelines:</span></span>  
  
-   <span data-ttu-id="9dbad-119">No reordene el código MSIL instrumentado.</span><span class="sxs-lookup"><span data-stu-id="9dbad-119">Do not reorder instrumented MSIL code.</span></span>  
  
-   <span data-ttu-id="9dbad-120">No quite el código MSIL original.</span><span class="sxs-lookup"><span data-stu-id="9dbad-120">Do not remove the original MSIL code.</span></span>  
  
-   <span data-ttu-id="9dbad-121">Incluya entradas para todos los puntos de secuencia del archivo de programa (PDB) de la base de datos en el mapa.</span><span class="sxs-lookup"><span data-stu-id="9dbad-121">Include entries for all the sequence points from the program database (PDB) file in the map.</span></span> <span data-ttu-id="9dbad-122">El mapa no interpola las entradas que faltan.</span><span class="sxs-lookup"><span data-stu-id="9dbad-122">The map does not interpolate missing entries.</span></span> <span data-ttu-id="9dbad-123">Por lo tanto, dado el mapa siguiente:</span><span class="sxs-lookup"><span data-stu-id="9dbad-123">So, given the following map:</span></span>  
  
     <span data-ttu-id="9dbad-124">(0 anterior, 0 nuevo)</span><span class="sxs-lookup"><span data-stu-id="9dbad-124">(0 old, 0 new)</span></span>  
  
     <span data-ttu-id="9dbad-125">(5 anterior, 10 nueva)</span><span class="sxs-lookup"><span data-stu-id="9dbad-125">(5 old, 10 new)</span></span>  
  
     <span data-ttu-id="9dbad-126">(9 antiguo, 20 nueva)</span><span class="sxs-lookup"><span data-stu-id="9dbad-126">(9 old, 20 new)</span></span>  
  
    -   <span data-ttu-id="9dbad-127">Un desplazamiento anterior de 0, 1, 2, 3 o 4 se asignarán al nuevo desplazamiento de 0.</span><span class="sxs-lookup"><span data-stu-id="9dbad-127">An old offset of 0, 1, 2, 3, or 4 will be mapped to new offset 0.</span></span>  
  
    -   <span data-ttu-id="9dbad-128">Un desplazamiento anterior de 5, 6, 7 u 8 se asignarán al nuevo desplazamiento de 10.</span><span class="sxs-lookup"><span data-stu-id="9dbad-128">An old offset of 5, 6, 7, or 8 will be mapped to new offset 10.</span></span>  
  
    -   <span data-ttu-id="9dbad-129">Un desplazamiento anterior de 9 o versiones posteriores se asignarán al nuevo desplazamiento de 20.</span><span class="sxs-lookup"><span data-stu-id="9dbad-129">An old offset of 9 or higher will be mapped to new offset 20.</span></span>  
  
    -   <span data-ttu-id="9dbad-130">Se asignará un nuevo desplazamiento de 0, 1, 2, 3, 4, 5, 6, 7, 8 o 9 al anterior desplazamiento de 0.</span><span class="sxs-lookup"><span data-stu-id="9dbad-130">A new offset of 0, 1, 2, 3, 4, 5, 6, 7, 8, or 9 will be mapped to old offset 0.</span></span>  
  
    -   <span data-ttu-id="9dbad-131">Un desplazamiento de 10, 11, 12, 13, 14, 15, 16, 17, 18 o 19 nuevos se asignarán al anterior desplazamiento de 5.</span><span class="sxs-lookup"><span data-stu-id="9dbad-131">A new offset of 10, 11, 12, 13, 14, 15, 16, 17, 18, or 19 will be mapped to old offset 5.</span></span>  
  
    -   <span data-ttu-id="9dbad-132">Se asignará un nuevo desplazamiento de 20 o superior al anterior desplazamiento de 9.</span><span class="sxs-lookup"><span data-stu-id="9dbad-132">A new offset of 20 or higher will be mapped to old offset 9.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9dbad-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dbad-133">Requirements</span></span>  
 <span data-ttu-id="9dbad-134">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9dbad-134">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9dbad-135">**Encabezado:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="9dbad-135">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="9dbad-136">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9dbad-136">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9dbad-137">**Versiones de .NET framework:**[!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9dbad-137">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9dbad-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9dbad-138">See Also</span></span>  
 [<span data-ttu-id="9dbad-139">ICorProfilerInfo (interfaz)</span><span class="sxs-lookup"><span data-stu-id="9dbad-139">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)