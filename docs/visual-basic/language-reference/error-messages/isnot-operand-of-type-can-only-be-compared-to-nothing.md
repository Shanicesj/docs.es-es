---
title: El operando 'IsNot' de tipo 'nombreDeTipo' solo se puede comparar con 'Nothing', porque 'nombreDeTipo' es un tipo que acepta valores NULL
ms.date: 07/20/2015
f1_keywords:
- bc32128
- vbc32128
helpviewer_keywords:
- BC32128
ms.assetid: 1155b23a-ad75-4bab-b9da-73f35c767a36
ms.openlocfilehash: caa009606825225dd4063780f9a22fb82f21cf4e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271296"
---
# <a name="isnot-operand-of-type-typename-can-only-be-compared-to-nothing-because-typename-is-a-nullable-type"></a>El operando 'IsNot' de tipo 'nombreDeTipo' solo se puede comparar con 'Nothing', porque 'nombreDeTipo' es un tipo que acepta valores NULL
Una variable declarada como que acepta valores NULL se ha comparado con una expresión distinta `Nothing` utilizando el `IsNot` operador.  
  
 **Identificador de error:** BC32128  
  
## <a name="to-correct-this-error"></a>Para corregir este error  
  
1.  Para comparar un tipo que acepta valores NULL con una expresión distinta de `Nothing` con el operador `IsNot` , llame al método `GetType` en el tipo que acepta valores NULL y compare el resultado con la expresión, como se muestra en el ejemplo siguiente.  
  
```vb  
Dim number? As Integer = 5  
  
If number IsNot Nothing Then  
  If number.GetType() IsNot Type.GetType("System.Int32") Then   
  
  End If  
End If  
```  
  
## <a name="see-also"></a>Vea también
- [Tipos de valor que aceptan valores NULL](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
- [IsNot (operador)](../../../visual-basic/language-reference/operators/isnot-operator.md)
