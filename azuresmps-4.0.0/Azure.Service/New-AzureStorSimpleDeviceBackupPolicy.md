---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EFAE7117-9B8B-4CB9-B4D9-3F08DCE1816E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 405b9d427c7e59dfb3628806a878d57a281a6b4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006414"
---
# <span data-ttu-id="e6b58-101">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="e6b58-101">New-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="e6b58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6b58-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b58-103">Erstellt eine Sicherungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="e6b58-103">Creates a backup policy.</span></span>

## <span data-ttu-id="e6b58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6b58-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6b58-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6b58-105">DESCRIPTION</span></span>
<span data-ttu-id="e6b58-106">Das Cmdlet **New-AzureStorSimpleDeviceBackupPolicy** erstellt eine Sicherungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="e6b58-106">The **New-AzureStorSimpleDeviceBackupPolicy** cmdlet creates a backup policy.</span></span>
<span data-ttu-id="e6b58-107">Eine Sicherungsrichtlinie enthält mindestens einen Sicherungszeitplan, der auf einem oder mehreren Volumes ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e6b58-107">A backup policy contains one or more backup schedules that can run on one or more volumes.</span></span>
<span data-ttu-id="e6b58-108">Verwenden Sie zum Erstellen eines Sicherungszeitplans das Cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .</span><span class="sxs-lookup"><span data-stu-id="e6b58-108">To create a backup schedule, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

## <span data-ttu-id="e6b58-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6b58-109">EXAMPLES</span></span>

### <span data-ttu-id="e6b58-110">Beispiel 1: Erstellen einer Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="e6b58-110">Example 1: Create a backup policy</span></span>
```
PS C:\>$Schedule01 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType LocalSnapshot -RecurrenceType Daily -RecurrenceValue 10 -RetentionCount 5 -Enabled $True
PS C:\> $Schedule02 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 5 -Enabled $True
PS C:\> $ScheduleArray = @()
PS C:\> $ScheduleArray += $Schedule01
PS C:\> $ScheduleArray += $Schedule02
PS C:\> $DeviceContainer = Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm"
PS C:\> $Volume = $(Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeContainer $DeviceContainer[0])
PS C:\> $VolumeArray = @()
PS C:\> $VolumeArray += $Volume[0].InstanceId
PS C:\> New-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralPolicy07" -BackupSchedulesToAdd $ScheduleArray -VolumeIdsToAdd $VolumeArray
VERBOSE: ClientRequestId: e9d6771e-c323-47b9-b424-cb98f8ed0273_PS
VERBOSE: ClientRequestId: db0e7c86-d0d2-4a5a-b1cb-182494cba027_PS
VERBOSE: ClientRequestId: 77708dfd-a386-4999-b7ed-5d53e288ae83_PS


JobId        : d4ce5340-d5d1-4471-9cc8-013193f021b3
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your add operation has completed successfully. 
VERBOSE: ClientRequestId: bbf7e9b9-b493-40b3-8348-f15bcfc4da8a_PS
BackupSchedules          : {36d21096-bbd1-47b7-91b5-40ad1792d992, 505fc91f-deb5-4dca-bfcb-98c20b75ebcc}
Volumes                  : {volume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 01-01-2010 05:30:00
NextBackup               : 16-12-2014 01:13:43
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : 8799c2f0-8850-4e91-aa23-ee18c67da8bd
Name                     : GeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="e6b58-111">Der erste Befehl erstellt mithilfe des Cmdlets **New-AzureStorSimpleDeviceBackupScheduleAddConfig** ein Konfigurationsobjekt für den Sicherungszeitplan und speichert dieses Objekt dann in der Variablen $Schedule 01.</span><span class="sxs-lookup"><span data-stu-id="e6b58-111">The first command creates a backup schedule configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet, and then stores that object in the $Schedule01 variable.</span></span>

<span data-ttu-id="e6b58-112">Der zweite Befehl erstellt ein weiteres Backup-Konfigurationsobjekt mithilfe von **New-AzureStorSimpleDeviceBackupScheduleAddConfig** und speichert dieses Objekt dann in der Variablen $Schedule 02.</span><span class="sxs-lookup"><span data-stu-id="e6b58-112">The second command creates another backup configuration object by using **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , and then stores that object in the $Schedule02 variable.</span></span>

<span data-ttu-id="e6b58-113">Der dritte Befehl erstellt eine leere Arrayvariable mit dem Namen $ScheduleArray.</span><span class="sxs-lookup"><span data-stu-id="e6b58-113">The third command creates an empty array variable, named $ScheduleArray.</span></span>
<span data-ttu-id="e6b58-114">Mit den nächsten beiden Befehlen werden die in den ersten beiden Befehlen erstellten Objekte $ScheduleArray hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e6b58-114">The next two commands add the objects created in the first two commands to $ScheduleArray.</span></span>

<span data-ttu-id="e6b58-115">Der sechste Befehl ruft mithilfe des Cmdlets **Get-AzureStorSimpleDeviceVolumeContainer** einen Volumen Container für das Gerät mit dem Namen Contoso63-AppVm ab und speichert dann das Containerobjekt in der $DeviceContainer Variablen.</span><span class="sxs-lookup"><span data-stu-id="e6b58-115">The sixth command gets a volume container for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet, and then stores that container object in the $DeviceContainer variable.</span></span>

<span data-ttu-id="e6b58-116">Der siebte Befehl ruft einen Datenträger für den Volumen Container ab, der im ersten Mitglied von $DeviceContainer mit dem Cmdlet **Get-AzureStorSimpleDeviceVolume** gespeichert ist, und speichert dann das Volume in der $Volume-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e6b58-116">The seventh command gets a volume for the volume container stored in the first member of $DeviceContainer by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then stores that volume in the $Volume variable.</span></span>

<span data-ttu-id="e6b58-117">Der achte Befehl erstellt eine leere Arrayvariable mit dem Namen $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="e6b58-117">The eighth command creates an empty array variable, named $VolumeArray.</span></span>
<span data-ttu-id="e6b58-118">Mit dem nächsten Befehl wird $VolumeArray eine Volumen-ID hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e6b58-118">The next command adds a volume ID to $VolumeArray.</span></span>
<span data-ttu-id="e6b58-119">Dieser Wert gibt den in $Volume gespeicherten Datenträger an, auf dem die Sicherungsrichtlinie ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6b58-119">This value identifies the volume, stored in $Volume, on which the backup policy runs.</span></span>
<span data-ttu-id="e6b58-120">Sie können $VolumeArray weitere Volumen-IDs hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e6b58-120">You can add additional volume IDs to $VolumeArray.</span></span>

<span data-ttu-id="e6b58-121">Der endgültige Befehl erstellt die Sicherungsrichtlinie mit dem Namen "GeneralPolicy07" für das Gerät mit dem Namen Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="e6b58-121">The final command creates the backup policy named GeneralPolicy07 for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="e6b58-122">Der Befehl gibt die Plan Konfigurationsobjekte an, die in $ScheduleArray gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="e6b58-122">The command specifies the schedule configuration objects stored in $ScheduleArray.</span></span>
<span data-ttu-id="e6b58-123">Der Befehl gibt die Volumes an, auf die die Richtlinie in $VolumeArray angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6b58-123">The command specifies the volume or volumes to which to apply the policy in $VolumeArray.</span></span>
<span data-ttu-id="e6b58-124">Sie können die Sicherungsrichtlinie mit dem Cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e6b58-124">You can verify the backup policy by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="e6b58-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6b58-125">PARAMETERS</span></span>

### <span data-ttu-id="e6b58-126">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="e6b58-126">-BackupPolicyName</span></span>
<span data-ttu-id="e6b58-127">Gibt den Namen der Sicherungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="e6b58-127">Specifies the name of the backup policy.</span></span>

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

### <span data-ttu-id="e6b58-128">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="e6b58-128">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="e6b58-129">Gibt ein Array von **BackupScheduleBase** -Objekten an, die der Richtlinie hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e6b58-129">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="e6b58-130">Jedes Objekt stellt einen Zeitplan dar.</span><span class="sxs-lookup"><span data-stu-id="e6b58-130">Each object represents a schedule.</span></span>
<span data-ttu-id="e6b58-131">Eine Sicherungsrichtlinie enthält einen oder mehrere Zeitpläne.</span><span class="sxs-lookup"><span data-stu-id="e6b58-131">A backup policy contains one or more schedules.</span></span>
<span data-ttu-id="e6b58-132">Verwenden Sie zum Abrufen eines **BackupScheduleBase** -Objekts das Cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .</span><span class="sxs-lookup"><span data-stu-id="e6b58-132">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b58-133">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e6b58-133">-DeviceName</span></span>
<span data-ttu-id="e6b58-134">Gibt den Namen des StorSimple-Geräts an, auf dem die Sicherungsrichtlinie erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6b58-134">Specifies the name of the StorSimple device on which to create the backup policy.</span></span>

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

### <span data-ttu-id="e6b58-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="e6b58-135">-Profile</span></span>
<span data-ttu-id="e6b58-136">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="e6b58-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="e6b58-137">-VolumeIdsToAdd</span><span class="sxs-lookup"><span data-stu-id="e6b58-137">-VolumeIdsToAdd</span></span>
<span data-ttu-id="e6b58-138">Gibt ein Array der IDs von Volumes an, die der Sicherungsrichtlinie hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e6b58-138">Specifies an array of the IDs of volumes to add to the backup policy.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b58-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="e6b58-139">-WaitForComplete</span></span>
<span data-ttu-id="e6b58-140">Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e6b58-140">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b58-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b58-141">CommonParameters</span></span>
<span data-ttu-id="e6b58-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6b58-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b58-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6b58-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b58-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6b58-144">INPUTS</span></span>

### <span data-ttu-id="e6b58-145">Keine</span><span class="sxs-lookup"><span data-stu-id="e6b58-145">None</span></span>

## <span data-ttu-id="e6b58-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6b58-146">OUTPUTS</span></span>

### <span data-ttu-id="e6b58-147">BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="e6b58-147">BackupPolicy</span></span>
<span data-ttu-id="e6b58-148">Dieses Cmdlet gibt ein **BackupPolicy** -Objekt zurück, das die neuen Zeitpläne und Volumes enthält.</span><span class="sxs-lookup"><span data-stu-id="e6b58-148">This cmdlet returns a **BackupPolicy** object that contains the new schedules and volumes.</span></span>

## <span data-ttu-id="e6b58-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6b58-149">NOTES</span></span>

## <span data-ttu-id="e6b58-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6b58-150">RELATED LINKS</span></span>

[<span data-ttu-id="e6b58-151">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="e6b58-151">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="e6b58-152">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="e6b58-152">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="e6b58-153">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="e6b58-153">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="e6b58-154">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="e6b58-154">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="e6b58-155">Satz-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="e6b58-155">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="e6b58-156">Neu – AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="e6b58-156">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)


