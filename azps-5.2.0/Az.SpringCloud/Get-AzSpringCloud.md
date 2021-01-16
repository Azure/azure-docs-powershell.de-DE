---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: 39324dc0f85ca4d6f9c3498fae92c340e2113dad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295774"
---
# <span data-ttu-id="09198-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="09198-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="09198-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09198-102">SYNOPSIS</span></span>
<span data-ttu-id="09198-103">Einen Dienst und dessen Eigenschaften erhalten.</span><span class="sxs-lookup"><span data-stu-id="09198-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="09198-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09198-104">SYNTAX</span></span>

### <span data-ttu-id="09198-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="09198-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="09198-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="09198-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="09198-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="09198-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="09198-108">Liste1</span><span class="sxs-lookup"><span data-stu-id="09198-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="09198-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09198-109">DESCRIPTION</span></span>
<span data-ttu-id="09198-110">Einen Dienst und dessen Eigenschaften erhalten.</span><span class="sxs-lookup"><span data-stu-id="09198-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="09198-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="09198-111">EXAMPLES</span></span>

### <span data-ttu-id="09198-112">Beispiel 1: Quell-Cloud-Dienst nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="09198-112">Example 1: Get Spring Cloud Service by name</span></span>
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

<span data-ttu-id="09198-113">Spring Cloud Service nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="09198-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="09198-114">Beispiel 2: Listen Sie den ganzen Quell-Cloud-Dienst unter der Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="09198-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="09198-115">Listen Sie den sämtlichen Quell-Cloud-Dienst unter der Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="09198-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="09198-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09198-116">PARAMETERS</span></span>

### <span data-ttu-id="09198-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09198-117">-DefaultProfile</span></span>
<span data-ttu-id="09198-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="09198-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09198-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09198-119">-InputObject</span></span>
<span data-ttu-id="09198-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="09198-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="09198-121">-Name</span><span class="sxs-lookup"><span data-stu-id="09198-121">-Name</span></span>
<span data-ttu-id="09198-122">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="09198-122">The name of the Service resource.</span></span>

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

### <span data-ttu-id="09198-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09198-123">-ResourceGroupName</span></span>
<span data-ttu-id="09198-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="09198-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="09198-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="09198-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="09198-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09198-126">-SubscriptionId</span></span>
<span data-ttu-id="09198-127">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="09198-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="09198-128">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="09198-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="09198-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09198-129">CommonParameters</span></span>
<span data-ttu-id="09198-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09198-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09198-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09198-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09198-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="09198-132">INPUTS</span></span>

### <span data-ttu-id="09198-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="09198-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="09198-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="09198-134">OUTPUTS</span></span>

### <span data-ttu-id="09198-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="09198-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="09198-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="09198-136">NOTES</span></span>

<span data-ttu-id="09198-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="09198-137">ALIASES</span></span>

<span data-ttu-id="09198-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="09198-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="09198-139">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="09198-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="09198-140">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="09198-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="09198-141">INPUTOBJECT <ISpringCloudIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="09198-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="09198-142">`[AppName <String>]`: Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="09198-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="09198-143">`[BindingName <String>]`: Der Name der Bindungsressource.</span><span class="sxs-lookup"><span data-stu-id="09198-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="09198-144">`[CertificateName <String>]`: Der Name der Zertifikatressource.</span><span class="sxs-lookup"><span data-stu-id="09198-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="09198-145">`[DeploymentName <String>]`: Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="09198-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="09198-146">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="09198-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="09198-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="09198-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="09198-148">`[Location <String>]`: Die Region</span><span class="sxs-lookup"><span data-stu-id="09198-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="09198-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="09198-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="09198-150">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="09198-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="09198-151">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="09198-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="09198-152">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="09198-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="09198-153">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="09198-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="09198-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="09198-154">RELATED LINKS</span></span>

