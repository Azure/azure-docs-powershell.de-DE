---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslotmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotMetrics.md
ms.openlocfilehash: 474f5a450adba9f01ef56fe99875d062ece1689d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842759"
---
# <span data-ttu-id="551ff-101">Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="551ff-101">Get-AzWebAppSlotMetrics</span></span>

## <span data-ttu-id="551ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="551ff-102">SYNOPSIS</span></span>
<span data-ttu-id="551ff-103">Ruft Metriken für einen Azure Web App-Slot ab.</span><span class="sxs-lookup"><span data-stu-id="551ff-103">Gets metrics for an Azure Web App slot.</span></span>

## <span data-ttu-id="551ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="551ff-104">SYNTAX</span></span>

### <span data-ttu-id="551ff-105">S1</span><span class="sxs-lookup"><span data-stu-id="551ff-105">S1</span></span>
```
Get-AzWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="551ff-106">S2</span><span class="sxs-lookup"><span data-stu-id="551ff-106">S2</span></span>
```
Get-AzWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="551ff-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="551ff-107">DESCRIPTION</span></span>
<span data-ttu-id="551ff-108">Der **Get-AzWebAppSlotMetrics** ruft Web App-Metriken für den angegebenen Slot ab.</span><span class="sxs-lookup"><span data-stu-id="551ff-108">The **Get-AzWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="551ff-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="551ff-109">EXAMPLES</span></span>

### <span data-ttu-id="551ff-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="551ff-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="551ff-111">Mit diesem Befehl wird die Anforderung der angegebenen Web-App pro Minute (PT1M-Abruf Zeit 1 Minute) zwischen Startzeit und EndTime abgerufen.</span><span class="sxs-lookup"><span data-stu-id="551ff-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="551ff-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="551ff-112">PARAMETERS</span></span>

### <span data-ttu-id="551ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="551ff-113">-DefaultProfile</span></span>
<span data-ttu-id="551ff-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="551ff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="551ff-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="551ff-115">-EndTime</span></span>
<span data-ttu-id="551ff-116">Endzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="551ff-116">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551ff-117">-Granularität</span><span class="sxs-lookup"><span data-stu-id="551ff-117">-Granularity</span></span>
<span data-ttu-id="551ff-118">Granularität</span><span class="sxs-lookup"><span data-stu-id="551ff-118">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551ff-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="551ff-119">-InstanceDetails</span></span>
<span data-ttu-id="551ff-120">Instanzen Details</span><span class="sxs-lookup"><span data-stu-id="551ff-120">Instance Details</span></span>

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

### <span data-ttu-id="551ff-121">-Metriken</span><span class="sxs-lookup"><span data-stu-id="551ff-121">-Metrics</span></span>
<span data-ttu-id="551ff-122">Metriken</span><span class="sxs-lookup"><span data-stu-id="551ff-122">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551ff-123">-Name</span><span class="sxs-lookup"><span data-stu-id="551ff-123">-Name</span></span>
<span data-ttu-id="551ff-124">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="551ff-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="551ff-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="551ff-125">-ResourceGroupName</span></span>
<span data-ttu-id="551ff-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="551ff-126">Resource Group Name</span></span>

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

### <span data-ttu-id="551ff-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="551ff-127">-Slot</span></span>
<span data-ttu-id="551ff-128">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="551ff-128">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551ff-129">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="551ff-129">-StartTime</span></span>
<span data-ttu-id="551ff-130">Startzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="551ff-130">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551ff-131">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="551ff-131">-WebApp</span></span>
<span data-ttu-id="551ff-132">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="551ff-132">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="551ff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="551ff-133">CommonParameters</span></span>
<span data-ttu-id="551ff-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="551ff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="551ff-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="551ff-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="551ff-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="551ff-136">INPUTS</span></span>

### <span data-ttu-id="551ff-137">Website</span><span class="sxs-lookup"><span data-stu-id="551ff-137">Site</span></span>
<span data-ttu-id="551ff-138">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="551ff-138">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="551ff-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="551ff-139">OUTPUTS</span></span>

## <span data-ttu-id="551ff-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="551ff-140">NOTES</span></span>

## <span data-ttu-id="551ff-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="551ff-141">RELATED LINKS</span></span>

[<span data-ttu-id="551ff-142">Get-AzAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="551ff-142">Get-AzAppServicePlanMetrics</span></span>](./Get-AzAppServicePlanMetrics.md)

[<span data-ttu-id="551ff-143">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="551ff-143">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="551ff-144">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="551ff-144">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)
