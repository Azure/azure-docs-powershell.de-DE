---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
ms.openlocfilehash: 8fa796b9b8940662c091e160cea55235816a29d6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305032"
---
# <span data-ttu-id="6fa3c-101">New-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="6fa3c-101">New-AzDiagnosticSetting</span></span>

## <span data-ttu-id="6fa3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fa3c-102">SYNOPSIS</span></span>
<span data-ttu-id="6fa3c-103">Erstellen Sie das PSServiceDiagnosticSettings-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6fa3c-103">Create PSServiceDiagnosticSettings object.</span></span>

## <span data-ttu-id="6fa3c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fa3c-104">SYNTAX</span></span>

```
New-AzDiagnosticSetting -TargetResourceId <String> -Name <String> [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-WorkspaceId <String>] [-DedicatedLogAnalyticsDestinationType] [-Setting <PSDiagnosticDetailSettings[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fa3c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fa3c-105">DESCRIPTION</span></span>
<span data-ttu-id="6fa3c-106">Erstellen Sie das PSServiceDiagnosticSettings-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6fa3c-106">Create PSServiceDiagnosticSettings object.</span></span>
<span data-ttu-id="6fa3c-107">Dies kann als Parameter `-InputObject` für `Set-AzDiagnosticSetting`</span><span class="sxs-lookup"><span data-stu-id="6fa3c-107">This can be used as parameter `-InputObject` for `Set-AzDiagnosticSetting`</span></span>

## <span data-ttu-id="6fa3c-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6fa3c-108">EXAMPLES</span></span>

### <span data-ttu-id="6fa3c-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6fa3c-109">Example 1</span></span>
```powershell
$TimeGrain=New-TimeSpan -Days 90
$metric = New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics
$log = New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
$setting = New-AzDiagnosticSetting -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX -Name diagnostic-test -WorkspaceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX -DedicatedLogAnalyticsDestinationType -Setting $log,$metric
Location                    :
Tags                        :
Id                          : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/diagnosticSettings/diagnostic-test
Name                        : diagnostic-test
StorageAccountId            :
ServiceBusRuleId            :
EventHubAuthorizationRuleId :
EventHubName                :
Metrics
    TimeGrain       :
    Category        : AllMetrics
    Enabled         : False
    RetentionPolicy
    Enabled : True
    Days    : 1


Logs
    Category        : Audit
    Enabled         : True
    RetentionPolicy
    Enabled : True
    Days    : 1


WorkspaceId                 : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX
LogAnalyticsDestinationType : Dedicated
Type                        :

Set-AzDiagnosticSetting -InputObject $setting
```

<span data-ttu-id="6fa3c-110">Erstellen Sie das PSServiceDiagnosticSettings-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6fa3c-110">Create PSServiceDiagnosticSettings object.</span></span> <span data-ttu-id="6fa3c-111">Und erstellen Sie eine Diagnoseeinstellung für die Zielressource.</span><span class="sxs-lookup"><span data-stu-id="6fa3c-111">And create diagnostic setting for target resource.</span></span>

## <span data-ttu-id="6fa3c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fa3c-112">PARAMETERS</span></span>

### <span data-ttu-id="6fa3c-113">-DedicatedLogAnalyticsDestinationType</span><span class="sxs-lookup"><span data-stu-id="6fa3c-113">-DedicatedLogAnalyticsDestinationType</span></span>
<span data-ttu-id="6fa3c-114">Der Wert, der angibt, ob in ressourcenspezifische (falls vorhanden) oder nach AzureDiagnostics (Standard, nicht vorhanden) exportiert werden soll</span><span class="sxs-lookup"><span data-stu-id="6fa3c-114">The value indicating whether to export (to ODS) to resource-specific (if present) or to AzureDiagnostics (default, not present)</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa3c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fa3c-115">-DefaultProfile</span></span>
<span data-ttu-id="6fa3c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6fa3c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fa3c-117">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="6fa3c-117">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="6fa3c-118">Die Ereignishubregel-ID</span><span class="sxs-lookup"><span data-stu-id="6fa3c-118">The event hub rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa3c-119">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="6fa3c-119">-EventHubName</span></span>
<span data-ttu-id="6fa3c-120">Die Regel-ID des Dienstbuss</span><span class="sxs-lookup"><span data-stu-id="6fa3c-120">The service bus rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa3c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6fa3c-121">-Name</span></span>
<span data-ttu-id="6fa3c-122">Der Name der Diagnoseeinstellung.</span><span class="sxs-lookup"><span data-stu-id="6fa3c-122">The name of the diagnostic setting.</span></span>
<span data-ttu-id="6fa3c-123">Standardeinstellung "Dienst"</span><span class="sxs-lookup"><span data-stu-id="6fa3c-123">Defaults to 'service'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa3c-124">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="6fa3c-124">-ServiceBusRuleId</span></span>
<span data-ttu-id="6fa3c-125">Die Regel-ID des Dienstbuss</span><span class="sxs-lookup"><span data-stu-id="6fa3c-125">The service bus rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa3c-126">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="6fa3c-126">-Setting</span></span>
<span data-ttu-id="6fa3c-127">Metrische Einstellungen oder Protokolleinstellungen</span><span class="sxs-lookup"><span data-stu-id="6fa3c-127">Metric settings or Log settings</span></span>

```yaml
Type: PSDiagnosticDetailSettings[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa3c-128">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6fa3c-128">-StorageAccountId</span></span>
<span data-ttu-id="6fa3c-129">Die Speicherkonto-ID</span><span class="sxs-lookup"><span data-stu-id="6fa3c-129">The storage account id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa3c-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6fa3c-130">-TargetResourceId</span></span>
<span data-ttu-id="6fa3c-131">Die Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6fa3c-131">The resource id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa3c-132">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="6fa3c-132">-WorkspaceId</span></span>
<span data-ttu-id="6fa3c-133">Die Ressourcen-ID des Log Analytics-Arbeitsbereichs, an den Protokolle/Metriken gesendet werden</span><span class="sxs-lookup"><span data-stu-id="6fa3c-133">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa3c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fa3c-134">CommonParameters</span></span>
<span data-ttu-id="6fa3c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fa3c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fa3c-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fa3c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fa3c-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6fa3c-137">INPUTS</span></span>

### <span data-ttu-id="6fa3c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6fa3c-138">System.String</span></span>

### <span data-ttu-id="6fa3c-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6fa3c-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6fa3c-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings[]</span><span class="sxs-lookup"><span data-stu-id="6fa3c-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings[]</span></span>

## <span data-ttu-id="6fa3c-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6fa3c-141">OUTPUTS</span></span>

### <span data-ttu-id="6fa3c-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="6fa3c-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="6fa3c-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6fa3c-143">NOTES</span></span>

## <span data-ttu-id="6fa3c-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6fa3c-144">RELATED LINKS</span></span>
