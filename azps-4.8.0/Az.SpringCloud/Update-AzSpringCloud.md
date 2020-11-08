---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
ms.openlocfilehash: 02a880d669e3e93693dc39823587fe1d676ac279
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008926"
---
# <span data-ttu-id="e4682-101">Update-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="e4682-101">Update-AzSpringCloud</span></span>

## <span data-ttu-id="e4682-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e4682-102">SYNOPSIS</span></span>
<span data-ttu-id="e4682-103">Vorgang zum Aktualisieren eines exiting-Diensts.</span><span class="sxs-lookup"><span data-stu-id="e4682-103">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="e4682-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4682-104">SYNTAX</span></span>

### <span data-ttu-id="e4682-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="e4682-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e4682-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e4682-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloud -InputObject <ISpringCloudIdentity> [-GitPropertyUri <String>] [-Location <String>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>] [-TraceAppInsightInstrumentationKey <String>]
 [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e4682-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e4682-107">DESCRIPTION</span></span>
<span data-ttu-id="e4682-108">Vorgang zum Aktualisieren eines exiting-Diensts.</span><span class="sxs-lookup"><span data-stu-id="e4682-108">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="e4682-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e4682-109">EXAMPLES</span></span>

### <span data-ttu-id="e4682-110">Beispiel 1: Aktualisieren des Spring Cloud-Diensts nach Name</span><span class="sxs-lookup"><span data-stu-id="e4682-110">Example 1: Update Spring Cloud Service by name.</span></span>
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

<span data-ttu-id="e4682-111">Aktualisieren Sie den Spring Cloud-Dienst nach Namen.</span><span class="sxs-lookup"><span data-stu-id="e4682-111">Update Spring Cloud Service by name.</span></span>

### <span data-ttu-id="e4682-112">Beispiel 2: Aktualisieren des Spring Cloud-Diensts aus Pipe</span><span class="sxs-lookup"><span data-stu-id="e4682-112">Example 2: Update Spring Cloud Service from pipe.</span></span>
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

<span data-ttu-id="e4682-113">Aktualisieren Sie den Spring Cloud-Dienst von Pipe.</span><span class="sxs-lookup"><span data-stu-id="e4682-113">Update Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="e4682-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4682-114">PARAMETERS</span></span>

### <span data-ttu-id="e4682-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4682-115">-AsJob</span></span>
<span data-ttu-id="e4682-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="e4682-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e4682-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4682-117">-DefaultProfile</span></span>
<span data-ttu-id="e4682-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e4682-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4682-119">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="e4682-119">-GitPropertyUri</span></span>
<span data-ttu-id="e4682-120">URI des Repositorys</span><span class="sxs-lookup"><span data-stu-id="e4682-120">URI of the repository</span></span>

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

### <span data-ttu-id="e4682-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e4682-121">-InputObject</span></span>
<span data-ttu-id="e4682-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e4682-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e4682-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="e4682-123">-Location</span></span>
<span data-ttu-id="e4682-124">Die Geo-Position der Ressource.</span><span class="sxs-lookup"><span data-stu-id="e4682-124">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="e4682-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e4682-125">-Name</span></span>
<span data-ttu-id="e4682-126">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="e4682-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="e4682-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e4682-127">-NoWait</span></span>
<span data-ttu-id="e4682-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="e4682-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e4682-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4682-129">-ResourceGroupName</span></span>
<span data-ttu-id="e4682-130">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="e4682-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e4682-131">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="e4682-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e4682-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e4682-132">-SkuName</span></span>
<span data-ttu-id="e4682-133">Name der SKU</span><span class="sxs-lookup"><span data-stu-id="e4682-133">Name of the Sku</span></span>

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

### <span data-ttu-id="e4682-134">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e4682-134">-SkuTier</span></span>
<span data-ttu-id="e4682-135">Stufe der SKU</span><span class="sxs-lookup"><span data-stu-id="e4682-135">Tier of the Sku</span></span>

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

### <span data-ttu-id="e4682-136">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e4682-136">-SubscriptionId</span></span>
<span data-ttu-id="e4682-137">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e4682-137">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e4682-138">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="e4682-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e4682-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="e4682-139">-Tag</span></span>
<span data-ttu-id="e4682-140">Tags des Diensts, bei denen es sich um eine Liste von Schlüsselwert Paaren handelt, die die Ressource beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e4682-140">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="e4682-141">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="e4682-141">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="e4682-142">Instrumentations Schlüssel für Ziel Anwendungs Insight</span><span class="sxs-lookup"><span data-stu-id="e4682-142">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="e4682-143">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="e4682-143">-TraceEnabled</span></span>
<span data-ttu-id="e4682-144">Gibt an, ob die Ablaufverfolgungsfunktion aktiviert werden soll</span><span class="sxs-lookup"><span data-stu-id="e4682-144">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="e4682-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e4682-145">-Confirm</span></span>
<span data-ttu-id="e4682-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e4682-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4682-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4682-147">-WhatIf</span></span>
<span data-ttu-id="e4682-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4682-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4682-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4682-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4682-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4682-150">CommonParameters</span></span>
<span data-ttu-id="e4682-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4682-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4682-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4682-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4682-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e4682-153">INPUTS</span></span>

### <span data-ttu-id="e4682-154">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="e4682-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="e4682-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e4682-155">OUTPUTS</span></span>

### <span data-ttu-id="e4682-156">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20190501Preview. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="e4682-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IServiceResource</span></span>

## <span data-ttu-id="e4682-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="e4682-157">NOTES</span></span>

<span data-ttu-id="e4682-158">Aliase</span><span class="sxs-lookup"><span data-stu-id="e4682-158">ALIASES</span></span>

<span data-ttu-id="e4682-159">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4682-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e4682-160">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e4682-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4682-161">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="e4682-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e4682-162">Inputobject <ISpringCloudIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="e4682-162">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e4682-163">`[AppName <String>]`: Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e4682-163">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="e4682-164">`[BindingName <String>]`: Der Name der Bindungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="e4682-164">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="e4682-165">`[CertificateName <String>]`: Der Name der Zertifikat Ressource.</span><span class="sxs-lookup"><span data-stu-id="e4682-165">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="e4682-166">`[DeploymentName <String>]`: Der Name der Bereitstellungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="e4682-166">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="e4682-167">`[DomainName <String>]`: Der Name der benutzerdefinierten Domänenressource.</span><span class="sxs-lookup"><span data-stu-id="e4682-167">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="e4682-168">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="e4682-168">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e4682-169">`[Location <String>]`: die Region</span><span class="sxs-lookup"><span data-stu-id="e4682-169">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="e4682-170">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="e4682-170">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e4682-171">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="e4682-171">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e4682-172">`[ServiceName <String>]`: Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="e4682-172">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="e4682-173">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e4682-173">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="e4682-174">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="e4682-174">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e4682-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e4682-175">RELATED LINKS</span></span>

