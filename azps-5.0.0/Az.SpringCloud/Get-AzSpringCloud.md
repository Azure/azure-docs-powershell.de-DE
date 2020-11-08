---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: 39324dc0f85ca4d6f9c3498fae92c340e2113dad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175447"
---
# <span data-ttu-id="f8336-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="f8336-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="f8336-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8336-102">SYNOPSIS</span></span>
<span data-ttu-id="f8336-103">Rufen Sie einen Dienst und dessen Eigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="f8336-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="f8336-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8336-104">SYNTAX</span></span>

### <span data-ttu-id="f8336-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8336-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f8336-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="f8336-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f8336-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f8336-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f8336-108">List1</span><span class="sxs-lookup"><span data-stu-id="f8336-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8336-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8336-109">DESCRIPTION</span></span>
<span data-ttu-id="f8336-110">Rufen Sie einen Dienst und dessen Eigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="f8336-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="f8336-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8336-111">EXAMPLES</span></span>

### <span data-ttu-id="f8336-112">Beispiel 1: Abrufen des Spring Cloud-Diensts nach Namen</span><span class="sxs-lookup"><span data-stu-id="f8336-112">Example 1: Get Spring Cloud Service by name</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="f8336-113">Abrufen des Spring Cloud-Diensts nach Namen</span><span class="sxs-lookup"><span data-stu-id="f8336-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="f8336-114">Beispiel 2: Auflisten des gesamten Spring Cloud-Diensts unter der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f8336-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="f8336-115">Auflisten des gesamten Spring Cloud-Diensts unter der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f8336-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="f8336-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8336-116">PARAMETERS</span></span>

### <span data-ttu-id="f8336-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8336-117">-DefaultProfile</span></span>
<span data-ttu-id="f8336-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8336-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8336-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f8336-119">-InputObject</span></span>
<span data-ttu-id="f8336-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f8336-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8336-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f8336-121">-Name</span></span>
<span data-ttu-id="f8336-122">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="f8336-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8336-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8336-123">-ResourceGroupName</span></span>
<span data-ttu-id="f8336-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="f8336-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f8336-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="f8336-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8336-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f8336-126">-SubscriptionId</span></span>
<span data-ttu-id="f8336-127">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f8336-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f8336-128">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="f8336-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8336-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8336-129">CommonParameters</span></span>
<span data-ttu-id="f8336-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8336-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8336-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8336-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8336-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8336-132">INPUTS</span></span>

### <span data-ttu-id="f8336-133">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="f8336-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="f8336-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8336-134">OUTPUTS</span></span>

### <span data-ttu-id="f8336-135">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20200701. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="f8336-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="f8336-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8336-136">NOTES</span></span>

<span data-ttu-id="f8336-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="f8336-137">ALIASES</span></span>

<span data-ttu-id="f8336-138">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f8336-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f8336-139">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f8336-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f8336-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="f8336-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f8336-141">Inputobject <ISpringCloudIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="f8336-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f8336-142">`[AppName <String>]`: Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="f8336-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="f8336-143">`[BindingName <String>]`: Der Name der Bindungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="f8336-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="f8336-144">`[CertificateName <String>]`: Der Name der Zertifikat Ressource.</span><span class="sxs-lookup"><span data-stu-id="f8336-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="f8336-145">`[DeploymentName <String>]`: Der Name der Bereitstellungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="f8336-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="f8336-146">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="f8336-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="f8336-147">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="f8336-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f8336-148">`[Location <String>]`: die Region</span><span class="sxs-lookup"><span data-stu-id="f8336-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="f8336-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="f8336-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f8336-150">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="f8336-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f8336-151">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="f8336-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="f8336-152">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f8336-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="f8336-153">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="f8336-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f8336-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8336-154">RELATED LINKS</span></span>

