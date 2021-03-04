---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: febe9b4c758fb96e37962d810ef765b66b79fd24
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927584"
---
# <span data-ttu-id="e5d7b-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="e5d7b-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="e5d7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d7b-103">Zusammengefasste Benachrichtigung zur IoT-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="e5d7b-103">Get IoT security aggregated alert</span></span>

## <span data-ttu-id="e5d7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5d7b-104">SYNTAX</span></span>

### <span data-ttu-id="e5d7b-105">SolutionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5d7b-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5d7b-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="e5d7b-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5d7b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5d7b-107">DESCRIPTION</span></span>
<span data-ttu-id="e5d7b-108">Das Get-AzIotSecurityAnalyticsAggregatedAlert-Cmdlet gibt eine oder mehrere aggregierte Benachrichtigungen auf Geräten des iot-Hubs zurück.</span><span class="sxs-lookup"><span data-stu-id="e5d7b-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated alerts on devices of iot hub.</span></span>
<span data-ttu-id="e5d7b-109">Der Name der aggregierten Benachrichtigungen ist eine Kombination aus dem Warnungstyp und dem Benachrichtigungsaggragted-Datum, getrennt durch "/".</span><span class="sxs-lookup"><span data-stu-id="e5d7b-109">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="e5d7b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e5d7b-110">EXAMPLES</span></span>

### <span data-ttu-id="e5d7b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5d7b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name "IoT_Bruteforce_Fail/2019-02-02"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedAlerts/IoT_Bruteforce_Fail/2019-02-02"
Name: "IoT_Bruteforce_Fail/2019-02-02"
Type: "Microsoft.Security/IoTSecurityAggregatedAlert"
AlertType: "IoT_Bruteforce_Fail"
AlertDisplayName: "Failed Bruteforce"
AggregatedDateUtc: "2019-02-02"
VendorName: "Microsoft"
ReportedSeverity: "Low"
RemediationSteps: ""
Description: "Multiple unsuccsseful login attempts identified. A Bruteforce attack on the device failed."
Count: 50
EffectedResourceType: "IoT Device"
SystemSource: "Devices"
ActionTaken: "Detected"
LogAnalyticsQuery: "SecurityAlert | where tolower(ResourceId) == tolower('/subscriptions/b77ec8a9-04ed-48d2-a87a-e5887b978ba6/resourceGroups/IoT-Solution-DemoEnv/providers/Microsoft.Devices/IotHubs/rtogm-hub') and tolower(AlertName) == tolower('Custom Alert - number of device to cloud messages in MQTT protocol is not in the allowed range') | extend DeviceId=parse_json(ExtendedProperties)['DeviceId'] | project DeviceId, TimeGenerated, DisplayName, AlertSeverity, Description, RemediationSteps, ExtendedProperties"
TopDevicesList: [
                {
                  DeviceId: "testDevice1"
                  AlertsCount: 45
                  LastOccurrence: "10:42"
                }
                {
                  DeviceId: "testDevice2"
                  AlertsCount: 30
                  LastOccurrence: "15:42"
                }
              ]
```

<span data-ttu-id="e5d7b-112">Holen Sie sich die aggregierte Benachrichtigung "IoT_Bruteforce_Fail/2019-02-02" (der Name kombiniert aus dem Warnungstyp und dem aggregierten Datum) in der Projektmappe "MySolution" und der Ressourcengruppe "MyResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="e5d7b-112">Get the aggregated alert "IoT_Bruteforce_Fail/2019-02-02" (the name combined from the alert type and its aggregated date) in solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="e5d7b-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e5d7b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated alert items as shown in example 1
```

<span data-ttu-id="e5d7b-114">Hier erhalten Sie eine Liste aller aggregierten Benachrichtigungen in der Projektmappe "MySolution" und der Ressourcengruppe "MyResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="e5d7b-114">Get a list of all aggregated alerts in solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="e5d7b-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e5d7b-115">PARAMETERS</span></span>

### <span data-ttu-id="e5d7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d7b-116">-DefaultProfile</span></span>
<span data-ttu-id="e5d7b-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5d7b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5d7b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e5d7b-118">-Name</span></span>
<span data-ttu-id="e5d7b-119">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="e5d7b-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d7b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5d7b-120">-ResourceGroupName</span></span>
<span data-ttu-id="e5d7b-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e5d7b-121">Resource group name.</span></span>

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

### <span data-ttu-id="e5d7b-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="e5d7b-122">-SolutionName</span></span>
<span data-ttu-id="e5d7b-123">Projektmappenname</span><span class="sxs-lookup"><span data-stu-id="e5d7b-123">Solution name</span></span>

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

### <span data-ttu-id="e5d7b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d7b-124">CommonParameters</span></span>
<span data-ttu-id="e5d7b-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5d7b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d7b-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5d7b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d7b-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e5d7b-127">INPUTS</span></span>

### <span data-ttu-id="e5d7b-128">Keine</span><span class="sxs-lookup"><span data-stu-id="e5d7b-128">None</span></span>

## <span data-ttu-id="e5d7b-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e5d7b-129">OUTPUTS</span></span>

### <span data-ttu-id="e5d7b-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="e5d7b-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

## <span data-ttu-id="e5d7b-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e5d7b-131">NOTES</span></span>

## <span data-ttu-id="e5d7b-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e5d7b-132">RELATED LINKS</span></span>
