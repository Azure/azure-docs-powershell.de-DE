---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
ms.openlocfilehash: c08ae63999582fd220005dde84316a2f4421d7b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842804"
---
# <span data-ttu-id="00195-101">Get-AzAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="00195-101">Get-AzAppServicePlanMetrics</span></span>

## <span data-ttu-id="00195-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="00195-102">SYNOPSIS</span></span>
<span data-ttu-id="00195-103">Ruft Azure Web Service Plan Metrics ab.</span><span class="sxs-lookup"><span data-stu-id="00195-103">Gets Azure Web service plan metrics.</span></span>

## <span data-ttu-id="00195-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="00195-104">SYNTAX</span></span>

### <span data-ttu-id="00195-105">S1</span><span class="sxs-lookup"><span data-stu-id="00195-105">S1</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00195-106">S2</span><span class="sxs-lookup"><span data-stu-id="00195-106">S2</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <AppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00195-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00195-107">DESCRIPTION</span></span>
<span data-ttu-id="00195-108">Der **Get-AzAppServicePlanMetrics** Ruft die Metriken für den App-Service Plan ab.</span><span class="sxs-lookup"><span data-stu-id="00195-108">The **Get-AzAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="00195-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00195-109">EXAMPLES</span></span>

### <span data-ttu-id="00195-110">1:</span><span class="sxs-lookup"><span data-stu-id="00195-110">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="00195-111">Dieser Befehl ruft den CPU-Prozentsatz des App-Service-Plans pro Minute ab (PT1M-Abruf Zeit 1 Minute) zwischen Startzeit und EndTime</span><span class="sxs-lookup"><span data-stu-id="00195-111">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="00195-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="00195-112">PARAMETERS</span></span>

### <span data-ttu-id="00195-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="00195-113">-AppServicePlan</span></span>
<span data-ttu-id="00195-114">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="00195-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00195-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00195-115">-DefaultProfile</span></span>
<span data-ttu-id="00195-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="00195-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00195-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="00195-117">-EndTime</span></span>
<span data-ttu-id="00195-118">Endzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="00195-118">End Time in UTC</span></span>

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

### <span data-ttu-id="00195-119">-Granularität</span><span class="sxs-lookup"><span data-stu-id="00195-119">-Granularity</span></span>
<span data-ttu-id="00195-120">Granularität</span><span class="sxs-lookup"><span data-stu-id="00195-120">Granularity</span></span>

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

### <span data-ttu-id="00195-121">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="00195-121">-InstanceDetails</span></span>
<span data-ttu-id="00195-122">Instanzen Details</span><span class="sxs-lookup"><span data-stu-id="00195-122">Instance Details</span></span>

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

### <span data-ttu-id="00195-123">-Metriken</span><span class="sxs-lookup"><span data-stu-id="00195-123">-Metrics</span></span>
<span data-ttu-id="00195-124">Metriken</span><span class="sxs-lookup"><span data-stu-id="00195-124">Metrics</span></span>

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

### <span data-ttu-id="00195-125">-Name</span><span class="sxs-lookup"><span data-stu-id="00195-125">-Name</span></span>
<span data-ttu-id="00195-126">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="00195-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="00195-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00195-127">-ResourceGroupName</span></span>
<span data-ttu-id="00195-128">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="00195-128">Resource Group Name</span></span>

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

### <span data-ttu-id="00195-129">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="00195-129">-StartTime</span></span>
<span data-ttu-id="00195-130">Startzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="00195-130">Start Time in UTC</span></span>

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

### <span data-ttu-id="00195-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00195-131">CommonParameters</span></span>
<span data-ttu-id="00195-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00195-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00195-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00195-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00195-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="00195-134">INPUTS</span></span>

### <span data-ttu-id="00195-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="00195-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="00195-136">Der Parameter "AppServicePlan" akzeptiert den Wert vom Typ "ServerFarmWithRichSku" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="00195-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="00195-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="00195-137">OUTPUTS</span></span>

## <span data-ttu-id="00195-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="00195-138">NOTES</span></span>

## <span data-ttu-id="00195-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="00195-139">RELATED LINKS</span></span>

