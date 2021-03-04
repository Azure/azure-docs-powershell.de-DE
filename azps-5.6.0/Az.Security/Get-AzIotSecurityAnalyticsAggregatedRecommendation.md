---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: f57d3b3eb254a547059cb2e7c37a0720ee5f6310
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927579"
---
# <span data-ttu-id="0c720-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="0c720-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="0c720-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c720-102">SYNOPSIS</span></span>
<span data-ttu-id="0c720-103">Zusammengefasste Empfehlung zur IoT-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="0c720-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="0c720-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c720-104">SYNTAX</span></span>

### <span data-ttu-id="0c720-105">SolutionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="0c720-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c720-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="0c720-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c720-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c720-107">DESCRIPTION</span></span>
<span data-ttu-id="0c720-108">Das Get-AzIotSecurityAnalyticsAggregatedAlert-Cmdlet gibt eine oder mehrere zusammengefasste Empfehlungen auf Geräten des iot-Hubs zurück.</span><span class="sxs-lookup"><span data-stu-id="0c720-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="0c720-109">Der Name einer aggregierten Empfehlung ist der Typ</span><span class="sxs-lookup"><span data-stu-id="0c720-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="0c720-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0c720-110">EXAMPLES</span></span>

### <span data-ttu-id="0c720-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0c720-111">Example 1</span></span>
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

<span data-ttu-id="0c720-112">Erhalten Sie die aggregierte Empfehlung "IoT_OpenPorts" in der Sicherheitslösung "MySolution" und der Ressourcengruppe "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="0c720-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="0c720-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0c720-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="0c720-114">Eine Liste der zusammengefassten Empfehlungen in der Sicherheitslösung "MySolution" und der Ressourcengruppe "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="0c720-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="0c720-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0c720-115">PARAMETERS</span></span>

### <span data-ttu-id="0c720-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c720-116">-DefaultProfile</span></span>
<span data-ttu-id="0c720-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0c720-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c720-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0c720-118">-Name</span></span>
<span data-ttu-id="0c720-119">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="0c720-119">Resource name.</span></span>

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

### <span data-ttu-id="0c720-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c720-120">-ResourceGroupName</span></span>
<span data-ttu-id="0c720-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0c720-121">Resource group name.</span></span>

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

### <span data-ttu-id="0c720-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="0c720-122">-SolutionName</span></span>
<span data-ttu-id="0c720-123">Projektmappenname</span><span class="sxs-lookup"><span data-stu-id="0c720-123">Solution name</span></span>

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

### <span data-ttu-id="0c720-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c720-124">CommonParameters</span></span>
<span data-ttu-id="0c720-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c720-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c720-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c720-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c720-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0c720-127">INPUTS</span></span>

### <span data-ttu-id="0c720-128">Keine</span><span class="sxs-lookup"><span data-stu-id="0c720-128">None</span></span>

## <span data-ttu-id="0c720-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0c720-129">OUTPUTS</span></span>

### <span data-ttu-id="0c720-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="0c720-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="0c720-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0c720-131">NOTES</span></span>

## <span data-ttu-id="0c720-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0c720-132">RELATED LINKS</span></span>
