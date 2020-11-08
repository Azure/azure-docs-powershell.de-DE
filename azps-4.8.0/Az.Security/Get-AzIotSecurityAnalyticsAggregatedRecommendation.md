---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: 944c029b4085316225887b821c4f6c8f52e7f92b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174192"
---
# <span data-ttu-id="621a6-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="621a6-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="621a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="621a6-102">SYNOPSIS</span></span>
<span data-ttu-id="621a6-103">Erhalten Sie viel Sicherheit zusammengefasste Empfehlung</span><span class="sxs-lookup"><span data-stu-id="621a6-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="621a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="621a6-104">SYNTAX</span></span>

### <span data-ttu-id="621a6-105">SolutionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="621a6-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="621a6-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="621a6-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="621a6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="621a6-107">DESCRIPTION</span></span>
<span data-ttu-id="621a6-108">Das Get-AzIotSecurityAnalyticsAggregatedAlert-Cmdlet gibt eine oder mehrere aggregierte Empfehlungen auf Geräten des viel-Hubs zurück.</span><span class="sxs-lookup"><span data-stu-id="621a6-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="621a6-109">Der Name einer aggregierten Empfehlung ist der Typ</span><span class="sxs-lookup"><span data-stu-id="621a6-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="621a6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="621a6-110">EXAMPLES</span></span>

### <span data-ttu-id="621a6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="621a6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name IoT_OpenPorts

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedRecommendations/IoT_OpenPorts"
Name: "IoT_OpenPorts"
Type: "Microsoft.Security/IoTSecurityAggregatedRecommendation"
RecommendationName: "IoT_OpenPorts"
RecommendationDisplayName: "Device has open ports"
RecommendationTypeId: ""
DetectedBy: "IoTSecurity"
HealthyDevices: -1
UnhealthyDeviceCount: 5
RemediationSteps: "Review open ports on the device and make sure they belong to legitimate and necessary processes for the device to function correctly."
ReportedSeverity: "Medium"
Description: "Found a listening endpoint on the device."
LogAnalyticsQuery: "SecurityRecommendation | where tolower(AssessedResourceId) == tolower('/subscriptions/075423e9-7d33-4166-8bdf-3920b04e3735/resourcegroups/iot-hub-demo/providers/microsoft.devices/iothubs/ascforiot-demo') and tolower(RecommendationName) == tolower('IoT_OpenPorts') and TimeGenerated  < now()"
```

<span data-ttu-id="621a6-112">Abrufen der aggregierten Empfehlung "IoT_OpenPorts" in der Sicherheitslösung "MySolution" und Ressourcengruppe "myresourcegroup"</span><span class="sxs-lookup"><span data-stu-id="621a6-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="621a6-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="621a6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="621a6-114">Abrufen einer Liste der aggregierten Empfehlungen in der Sicherheitslösung "MySolution" und Ressourcengruppe "myresourcegroup"</span><span class="sxs-lookup"><span data-stu-id="621a6-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="621a6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="621a6-115">PARAMETERS</span></span>

### <span data-ttu-id="621a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="621a6-116">-DefaultProfile</span></span>
<span data-ttu-id="621a6-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="621a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="621a6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="621a6-118">-Name</span></span>
<span data-ttu-id="621a6-119">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="621a6-119">Resource name.</span></span>

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

### <span data-ttu-id="621a6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="621a6-120">-ResourceGroupName</span></span>
<span data-ttu-id="621a6-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="621a6-121">Resource group name.</span></span>

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

### <span data-ttu-id="621a6-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="621a6-122">-SolutionName</span></span>
<span data-ttu-id="621a6-123">Projektmappenname</span><span class="sxs-lookup"><span data-stu-id="621a6-123">Solution name</span></span>

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

### <span data-ttu-id="621a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="621a6-124">CommonParameters</span></span>
<span data-ttu-id="621a6-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="621a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="621a6-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="621a6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="621a6-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="621a6-127">INPUTS</span></span>

### <span data-ttu-id="621a6-128">Keine</span><span class="sxs-lookup"><span data-stu-id="621a6-128">None</span></span>

## <span data-ttu-id="621a6-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="621a6-129">OUTPUTS</span></span>

### <span data-ttu-id="621a6-130">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="621a6-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="621a6-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="621a6-131">NOTES</span></span>

## <span data-ttu-id="621a6-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="621a6-132">RELATED LINKS</span></span>
