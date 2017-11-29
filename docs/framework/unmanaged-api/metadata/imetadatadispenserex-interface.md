---
title: IMetaDataDispenserEx (Interfaz)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataDispenserEx
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataDispenserEx
helpviewer_keywords: IMetaDataDispenserEx interface [.NET Framework metadata]
ms.assetid: 78b3629e-77a2-4406-89c3-56b5cc2c4594
topic_type: apiref
caps.latest.revision: "14"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 5ecb4e94c0deed3ed62b2d2eb8b0309ca092abf8
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="imetadatadispenserex-interface"></a><span data-ttu-id="6d446-102">IMetaDataDispenserEx (Interfaz)</span><span class="sxs-lookup"><span data-stu-id="6d446-102">IMetaDataDispenserEx Interface</span></span>
<span data-ttu-id="6d446-103">Extiende la [IMetaDataDispenser (interfaz)](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md) interfaz para proporcionar la capacidad para controlar el funcionamiento de las API de metadatos en el ámbito de metadatos actual.</span><span class="sxs-lookup"><span data-stu-id="6d446-103">Extends the [IMetaDataDispenser Interface](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md) interface to provide the capability to control how the metadata APIs operate on the current metadata scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="6d446-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="6d446-104">Methods</span></span>  
  
|<span data-ttu-id="6d446-105">Método</span><span class="sxs-lookup"><span data-stu-id="6d446-105">Method</span></span>|<span data-ttu-id="6d446-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d446-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="6d446-107">FindAssembly (método)</span><span class="sxs-lookup"><span data-stu-id="6d446-107">FindAssembly Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-findassembly-method.md)|<span data-ttu-id="6d446-108">Este método no se implementa.</span><span class="sxs-lookup"><span data-stu-id="6d446-108">This method is not implemented.</span></span> <span data-ttu-id="6d446-109">Si se llama, devuelve E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="6d446-109">If called, it returns E_NOTIMPL.</span></span>|  
|[<span data-ttu-id="6d446-110">FindAssemblyModule (método)</span><span class="sxs-lookup"><span data-stu-id="6d446-110">FindAssemblyModule Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-findassemblymodule-method.md)|<span data-ttu-id="6d446-111">Este método no se implementa.</span><span class="sxs-lookup"><span data-stu-id="6d446-111">This method is not implemented.</span></span> <span data-ttu-id="6d446-112">Si se llama, devuelve E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="6d446-112">If called, it returns E_NOTIMPL.</span></span>|  
|[<span data-ttu-id="6d446-113">GetCORSystemDirectory (método)</span><span class="sxs-lookup"><span data-stu-id="6d446-113">GetCORSystemDirectory Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-getcorsystemdirectory-method.md)|<span data-ttu-id="6d446-114">Obtiene el directorio que contiene actual common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="6d446-114">Gets the directory that holds the current common language runtime (CLR).</span></span> <span data-ttu-id="6d446-115">Este método es compatible únicamente para su uso con depuradores fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="6d446-115">This method is supported only for use by out-of-process debuggers.</span></span> <span data-ttu-id="6d446-116">Si se llama desde otro componente, devolverá E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="6d446-116">If called from another component, it will return E_NOTIMPL.</span></span>|  
|[<span data-ttu-id="6d446-117">GetOption (método)</span><span class="sxs-lookup"><span data-stu-id="6d446-117">GetOption Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-getoption-method.md)|<span data-ttu-id="6d446-118">Obtiene el valor de la opción especificada para el ámbito de metadatos actual.</span><span class="sxs-lookup"><span data-stu-id="6d446-118">Gets the value of the specified option for the current metadata scope.</span></span> <span data-ttu-id="6d446-119">La opción controla cómo se administran las llamadas al ámbito de metadatos actual.</span><span class="sxs-lookup"><span data-stu-id="6d446-119">The option controls how calls to the current metadata scope are handled.</span></span>|  
|[<span data-ttu-id="6d446-120">OpenScopeOnITypeInfo (método)</span><span class="sxs-lookup"><span data-stu-id="6d446-120">OpenScopeOnITypeInfo Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-openscopeonitypeinfo-method.md)|<span data-ttu-id="6d446-121">Este método no se implementa.</span><span class="sxs-lookup"><span data-stu-id="6d446-121">This method is not implemented.</span></span> <span data-ttu-id="6d446-122">Si se llama, devuelve E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="6d446-122">If called, it returns E_NOTIMPL.</span></span>|  
|[<span data-ttu-id="6d446-123">SetOption (método)</span><span class="sxs-lookup"><span data-stu-id="6d446-123">SetOption Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-setoption-method.md)|<span data-ttu-id="6d446-124">Establece la opción especificada en un valor determinado para el ámbito de metadatos actual.</span><span class="sxs-lookup"><span data-stu-id="6d446-124">Sets the specified option to a given value for the current metadata scope.</span></span> <span data-ttu-id="6d446-125">La opción controla cómo se administran las llamadas al ámbito de metadatos actual.</span><span class="sxs-lookup"><span data-stu-id="6d446-125">The option controls how calls to the current metadata scope are handled.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="6d446-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d446-126">Requirements</span></span>  
 <span data-ttu-id="6d446-127">**Plataforma:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6d446-127">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6d446-128">**Encabezado:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="6d446-128">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="6d446-129">**Biblioteca:** usada como recurso en MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6d446-129">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="6d446-130">**Versiones de .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6d446-130">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6d446-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d446-131">See Also</span></span>  
 [<span data-ttu-id="6d446-132">Interfaces de metadatos</span><span class="sxs-lookup"><span data-stu-id="6d446-132">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)  
 [<span data-ttu-id="6d446-133">IMetaDataDispenser (interfaz)</span><span class="sxs-lookup"><span data-stu-id="6d446-133">IMetaDataDispenser Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)  
 [<span data-ttu-id="6d446-134">IMetaDataEmit (interfaz)</span><span class="sxs-lookup"><span data-stu-id="6d446-134">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="6d446-135">IMetaDataImport (interfaz)</span><span class="sxs-lookup"><span data-stu-id="6d446-135">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)