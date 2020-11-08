---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F619B52A-6BFD-43E4-B313-F4C8D95EA966
online version: ''
schema: 2.0.0
ms.openlocfilehash: 570fdc21d650666e1cededbea597a5ef34023596
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006058"
---
# <span data-ttu-id="69d16-101">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="69d16-101">Set-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="69d16-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69d16-102">SYNOPSIS</span></span>
<span data-ttu-id="69d16-103">Aktualisiert eine vorhandene Sicherungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="69d16-103">Updates an existing backup policy.</span></span>

## <span data-ttu-id="69d16-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69d16-104">SYNTAX</span></span>

```
Set-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> -BackupPolicyName <String>
 [-BackupSchedulesToAdd <PSObject[]>] [-BackupSchedulesToUpdate <PSObject[]>]
 [-BackupScheduleIdsToDelete <PSObject[]>] [-VolumeIdsToUpdate <PSObject[]>] [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="69d16-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69d16-105">DESCRIPTION</span></span>
<span data-ttu-id="69d16-106">Das Cmdlet " **Satz-AzureStorSimpleDeviceBackupPolicy** " aktualisiert eine vorhandene Sicherungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="69d16-106">The **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet updates an existing backup policy.</span></span>
<span data-ttu-id="69d16-107">Sie können die Richtlinie umbenennen, Zeitpläne hinzufügen, aktualisieren oder löschen und die mit der Richtlinie verknüpften Volumes aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="69d16-107">You can rename the policy, add, update or delete schedules, and update the volumes associated with the policy.</span></span>

## <span data-ttu-id="69d16-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69d16-108">EXAMPLES</span></span>

### <span data-ttu-id="69d16-109">Beispiel 1: Ändern des Namens einer Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="69d16-109">Example 1: Change the name of a backup policy</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "e6d9f1b3-a250-4d57-966a-039c8eaef9e9" -BackupPolicyName "UpdatedGeneralPolicy07" -WaitForComplete
VERBOSE: ClientRequestId: f4465b46-26cc-40ff-88da-7a28df88c35c_PS
VERBOSE: ClientRequestId: 5e33a35c-e089-47c1-b760-474635b1ead8_PS
VERBOSE: About to run a task to update your backuppolicy! 
VERBOSE: ClientRequestId: e379ebdb-667f-45a9-aafa-a6cd61e5f6f6_PS


JobId        : 9d621bfd-3faa-4d1c-b28b-45c5f4a96975
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: 4fe965ea-4e12-4869-9d67-e42a24b6c5d8_PS
BackupSchedules          : {58e9cd7c-4c6a-4e33-9109-5ec0b8fcb2cc, b10e1bf4-ef0a-4ad3-8fde-eecfc9971dd2}
Volumes                  : {testvolume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 12/16/2014 2:13:28 PM
NextBackup               : 12/16/2014 3:13:43 PM
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : e6d9f1b3-a250-4d57-966a-039c8eaef9e9
Name                     : UpdatedGeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="69d16-110">Mit diesem Befehl wird der Name der Sicherungsrichtlinie mit der angegebenen ID in UpdatedGeneralPolicy07 geändert.</span><span class="sxs-lookup"><span data-stu-id="69d16-110">This command changes the name of the backup policy that has the specified ID to UpdatedGeneralPolicy07.</span></span>
<span data-ttu-id="69d16-111">Dieser Befehl gibt den *WaitForComplete* -Parameter an, sodass der Befehl die Aufgabe ausführt und dann ein **TaskStatusInfo** -Objekt für die Aufgabe zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="69d16-111">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the task.</span></span>

### <span data-ttu-id="69d16-112">Beispiel 2: Aktualisieren des Zeitplans für eine Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="69d16-112">Example 2: Update the schedule for a backup policy</span></span>
```
PS C:\>$UpdateConfig = New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "3a6c6247-6b4d-42e2-aa87-16f4f21476ea" -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 3 -RetentionCount 2 -Enabled $True
PS C:\> $UpdateArray = @()
PS C:\> $UpdateArray += $UpdateConfig
PS C:\> Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "712605f6-eb03-4db8-8f79-e0ce64b2cce1" -BackupSchedulesToUpdate $UpdateArray
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 7b265417-a5f1-45ad-8fbc-33bad4f63ec9
JobSteps   : {Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep...} 
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : d2e10d44e699b371a84db44d19daf1c3
```

<span data-ttu-id="69d16-113">Der erste Befehl erstellt ein Update-Konfigurationsobjekt mit dem Cmdlet **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** und speichert es dann in der $UpdateConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="69d16-113">The first command creates an update configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet, and then stores it in the $UpdateConfig variable.</span></span>

<span data-ttu-id="69d16-114">Der zweite Befehl erstellt eine neue Arrayvariable mit dem Namen $UpdateArray.</span><span class="sxs-lookup"><span data-stu-id="69d16-114">The second command creates a new array variable, named $UpdateArray.</span></span>
<span data-ttu-id="69d16-115">Mit dem nächsten Befehl wird das in $UpdateConfig gespeicherte Update diesem Array hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="69d16-115">The next command adds the update stored in $UpdateConfig to that array.</span></span>
<span data-ttu-id="69d16-116">Sie können dem Array mehr als ein Update hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="69d16-116">You can add more than one update to the array.</span></span>

<span data-ttu-id="69d16-117">Der endgültige Befehl aktualisiert die Sicherungsrichtlinie mit der angegebenen ID auf dem Gerät mit dem Namen Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="69d16-117">The final command updates the backup policy that has the specified ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="69d16-118">Die Richtlinie hat nun den aktualisierten Zeitplan in $UpdateArray gespeichert.</span><span class="sxs-lookup"><span data-stu-id="69d16-118">The policy now has the updated schedule stored in $UpdateArray.</span></span>

## <span data-ttu-id="69d16-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="69d16-119">PARAMETERS</span></span>

### <span data-ttu-id="69d16-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="69d16-120">-BackupPolicyId</span></span>
<span data-ttu-id="69d16-121">Gibt die Instanz-ID des zu Aktualisier **BackupPolicy** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="69d16-121">Specifies the instance ID of the **BackupPolicy** object to update.</span></span>

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

### <span data-ttu-id="69d16-122">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="69d16-122">-BackupPolicyName</span></span>
<span data-ttu-id="69d16-123">Gibt einen neuen Namen für die Sicherungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="69d16-123">Specifies a new name for the backup policy.</span></span>

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

### <span data-ttu-id="69d16-124">-BackupScheduleIdsToDelete</span><span class="sxs-lookup"><span data-stu-id="69d16-124">-BackupScheduleIdsToDelete</span></span>
<span data-ttu-id="69d16-125">Gibt ein Array von Instanz-IDs von **BackupSchedule** -Objekten an, die gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="69d16-125">Specifies an array of instance IDs of **BackupSchedule** objects to delete.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69d16-126">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="69d16-126">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="69d16-127">Gibt ein Array von **BackupScheduleBase** -Objekten an, die der Richtlinie hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="69d16-127">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="69d16-128">Verwenden Sie zum Abrufen eines **BackupScheduleBase** -Objekts das Cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .</span><span class="sxs-lookup"><span data-stu-id="69d16-128">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69d16-129">-BackupSchedulesToUpdate</span><span class="sxs-lookup"><span data-stu-id="69d16-129">-BackupSchedulesToUpdate</span></span>
<span data-ttu-id="69d16-130">Gibt ein Array von **BackupScheduleUpdateRequest** -Objekten an, die aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="69d16-130">Specifies an array of **BackupScheduleUpdateRequest** objects to update.</span></span>
<span data-ttu-id="69d16-131">Verwenden Sie zum Abrufen eines **BackupScheduleUpdateRequest** -Objekts das Cmdlet **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** .</span><span class="sxs-lookup"><span data-stu-id="69d16-131">To obtain a **BackupScheduleUpdateRequest** object, use the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69d16-132">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="69d16-132">-DeviceName</span></span>
<span data-ttu-id="69d16-133">Gibt den Namen des StorSimple-Geräts an, für das die Sicherungsrichtlinie aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="69d16-133">Specifies the name of the StorSimple device for which to update the backup policy.</span></span>

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

### <span data-ttu-id="69d16-134">-Name</span><span class="sxs-lookup"><span data-stu-id="69d16-134">-NewName</span></span>
<span data-ttu-id="69d16-135">Gibt einen Namen für das Gerät an.</span><span class="sxs-lookup"><span data-stu-id="69d16-135">Specifies a name for the device.</span></span>

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

### <span data-ttu-id="69d16-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="69d16-136">-Profile</span></span>
<span data-ttu-id="69d16-137">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="69d16-137">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="69d16-138">-VolumeIdsToUpdate</span><span class="sxs-lookup"><span data-stu-id="69d16-138">-VolumeIdsToUpdate</span></span>
<span data-ttu-id="69d16-139">Gibt ein Array von IDs von Volumes an, für die Sicherungsrichtlinien aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="69d16-139">Specifies an array of IDs of volumes for which to update backup policies.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69d16-140">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="69d16-140">-WaitForComplete</span></span>
<span data-ttu-id="69d16-141">Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="69d16-141">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="69d16-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69d16-142">CommonParameters</span></span>
<span data-ttu-id="69d16-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69d16-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69d16-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69d16-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69d16-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69d16-145">INPUTS</span></span>

### <span data-ttu-id="69d16-146">Keine</span><span class="sxs-lookup"><span data-stu-id="69d16-146">None</span></span>

## <span data-ttu-id="69d16-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69d16-147">OUTPUTS</span></span>

### <span data-ttu-id="69d16-148">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="69d16-148">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="69d16-149">Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="69d16-149">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="69d16-150">Wenn Sie diesen Parameter nicht angeben, wird ein **TaskResponse** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="69d16-150">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="69d16-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="69d16-151">NOTES</span></span>

## <span data-ttu-id="69d16-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69d16-152">RELATED LINKS</span></span>

[<span data-ttu-id="69d16-153">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="69d16-153">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="69d16-154">Neu – AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="69d16-154">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="69d16-155">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="69d16-155">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="69d16-156">Neu – AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="69d16-156">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)


