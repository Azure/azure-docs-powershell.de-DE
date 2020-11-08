---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: d2b34063f5ece370d52b8a4c3c0dab35cff77c54
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180108"
---
# <span data-ttu-id="291ab-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="291ab-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="291ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="291ab-102">SYNOPSIS</span></span>
<span data-ttu-id="291ab-103">Entfernt eine metrische Warnungsregel v2 (nicht klassisch).</span><span class="sxs-lookup"><span data-stu-id="291ab-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="291ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="291ab-104">SYNTAX</span></span>

### <span data-ttu-id="291ab-105">ByMetricRuleResourceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="291ab-105">ByMetricRuleResourceName (Default)</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="291ab-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="291ab-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="291ab-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="291ab-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="291ab-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="291ab-108">DESCRIPTION</span></span>
<span data-ttu-id="291ab-109">Das Cmdlet **Remove-AzMetricAlertRuleV2** entfernt eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="291ab-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="291ab-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="291ab-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="291ab-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="291ab-111">EXAMPLES</span></span>

### <span data-ttu-id="291ab-112">Beispiel 1: Entfernen einer Warnungsregel nach Namen</span><span class="sxs-lookup"><span data-stu-id="291ab-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="291ab-113">Dieser Befehl entfernt die Warnungsregel mit dem Namen PsSdk</span><span class="sxs-lookup"><span data-stu-id="291ab-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="291ab-114">Beispiel 2: Entfernen einer Warnungsregel nach ID</span><span class="sxs-lookup"><span data-stu-id="291ab-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="291ab-115">Mit diesem Befehl wird die Warnungsregel mit der Ressourcen-ID entfernt `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="291ab-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>

### <span data-ttu-id="291ab-116">Beispiel 3: besorgen Sie sich eine Benachrichtigung, und entfernen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="291ab-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="291ab-117">Dieser Befehl ruft eine Benachrichtigung ab und entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="291ab-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="291ab-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="291ab-118">PARAMETERS</span></span>

### <span data-ttu-id="291ab-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="291ab-119">-AsJob</span></span>
<span data-ttu-id="291ab-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="291ab-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="291ab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="291ab-121">-DefaultProfile</span></span>
<span data-ttu-id="291ab-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="291ab-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="291ab-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="291ab-123">-InputObject</span></span>
<span data-ttu-id="291ab-124">Das metrische Regelobjekt</span><span class="sxs-lookup"><span data-stu-id="291ab-124">The Metric rule object</span></span>

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

### <span data-ttu-id="291ab-125">-Name</span><span class="sxs-lookup"><span data-stu-id="291ab-125">-Name</span></span>
<span data-ttu-id="291ab-126">Der Name der Metrik-Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="291ab-126">The name of metric alert rule</span></span>

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

### <span data-ttu-id="291ab-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="291ab-127">-PassThru</span></span>
<span data-ttu-id="291ab-128">Beim erfolgreichen löschen wird true zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="291ab-128">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="291ab-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="291ab-129">-ResourceGroupName</span></span>
<span data-ttu-id="291ab-130">Die ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="291ab-130">The ResourceGroupName</span></span>

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

### <span data-ttu-id="291ab-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="291ab-131">-ResourceId</span></span>
<span data-ttu-id="291ab-132">Die RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="291ab-132">The RuleResourceId</span></span>

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

### <span data-ttu-id="291ab-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="291ab-133">-Confirm</span></span>
<span data-ttu-id="291ab-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="291ab-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="291ab-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="291ab-135">-WhatIf</span></span>
<span data-ttu-id="291ab-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="291ab-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="291ab-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="291ab-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="291ab-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="291ab-138">CommonParameters</span></span>
<span data-ttu-id="291ab-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="291ab-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="291ab-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="291ab-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="291ab-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="291ab-141">INPUTS</span></span>

### <span data-ttu-id="291ab-142">System. String</span><span class="sxs-lookup"><span data-stu-id="291ab-142">System.String</span></span>

### <span data-ttu-id="291ab-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="291ab-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="291ab-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="291ab-144">OUTPUTS</span></span>

### <span data-ttu-id="291ab-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="291ab-145">System.Boolean</span></span>

## <span data-ttu-id="291ab-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="291ab-146">NOTES</span></span>

## <span data-ttu-id="291ab-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="291ab-147">RELATED LINKS</span></span>
