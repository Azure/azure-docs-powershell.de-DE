---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: db0ad78a942905846f764bb5d72a8ef3b209b6a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921512"
---
# <span data-ttu-id="43757-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="43757-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="43757-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43757-102">SYNOPSIS</span></span>
<span data-ttu-id="43757-103">Erstellen einer neuen Ressource für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="43757-103">Create a new application insights resource</span></span>

## <span data-ttu-id="43757-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43757-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43757-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43757-105">DESCRIPTION</span></span>
<span data-ttu-id="43757-106">Erstellen einer neuen Ressource für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="43757-106">Create a new application insights resource</span></span>

## <span data-ttu-id="43757-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="43757-107">EXAMPLES</span></span>

### <span data-ttu-id="43757-108">Beispiel 1 Erstellen einer neuen Ressource für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="43757-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test1027
ResourceGroupName  : testgroup
Name               : test1027
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 8323fb13-32aa-46af-b467-8355cf4f8f98
ApplicationType    : web
Tags               : {}
CreationDate       : 10/27/2017 4:56:40 PM
FlowType           :
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 083112ed-ed9b-464e-a9b0-8cf126fbfced
ProvisioningState  : Succeeded
RequestSource      : AzurePowerShell
SamplingPercentage :
TenantId           : {subid}
PublicNetworkAccessForIngestion : Enabled
PublicNetworkAccessForQuery     : Enabled
PrivateLinkScopedResources      :
```

<span data-ttu-id="43757-109">Hinzufügen einer neuen Ressource für Anwendungseinblicke mit dem Namen "Test" in der Ressourcengruppe "Testgruppe" mit der Art "java"</span><span class="sxs-lookup"><span data-stu-id="43757-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java"</span></span>

## <span data-ttu-id="43757-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="43757-110">PARAMETERS</span></span>

### <span data-ttu-id="43757-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43757-111">-DefaultProfile</span></span>
<span data-ttu-id="43757-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43757-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43757-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="43757-113">-Kind</span></span>
<span data-ttu-id="43757-114">Anwendungs art.</span><span class="sxs-lookup"><span data-stu-id="43757-114">Application kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43757-115">-Location</span><span class="sxs-lookup"><span data-stu-id="43757-115">-Location</span></span>
<span data-ttu-id="43757-116">Ressourcenspeicherort für Application Insights.</span><span class="sxs-lookup"><span data-stu-id="43757-116">Application Insights Resource Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43757-117">-Name</span><span class="sxs-lookup"><span data-stu-id="43757-117">-Name</span></span>
<span data-ttu-id="43757-118">Application Insights Resource Name.</span><span class="sxs-lookup"><span data-stu-id="43757-118">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43757-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="43757-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="43757-120">Der Netzwerkzugriffstyp für den Zugriff auf application insights ingestion.</span><span class="sxs-lookup"><span data-stu-id="43757-120">The network access type for accessing Application Insights ingestion.</span></span> <span data-ttu-id="43757-121">Der Wert sollte "Aktiviert" oder "Deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="43757-121">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43757-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="43757-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="43757-123">Der Netzwerkzugriffstyp für den Zugriff auf die Application Insights-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="43757-123">The network access type for accessing Application Insights query.</span></span> <span data-ttu-id="43757-124">Der Wert sollte "Aktiviert" oder "Deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="43757-124">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43757-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43757-125">-ResourceGroupName</span></span>
<span data-ttu-id="43757-126">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="43757-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43757-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="43757-127">-RetentionInDays</span></span>
<span data-ttu-id="43757-128">Aufbewahrung in Tagen, standardmäßig 90.</span><span class="sxs-lookup"><span data-stu-id="43757-128">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43757-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="43757-129">-Tag</span></span>
<span data-ttu-id="43757-130">Komponententags.</span><span class="sxs-lookup"><span data-stu-id="43757-130">Component Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43757-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="43757-131">-Confirm</span></span>
<span data-ttu-id="43757-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="43757-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43757-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43757-133">-WhatIf</span></span>
<span data-ttu-id="43757-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43757-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43757-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43757-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43757-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43757-136">CommonParameters</span></span>
<span data-ttu-id="43757-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43757-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43757-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43757-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43757-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="43757-139">INPUTS</span></span>

### <span data-ttu-id="43757-140">Keine</span><span class="sxs-lookup"><span data-stu-id="43757-140">None</span></span>

## <span data-ttu-id="43757-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="43757-141">OUTPUTS</span></span>

### <span data-ttu-id="43757-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="43757-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="43757-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="43757-143">NOTES</span></span>

## <span data-ttu-id="43757-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="43757-144">RELATED LINKS</span></span>
