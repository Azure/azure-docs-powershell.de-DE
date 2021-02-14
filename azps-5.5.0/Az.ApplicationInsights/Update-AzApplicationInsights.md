---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: f34868c31a99e67596d244a1f69224db5c25349a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176164"
---
# <span data-ttu-id="7f730-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7f730-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="7f730-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f730-102">SYNOPSIS</span></span>
<span data-ttu-id="7f730-103">Aktualisieren einer vorhandenen Ressource für Anwendungserkenntnisse</span><span class="sxs-lookup"><span data-stu-id="7f730-103">update an existing application insights resource</span></span>

## <span data-ttu-id="7f730-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f730-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f730-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f730-105">DESCRIPTION</span></span>
<span data-ttu-id="7f730-106">Aktualisieren einer vorhandenen Ressource für Anwendungserkenntnisse</span><span class="sxs-lookup"><span data-stu-id="7f730-106">update an existing application insights resource</span></span>

## <span data-ttu-id="7f730-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7f730-107">EXAMPLES</span></span>

### <span data-ttu-id="7f730-108">Beispiel 1 Aktualisieren der Komponente für Anwendungserkenntnisse</span><span class="sxs-lookup"><span data-stu-id="7f730-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="7f730-109">App insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span><span class="sxs-lookup"><span data-stu-id="7f730-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="7f730-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f730-110">PARAMETERS</span></span>

### <span data-ttu-id="7f730-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f730-111">-DefaultProfile</span></span>
<span data-ttu-id="7f730-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f730-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f730-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7f730-113">-Name</span></span>
<span data-ttu-id="7f730-114">Ressourcenname von Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7f730-114">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="7f730-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="7f730-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="7f730-116">Der Netzwerkzugriffstyp für den Zugriff auf "Erfassung von Application Insights".</span><span class="sxs-lookup"><span data-stu-id="7f730-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="7f730-117">Der Wert sollte "Enabled" oder "Disabled" sein.</span><span class="sxs-lookup"><span data-stu-id="7f730-117">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f730-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="7f730-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="7f730-119">Der Netzwerkzugriffstyp für den Zugriff auf eine Application Insights-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="7f730-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="7f730-120">Der Wert sollte "Enabled" oder "Disabled" sein.</span><span class="sxs-lookup"><span data-stu-id="7f730-120">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f730-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f730-121">-ResourceGroupName</span></span>
<span data-ttu-id="7f730-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="7f730-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="7f730-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7f730-123">-RetentionInDays</span></span>
<span data-ttu-id="7f730-124">Aufbewahrung in Tagen, standardmäßig 90.</span><span class="sxs-lookup"><span data-stu-id="7f730-124">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f730-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="7f730-125">-Tag</span></span>
<span data-ttu-id="7f730-126">Komponententags.</span><span class="sxs-lookup"><span data-stu-id="7f730-126">Component Tags.</span></span>

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

### <span data-ttu-id="7f730-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f730-127">-Confirm</span></span>
<span data-ttu-id="7f730-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f730-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f730-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7f730-129">-WhatIf</span></span>
<span data-ttu-id="7f730-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f730-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f730-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f730-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f730-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f730-132">CommonParameters</span></span>
<span data-ttu-id="7f730-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f730-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f730-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f730-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f730-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7f730-135">INPUTS</span></span>

### <span data-ttu-id="7f730-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7f730-136">System.String</span></span>

## <span data-ttu-id="7f730-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7f730-137">OUTPUTS</span></span>

### <span data-ttu-id="7f730-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7f730-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="7f730-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7f730-139">NOTES</span></span>

## <span data-ttu-id="7f730-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7f730-140">RELATED LINKS</span></span>
