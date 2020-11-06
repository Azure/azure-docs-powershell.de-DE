---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
ms.openlocfilehash: a8bb330315cfdd43e30ab790afcdeba0b09cef08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497189"
---
# <span data-ttu-id="59947-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="59947-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="59947-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59947-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59947-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="59947-103">SYNTAX</span></span>

### <span data-ttu-id="59947-104">S1</span><span class="sxs-lookup"><span data-stu-id="59947-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59947-105">S2</span><span class="sxs-lookup"><span data-stu-id="59947-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59947-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59947-106">DESCRIPTION</span></span>
<span data-ttu-id="59947-107">Der **Get-AzureRmAppServicePlanMetrics** Ruft die Metriken für den App-Service Plan ab.</span><span class="sxs-lookup"><span data-stu-id="59947-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="59947-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59947-108">EXAMPLES</span></span>

### <span data-ttu-id="59947-109">1:</span><span class="sxs-lookup"><span data-stu-id="59947-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "CPU Percentage"
```

<span data-ttu-id="59947-110">Dieser Befehl ruft den CPU-Prozentsatz des App-Service-Plans pro Minute ab (PT1M-Abruf Zeit 1 Minute) zwischen Startzeit und EndTime</span><span class="sxs-lookup"><span data-stu-id="59947-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="59947-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="59947-111">PARAMETERS</span></span>

### <span data-ttu-id="59947-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="59947-112">-AppServicePlan</span></span>
<span data-ttu-id="59947-113">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="59947-113">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59947-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59947-114">-DefaultProfile</span></span>
<span data-ttu-id="59947-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59947-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59947-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="59947-116">-EndTime</span></span>
<span data-ttu-id="59947-117">Endzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="59947-117">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59947-118">-Granularität</span><span class="sxs-lookup"><span data-stu-id="59947-118">-Granularity</span></span>
<span data-ttu-id="59947-119">Granularität</span><span class="sxs-lookup"><span data-stu-id="59947-119">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59947-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="59947-120">-InstanceDetails</span></span>
<span data-ttu-id="59947-121">Instanzen Details</span><span class="sxs-lookup"><span data-stu-id="59947-121">Instance Details</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59947-122">-Metriken</span><span class="sxs-lookup"><span data-stu-id="59947-122">-Metrics</span></span>
<span data-ttu-id="59947-123">Metriken</span><span class="sxs-lookup"><span data-stu-id="59947-123">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59947-124">-Name</span><span class="sxs-lookup"><span data-stu-id="59947-124">-Name</span></span>
<span data-ttu-id="59947-125">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="59947-125">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59947-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59947-126">-ResourceGroupName</span></span>
<span data-ttu-id="59947-127">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="59947-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59947-128">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="59947-128">-StartTime</span></span>
<span data-ttu-id="59947-129">Startzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="59947-129">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59947-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59947-130">CommonParameters</span></span>
<span data-ttu-id="59947-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59947-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59947-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59947-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59947-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59947-133">INPUTS</span></span>

### <span data-ttu-id="59947-134">Microsoft. Azure. Management. Websites. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="59947-134">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="59947-135">Parameter: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="59947-135">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="59947-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59947-136">OUTPUTS</span></span>

### <span data-ttu-id="59947-137">Microsoft. Azure. Management. Websites. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="59947-137">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="59947-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="59947-138">NOTES</span></span>

## <span data-ttu-id="59947-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59947-139">RELATED LINKS</span></span>
