---
title: IMetaDataEmit::DefineTypeRefByName (Método)
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineTypeRefByName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineTypeRefByName
helpviewer_keywords:
- DefineTypeRefByName method [.NET Framework metadata]
- IMetaDataEmit::DefineTypeRefByName method [.NET Framework metadata]
ms.assetid: c30a4ce3-2d3e-411a-98df-e62ac4a5dd50
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4dd08afba664a491b3ba398f3da4c6a73cda5378
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54517141"
---
# <a name="imetadataemitdefinetyperefbyname-method"></a>IMetaDataEmit::DefineTypeRefByName (Método)
Obtiene los metadatos de un token para un tipo que se define en el ámbito especificado, que está fuera del ámbito actual.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
HRESULT DefineTypeRefByName (   
    [in]  mdToken     tkResolutionScope,   
    [in]  LPCWSTR     szName,   
    [out] mdTypeRef   *ptr   
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 `tkResolutionScope`  
 [in] El token que especifica el ámbito de resolución. Los siguientes tipos de token son válidos:  
  
-   `mdModuleRef`, si el tipo se define en el mismo ensamblado en el que se define el llamador.  
  
-   `mdAssemblyRef`, si el tipo está definido en un ensamblado distinto de aquél donde se define el autor de llamada.  
  
-   `mdTypeRef`, si el tipo es un tipo anidado.  
  
-   `mdModule`, si el tipo se define en el mismo módulo en el que se define el llamador.  
  
-   Es null, si el tipo está definido globalmente.  
  
 `szName`  
 [in] El nombre del tipo de destino en Unicode.  
  
 `ptr`  
 [out] Un puntero a la `mdTypeRef` símbolo (token) que se asigna al tipo.  
  
## <a name="requirements"></a>Requisitos  
 **Plataformas:** Consulte [Requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Encabezado**: Cor.h  
  
 **Biblioteca:** Usar como un recurso en MSCorEE.dll  
  
 **Versiones de .NET Framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Vea también
- [IMetaDataEmit (interfaz)](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [IMetaDataEmit2 (interfaz)](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
