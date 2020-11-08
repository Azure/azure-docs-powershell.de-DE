---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 717023DA-AA2D-4F1B-AE46-67ED75AA0D15
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6d8dae704946680dd72ff8227d2a88d55f8b77a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006477"
---
# <span data-ttu-id="8920e-101">Get-AzureWebsiteMetric</span><span class="sxs-lookup"><span data-stu-id="8920e-101">Get-AzureWebsiteMetric</span></span>

## <span data-ttu-id="8920e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8920e-102">SYNOPSIS</span></span>
<span data-ttu-id="8920e-103">Ruft Metriken für die Azure-Website im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="8920e-103">Gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="8920e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8920e-104">SYNTAX</span></span>

```
Get-AzureWebsiteMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-SlotView] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8920e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8920e-105">DESCRIPTION</span></span>
<span data-ttu-id="8920e-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8920e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8920e-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8920e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8920e-108">Das Cmdlet " **Get-AzureWebsiteMetric** " ruft Metriken für die Azure-Website im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="8920e-108">The **Get-AzureWebsiteMetric** cmdlet gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="8920e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8920e-109">EXAMPLES</span></span>

### <span data-ttu-id="8920e-110">Beispiel 1: Abrufen von Metriken für die letzten drei Stunden auf einer Ebene pro Instanz für eine Website</span><span class="sxs-lookup"><span data-stu-id="8920e-110">Example 1: Get metrics for the last three hours on a per-instance level for a website</span></span>
```
PS C:\> Get-AzureWebsiteMetric -Name "ContosoWebSite" -StartDate (get-date).AddHours(-3) -MetricNames "Requests" -InstanceDetails -SlotView -TimeGrain "PT1M" 
PS C:\> $metrics[1].Data Name : Requests 

Unit : Count 

StartTime : 8/11/2014 7:05:00 AM 

EndTime : 8/11/2014 5:06:01 PM 

TimeGrain : PT1M 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:05:00 AM, Total:4, Min:, Max:, Time:8/11/2014 7:06:00 AM, Total:3, Min:, Max:, 
Time:8/11/2014 7:07:00 AM, Total:3, Min:, Max:, Time:8/11/2014 7:08:00 AM, Total:12, Min:, Max:...} 
$metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName 
----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:05:00 AM 4 1 RD00155DC24599 
8/11/2014 7:06:00 AM 3 1 RD00155DC24599 
8/11/2014 7:07:00 AM 3 1 RD00155DC24589 
8/11/2014 7:08:00 AM 12 1 RD00155DC24599
8/11/2014 7:09:00 AM 37 1 RD00155DC24599 
8/11/2014 7:10:00 AM 9 1 RD00155DC24599
```

<span data-ttu-id="8920e-111">Dieser Befehl ruft Metriken für die letzten drei Stunden auf einer Ebene pro Instanz für eine Website ab.</span><span class="sxs-lookup"><span data-stu-id="8920e-111">This command gets metrics for the last three hours on a per-instance level for a website.</span></span>

## <span data-ttu-id="8920e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8920e-112">PARAMETERS</span></span>

### <span data-ttu-id="8920e-113">-Enddate</span><span class="sxs-lookup"><span data-stu-id="8920e-113">-EndDate</span></span>
<span data-ttu-id="8920e-114">Gibt die Uhrzeit als **DateTime** -Objekt an, um das Abrufen von Metriken zu beenden.</span><span class="sxs-lookup"><span data-stu-id="8920e-114">Specifies the time, as a **DateTime** object, to stop getting metrics.</span></span>
<span data-ttu-id="8920e-115">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8920e-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="8920e-116">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="8920e-116">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8920e-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="8920e-117">-InstanceDetails</span></span>
<span data-ttu-id="8920e-118">Gibt an, dass dieses Cmdlet Details auf einer Ebene pro Instanz enthält.</span><span class="sxs-lookup"><span data-stu-id="8920e-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="8920e-119">Wenn der Webhosting-Plan auf zwei oder mehr Computern ausgeführt wird, gibt dieses Cmdlet Metriken für jeden Computer zurück.</span><span class="sxs-lookup"><span data-stu-id="8920e-119">If the web hosting plan runs on two or more computers, this cmdlet returns metrics for each computer.</span></span>

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

### <span data-ttu-id="8920e-120">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="8920e-120">-MetricNames</span></span>
<span data-ttu-id="8920e-121">Gibt ein Array von Metriken an, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8920e-121">Specifies an array of metrics to get.</span></span>
<span data-ttu-id="8920e-122">Wenn Sie diesen Parameter nicht angeben, ruft das Cmdlet alle Metriken ab.</span><span class="sxs-lookup"><span data-stu-id="8920e-122">If you do not specify this parameter, the cmdlet gets all metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8920e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8920e-123">-Name</span></span>
<span data-ttu-id="8920e-124">Gibt den Namen einer Website im Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="8920e-124">Specifies the name of a website in the subscription.</span></span>
<span data-ttu-id="8920e-125">Dieser Parameter unterstützt keine Platzhalterzeichen.</span><span class="sxs-lookup"><span data-stu-id="8920e-125">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="8920e-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="8920e-126">-Profile</span></span>
<span data-ttu-id="8920e-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8920e-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8920e-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8920e-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8920e-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="8920e-129">-Slot</span></span>
<span data-ttu-id="8920e-130">Gibt die Umgebung einer Cloud-Dienstbereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="8920e-130">Specifies the environment of a cloud service deployment.</span></span>
<span data-ttu-id="8920e-131">Gültige Werte sind: Production und Staging.</span><span class="sxs-lookup"><span data-stu-id="8920e-131">Valid values are: Production and Staging.</span></span>

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

### <span data-ttu-id="8920e-132">-SlotView</span><span class="sxs-lookup"><span data-stu-id="8920e-132">-SlotView</span></span>
<span data-ttu-id="8920e-133">Gibt an, dass dieses Cmdlet Metriken für die Hostnamen erhält, die Datenverkehr am aktuellen Steckplatz empfangen.</span><span class="sxs-lookup"><span data-stu-id="8920e-133">Indicates that this cmdlet gets metrics for the host names that receive traffic at the current slot.</span></span>
<span data-ttu-id="8920e-134">Wenn während des Zeitraums ein Swap erfolgt, werden die Metriken zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="8920e-134">If a swap occurs during the time period, the metrics are merged.</span></span>

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

### <span data-ttu-id="8920e-135">-StartDate</span><span class="sxs-lookup"><span data-stu-id="8920e-135">-StartDate</span></span>
<span data-ttu-id="8920e-136">Gibt die Zeit als **DateTime** -Objekt an, um zu beginnen, Metriken zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8920e-136">Specifies the time, as a **DateTime** object, to start getting metrics.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8920e-137">-Zeitkorn</span><span class="sxs-lookup"><span data-stu-id="8920e-137">-TimeGrain</span></span>
<span data-ttu-id="8920e-138">Gibt die Zeiteinheit für Metriken an.</span><span class="sxs-lookup"><span data-stu-id="8920e-138">Specifies the time unit for metrics.</span></span>
<span data-ttu-id="8920e-139">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="8920e-139">Valid values are:</span></span> 

- <span data-ttu-id="8920e-140">PT1M (Minuten)</span><span class="sxs-lookup"><span data-stu-id="8920e-140">PT1M (Minute)</span></span> 
- <span data-ttu-id="8920e-141">PT1H (Stunde)</span><span class="sxs-lookup"><span data-stu-id="8920e-141">PT1H (Hour)</span></span> 
- <span data-ttu-id="8920e-142">P1D (Tag)</span><span class="sxs-lookup"><span data-stu-id="8920e-142">P1D (Day)</span></span>

<span data-ttu-id="8920e-143">Der Standardwert ist PT1H.</span><span class="sxs-lookup"><span data-stu-id="8920e-143">The default value is PT1H.</span></span>

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

### <span data-ttu-id="8920e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8920e-144">CommonParameters</span></span>
<span data-ttu-id="8920e-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8920e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8920e-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8920e-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8920e-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8920e-147">INPUTS</span></span>

###  
<span data-ttu-id="8920e-148">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="8920e-148">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="8920e-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8920e-149">OUTPUTS</span></span>

### <span data-ttu-id="8920e-150">Microsoft. WindowsAzure. Commands. Utilities. Websites. Services. webentities. MetricResponse</span><span class="sxs-lookup"><span data-stu-id="8920e-150">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>
<span data-ttu-id="8920e-151">Standardmäßig gibt **Get-AzureWebsiteMetric** ein Array von **MetricResponse** -Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="8920e-151">By default, **Get-AzureWebsiteMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="8920e-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="8920e-152">NOTES</span></span>

## <span data-ttu-id="8920e-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8920e-153">RELATED LINKS</span></span>

[<span data-ttu-id="8920e-154">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8920e-154">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


