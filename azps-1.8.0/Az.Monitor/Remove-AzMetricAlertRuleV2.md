---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: 698f05840df6578d8595e2ca8e31c9f0a11bc722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660997"
---
# <span data-ttu-id="c5668-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c5668-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="c5668-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5668-102">SYNOPSIS</span></span>
<span data-ttu-id="c5668-103">Entfernt eine metrische Warnungsregel v2 (nicht klassisch).</span><span class="sxs-lookup"><span data-stu-id="c5668-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="c5668-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5668-104">SYNTAX</span></span>

### <span data-ttu-id="c5668-105">ByMetricRuleResourceName</span><span class="sxs-lookup"><span data-stu-id="c5668-105">ByMetricRuleResourceName</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5668-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="c5668-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5668-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="c5668-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5668-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5668-108">DESCRIPTION</span></span>
<span data-ttu-id="c5668-109">Das Cmdlet **Remove-AzMetricAlertRuleV2** entfernt eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="c5668-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="c5668-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c5668-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="c5668-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5668-111">EXAMPLES</span></span>

### <span data-ttu-id="c5668-112">Beispiel 1: Entfernen einer Warnungsregel nach Namen</span><span class="sxs-lookup"><span data-stu-id="c5668-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="c5668-113">Dieser Befehl entfernt die Warnungsregel mit dem Namen PsSdk</span><span class="sxs-lookup"><span data-stu-id="c5668-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="c5668-114">Beispiel 2: Entfernen einer Warnungsregel nach ID</span><span class="sxs-lookup"><span data-stu-id="c5668-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="c5668-115">Mit diesem Befehl wird die Warnungsregel mit der Ressourcen-ID entfernt `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="c5668-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>
### <span data-ttu-id="c5668-116">Beispiel 3: besorgen Sie sich eine Benachrichtigung, und entfernen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="c5668-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="c5668-117">Dieser Befehl ruft eine Benachrichtigung ab und entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="c5668-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="c5668-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5668-118">PARAMETERS</span></span>

### <span data-ttu-id="c5668-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5668-119">-AsJob</span></span>
<span data-ttu-id="c5668-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c5668-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5668-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c5668-121">-Confirm</span></span>
<span data-ttu-id="c5668-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c5668-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5668-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5668-123">-DefaultProfile</span></span>
<span data-ttu-id="c5668-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5668-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5668-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c5668-125">-InputObject</span></span>
<span data-ttu-id="c5668-126">Das metrische Regelobjekt</span><span class="sxs-lookup"><span data-stu-id="c5668-126">The Metric rule object</span></span>

```yaml
Type: PSMetricAlertRuleV2
Parameter Sets: ByRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5668-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c5668-127">-Name</span></span>
<span data-ttu-id="c5668-128">Der Name der Metrik-Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="c5668-128">The name of metric alert rule</span></span>

```yaml
Type: String
Parameter Sets: ByMetricRuleResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5668-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5668-129">-PassThru</span></span>
<span data-ttu-id="c5668-130">Beim erfolgreichen löschen wird true zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c5668-130">Return true upon successful deletion.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5668-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5668-131">-ResourceGroupName</span></span>
<span data-ttu-id="c5668-132">Die ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5668-132">The ResourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: ByMetricRuleResourceName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5668-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c5668-133">-ResourceId</span></span>
<span data-ttu-id="c5668-134">Die RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="c5668-134">The RuleResourceId</span></span>

```yaml
Type: String
Parameter Sets: ByMetricRuleResourceId
Aliases: RuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5668-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5668-135">-WhatIf</span></span>
<span data-ttu-id="c5668-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c5668-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5668-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5668-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5668-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5668-138">CommonParameters</span></span>
<span data-ttu-id="c5668-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5668-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c5668-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5668-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5668-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5668-141">INPUTS</span></span>

### <span data-ttu-id="c5668-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c5668-142">System.String</span></span>

### <span data-ttu-id="c5668-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c5668-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="c5668-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5668-144">OUTPUTS</span></span>

### <span data-ttu-id="c5668-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c5668-145">System.Boolean</span></span>

## <span data-ttu-id="c5668-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5668-146">NOTES</span></span>

## <span data-ttu-id="c5668-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5668-147">RELATED LINKS</span></span>
