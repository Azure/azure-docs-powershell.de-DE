---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
ms.openlocfilehash: f3376f40246640b8de52ffa138912c768486a3dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663735"
---
# <span data-ttu-id="c0c61-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="c0c61-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="c0c61-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0c61-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0c61-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0c61-103">SYNTAX</span></span>

### <span data-ttu-id="c0c61-104">S1</span><span class="sxs-lookup"><span data-stu-id="c0c61-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0c61-105">S2</span><span class="sxs-lookup"><span data-stu-id="c0c61-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <ServerFarmWithRichSku>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0c61-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0c61-106">DESCRIPTION</span></span>
<span data-ttu-id="c0c61-107">Der **Get-AzureRmAppServicePlanMetrics** Ruft die Metriken für den App-Service Plan ab.</span><span class="sxs-lookup"><span data-stu-id="c0c61-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="c0c61-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0c61-108">EXAMPLES</span></span>

### <span data-ttu-id="c0c61-109">1:</span><span class="sxs-lookup"><span data-stu-id="c0c61-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="c0c61-110">Dieser Befehl ruft den CPU-Prozentsatz des App-Service-Plans pro Minute ab (PT1M-Abruf Zeit 1 Minute) zwischen Startzeit und EndTime</span><span class="sxs-lookup"><span data-stu-id="c0c61-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="c0c61-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0c61-111">PARAMETERS</span></span>

### <span data-ttu-id="c0c61-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c0c61-112">-AppServicePlan</span></span>
<span data-ttu-id="c0c61-113">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="c0c61-113">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c61-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c61-114">-DefaultProfile</span></span>
<span data-ttu-id="c0c61-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0c61-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c61-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c0c61-116">-EndTime</span></span>
<span data-ttu-id="c0c61-117">Endzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="c0c61-117">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c61-118">-Granularität</span><span class="sxs-lookup"><span data-stu-id="c0c61-118">-Granularity</span></span>
<span data-ttu-id="c0c61-119">Granularität</span><span class="sxs-lookup"><span data-stu-id="c0c61-119">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c61-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="c0c61-120">-InstanceDetails</span></span>
<span data-ttu-id="c0c61-121">Instanzen Details</span><span class="sxs-lookup"><span data-stu-id="c0c61-121">Instance Details</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c61-122">-Metriken</span><span class="sxs-lookup"><span data-stu-id="c0c61-122">-Metrics</span></span>
<span data-ttu-id="c0c61-123">Metriken</span><span class="sxs-lookup"><span data-stu-id="c0c61-123">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c61-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c0c61-124">-Name</span></span>
<span data-ttu-id="c0c61-125">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="c0c61-125">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c61-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0c61-126">-ResourceGroupName</span></span>
<span data-ttu-id="c0c61-127">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="c0c61-127">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c61-128">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="c0c61-128">-StartTime</span></span>
<span data-ttu-id="c0c61-129">Startzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="c0c61-129">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c61-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c61-130">CommonParameters</span></span>
<span data-ttu-id="c0c61-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0c61-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c61-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0c61-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c61-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0c61-133">INPUTS</span></span>

### <span data-ttu-id="c0c61-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="c0c61-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="c0c61-135">Der Parameter "AppServicePlan" akzeptiert den Wert vom Typ "ServerFarmWithRichSku" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c0c61-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="c0c61-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0c61-136">OUTPUTS</span></span>

## <span data-ttu-id="c0c61-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0c61-137">NOTES</span></span>

## <span data-ttu-id="c0c61-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0c61-138">RELATED LINKS</span></span>

