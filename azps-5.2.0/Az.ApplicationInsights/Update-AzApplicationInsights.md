---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: f34868c31a99e67596d244a1f69224db5c25349a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306723"
---
# <span data-ttu-id="f1f7d-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f1f7d-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="f1f7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f7d-103">Aktualisieren einer vorhandenen Ressource für Anwendungserkenntnisse</span><span class="sxs-lookup"><span data-stu-id="f1f7d-103">update an existing application insights resource</span></span>

## <span data-ttu-id="f1f7d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1f7d-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1f7d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1f7d-105">DESCRIPTION</span></span>
<span data-ttu-id="f1f7d-106">Aktualisieren einer vorhandenen Ressource für Anwendungserkenntnisse</span><span class="sxs-lookup"><span data-stu-id="f1f7d-106">update an existing application insights resource</span></span>

## <span data-ttu-id="f1f7d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1f7d-107">EXAMPLES</span></span>

### <span data-ttu-id="f1f7d-108">Beispiel 1 Aktualisieren der Komponente für Anwendungserkenntnisse</span><span class="sxs-lookup"><span data-stu-id="f1f7d-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="f1f7d-109">App insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span><span class="sxs-lookup"><span data-stu-id="f1f7d-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="f1f7d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1f7d-110">PARAMETERS</span></span>

### <span data-ttu-id="f1f7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f7d-111">-DefaultProfile</span></span>
<span data-ttu-id="f1f7d-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1f7d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1f7d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f1f7d-113">-Name</span></span>
<span data-ttu-id="f1f7d-114">Ressourcenname von Application Insights.</span><span class="sxs-lookup"><span data-stu-id="f1f7d-114">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="f1f7d-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="f1f7d-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="f1f7d-116">Der Netzwerkzugriffstyp für den Zugriff auf Die Erfassung von Anwendungseinblicken.</span><span class="sxs-lookup"><span data-stu-id="f1f7d-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="f1f7d-117">Der Wert sollte "Enabled" oder "Disabled" sein.</span><span class="sxs-lookup"><span data-stu-id="f1f7d-117">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="f1f7d-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="f1f7d-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="f1f7d-119">Der Netzwerkzugriffstyp für den Zugriff auf eine Application Insights-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="f1f7d-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="f1f7d-120">Der Wert sollte "Enabled" oder "Disabled" sein.</span><span class="sxs-lookup"><span data-stu-id="f1f7d-120">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="f1f7d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1f7d-121">-ResourceGroupName</span></span>
<span data-ttu-id="f1f7d-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="f1f7d-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="f1f7d-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f1f7d-123">-RetentionInDays</span></span>
<span data-ttu-id="f1f7d-124">Aufbewahrung in Tagen, standardmäßig 90.</span><span class="sxs-lookup"><span data-stu-id="f1f7d-124">Retention In Days, 90 by default.</span></span>

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

### <span data-ttu-id="f1f7d-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="f1f7d-125">-Tag</span></span>
<span data-ttu-id="f1f7d-126">Komponententags.</span><span class="sxs-lookup"><span data-stu-id="f1f7d-126">Component Tags.</span></span>

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

### <span data-ttu-id="f1f7d-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1f7d-127">-Confirm</span></span>
<span data-ttu-id="f1f7d-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1f7d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1f7d-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f1f7d-129">-WhatIf</span></span>
<span data-ttu-id="f1f7d-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1f7d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1f7d-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1f7d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1f7d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f7d-132">CommonParameters</span></span>
<span data-ttu-id="f1f7d-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1f7d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f7d-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1f7d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f7d-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1f7d-135">INPUTS</span></span>

### <span data-ttu-id="f1f7d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f1f7d-136">System.String</span></span>

## <span data-ttu-id="f1f7d-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1f7d-137">OUTPUTS</span></span>

### <span data-ttu-id="f1f7d-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f1f7d-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="f1f7d-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f1f7d-139">NOTES</span></span>

## <span data-ttu-id="f1f7d-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f1f7d-140">RELATED LINKS</span></span>
