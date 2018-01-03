---
title: Flujo de trabajo de DevOps para aplicaciones de Docker con herramientas de Microsoft
description: Ciclo de vida de aplicaciones de Docker en contenedor con la plataforma de Microsoft y flujo de trabajo de DevOps de aplicaciones con las herramientas de Microsoft
keywords: Docker, microservicios, ASP.NET, contenedor
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: b6a625cdf7a27748c4278c1b3f04db33a390712e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="docker-application-devops-workflow-with-microsoft-tools"></a><span data-ttu-id="46d9a-104">Flujo de trabajo de DevOps para aplicaciones de Docker con herramientas de Microsoft</span><span class="sxs-lookup"><span data-stu-id="46d9a-104">Docker application DevOps workflow with Microsoft tools</span></span>

<span data-ttu-id="46d9a-105">Microsoft Visual Studio, Visual Studio Team Services, Team Foundation Server y Application Insights proporcionan un ecosistema completo para el desarrollo y las operaciones de TI que proporcionan a su equipo las herramientas para administrar proyectos y compilar, probar e implementar rápidamente las aplicaciones en contenedor.</span><span class="sxs-lookup"><span data-stu-id="46d9a-105">Microsoft Visual Studio, Visual Studio Team Services, Team Foundation Server, and Application Insights provide a comprehensive ecosystem for development and IT operations that give your team the tools to manage projects and rapidly build, test, and deploy containerized applications.</span></span>

<span data-ttu-id="46d9a-106">Con Visual Studio y Visual Studio Team Services en la nube, junto con Team Foundation Server local, los equipos de desarrollo puede crear, probar y publicar aplicaciones en contenedor de manera productiva dirigidas a cualquier plataforma (Windows o Linux).</span><span class="sxs-lookup"><span data-stu-id="46d9a-106">With Visual Studio and Visual Studio Team Services in the cloud, along with Team Foundation Server on-premises, development teams can productively build, test, and release containerized applications directed toward any platform (Windows or Linux).</span></span>

<span data-ttu-id="46d9a-107">Las herramientas de Microsoft puede automatizar la canalización de implementaciones específicas de aplicaciones en contenedor (Docker, .NET Core o cualquier combinación con otras plataformas) desde compilaciones globales e integración continua y pruebas con Visual Studio Team Services o Team Foundation Server, a fin de realizar una implementación continua en entornos de Docker (desarrollo, almacenamiento provisional y producción) y para transmitir información de análisis sobre los servicios al equipo de desarrollo a través de Application Insights.</span><span class="sxs-lookup"><span data-stu-id="46d9a-107">Microsoft tools can automate the pipeline for specific implementations of containerized applications—Docker, .NET Core, or any combination with other platforms—from global builds and Continuous Integration (CI) and tests with Visual Studio Team Services or Team Foundation Server, to Continuous Deployment (CD) to Docker environments (Development, Staging, Production), and to transmit analytics information about the services to the development team through Application Insights.</span></span> <span data-ttu-id="46d9a-108">Cada confirmación de código puede iniciar una compilación (CI) e implementar automáticamente los servicios en entornos en contenedores específicos (CD).</span><span class="sxs-lookup"><span data-stu-id="46d9a-108">Every code commit can initiate a build (CI) and automatically deploy the services to specific containerized environments (CD).</span></span>

<span data-ttu-id="46d9a-109">Los desarrolladores y evaluadores pueden aprovisionar con facilidad y rapidez entornos de prueba y desarrollo tipo producción basados en Docker con el uso de plantillas de Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="46d9a-109">Developers and testers can easily and quickly provision production-like development and test environments based on Docker by using templates in Microsoft Azure.</span></span>

<span data-ttu-id="46d9a-110">La complejidad del desarrollo de aplicaciones en contenedores aumenta de forma constante según las necesidades empresariales de complejidad y escalabilidad.</span><span class="sxs-lookup"><span data-stu-id="46d9a-110">The complexity of containerized application development increases steadily depending on the business complexity and scalability needs.</span></span> <span data-ttu-id="46d9a-111">Un buen ejemplo de esto son las aplicaciones basadas en arquitecturas de microservicios.</span><span class="sxs-lookup"><span data-stu-id="46d9a-111">A good example of this are applications based on microservices architectures.</span></span> <span data-ttu-id="46d9a-112">Para tener éxito en un entorno de este tipo, el proyecto debe automatizar todo el ciclo de vida, no solo la compilación y el desarrollo, sino que también debe administrar versiones junto con la colección de telemetría.</span><span class="sxs-lookup"><span data-stu-id="46d9a-112">To succeed in such an environment, your project must automate the entire life cycle—not only the build and deployment, but it also must manage versions along with the collection of telemetry.</span></span> <span data-ttu-id="46d9a-113">Visual Studio Team Services y Azure ofrecen las siguientes funcionalidades:</span><span class="sxs-lookup"><span data-stu-id="46d9a-113">Visual Studio Team Services and Azure offer the following capabilities:</span></span>

-   <span data-ttu-id="46d9a-114">Administración del código fuente de Visual Studio Team Services/Team Foundation Server (basada en Git o en el Control de versiones de Team Foundation), planeación de Agile (Agile, Scrum y CMMI son compatibles), integración continua, administración de versiones y otras herramientas para equipos de Agile.</span><span class="sxs-lookup"><span data-stu-id="46d9a-114">Visual Studio Team Services/Team Foundation Server source code management (based on Git or Team Foundation Version Control), Agile planning (Agile, Scrum, and CMMI are supported), CI, release management, and other tools for Agile teams.</span></span>

-   <span data-ttu-id="46d9a-115">Visual Studio Team Services/Team Foundation Server incluyen un eficaz y creciente ecosistema de extensiones propias y de terceros con las que puede crear con facilidad una integración continua, así como compilar, probar, entregar y publicar la canalización de administración de microservicios.</span><span class="sxs-lookup"><span data-stu-id="46d9a-115">Visual Studio Team Services/Team Foundation Server include a powerful and growing ecosystem of first- and third-party extensions with which you easily can construct a CI, build, test, delivery, and release management pipeline for microservices.</span></span>

-   <span data-ttu-id="46d9a-116">Ejecutar pruebas automatizadas como parte de la canalización de compilación de Visual Studio Team Services.</span><span class="sxs-lookup"><span data-stu-id="46d9a-116">Run automated tests as part of your build pipeline in Visual Studio Team Services.</span></span>

-   <span data-ttu-id="46d9a-117">Visual Studio Team Services puede reforzar el ciclo de vida de DevOps con la entrega a varios entornos, no solo para entornos de producción, sino también para pruebas, incluida la experimentación de A/B, [versiones de valor controlado](http://martinfowler.com/bliki/CanaryRelease.html), etc.</span><span class="sxs-lookup"><span data-stu-id="46d9a-117">Visual Studio Team Services can tighten the DevOps life cycle with delivery to multiple environments, not just for production environments, but also for testing, including A/B experimentation, [canary releases](http://martinfowler.com/bliki/CanaryRelease.html), and so on.</span></span>

-   <span data-ttu-id="46d9a-118">Las organizaciones pueden aprovisionar fácilmente contenedores de Docker en imágenes privadas almacenadas en Azure Container Registry junto con cualquier dependencia de componentes de Azure (Data, PaaS, etc.) mediante el uso de plantillas de Azure Resource Manager con herramientas con las que se sienten cómodas para trabajar.</span><span class="sxs-lookup"><span data-stu-id="46d9a-118">Organizations easily can provision Docker containers from private images stored in Azure Container Registry along with any dependency on Azure components (Data, PaaS, etc.) using Azure Resource Manager templates with tools with which they are already comfortable working.</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="46d9a-119">[Anterior] (../design-develop-containerized-apps/set-up-windows-containers-with-powershell.md) [Siguiente] (docker-application-outer-loop-devops-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="46d9a-119">[Previous] (../design-develop-containerized-apps/set-up-windows-containers-with-powershell.md) [Next] (docker-application-outer-loop-devops-workflow.md)</span></span>