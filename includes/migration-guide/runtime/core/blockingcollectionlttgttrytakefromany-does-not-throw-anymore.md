### <a name="blockingcollectionlttgttrytakefromany-does-not-throw-anymore"></a><span data-ttu-id="81bba-101">BlockingCollection&lt;T&gt;.TryTakeFromAny ya no inicia excepciones</span><span class="sxs-lookup"><span data-stu-id="81bba-101">BlockingCollection&lt;T&gt;.TryTakeFromAny does not throw anymore</span></span>

|   |   |
|---|---|
|<span data-ttu-id="81bba-102">Detalles</span><span class="sxs-lookup"><span data-stu-id="81bba-102">Details</span></span>|<span data-ttu-id="81bba-103">Si alguna de las colecciones de entrada está marcada como completada, <xref:System.Collections.Concurrent.BlockingCollection%601.TryTakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@)> no devuelve -1 y <xref:System.Collections.Concurrent.BlockingCollection%601.TakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@)> deja de iniciar una excepción.</span><span class="sxs-lookup"><span data-stu-id="81bba-103">If one of the input collections is marked completed, <xref:System.Collections.Concurrent.BlockingCollection%601.TryTakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@)> no longer returns -1 and <xref:System.Collections.Concurrent.BlockingCollection%601.TakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@)> no longer throws an exception.</span></span> <span data-ttu-id="81bba-104">Este cambio permite trabajar con colecciones cuando una de las colecciones está vacía o completa y la otra colección todavía tiene elementos que se pueden recuperar.</span><span class="sxs-lookup"><span data-stu-id="81bba-104">This change makes it possible to work with collections when one of the collections is either empty or completed, but the other collection still has items that can be retrieved.</span></span>|
|<span data-ttu-id="81bba-105">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="81bba-105">Suggestion</span></span>|<span data-ttu-id="81bba-106">Si se han usado un método TryTakeFromAny que devuelva -1 o un método TakeFromAny de inicio para el control de flujo en casos en los que se complete una recolección de bloqueo, es necesario cambiar dicho código para que use <code>.Any(b =&gt; b.IsCompleted)</code> para detectar dicha condición.</span><span class="sxs-lookup"><span data-stu-id="81bba-106">If TryTakeFromAny returning -1 or TakeFromAny throwing were used for control-flow purposes in cases of a blocking collection being completed, such code should now be changed to use <code>.Any(b =&gt; b.IsCompleted)</code> to detect that condition.</span></span>|
|<span data-ttu-id="81bba-107">Ámbito</span><span class="sxs-lookup"><span data-stu-id="81bba-107">Scope</span></span>|<span data-ttu-id="81bba-108">Secundaria</span><span class="sxs-lookup"><span data-stu-id="81bba-108">Minor</span></span>|
|<span data-ttu-id="81bba-109">Versión</span><span class="sxs-lookup"><span data-stu-id="81bba-109">Version</span></span>|<span data-ttu-id="81bba-110">4.5</span><span class="sxs-lookup"><span data-stu-id="81bba-110">4.5</span></span>|
|<span data-ttu-id="81bba-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="81bba-111">Type</span></span>|<span data-ttu-id="81bba-112">Tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="81bba-112">Runtime</span></span>|
|<span data-ttu-id="81bba-113">API afectadas</span><span class="sxs-lookup"><span data-stu-id="81bba-113">Affected APIs</span></span>|<ul><li><xref:System.Collections.Concurrent.BlockingCollection%601.TakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@)?displayProperty=nameWithType></li><li><xref:System.Collections.Concurrent.BlockingCollection%601.TakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@,System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Collections.Concurrent.BlockingCollection%601.TryTakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@)?displayProperty=nameWithType></li><li><xref:System.Collections.Concurrent.BlockingCollection%601.TryTakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@,System.Int32)?displayProperty=nameWithType></li><li><xref:System.Collections.Concurrent.BlockingCollection%601.TryTakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@,System.TimeSpan)?displayProperty=nameWithType></li><li><xref:System.Collections.Concurrent.BlockingCollection%601.TryTakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@,System.TimeSpan)?displayProperty=nameWithType></li></ul>|
