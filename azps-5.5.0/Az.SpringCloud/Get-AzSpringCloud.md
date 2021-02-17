---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: 39324dc0f85ca4d6f9c3498fae92c340e2113dad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156252"
---
# <span data-ttu-id="85b52-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="85b52-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="85b52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85b52-102">SYNOPSIS</span></span>
<span data-ttu-id="85b52-103">Einen Dienst und dessen Eigenschaften erhalten.</span><span class="sxs-lookup"><span data-stu-id="85b52-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="85b52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85b52-104">SYNTAX</span></span>

### <span data-ttu-id="85b52-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="85b52-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="85b52-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="85b52-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="85b52-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="85b52-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="85b52-108">Liste1</span><span class="sxs-lookup"><span data-stu-id="85b52-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="85b52-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85b52-109">DESCRIPTION</span></span>
<span data-ttu-id="85b52-110">Einen Dienst und dessen Eigenschaften erhalten.</span><span class="sxs-lookup"><span data-stu-id="85b52-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="85b52-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="85b52-111">EXAMPLES</span></span>

### <span data-ttu-id="85b52-112">Beispiel 1: Quell-Cloud-Dienst nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="85b52-112">Example 1: Get Spring Cloud Service by name</span></span>
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

<span data-ttu-id="85b52-113">Spring Cloud Service nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="85b52-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="85b52-114">Beispiel 2: Auflisten des sämtlichen Quell-Cloud-Diensts unter der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="85b52-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="85b52-115">Listen Sie den sämtlichen Quell-Cloud-Dienst unter der Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="85b52-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="85b52-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85b52-116">PARAMETERS</span></span>

### <span data-ttu-id="85b52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85b52-117">-DefaultProfile</span></span>
<span data-ttu-id="85b52-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85b52-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85b52-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85b52-119">-InputObject</span></span>
<span data-ttu-id="85b52-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="85b52-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="85b52-121">-Name</span><span class="sxs-lookup"><span data-stu-id="85b52-121">-Name</span></span>
<span data-ttu-id="85b52-122">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="85b52-122">The name of the Service resource.</span></span>

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

### <span data-ttu-id="85b52-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85b52-123">-ResourceGroupName</span></span>
<span data-ttu-id="85b52-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="85b52-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="85b52-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="85b52-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="85b52-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85b52-126">-SubscriptionId</span></span>
<span data-ttu-id="85b52-127">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="85b52-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="85b52-128">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="85b52-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="85b52-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85b52-129">CommonParameters</span></span>
<span data-ttu-id="85b52-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85b52-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85b52-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85b52-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85b52-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="85b52-132">INPUTS</span></span>

### <span data-ttu-id="85b52-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="85b52-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="85b52-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="85b52-134">OUTPUTS</span></span>

### <span data-ttu-id="85b52-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="85b52-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="85b52-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="85b52-136">NOTES</span></span>

<span data-ttu-id="85b52-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="85b52-137">ALIASES</span></span>

<span data-ttu-id="85b52-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="85b52-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="85b52-139">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="85b52-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="85b52-140">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="85b52-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="85b52-141">INPUTOBJECT <ISpringCloudIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="85b52-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="85b52-142">`[AppName <String>]`: Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="85b52-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="85b52-143">`[BindingName <String>]`: Der Name der Bindungsressource.</span><span class="sxs-lookup"><span data-stu-id="85b52-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="85b52-144">`[CertificateName <String>]`: Der Name der Zertifikatressource.</span><span class="sxs-lookup"><span data-stu-id="85b52-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="85b52-145">`[DeploymentName <String>]`: Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="85b52-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="85b52-146">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="85b52-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="85b52-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="85b52-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="85b52-148">`[Location <String>]`: Die Region</span><span class="sxs-lookup"><span data-stu-id="85b52-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="85b52-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="85b52-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="85b52-150">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="85b52-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="85b52-151">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="85b52-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="85b52-152">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="85b52-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="85b52-153">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="85b52-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="85b52-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="85b52-154">RELATED LINKS</span></span>

