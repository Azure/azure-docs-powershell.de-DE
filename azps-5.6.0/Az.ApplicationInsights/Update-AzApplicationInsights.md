---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: ac5e8bbc65a8435042d9f525cd1a3d35fa050398
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949776"
---
# <span data-ttu-id="694ff-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="694ff-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="694ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="694ff-102">SYNOPSIS</span></span>
<span data-ttu-id="694ff-103">Aktualisieren einer vorhandenen Ressource für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="694ff-103">update an existing application insights resource</span></span>

## <span data-ttu-id="694ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="694ff-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="694ff-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="694ff-105">DESCRIPTION</span></span>
<span data-ttu-id="694ff-106">Aktualisieren einer vorhandenen Ressource für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="694ff-106">update an existing application insights resource</span></span>

## <span data-ttu-id="694ff-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="694ff-107">EXAMPLES</span></span>

### <span data-ttu-id="694ff-108">Beispiel 1 Komponente "Anwendungseinblicke aktualisieren"</span><span class="sxs-lookup"><span data-stu-id="694ff-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="694ff-109">Aktualisieren der Komponente "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery auf "Disabled"</span><span class="sxs-lookup"><span data-stu-id="694ff-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="694ff-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="694ff-110">PARAMETERS</span></span>

### <span data-ttu-id="694ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="694ff-111">-DefaultProfile</span></span>
<span data-ttu-id="694ff-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="694ff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="694ff-113">-Name</span><span class="sxs-lookup"><span data-stu-id="694ff-113">-Name</span></span>
<span data-ttu-id="694ff-114">Application Insights Resource Name.</span><span class="sxs-lookup"><span data-stu-id="694ff-114">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="694ff-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="694ff-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="694ff-116">Der Netzwerkzugriffstyp für den Zugriff auf application insights ingestion.</span><span class="sxs-lookup"><span data-stu-id="694ff-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="694ff-117">Der Wert sollte "Aktiviert" oder "Deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="694ff-117">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="694ff-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="694ff-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="694ff-119">Der Netzwerkzugriffstyp für den Zugriff auf die Application Insights-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="694ff-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="694ff-120">Der Wert sollte "Aktiviert" oder "Deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="694ff-120">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="694ff-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="694ff-121">-ResourceGroupName</span></span>
<span data-ttu-id="694ff-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="694ff-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="694ff-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="694ff-123">-RetentionInDays</span></span>
<span data-ttu-id="694ff-124">Aufbewahrung in Tagen, standardmäßig 90.</span><span class="sxs-lookup"><span data-stu-id="694ff-124">Retention In Days, 90 by default.</span></span>

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

### <span data-ttu-id="694ff-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="694ff-125">-Tag</span></span>
<span data-ttu-id="694ff-126">Komponententags.</span><span class="sxs-lookup"><span data-stu-id="694ff-126">Component Tags.</span></span>

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

### <span data-ttu-id="694ff-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="694ff-127">-Confirm</span></span>
<span data-ttu-id="694ff-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="694ff-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="694ff-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="694ff-129">-WhatIf</span></span>
<span data-ttu-id="694ff-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="694ff-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="694ff-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="694ff-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="694ff-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="694ff-132">CommonParameters</span></span>
<span data-ttu-id="694ff-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="694ff-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="694ff-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="694ff-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="694ff-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="694ff-135">INPUTS</span></span>

### <span data-ttu-id="694ff-136">System.String</span><span class="sxs-lookup"><span data-stu-id="694ff-136">System.String</span></span>

## <span data-ttu-id="694ff-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="694ff-137">OUTPUTS</span></span>

### <span data-ttu-id="694ff-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="694ff-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="694ff-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="694ff-139">NOTES</span></span>

## <span data-ttu-id="694ff-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="694ff-140">RELATED LINKS</span></span>
