---
title: <httpDigest> (Elemento)
ms.date: 03/30/2017
ms.assetid: 3da4f276-dfd9-4247-8c07-01d83618727c
ms.openlocfilehash: c930efbc2cd7a6dc12795d5ac1c26ea92fc36599
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/30/2019
ms.locfileid: "55259012"
---
# <a name="httpdigest-element"></a>\<httpDigest > elemento
Especifica una credencial de tipo de resumen utilizada al autenticar el cliente a un servicio.  
  
 \<system.ServiceModel>  
\<comportamientos >  
\<endpointBehaviors>  
\<comportamiento >  
\<clientCredentials>  
\<httpDigest>  
  
## <a name="syntax"></a>Sintaxis  
  
```xml  
<digest impersonationLevel="Identification/Impersonation/Delegation/Anonymous/None" />
```  
  
## <a name="attributes-and-elements"></a>Atributos y elementos  
 En las siguientes secciones se describen los atributos, los elementos secundarios y los elementos primarios.  
  
### <a name="attributes"></a>Atributos  
  
|Atributo|Descripción|  
|---------------|-----------------|  
|`impersonationLevel`|Establece la preferencia de suplantación que el cliente comunica al servidor. El modo de suplantación que el cliente elige no se exige en el servidor. Los valores válidos son los siguientes:<br /><br /> -Identificación: El servidor puede obtener la identidad y los privilegios del cliente, pero no puede suplantar al cliente.<br />-Suplantación: El servidor puede suplantar el contexto de seguridad del cliente en el sistema local.<br />-Delegación: El servidor puede suplantar el contexto de seguridad del cliente en sistemas remotos.<br />-Anónimo: El servidor no puede suplantar o identificar al cliente.<br />-None: No se asigna un nivel de suplantación.<br /><br /> El valor predeterminado es Identification. Este atributo es del tipo <xref:System.Security.Principal.TokenImpersonationLevel>.|  
  
### <a name="child-elements"></a>Elementos secundarios  
 Ninguna  
  
### <a name="parent-elements"></a>Elementos primarios  
  
|Elemento|Descripción|  
|-------------|-----------------|  
|[\<clientCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)|Especifica las credenciales usadas para autenticar un cliente a un servicio.|  
  
## <a name="remarks"></a>Comentarios  
 Un resumen es un hash determinado mediante un algoritmo y un conjunto de entradas. El autenticador y los autenticados están de acuerdo en un algoritmo e intercambian los datos utilizados como entradas. El cliente puede calcular el hash y enviarlo al servicio. El servicio también calcula el hash y compara los valores. La coincidencia valida al cliente.  
  
 Esta característica se debe habilitar con Active Directory en Windows e Internet Information Services (IIS). Para obtener más información, consulte [la autenticación implícita en IIS 6.0](https://go.microsoft.com/fwlink/?LinkId=88443).  
  
## <a name="see-also"></a>Vea también
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement.HttpDigest%2A>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Description.ClientCredentials.HttpDigest%2A>
- <xref:System.ServiceModel.Configuration.HttpDigestClientElement>
- <xref:System.ServiceModel.Security.HttpDigestClientCredential>
- [Comportamientos de seguridad](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [Protección de clientes](../../../../../docs/framework/wcf/securing-clients.md)
- [Trabajo con certificados](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)
- [Protección de servicios y clientes](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
