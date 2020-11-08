---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D28DD808-E8EF-4C71-A353-8BF1E458DF6F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9fcae4a0232331a020a716b3f7284b8f6dfc3212
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006425"
---
# <span data-ttu-id="526e5-101">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="526e5-101">New-AzureAutomationSchedule</span></span>

## <span data-ttu-id="526e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="526e5-102">SYNOPSIS</span></span>

<span data-ttu-id="526e5-103">Erstellt einen Automatisierungs Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="526e5-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="526e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="526e5-104">SYNTAX</span></span>

### <span data-ttu-id="526e5-105">ByDaily (Standard)</span><span class="sxs-lookup"><span data-stu-id="526e5-105">ByDaily (Default)</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="526e5-106">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="526e5-106">ByOneTime</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>] [-OneTime]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="526e5-107">ByHourly</span><span class="sxs-lookup"><span data-stu-id="526e5-107">ByHourly</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="526e5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="526e5-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="526e5-109">Das Cmdlet **New-AzureAutomationSchedule** erstellt einen Zeitplan in der Microsoft Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="526e5-109">The **New-AzureAutomationSchedule** cmdlet creates a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="526e5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="526e5-110">EXAMPLES</span></span>

### <span data-ttu-id="526e5-111">Beispiel 1: Erstellen eines einmaligen Zeitplans</span><span class="sxs-lookup"><span data-stu-id="526e5-111">Example 1: Create a one-time schedule</span></span>
```
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime
```

<span data-ttu-id="526e5-112">Mit dem folgenden Befehl wird ein Zeitplan erstellt, der zum aktuellen Datum um 11:00 Uhr einmal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="526e5-112">The following command creates a schedule that runs one time on the current date at 11:00 PM.</span></span>

### <span data-ttu-id="526e5-113">Beispiel 2: Erstellen eines wiederkehrenden Zeitplans</span><span class="sxs-lookup"><span data-stu-id="526e5-113">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1
```

<span data-ttu-id="526e5-114">Mit den folgenden Befehlen wird ein neuer Zeitplan erstellt, der täglich um 1:00 Uhr für ein Jahr ab dem aktuellen Tag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="526e5-114">The following commands create a new schedule that runs at 1:00 PM every day for one year starting on the current day.</span></span>

## <span data-ttu-id="526e5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="526e5-115">PARAMETERS</span></span>

### <span data-ttu-id="526e5-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="526e5-116">-AutomationAccountName</span></span>
<span data-ttu-id="526e5-117">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="526e5-117">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="526e5-118">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="526e5-118">-DayInterval</span></span>
<span data-ttu-id="526e5-119">Gibt ein Intervall in Tagen für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="526e5-119">Specifies an interval, in days, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByDaily
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="526e5-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="526e5-120">-Description</span></span>
<span data-ttu-id="526e5-121">Gibt eine Beschreibung an.</span><span class="sxs-lookup"><span data-stu-id="526e5-121">Specifies a description.</span></span>

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

### <span data-ttu-id="526e5-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="526e5-122">-ExpiryTime</span></span>
<span data-ttu-id="526e5-123">Gibt die Ablaufzeit eines Zeitplans an.</span><span class="sxs-lookup"><span data-stu-id="526e5-123">Specifies the expiry time of a schedule.</span></span>
<span data-ttu-id="526e5-124">Eine Zeichenfolge kann bereitgestellt werden, wenn Sie in einen gültigen **DateTime-Datentyp** konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="526e5-124">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByDaily, ByHourly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="526e5-125">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="526e5-125">-HourInterval</span></span>
<span data-ttu-id="526e5-126">Gibt ein Intervall in Stunden für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="526e5-126">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByHourly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="526e5-127">-Name</span><span class="sxs-lookup"><span data-stu-id="526e5-127">-Name</span></span>
<span data-ttu-id="526e5-128">Gibt einen Namen für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="526e5-128">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="526e5-129">-Einmalig</span><span class="sxs-lookup"><span data-stu-id="526e5-129">-OneTime</span></span>
<span data-ttu-id="526e5-130">Gibt an, dass dieser Vorgang einen einmaligen Zeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="526e5-130">Indicates that this operation creates a one-time schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByOneTime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="526e5-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="526e5-131">-Profile</span></span>
<span data-ttu-id="526e5-132">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="526e5-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="526e5-133">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="526e5-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="526e5-134">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="526e5-134">-StartTime</span></span>
<span data-ttu-id="526e5-135">Gibt die Startzeit eines Zeitplans an.</span><span class="sxs-lookup"><span data-stu-id="526e5-135">Specifies the start time of a schedule.</span></span>
<span data-ttu-id="526e5-136">Eine Zeichenfolge kann bereitgestellt werden, wenn Sie in einen gültigen **DateTime-Datentyp** konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="526e5-136">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="526e5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="526e5-137">CommonParameters</span></span>
<span data-ttu-id="526e5-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="526e5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="526e5-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="526e5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="526e5-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="526e5-140">INPUTS</span></span>

## <span data-ttu-id="526e5-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="526e5-141">OUTPUTS</span></span>

### <span data-ttu-id="526e5-142">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="526e5-142">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="526e5-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="526e5-143">NOTES</span></span>

## <span data-ttu-id="526e5-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="526e5-144">RELATED LINKS</span></span>

[<span data-ttu-id="526e5-145">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="526e5-145">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="526e5-146">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="526e5-146">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="526e5-147">Satz-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="526e5-147">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


