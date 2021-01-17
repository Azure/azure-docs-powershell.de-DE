---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: d5b8d521c72b553143f75b0911cb9b933b0795e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470347"
---
# <span data-ttu-id="7836c-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="7836c-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="7836c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7836c-102">SYNOPSIS</span></span>
<span data-ttu-id="7836c-103">Erstellen Sie einen neuen Dienst, oder aktualisieren Sie einen verlassenden Dienst.</span><span class="sxs-lookup"><span data-stu-id="7836c-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="7836c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7836c-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7836c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7836c-105">DESCRIPTION</span></span>
<span data-ttu-id="7836c-106">Erstellen Sie einen neuen Dienst, oder aktualisieren Sie einen verlassenden Dienst.</span><span class="sxs-lookup"><span data-stu-id="7836c-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="7836c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7836c-107">EXAMPLES</span></span>

### <span data-ttu-id="7836c-108">Beispiel 1: Erstellen eines Quell-Cloud-Diensts.</span><span class="sxs-lookup"><span data-stu-id="7836c-108">Example 1: Create a spring cloud service.</span></span>
```powershell
PS C:\> New-AzSpringCloud -ResourceGroupName spring-cloud-rp -name spring-cloud-service -Location eastus

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

<span data-ttu-id="7836c-109">Erstellen Sie einen Quell-Cloud-Dienst.</span><span class="sxs-lookup"><span data-stu-id="7836c-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="7836c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7836c-110">PARAMETERS</span></span>

### <span data-ttu-id="7836c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7836c-111">-AsJob</span></span>
<span data-ttu-id="7836c-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="7836c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="7836c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7836c-113">-DefaultProfile</span></span>
<span data-ttu-id="7836c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7836c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7836c-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="7836c-115">-GitPropertyUri</span></span>
<span data-ttu-id="7836c-116">URI des Repositorys</span><span class="sxs-lookup"><span data-stu-id="7836c-116">URI of the repository</span></span>

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

### <span data-ttu-id="7836c-117">-Location</span><span class="sxs-lookup"><span data-stu-id="7836c-117">-Location</span></span>
<span data-ttu-id="7836c-118">Der GEO-Standort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="7836c-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="7836c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7836c-119">-Name</span></span>
<span data-ttu-id="7836c-120">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="7836c-120">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7836c-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7836c-121">-NoWait</span></span>
<span data-ttu-id="7836c-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="7836c-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7836c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7836c-123">-ResourceGroupName</span></span>
<span data-ttu-id="7836c-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="7836c-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7836c-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="7836c-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7836c-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7836c-126">-SkuName</span></span>
<span data-ttu-id="7836c-127">Name der SKU</span><span class="sxs-lookup"><span data-stu-id="7836c-127">Name of the Sku</span></span>

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

### <span data-ttu-id="7836c-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="7836c-128">-SkuTier</span></span>
<span data-ttu-id="7836c-129">Stufe der SKU</span><span class="sxs-lookup"><span data-stu-id="7836c-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="7836c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7836c-130">-SubscriptionId</span></span>
<span data-ttu-id="7836c-131">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7836c-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7836c-132">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="7836c-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7836c-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="7836c-133">-Tag</span></span>
<span data-ttu-id="7836c-134">Tags des Diensts, bei dem es sich um eine Liste von Schlüsselwertpaaren handelt, die die Ressource beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7836c-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="7836c-135">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="7836c-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="7836c-136">Zielanwendungsinblick-Instrumentationsschlüssel</span><span class="sxs-lookup"><span data-stu-id="7836c-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="7836c-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="7836c-137">-TraceEnabled</span></span>
<span data-ttu-id="7836c-138">Gibt an, ob die Ablaufverfolgungsfunktion aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="7836c-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="7836c-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7836c-139">-Confirm</span></span>
<span data-ttu-id="7836c-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7836c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7836c-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7836c-141">-WhatIf</span></span>
<span data-ttu-id="7836c-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7836c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7836c-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7836c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7836c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7836c-144">CommonParameters</span></span>
<span data-ttu-id="7836c-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7836c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7836c-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7836c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7836c-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7836c-147">INPUTS</span></span>

## <span data-ttu-id="7836c-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7836c-148">OUTPUTS</span></span>

### <span data-ttu-id="7836c-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="7836c-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="7836c-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7836c-150">NOTES</span></span>

<span data-ttu-id="7836c-151">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7836c-151">ALIASES</span></span>

## <span data-ttu-id="7836c-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7836c-152">RELATED LINKS</span></span>

