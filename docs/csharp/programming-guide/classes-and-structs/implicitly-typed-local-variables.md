---
title: Variables locales con asignación implícita de tipos (Guía de programación de C#)
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- implicitly-typed local variables [C#]
- var [C#]
ms.assetid: b9218fb2-ef5d-4814-8a8e-2bc29b0bbc9b
ms.openlocfilehash: 9c6f7ae5d7a579abead2a62f8fdc7c63e5c53328
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "54222716"
---
# <a name="implicitly-typed-local-variables-c-programming-guide"></a>Variables locales con asignación implícita de tipos (Guía de programación de C#)

Las variables locales pueden declararse sin proporcionar un tipo explícito. La palabra clave `var` indica al compilador que infiera el tipo de la variable a partir de la expresión de la derecha de la instrucción de inicialización. El tipo inferido puede ser un tipo integrado, un tipo anónimo, un tipo definido por el usuario o un tipo definido en la biblioteca de clases .NET Framework. Para obtener más información sobre cómo inicializar las matrices con `var`, vea [Matrices con tipo implícito](../arrays/implicitly-typed-arrays.md).

Los ejemplos siguientes muestran distintas formas en que se pueden declarar variables locales con `var`:

[!code-csharp[csProgGuideLINQ#43](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideLINQ/CS/csRef30LangFeatures_2.cs#43)]

Es importante comprender que la palabra clave `var` no significa "variant" ni indica que la variable esté débilmente tipada o esté enlazada en tiempo de ejecución. Solo significa que el compilador determina y asigna el tipo más adecuado.

La palabra clave `var` se puede usar en los contextos siguientes:

- En variables locales (variables declaradas en el ámbito del método), tal y como se muestra en el ejemplo anterior.

- En una instrucción de inicialización [for](../../language-reference/keywords/for.md).

    ```csharp
    for(var x = 1; x < 10; x++)
    ```

- En una instrucción de inicialización [foreach](../../language-reference/keywords/foreach-in.md).

    ```csharp
    foreach(var item in list){...}
    ```

- En una instrucción [using](../../language-reference/keywords/using-statement.md).

    ```csharp
    using (var file = new StreamReader("C:\\myfile.txt")) {...}
    ```

Para obtener más información, vea [Cómo: Usar matrices y variables locales con tipo implícito en expresiones de consulta](how-to-use-implicitly-typed-local-variables-and-arrays-in-a-query-expression.md).

## <a name="var-and-anonymous-types"></a>var y tipos anónimos

En muchos casos, el uso de `var` es opcional y es simplemente una comodidad sintáctica. Pero cuando una variable se inicializa con un tipo anónimo, la variable se debe declarar como `var` si necesita acceder más adelante a las propiedades del objeto. Se trata de un escenario común en expresiones de consulta [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)]. Para obtener más información, consulte [Anonymous Types](anonymous-types.md) (Tipos anónimos [Guía de programación de C#]).

Desde el punto de vista del código fuente, un tipo anónimo no tiene nombre. Por lo tanto, si una variable de consulta se ha inicializado con `var`, la única manera de tener acceso a las propiedades de la secuencia de objetos devuelta consiste en usar `var` como el tipo de la variable de iteración en la instrucción `foreach`.

[!code-csharp[csProgGuideLINQ#44](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideLINQ/CS/csRef30LangFeatures_2.cs#44)]

## <a name="remarks"></a>Comentarios

Las siguientes restricciones se aplican a las declaraciones de variable con tipo implícito:

- `var` solo se puede usar cuando una variable local se declara e inicializa en la misma instrucción; la variable no se puede inicializar en null ni en un grupo de métodos o una función anónima.

- `var` no se puede usar en campos en el ámbito de clase.

- Las variables declaradas con `var` no se pueden usar en la expresión de inicialización. En otras palabras, esta expresión es válida `: int i = (i = 20);`, pero esta expresión genera un error en tiempo de compilación: `var i = (i = 20);`

- No se pueden inicializar varias variables con tipo implícito en la misma instrucción.

- Si en el ámbito se encuentra un tipo con nombre `var`, la palabra clave `var` se resolverá en ese nombre de tipo y no se tratará como parte de una declaración de variable local con tipo implícito.

Es posible que `var` también pueda resultar útil con expresiones de consulta en las que es difícil determinar el tipo construido exacto de la variable de consulta. Esto puede ocurrir con las operaciones de agrupamiento y ordenación.

La palabra clave `var` también puede ser útil cuando resulte tedioso escribir el tipo específico de la variable en el teclado, o sea obvio o no aumente la legibilidad del código. Un ejemplo en el que `var` resulta útil de esta manera es cuando se usa con tipos genéricos anidados, como los que se emplean con las operaciones de grupo. En la siguiente consulta, el tipo de la variable de consulta es `IEnumerable<IGrouping<string, Student>>`. Siempre que usted y otras personas que deban mantener el código comprendan esto, no hay ningún problema con el uso de tipos implícitos por comodidad y brevedad.

[!code-csharp[cscsrefQueryKeywords#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/CsCsrefQueryKeywords/CS/Group.cs#13)]

Pero el uso de `var` supone al menos la posibilidad de que el código sea más difícil de comprender para otros programadores. Por ese motivo, la documentación de C# por lo general solo usa `var` cuando es necesario.

## <a name="see-also"></a>Vea también

- [Referencia de C#](../../language-reference/index.md)
- [Matrices con tipo implícito](../arrays/implicitly-typed-arrays.md)
- [Cómo: Usar matrices y variables locales con tipo implícito en expresiones de consulta](how-to-use-implicitly-typed-local-variables-and-arrays-in-a-query-expression.md)
- [Tipos anónimos](anonymous-types.md)
- [Inicializadores de objeto y colección](object-and-collection-initializers.md)
- [var](../../language-reference/keywords/var.md)
- [Expresiones de consulta LINQ](../linq-query-expressions/index.md)
- [LINQ (Language Integrated Query)](../../linq/index.md)
- [for](../../language-reference/keywords/for.md)
- [foreach, in](../../language-reference/keywords/foreach-in.md)
- [using (instrucción)](../../language-reference/keywords/using-statement.md)