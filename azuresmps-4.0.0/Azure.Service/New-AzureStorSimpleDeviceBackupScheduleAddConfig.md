---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EE7EC812-640B-4672-B23C-673F912F0EDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 945d06ddc1be6d2b0864b0421a5a087e14d98218
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005734"
---
# <span data-ttu-id="b1fc0-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="b1fc0-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>

## <span data-ttu-id="b1fc0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="b1fc0-103">Erstellt ein Konfigurationsobjekt für den Sicherungszeitplan.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-103">Creates a backup schedule configuration object.</span></span>

## <span data-ttu-id="b1fc0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1fc0-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] -Enabled <Boolean>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b1fc0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1fc0-105">DESCRIPTION</span></span>
<span data-ttu-id="b1fc0-106">Mit dem Cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** wird ein **BackupScheduleBase** -Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-106">The **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet creates a **BackupScheduleBase** configuration object.</span></span>
<span data-ttu-id="b1fc0-107">Verwenden Sie dieses Konfigurationsobjekt, um neue Sicherungsrichtlinien mithilfe des Cmdlets **New-AzureStorSimpleDeviceBackupPolicy** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-107">Use this configuration object to create new backup policy by using the **New-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="b1fc0-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1fc0-108">EXAMPLES</span></span>

### <span data-ttu-id="b1fc0-109">Beispiel 1: Erstellen eines Backup-Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="b1fc0-109">Example 1: Create a backup configuration object</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 1 -RetentionCount 100 -Enabled $True
VERBOSE: ClientRequestId: 426a79ee-fed3-4d3d-9123-e371f83222b3_PS


BackupType     : CloudSnapshot
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 100
StartTime      : 2014-12-16T00:37:19+05:30
Status         : Enabled
```

<span data-ttu-id="b1fc0-110">Mit diesem Befehl wird ein Sicherungszeitplan-Basisobjekt für Cloud-Snapshot-Backups erstellt.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-110">This command creates a backup schedule base object for cloud snapshot backups.</span></span>
<span data-ttu-id="b1fc0-111">Die Sicherung erfolgt täglich, und die Sicherungen werden für 100 Tage aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-111">The backup occurs every day, and the backups are kept for 100 days.</span></span>
<span data-ttu-id="b1fc0-112">Dieser Zeitplan ist ab der Standardzeit, also der aktuellen Uhrzeit, aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-112">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="b1fc0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1fc0-113">PARAMETERS</span></span>

### <span data-ttu-id="b1fc0-114">-Backuptype</span><span class="sxs-lookup"><span data-stu-id="b1fc0-114">-BackupType</span></span>
<span data-ttu-id="b1fc0-115">Gibt den Sicherungstyp an.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-115">Specifies the backup type.</span></span>
<span data-ttu-id="b1fc0-116">Gültige Werte sind: LocalSnapshot und CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-116">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fc0-117">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="b1fc0-117">-Enabled</span></span>
<span data-ttu-id="b1fc0-118">Gibt an, ob der Sicherungszeitplan aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-118">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fc0-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="b1fc0-119">-Profile</span></span>
<span data-ttu-id="b1fc0-120">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="b1fc0-121">-Serietype</span><span class="sxs-lookup"><span data-stu-id="b1fc0-121">-RecurrenceType</span></span>
<span data-ttu-id="b1fc0-122">Gibt den Typ der Serie für diesen Sicherungszeitplan an.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-122">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="b1fc0-123">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b1fc0-123">Valid values are:</span></span> 

- <span data-ttu-id="b1fc0-124">Minuten</span><span class="sxs-lookup"><span data-stu-id="b1fc0-124">Minutes</span></span>
- <span data-ttu-id="b1fc0-125">Grenzen</span><span class="sxs-lookup"><span data-stu-id="b1fc0-125">Hourly</span></span>
- <span data-ttu-id="b1fc0-126">Täglich</span><span class="sxs-lookup"><span data-stu-id="b1fc0-126">Daily</span></span>
- <span data-ttu-id="b1fc0-127">Wochen</span><span class="sxs-lookup"><span data-stu-id="b1fc0-127">Weekly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fc0-128">-Seriewert</span><span class="sxs-lookup"><span data-stu-id="b1fc0-128">-RecurrenceValue</span></span>
<span data-ttu-id="b1fc0-129">Gibt an, wie oft eine Sicherung erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-129">Specifies how often to make a backup.</span></span>
<span data-ttu-id="b1fc0-130">Dieser Parameter verwendet die vom *Serientyp* -Parameter angegebene Einheit.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-130">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fc0-131">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="b1fc0-131">-RetentionCount</span></span>
<span data-ttu-id="b1fc0-132">Gibt die Anzahl der Tage an, für die eine Sicherung aufbewahrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-132">Specifies the number of days to keep a backup.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fc0-133">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="b1fc0-133">-StartFromDateTime</span></span>
<span data-ttu-id="b1fc0-134">Gibt das Datum an, ab dem Sicherungskopien erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-134">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="b1fc0-135">Der Standardwert ist die aktuelle Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-135">The default value is the current time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fc0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1fc0-136">CommonParameters</span></span>
<span data-ttu-id="b1fc0-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1fc0-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1fc0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1fc0-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1fc0-139">INPUTS</span></span>

### <span data-ttu-id="b1fc0-140">Keine</span><span class="sxs-lookup"><span data-stu-id="b1fc0-140">None</span></span>

## <span data-ttu-id="b1fc0-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1fc0-141">OUTPUTS</span></span>

### <span data-ttu-id="b1fc0-142">BackupScheduleBase</span><span class="sxs-lookup"><span data-stu-id="b1fc0-142">BackupScheduleBase</span></span>
<span data-ttu-id="b1fc0-143">Dieses Cmdlet gibt ein **BackupScheduleBase** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-143">This cmdlet returns a **BackupScheduleBase** object.</span></span>
<span data-ttu-id="b1fc0-144">Verwenden Sie eine **BackupScheduleBase** , um neue Sicherungsrichtlinien zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b1fc0-144">Use a **BackupScheduleBase** to construct new backup policy.</span></span>

## <span data-ttu-id="b1fc0-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1fc0-145">NOTES</span></span>

## <span data-ttu-id="b1fc0-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1fc0-146">RELATED LINKS</span></span>

[<span data-ttu-id="b1fc0-147">Neu – AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="b1fc0-147">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)

[<span data-ttu-id="b1fc0-148">Neu – AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b1fc0-148">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)


