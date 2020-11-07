---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: 4a5863573b207d3c1319b48f6ca00ab11a7b56a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822643"
---
# <span data-ttu-id="c2287-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c2287-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="c2287-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2287-102">SYNOPSIS</span></span>
<span data-ttu-id="c2287-103">Entfernt eine metrische Warnungsregel v2 (nicht klassisch).</span><span class="sxs-lookup"><span data-stu-id="c2287-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="c2287-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2287-104">SYNTAX</span></span>

### <span data-ttu-id="c2287-105">ByMetricRuleResourceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2287-105">ByMetricRuleResourceName (Default)</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2287-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="c2287-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2287-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="c2287-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2287-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2287-108">DESCRIPTION</span></span>
<span data-ttu-id="c2287-109">Das Cmdlet **Remove-AzMetricAlertRuleV2** entfernt eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="c2287-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="c2287-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c2287-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="c2287-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2287-111">EXAMPLES</span></span>

### <span data-ttu-id="c2287-112">Beispiel 1: Entfernen einer Warnungsregel nach Namen</span><span class="sxs-lookup"><span data-stu-id="c2287-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="c2287-113">Dieser Befehl entfernt die Warnungsregel mit dem Namen PsSdk</span><span class="sxs-lookup"><span data-stu-id="c2287-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="c2287-114">Beispiel 2: Entfernen einer Warnungsregel nach ID</span><span class="sxs-lookup"><span data-stu-id="c2287-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="c2287-115">Mit diesem Befehl wird die Warnungsregel mit der Ressourcen-ID entfernt `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="c2287-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>

### <span data-ttu-id="c2287-116">Beispiel 3: besorgen Sie sich eine Benachrichtigung, und entfernen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="c2287-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="c2287-117">Dieser Befehl ruft eine Benachrichtigung ab und entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="c2287-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="c2287-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2287-118">PARAMETERS</span></span>

### <span data-ttu-id="c2287-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2287-119">-AsJob</span></span>
<span data-ttu-id="c2287-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c2287-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2287-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2287-121">-DefaultProfile</span></span>
<span data-ttu-id="c2287-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2287-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2287-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c2287-123">-InputObject</span></span>
<span data-ttu-id="c2287-124">Das metrische Regelobjekt</span><span class="sxs-lookup"><span data-stu-id="c2287-124">The Metric rule object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2
Parameter Sets: ByRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2287-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c2287-125">-Name</span></span>
<span data-ttu-id="c2287-126">Der Name der Metrik-Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="c2287-126">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2287-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2287-127">-PassThru</span></span>
<span data-ttu-id="c2287-128">Beim erfolgreichen löschen wird true zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c2287-128">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="c2287-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2287-129">-ResourceGroupName</span></span>
<span data-ttu-id="c2287-130">Die ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2287-130">The ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2287-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c2287-131">-ResourceId</span></span>
<span data-ttu-id="c2287-132">Die RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="c2287-132">The RuleResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceId
Aliases: RuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2287-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2287-133">-Confirm</span></span>
<span data-ttu-id="c2287-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2287-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2287-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2287-135">-WhatIf</span></span>
<span data-ttu-id="c2287-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2287-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2287-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2287-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2287-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2287-138">CommonParameters</span></span>
<span data-ttu-id="c2287-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2287-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2287-140">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2287-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2287-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2287-141">INPUTS</span></span>

### <span data-ttu-id="c2287-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c2287-142">System.String</span></span>

### <span data-ttu-id="c2287-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c2287-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="c2287-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2287-144">OUTPUTS</span></span>

### <span data-ttu-id="c2287-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2287-145">System.Boolean</span></span>

## <span data-ttu-id="c2287-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2287-146">NOTES</span></span>

## <span data-ttu-id="c2287-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2287-147">RELATED LINKS</span></span>
