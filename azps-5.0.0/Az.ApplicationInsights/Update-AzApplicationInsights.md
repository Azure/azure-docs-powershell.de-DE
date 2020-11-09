---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: f34868c31a99e67596d244a1f69224db5c25349a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300861"
---
# <span data-ttu-id="e1262-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e1262-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="e1262-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1262-102">SYNOPSIS</span></span>
<span data-ttu-id="e1262-103">Aktualisieren einer vorhandenen Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="e1262-103">update an existing application insights resource</span></span>

## <span data-ttu-id="e1262-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1262-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1262-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1262-105">DESCRIPTION</span></span>
<span data-ttu-id="e1262-106">Aktualisieren einer vorhandenen Application Insights-Ressource</span><span class="sxs-lookup"><span data-stu-id="e1262-106">update an existing application insights resource</span></span>

## <span data-ttu-id="e1262-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1262-107">EXAMPLES</span></span>

### <span data-ttu-id="e1262-108">Beispiel 1 Update Application Insights-Komponente</span><span class="sxs-lookup"><span data-stu-id="e1262-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="e1262-109">Aktualisieren der Anwendungs Einblicke-Komponente "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery sowohl auf "deaktiviert"</span><span class="sxs-lookup"><span data-stu-id="e1262-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="e1262-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1262-110">PARAMETERS</span></span>

### <span data-ttu-id="e1262-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1262-111">-DefaultProfile</span></span>
<span data-ttu-id="e1262-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1262-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1262-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e1262-113">-Name</span></span>
<span data-ttu-id="e1262-114">Ressourcen Name für Application Insights</span><span class="sxs-lookup"><span data-stu-id="e1262-114">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="e1262-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="e1262-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="e1262-116">Der Netzwerkzugriffstyp für den Zugriff auf die Einnahme von Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e1262-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="e1262-117">Der Wert sollte "aktiviert" oder "deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="e1262-117">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="e1262-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="e1262-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="e1262-119">Der Netzwerkzugriffstyp für den Zugriff auf die Abfrage von Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e1262-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="e1262-120">Der Wert sollte "aktiviert" oder "deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="e1262-120">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="e1262-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1262-121">-ResourceGroupName</span></span>
<span data-ttu-id="e1262-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e1262-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="e1262-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e1262-123">-RetentionInDays</span></span>
<span data-ttu-id="e1262-124">Aufbewahrung in Tagen, 90 standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="e1262-124">Retention In Days, 90 by default.</span></span>

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

### <span data-ttu-id="e1262-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="e1262-125">-Tag</span></span>
<span data-ttu-id="e1262-126">Komponentenkategorien.</span><span class="sxs-lookup"><span data-stu-id="e1262-126">Component Tags.</span></span>

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

### <span data-ttu-id="e1262-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e1262-127">-Confirm</span></span>
<span data-ttu-id="e1262-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1262-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1262-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1262-129">-WhatIf</span></span>
<span data-ttu-id="e1262-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1262-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1262-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1262-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1262-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1262-132">CommonParameters</span></span>
<span data-ttu-id="e1262-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1262-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1262-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1262-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1262-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1262-135">INPUTS</span></span>

### <span data-ttu-id="e1262-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e1262-136">System.String</span></span>

## <span data-ttu-id="e1262-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1262-137">OUTPUTS</span></span>

### <span data-ttu-id="e1262-138">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e1262-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="e1262-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1262-139">NOTES</span></span>

## <span data-ttu-id="e1262-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1262-140">RELATED LINKS</span></span>
