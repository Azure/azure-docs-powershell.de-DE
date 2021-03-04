---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/update-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
ms.openlocfilehash: 9c9ec2f2a48d3bc94ef0e0ab72b5b2bf4edd9045
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945592"
---
# <span data-ttu-id="7652e-101">Update-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="7652e-101">Update-AzSpringCloud</span></span>

## <span data-ttu-id="7652e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7652e-102">SYNOPSIS</span></span>
<span data-ttu-id="7652e-103">Vorgang zum Aktualisieren eines beendenden Diensts.</span><span class="sxs-lookup"><span data-stu-id="7652e-103">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="7652e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7652e-104">SYNTAX</span></span>

### <span data-ttu-id="7652e-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="7652e-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7652e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7652e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloud -InputObject <ISpringCloudIdentity> [-GitPropertyUri <String>] [-Location <String>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>] [-TraceAppInsightInstrumentationKey <String>]
 [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7652e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7652e-107">DESCRIPTION</span></span>
<span data-ttu-id="7652e-108">Vorgang zum Aktualisieren eines beendenden Diensts.</span><span class="sxs-lookup"><span data-stu-id="7652e-108">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="7652e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7652e-109">EXAMPLES</span></span>

### <span data-ttu-id="7652e-110">Beispiel 1: Aktualisieren des Quellwolkendiensts nach Name.</span><span class="sxs-lookup"><span data-stu-id="7652e-110">Example 1: Update Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
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

<span data-ttu-id="7652e-111">Aktualisieren Sie den Spring Cloud Service nach Name.</span><span class="sxs-lookup"><span data-stu-id="7652e-111">Update Spring Cloud Service by name.</span></span>

### <span data-ttu-id="7652e-112">Beispiel 2: Aktualisieren des Quellwolkendiensts von pipe.</span><span class="sxs-lookup"><span data-stu-id="7652e-112">Example 2: Update Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Update-AzSpringCloud
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

<span data-ttu-id="7652e-113">Aktualisieren Sie den Frühlingswolkendienst über pipe.</span><span class="sxs-lookup"><span data-stu-id="7652e-113">Update Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="7652e-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7652e-114">PARAMETERS</span></span>

### <span data-ttu-id="7652e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7652e-115">-AsJob</span></span>
<span data-ttu-id="7652e-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="7652e-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7652e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7652e-117">-DefaultProfile</span></span>
<span data-ttu-id="7652e-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7652e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7652e-119">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="7652e-119">-GitPropertyUri</span></span>
<span data-ttu-id="7652e-120">URI des Repositorys</span><span class="sxs-lookup"><span data-stu-id="7652e-120">URI of the repository</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7652e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7652e-121">-InputObject</span></span>
<span data-ttu-id="7652e-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7652e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7652e-123">-Location</span><span class="sxs-lookup"><span data-stu-id="7652e-123">-Location</span></span>
<span data-ttu-id="7652e-124">Der GEO-Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="7652e-124">The GEO location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7652e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7652e-125">-Name</span></span>
<span data-ttu-id="7652e-126">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="7652e-126">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7652e-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7652e-127">-NoWait</span></span>
<span data-ttu-id="7652e-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="7652e-128">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7652e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7652e-129">-ResourceGroupName</span></span>
<span data-ttu-id="7652e-130">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="7652e-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7652e-131">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="7652e-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7652e-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7652e-132">-SkuName</span></span>
<span data-ttu-id="7652e-133">Name der Sku</span><span class="sxs-lookup"><span data-stu-id="7652e-133">Name of the Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7652e-134">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="7652e-134">-SkuTier</span></span>
<span data-ttu-id="7652e-135">Stufe der Sku</span><span class="sxs-lookup"><span data-stu-id="7652e-135">Tier of the Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7652e-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7652e-136">-SubscriptionId</span></span>
<span data-ttu-id="7652e-137">Ruft die Abonnement-ID ab, mit der das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="7652e-137">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7652e-138">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="7652e-138">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7652e-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="7652e-139">-Tag</span></span>
<span data-ttu-id="7652e-140">Tags des Diensts, bei dem es sich um eine Liste von Schlüsselwertpaaren handelt, die die Ressource beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7652e-140">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7652e-141">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="7652e-141">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="7652e-142">Instrumentierungsschlüssel für die Zielanwendungserblicke</span><span class="sxs-lookup"><span data-stu-id="7652e-142">Target application insight instrumentation key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7652e-143">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="7652e-143">-TraceEnabled</span></span>
<span data-ttu-id="7652e-144">Gibt an, ob die Ablaufverfolgungsfunktion aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="7652e-144">Indicates whether enable the tracing functionality</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7652e-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7652e-145">-Confirm</span></span>
<span data-ttu-id="7652e-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7652e-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7652e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7652e-147">-WhatIf</span></span>
<span data-ttu-id="7652e-148">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7652e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7652e-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7652e-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7652e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7652e-150">CommonParameters</span></span>
<span data-ttu-id="7652e-151">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7652e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7652e-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7652e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7652e-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7652e-153">INPUTS</span></span>

### <span data-ttu-id="7652e-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="7652e-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="7652e-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7652e-155">OUTPUTS</span></span>

### <span data-ttu-id="7652e-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="7652e-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="7652e-157">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7652e-157">NOTES</span></span>

<span data-ttu-id="7652e-158">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7652e-158">ALIASES</span></span>

<span data-ttu-id="7652e-159">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="7652e-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7652e-160">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="7652e-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7652e-161">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7652e-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7652e-162">INPUTOBJECT <ISpringCloudIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="7652e-162">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7652e-163">`[AppName <String>]`: Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="7652e-163">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="7652e-164">`[BindingName <String>]`: Der Name der Bindungsressource.</span><span class="sxs-lookup"><span data-stu-id="7652e-164">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="7652e-165">`[CertificateName <String>]`: Der Name der Zertifikatressource.</span><span class="sxs-lookup"><span data-stu-id="7652e-165">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="7652e-166">`[DeploymentName <String>]`: Der Name der Bereitstellungsressource.</span><span class="sxs-lookup"><span data-stu-id="7652e-166">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="7652e-167">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="7652e-167">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="7652e-168">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="7652e-168">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7652e-169">`[Location <String>]`: die Region</span><span class="sxs-lookup"><span data-stu-id="7652e-169">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="7652e-170">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="7652e-170">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="7652e-171">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="7652e-171">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="7652e-172">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="7652e-172">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="7652e-173">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7652e-173">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="7652e-174">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="7652e-174">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7652e-175">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7652e-175">RELATED LINKS</span></span>

