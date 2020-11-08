---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: c84037fd402e5ecea51cc4f60dcddb1873878f5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174147"
---
# <span data-ttu-id="b5483-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="b5483-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="b5483-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b5483-102">SYNOPSIS</span></span>
<span data-ttu-id="b5483-103">Erstellen Sie einen neuen Dienst, oder aktualisieren Sie einen beendenden Dienst.</span><span class="sxs-lookup"><span data-stu-id="b5483-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="b5483-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5483-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b5483-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b5483-105">DESCRIPTION</span></span>
<span data-ttu-id="b5483-106">Erstellen Sie einen neuen Dienst, oder aktualisieren Sie einen beendenden Dienst.</span><span class="sxs-lookup"><span data-stu-id="b5483-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="b5483-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b5483-107">EXAMPLES</span></span>

### <span data-ttu-id="b5483-108">Beispiel 1: Erstellen eines Spring Cloud-Diensts</span><span class="sxs-lookup"><span data-stu-id="b5483-108">Example 1: Create a spring cloud service.</span></span>
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

<span data-ttu-id="b5483-109">Erstellen Sie einen Spring Cloud-Dienst.</span><span class="sxs-lookup"><span data-stu-id="b5483-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="b5483-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5483-110">PARAMETERS</span></span>

### <span data-ttu-id="b5483-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5483-111">-AsJob</span></span>
<span data-ttu-id="b5483-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="b5483-112">Run the command as a job</span></span>

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

### <span data-ttu-id="b5483-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5483-113">-DefaultProfile</span></span>
<span data-ttu-id="b5483-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b5483-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5483-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="b5483-115">-GitPropertyUri</span></span>
<span data-ttu-id="b5483-116">URI des Repositorys</span><span class="sxs-lookup"><span data-stu-id="b5483-116">URI of the repository</span></span>

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

### <span data-ttu-id="b5483-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="b5483-117">-Location</span></span>
<span data-ttu-id="b5483-118">Die Geo-Position der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b5483-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="b5483-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b5483-119">-Name</span></span>
<span data-ttu-id="b5483-120">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="b5483-120">The name of the Service resource.</span></span>

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

### <span data-ttu-id="b5483-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b5483-121">-NoWait</span></span>
<span data-ttu-id="b5483-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="b5483-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b5483-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5483-123">-ResourceGroupName</span></span>
<span data-ttu-id="b5483-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="b5483-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b5483-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="b5483-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b5483-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b5483-126">-SkuName</span></span>
<span data-ttu-id="b5483-127">Name der SKU</span><span class="sxs-lookup"><span data-stu-id="b5483-127">Name of the Sku</span></span>

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

### <span data-ttu-id="b5483-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b5483-128">-SkuTier</span></span>
<span data-ttu-id="b5483-129">Stufe der SKU</span><span class="sxs-lookup"><span data-stu-id="b5483-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="b5483-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b5483-130">-SubscriptionId</span></span>
<span data-ttu-id="b5483-131">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b5483-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b5483-132">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="b5483-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b5483-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="b5483-133">-Tag</span></span>
<span data-ttu-id="b5483-134">Tags des Diensts, bei denen es sich um eine Liste von Schlüsselwert Paaren handelt, die die Ressource beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b5483-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="b5483-135">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="b5483-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="b5483-136">Instrumentations Schlüssel für Ziel Anwendungs Insight</span><span class="sxs-lookup"><span data-stu-id="b5483-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="b5483-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="b5483-137">-TraceEnabled</span></span>
<span data-ttu-id="b5483-138">Gibt an, ob die Ablaufverfolgungsfunktion aktiviert werden soll</span><span class="sxs-lookup"><span data-stu-id="b5483-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="b5483-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b5483-139">-Confirm</span></span>
<span data-ttu-id="b5483-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5483-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5483-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5483-141">-WhatIf</span></span>
<span data-ttu-id="b5483-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5483-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5483-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5483-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5483-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5483-144">CommonParameters</span></span>
<span data-ttu-id="b5483-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5483-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5483-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5483-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5483-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b5483-147">INPUTS</span></span>

## <span data-ttu-id="b5483-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b5483-148">OUTPUTS</span></span>

### <span data-ttu-id="b5483-149">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20190501Preview. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="b5483-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IServiceResource</span></span>

## <span data-ttu-id="b5483-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="b5483-150">NOTES</span></span>

<span data-ttu-id="b5483-151">Aliase</span><span class="sxs-lookup"><span data-stu-id="b5483-151">ALIASES</span></span>

## <span data-ttu-id="b5483-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b5483-152">RELATED LINKS</span></span>

