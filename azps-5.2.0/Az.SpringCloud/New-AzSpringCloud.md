---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: d5b8d521c72b553143f75b0911cb9b933b0795e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292084"
---
# <span data-ttu-id="3f752-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="3f752-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="3f752-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f752-102">SYNOPSIS</span></span>
<span data-ttu-id="3f752-103">Erstellen Sie einen neuen Dienst, oder aktualisieren Sie einen verlassenden Dienst.</span><span class="sxs-lookup"><span data-stu-id="3f752-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="3f752-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f752-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3f752-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f752-105">DESCRIPTION</span></span>
<span data-ttu-id="3f752-106">Erstellen Sie einen neuen Dienst, oder aktualisieren Sie einen verlassenden Dienst.</span><span class="sxs-lookup"><span data-stu-id="3f752-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="3f752-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f752-107">EXAMPLES</span></span>

### <span data-ttu-id="3f752-108">Beispiel 1: Erstellen eines Quell-Cloud-Diensts.</span><span class="sxs-lookup"><span data-stu-id="3f752-108">Example 1: Create a spring cloud service.</span></span>
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

<span data-ttu-id="3f752-109">Erstellen Sie einen Quell-Cloud-Dienst.</span><span class="sxs-lookup"><span data-stu-id="3f752-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="3f752-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f752-110">PARAMETERS</span></span>

### <span data-ttu-id="3f752-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f752-111">-AsJob</span></span>
<span data-ttu-id="3f752-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="3f752-112">Run the command as a job</span></span>

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

### <span data-ttu-id="3f752-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f752-113">-DefaultProfile</span></span>
<span data-ttu-id="3f752-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f752-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f752-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="3f752-115">-GitPropertyUri</span></span>
<span data-ttu-id="3f752-116">URI des Repositorys</span><span class="sxs-lookup"><span data-stu-id="3f752-116">URI of the repository</span></span>

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

### <span data-ttu-id="3f752-117">-Location</span><span class="sxs-lookup"><span data-stu-id="3f752-117">-Location</span></span>
<span data-ttu-id="3f752-118">Der GEO-Standort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="3f752-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="3f752-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3f752-119">-Name</span></span>
<span data-ttu-id="3f752-120">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="3f752-120">The name of the Service resource.</span></span>

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

### <span data-ttu-id="3f752-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3f752-121">-NoWait</span></span>
<span data-ttu-id="3f752-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="3f752-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3f752-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f752-123">-ResourceGroupName</span></span>
<span data-ttu-id="3f752-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="3f752-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3f752-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="3f752-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3f752-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3f752-126">-SkuName</span></span>
<span data-ttu-id="3f752-127">Name der SKU</span><span class="sxs-lookup"><span data-stu-id="3f752-127">Name of the Sku</span></span>

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

### <span data-ttu-id="3f752-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="3f752-128">-SkuTier</span></span>
<span data-ttu-id="3f752-129">Stufe der SKU</span><span class="sxs-lookup"><span data-stu-id="3f752-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="3f752-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f752-130">-SubscriptionId</span></span>
<span data-ttu-id="3f752-131">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3f752-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3f752-132">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="3f752-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3f752-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="3f752-133">-Tag</span></span>
<span data-ttu-id="3f752-134">Tags des Diensts, bei dem es sich um eine Liste von Schlüsselwertpaaren handelt, die die Ressource beschreiben.</span><span class="sxs-lookup"><span data-stu-id="3f752-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="3f752-135">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="3f752-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="3f752-136">Zielanwendungsinblick-Instrumentationsschlüssel</span><span class="sxs-lookup"><span data-stu-id="3f752-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="3f752-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="3f752-137">-TraceEnabled</span></span>
<span data-ttu-id="3f752-138">Gibt an, ob die Ablaufverfolgungsfunktion aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="3f752-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="3f752-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f752-139">-Confirm</span></span>
<span data-ttu-id="3f752-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f752-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f752-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3f752-141">-WhatIf</span></span>
<span data-ttu-id="3f752-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f752-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f752-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f752-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f752-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f752-144">CommonParameters</span></span>
<span data-ttu-id="3f752-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f752-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f752-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f752-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f752-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f752-147">INPUTS</span></span>

## <span data-ttu-id="3f752-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f752-148">OUTPUTS</span></span>

### <span data-ttu-id="3f752-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="3f752-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="3f752-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3f752-150">NOTES</span></span>

<span data-ttu-id="3f752-151">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3f752-151">ALIASES</span></span>

## <span data-ttu-id="3f752-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3f752-152">RELATED LINKS</span></span>

