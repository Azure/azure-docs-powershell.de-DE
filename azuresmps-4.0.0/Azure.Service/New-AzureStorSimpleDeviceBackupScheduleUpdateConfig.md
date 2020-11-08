---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 22C6845E-D7BD-4BBC-B373-394A23488A94
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0695dc42d9c540e30ddf9ac55bd6fc136c84bff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005730"
---
# <span data-ttu-id="5460b-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="5460b-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>

## <span data-ttu-id="5460b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5460b-102">SYNOPSIS</span></span>
<span data-ttu-id="5460b-103">Erstellt ein Konfigurationsobjekt für das Aktualisierungszeitplan-Update.</span><span class="sxs-lookup"><span data-stu-id="5460b-103">Creates a backup schedule update configuration object.</span></span>

## <span data-ttu-id="5460b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5460b-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id <String> -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] [-Enabled <Boolean>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5460b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5460b-105">DESCRIPTION</span></span>
<span data-ttu-id="5460b-106">Mit dem Cmdlet **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** wird ein **BackupScheduleUpdateRequest** -Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="5460b-106">The **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet creates a **BackupScheduleUpdateRequest** configuration object.</span></span>
<span data-ttu-id="5460b-107">Verwenden Sie dieses Konfigurationsobjekt, um eine Sicherungsrichtlinie mithilfe des Cmdlets " **festlegen-AzureStorSimpleDeviceBackupPolicy** " zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5460b-107">Use this configuration object to update a backup policy by using the **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="5460b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5460b-108">EXAMPLES</span></span>

### <span data-ttu-id="5460b-109">Beispiel 1: Erstellen einer Aktualisierungsanforderung für einen Zeitplan</span><span class="sxs-lookup"><span data-stu-id="5460b-109">Example 1: Create a schedule update request</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "147f734d-a31a-4473-8501-6ba38be2cb30" -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 50 -Enabled $True
VERBOSE: ClientRequestId: ef346641-54b4-4273-8898-7f863e7c5b7e_PS


BackupType     : CloudSnapshot
Id             : 147f734d-a31a-4473-8501-6ba38be2cb30
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 50
StartTime      : 2014-12-16T00:39:32+05:30
Status         : Enabled
```

<span data-ttu-id="5460b-110">Mit diesem Befehl wird eine Aktualisierungsanforderung für den Terminplan für den Zeitplan erstellt, die die angegebene ID aufweist.</span><span class="sxs-lookup"><span data-stu-id="5460b-110">This command creates a backup schedule update request for the schedule that has the specified ID.</span></span>
<span data-ttu-id="5460b-111">Die Anforderung besteht darin, den Zeitplan zu einer Cloud-Snapshot-Sicherung zu machen, die stündlich wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="5460b-111">The request is to make the schedule a cloud snapshot backup that recurs every hour.</span></span>
<span data-ttu-id="5460b-112">Die Sicherungen werden für 50 Tage aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="5460b-112">The backups are kept for 50 days.</span></span>
<span data-ttu-id="5460b-113">Dieser Zeitplan ist ab der Standardzeit, also der aktuellen Uhrzeit, aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5460b-113">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="5460b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5460b-114">PARAMETERS</span></span>

### <span data-ttu-id="5460b-115">-Backuptype</span><span class="sxs-lookup"><span data-stu-id="5460b-115">-BackupType</span></span>
<span data-ttu-id="5460b-116">Gibt den Sicherungstyp an.</span><span class="sxs-lookup"><span data-stu-id="5460b-116">Specifies the backup type.</span></span>
<span data-ttu-id="5460b-117">Gültige Werte sind: LocalSnapshot und CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="5460b-117">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

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

### <span data-ttu-id="5460b-118">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="5460b-118">-Enabled</span></span>
<span data-ttu-id="5460b-119">Gibt an, ob der Sicherungszeitplan aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5460b-119">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5460b-120">-ID</span><span class="sxs-lookup"><span data-stu-id="5460b-120">-Id</span></span>
<span data-ttu-id="5460b-121">Gibt die Instanz-ID des zu aktualisierende Backup-Zeitplans an.</span><span class="sxs-lookup"><span data-stu-id="5460b-121">Specifies the instance ID of the backup schedule to update.</span></span>

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

### <span data-ttu-id="5460b-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="5460b-122">-Profile</span></span>
<span data-ttu-id="5460b-123">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="5460b-123">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="5460b-124">-Serietype</span><span class="sxs-lookup"><span data-stu-id="5460b-124">-RecurrenceType</span></span>
<span data-ttu-id="5460b-125">Gibt den Typ der Serie für diesen Sicherungszeitplan an.</span><span class="sxs-lookup"><span data-stu-id="5460b-125">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="5460b-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="5460b-126">Valid values are:</span></span> 

- <span data-ttu-id="5460b-127">Minuten</span><span class="sxs-lookup"><span data-stu-id="5460b-127">Minutes</span></span>
- <span data-ttu-id="5460b-128">Grenzen</span><span class="sxs-lookup"><span data-stu-id="5460b-128">Hourly</span></span>
- <span data-ttu-id="5460b-129">Täglich</span><span class="sxs-lookup"><span data-stu-id="5460b-129">Daily</span></span>
- <span data-ttu-id="5460b-130">Wochen</span><span class="sxs-lookup"><span data-stu-id="5460b-130">Weekly</span></span>

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

### <span data-ttu-id="5460b-131">-Seriewert</span><span class="sxs-lookup"><span data-stu-id="5460b-131">-RecurrenceValue</span></span>
<span data-ttu-id="5460b-132">Gibt an, wie oft eine Sicherung erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5460b-132">Specifies how often to make a backup.</span></span>
<span data-ttu-id="5460b-133">Dieser Parameter verwendet die vom *Serientyp* -Parameter angegebene Einheit.</span><span class="sxs-lookup"><span data-stu-id="5460b-133">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

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

### <span data-ttu-id="5460b-134">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="5460b-134">-RetentionCount</span></span>
<span data-ttu-id="5460b-135">Gibt die Anzahl der Tage an, für die eine Sicherung aufbewahrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5460b-135">Specifies the number of days to keep a backup.</span></span>

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

### <span data-ttu-id="5460b-136">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="5460b-136">-StartFromDateTime</span></span>
<span data-ttu-id="5460b-137">Gibt das Datum an, ab dem Sicherungskopien erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5460b-137">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="5460b-138">Der Standardwert ist die aktuelle Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="5460b-138">The default value is the current time.</span></span>

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

### <span data-ttu-id="5460b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5460b-139">CommonParameters</span></span>
<span data-ttu-id="5460b-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5460b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5460b-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5460b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5460b-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5460b-142">INPUTS</span></span>

### <span data-ttu-id="5460b-143">Keine</span><span class="sxs-lookup"><span data-stu-id="5460b-143">None</span></span>

## <span data-ttu-id="5460b-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5460b-144">OUTPUTS</span></span>

### <span data-ttu-id="5460b-145">BackupScheduleUpdateRequest</span><span class="sxs-lookup"><span data-stu-id="5460b-145">BackupScheduleUpdateRequest</span></span>
<span data-ttu-id="5460b-146">Dieses Cmdlet gibt ein **BackupScheduleUpdateRequest** -Objekt zurück, das Informationen zu aktualisierten Sicherungszeitplänen enthält.</span><span class="sxs-lookup"><span data-stu-id="5460b-146">This cmdlet returns a **BackupScheduleUpdateRequest** object that contains information about updated backup schedules.</span></span>

## <span data-ttu-id="5460b-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="5460b-147">NOTES</span></span>

## <span data-ttu-id="5460b-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5460b-148">RELATED LINKS</span></span>

[<span data-ttu-id="5460b-149">Neu – AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="5460b-149">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)

[<span data-ttu-id="5460b-150">Satz-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="5460b-150">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)


