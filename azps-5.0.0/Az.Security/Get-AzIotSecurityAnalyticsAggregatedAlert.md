---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 5687497c55c6da914b28022320df1d7241f2eba1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179677"
---
# <span data-ttu-id="10839-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="10839-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="10839-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="10839-102">SYNOPSIS</span></span>
<span data-ttu-id="10839-103">Erhalten Sie viel Sicherheit aggregierte Warnung</span><span class="sxs-lookup"><span data-stu-id="10839-103">Get IoT security aggregated alert</span></span>

## <span data-ttu-id="10839-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="10839-104">SYNTAX</span></span>

### <span data-ttu-id="10839-105">SolutionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="10839-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10839-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="10839-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10839-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10839-107">DESCRIPTION</span></span>
<span data-ttu-id="10839-108">Das Get-AzIotSecurityAnalyticsAggregatedAlert-Cmdlet gibt mindestens eine aggregierte Warnung auf Geräten von viel Hub zurück.</span><span class="sxs-lookup"><span data-stu-id="10839-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated alerts on devices of iot hub.</span></span>
<span data-ttu-id="10839-109">Der Name der aggregierten Alerts ist eine Kombination aus dem Warnungstyp und dem Warnungs aggragted Datum, getrennt durch "/".</span><span class="sxs-lookup"><span data-stu-id="10839-109">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="10839-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10839-110">EXAMPLES</span></span>

### <span data-ttu-id="10839-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="10839-111">Example 1</span></span>
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

<span data-ttu-id="10839-112">Besorgen Sie sich die aggregierte Warnung "IoT_Bruteforce_Fail/2019-02-02" (der Name kombiniert vom Warnungstyp und dem aggregierten Datum) in der Projektmappe "MySolution" und der Ressourcengruppe "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="10839-112">Get the aggregated alert "IoT_Bruteforce_Fail/2019-02-02" (the name combined from the alert type and its aggregated date) in solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="10839-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="10839-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated alert items as shown in example 1
```

<span data-ttu-id="10839-114">Abrufen einer Liste aller aggregierten Warnungen in der Projektmappe "MySolution" und Ressourcengruppe "myresourcegroup"</span><span class="sxs-lookup"><span data-stu-id="10839-114">Get a list of all aggregated alerts in solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="10839-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="10839-115">PARAMETERS</span></span>

### <span data-ttu-id="10839-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10839-116">-DefaultProfile</span></span>
<span data-ttu-id="10839-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="10839-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10839-118">-Name</span><span class="sxs-lookup"><span data-stu-id="10839-118">-Name</span></span>
<span data-ttu-id="10839-119">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="10839-119">Resource name.</span></span>

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

### <span data-ttu-id="10839-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10839-120">-ResourceGroupName</span></span>
<span data-ttu-id="10839-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="10839-121">Resource group name.</span></span>

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

### <span data-ttu-id="10839-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="10839-122">-SolutionName</span></span>
<span data-ttu-id="10839-123">Projektmappenname</span><span class="sxs-lookup"><span data-stu-id="10839-123">Solution name</span></span>

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

### <span data-ttu-id="10839-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10839-124">CommonParameters</span></span>
<span data-ttu-id="10839-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10839-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10839-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10839-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10839-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="10839-127">INPUTS</span></span>

### <span data-ttu-id="10839-128">Keine</span><span class="sxs-lookup"><span data-stu-id="10839-128">None</span></span>

## <span data-ttu-id="10839-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="10839-129">OUTPUTS</span></span>

### <span data-ttu-id="10839-130">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="10839-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

## <span data-ttu-id="10839-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="10839-131">NOTES</span></span>

## <span data-ttu-id="10839-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="10839-132">RELATED LINKS</span></span>
