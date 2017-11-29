---
title: "Funciones estáticas globales para la depuración"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
helpviewer_keywords:
- global static functions [.NET Framework debugging]
- debugging global static functions [.NET Framework]
- unmanaged global static functions [.NET Framework], debugging
ms.assetid: efc64414-77c3-48d0-881a-8594ed416aad
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: ad5d3ef689a251ea4b154afc5d1bfb387388ddb3
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="debugging-global-static-functions"></a><span data-ttu-id="4035b-102">Funciones estáticas globales para la depuración</span><span class="sxs-lookup"><span data-stu-id="4035b-102">Debugging Global Static Functions</span></span>
<span data-ttu-id="4035b-103">Esta sección describe las funciones estáticas globales no administradas que utiliza la API de depuración.</span><span class="sxs-lookup"><span data-stu-id="4035b-103">This section describes the unmanaged global static functions that the debugging API uses.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="4035b-104">En esta sección</span><span class="sxs-lookup"><span data-stu-id="4035b-104">In This Section</span></span>  
 [<span data-ttu-id="4035b-105">_EFN_GetManagedExcepStack (función)</span><span class="sxs-lookup"><span data-stu-id="4035b-105">_EFN_GetManagedExcepStack Function</span></span>](../../../../docs/framework/unmanaged-api/debugging/efn-getmanagedexcepstack-function.md)  
 <span data-ttu-id="4035b-106">Dada una dirección de objeto de excepción administrado, devuelve una versión de cadena del seguimiento de pila que contiene.</span><span class="sxs-lookup"><span data-stu-id="4035b-106">Given a managed exception object address, returns a string version of the stack trace contained inside.</span></span>  
  
 [<span data-ttu-id="4035b-107">_EFN_GetManagedObjectFieldInfo (función)</span><span class="sxs-lookup"><span data-stu-id="4035b-107">_EFN_GetManagedObjectFieldInfo Function</span></span>](../../../../docs/framework/unmanaged-api/debugging/efn-getmanagedobjectfieldinfo-function.md)  
 <span data-ttu-id="4035b-108">Obtiene el desplazamiento desde el inicio de un objeto hasta un campo y el valor del campo, a partir del puntero de objeto y nombre de campo especificados.</span><span class="sxs-lookup"><span data-stu-id="4035b-108">Gets the offset from the start of an object to a field and the field's value, using the provided object pointer and field name.</span></span>  
  
 [<span data-ttu-id="4035b-109">_EFN_GetManagedObjectName (función)</span><span class="sxs-lookup"><span data-stu-id="4035b-109">_EFN_GetManagedObjectName Function</span></span>](../../../../docs/framework/unmanaged-api/debugging/efn-getmanagedobjectname-function.md)  
 <span data-ttu-id="4035b-110">Obtiene el nombre de un tipo mediante el puntero de objeto administrado proporcionado.</span><span class="sxs-lookup"><span data-stu-id="4035b-110">Gets the name of a type by using the provided managed object pointer.</span></span>  
  
 [<span data-ttu-id="4035b-111">_EFN_StackTrace (función)</span><span class="sxs-lookup"><span data-stu-id="4035b-111">_EFN_StackTrace Function</span></span>](../../../../docs/framework/unmanaged-api/debugging/efn-stacktrace-function.md)  
 <span data-ttu-id="4035b-112">Proporciona una representación de texto de un seguimiento de pila administrado y una matriz de registros `CONTEXT`, uno por cada transición entre código no administrado y código administrado.</span><span class="sxs-lookup"><span data-stu-id="4035b-112">Provides a text representation of a managed stack trace and an array of `CONTEXT` records, one for each transition between unmanaged and managed code.</span></span>  
  
 [<span data-ttu-id="4035b-113">CLRDataCreateInstance (función)</span><span class="sxs-lookup"><span data-stu-id="4035b-113">CLRDataCreateInstance Function</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatacreateinstance-function.md)  
 <span data-ttu-id="4035b-114">Los servicios de acceso a datos de Common Language Runtime (CLR) llaman a esta función para crear el objeto de interfaz especificado para el proceso de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="4035b-114">Called by the common language runtime (CLR) data access services to create the specified interface object for the specified target process.</span></span>  
  
 [<span data-ttu-id="4035b-115">La función Pfn_clrdatacreateinstance</span><span class="sxs-lookup"><span data-stu-id="4035b-115">PFN_CLRDataCreateInstance Function Pointer</span></span>](../../../../docs/framework/unmanaged-api/debugging/pfn-clrdatacreateinstance-function-pointer.md)  
 <span data-ttu-id="4035b-116">Señala una función a la que llaman los servicios de acceso a datos de CLR para crear el objeto de interfaz especificado para el proceso de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="4035b-116">Points to a function that is called by the CLR data access services to create the specified interface object for the specified target process.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="4035b-117">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="4035b-117">Related Sections</span></span>  
 [<span data-ttu-id="4035b-118">Coclases para la depuración</span><span class="sxs-lookup"><span data-stu-id="4035b-118">Debugging Coclasses</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-coclasses.md)  
  
 [<span data-ttu-id="4035b-119">Interfaces de depuración</span><span class="sxs-lookup"><span data-stu-id="4035b-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
  
 [<span data-ttu-id="4035b-120">Enumeraciones de depuración</span><span class="sxs-lookup"><span data-stu-id="4035b-120">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)  
  
 [<span data-ttu-id="4035b-121">Estructuras de depuración</span><span class="sxs-lookup"><span data-stu-id="4035b-121">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)