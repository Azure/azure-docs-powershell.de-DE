---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F9C8D0AA-ED97-43E8-ADB1-5AE1A4517666
online version: ''
schema: 2.0.0
ms.openlocfilehash: c524bb90d84df6ad3e37b552b957dac2d75b6a6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005953"
---
# <span data-ttu-id="d02cd-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="d02cd-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>

## <span data-ttu-id="d02cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d02cd-102">SYNOPSIS</span></span>
<span data-ttu-id="d02cd-103">Startet einen Auftrag, der eine Sicherung auf einem StorSimple-Gerät wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="d02cd-103">Starts a job that restores a backup on a StorSimple device.</span></span>

## <span data-ttu-id="d02cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d02cd-104">SYNTAX</span></span>

### <span data-ttu-id="d02cd-105">Leer (Standard)</span><span class="sxs-lookup"><span data-stu-id="d02cd-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d02cd-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="d02cd-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> -SnapshotId <String>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d02cd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d02cd-107">DESCRIPTION</span></span>
<span data-ttu-id="d02cd-108">Mit dem Cmdlet **Start-AzureStorSimpleDeviceBackupRestoreJob** wird ein Auftrag gestartet, der eine Sicherung auf einem StorSimple-Gerät wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="d02cd-108">The **Start-AzureStorSimpleDeviceBackupRestoreJob** cmdlet starts a job that restores a backup on a StorSimple device.</span></span>
<span data-ttu-id="d02cd-109">Geben Sie eine Sicherungs-ID und eine optionale Snapshot-ID an.</span><span class="sxs-lookup"><span data-stu-id="d02cd-109">Specify a backup ID and an optional snapshot ID.</span></span>

## <span data-ttu-id="d02cd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d02cd-110">EXAMPLES</span></span>

### <span data-ttu-id="d02cd-111">Beispiel 1: Starten eines Auftrags zum Wiederherstellen einer Sicherung</span><span class="sxs-lookup"><span data-stu-id="d02cd-111">Example 1: Start a job to restore a backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -WaitForComplete
Confirm
Are you sure you want to restore the backup with backupId b3b50534-763c-4b05-9724-5ecf62bde721? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y


Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 217d0647-c001-4f43-9833-f8155a458e95
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e0aa2dcd2f197a8588c40a067fe0e519
```

<span data-ttu-id="d02cd-112">Mit diesem Befehl wird ein Auftrag gestartet, der das Sicherungsobjekt mit der angegebenen ID und den zugehörigen Snapshots auf dem Gerät mit dem Namen Contoso63-AppVm wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="d02cd-112">This command starts a job that restores the backup object that has the specified ID, and its associated snapshots, on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="d02cd-113">Der Befehl gibt den *WaitForComplete* -Parameter an, sodass der Auftrag abgeschlossen wird, bevor das Cmdlet die Steuerung an die Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d02cd-113">The command specifies the *WaitForComplete* parameter, so the job finishes before the cmdlet returns control to the console.</span></span>

### <span data-ttu-id="d02cd-114">Beispiel 2: Starten eines Auftrags zum Wiederherstellen eines bestimmten Snapshots</span><span class="sxs-lookup"><span data-stu-id="d02cd-114">Example 2: Start a job to restore a specific snapshot</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -SnapshotId "2d0cfad7-46bf-4266-8859-96549646e947_0000000000000000" -Force

The start job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 9102ed9a-078f-4648-a
721-3cffbba31336 for tracking the job status
```

<span data-ttu-id="d02cd-115">Mit diesem Befehl wird ein Auftrag gestartet, der den Sicherungssnapshot mit der angegebenen ID wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="d02cd-115">This command starts a job that restores the backup snapshot that has the specified ID.</span></span>
<span data-ttu-id="d02cd-116">Der Befehl gibt das Sicherungsobjekt anhand der ID auf dem Gerät mit dem Namen Contoso63-AppVm an.</span><span class="sxs-lookup"><span data-stu-id="d02cd-116">The command specifies the backup object by ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="d02cd-117">Der Befehl gibt den *Force* -Parameter an, sodass der Auftrag gestartet wird, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="d02cd-117">The command specifies the *Force* parameter, so it starts the job without prompting you to confirm.</span></span>

## <span data-ttu-id="d02cd-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="d02cd-118">PARAMETERS</span></span>

### <span data-ttu-id="d02cd-119">-Backup-Nr.</span><span class="sxs-lookup"><span data-stu-id="d02cd-119">-BackupId</span></span>
<span data-ttu-id="d02cd-120">Gibt die Instanz-ID der wiederherzustellenden Sicherung an.</span><span class="sxs-lookup"><span data-stu-id="d02cd-120">Specifies the instance ID of the backup to restore.</span></span>

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

### <span data-ttu-id="d02cd-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d02cd-121">-DeviceName</span></span>
<span data-ttu-id="d02cd-122">Gibt den Namen des StorSimple-Geräts an, auf dem die Sicherung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d02cd-122">Specifies the name of the StorSimple device on which the backup exists.</span></span>

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

### <span data-ttu-id="d02cd-123">-Force</span><span class="sxs-lookup"><span data-stu-id="d02cd-123">-Force</span></span>
<span data-ttu-id="d02cd-124">Gibt an, dass Sie von diesem Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="d02cd-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="d02cd-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="d02cd-125">-Profile</span></span>
<span data-ttu-id="d02cd-126">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="d02cd-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="d02cd-127">-Snapshot-Nr</span><span class="sxs-lookup"><span data-stu-id="d02cd-127">-SnapshotId</span></span>
<span data-ttu-id="d02cd-128">Gibt die Instanz-ID des wiederherzustellenden Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="d02cd-128">Specifies the instance ID of the snapshot to restore.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d02cd-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="d02cd-129">-WaitForComplete</span></span>
<span data-ttu-id="d02cd-130">Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d02cd-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="d02cd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d02cd-131">CommonParameters</span></span>
<span data-ttu-id="d02cd-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d02cd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d02cd-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d02cd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d02cd-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d02cd-134">INPUTS</span></span>

### <span data-ttu-id="d02cd-135">Keine</span><span class="sxs-lookup"><span data-stu-id="d02cd-135">None</span></span>

## <span data-ttu-id="d02cd-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d02cd-136">OUTPUTS</span></span>

### <span data-ttu-id="d02cd-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="d02cd-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="d02cd-138">Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="d02cd-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="d02cd-139">Wenn Sie diesen Parameter nicht angeben, wird ein **TaskResponse** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d02cd-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="d02cd-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="d02cd-140">NOTES</span></span>

## <span data-ttu-id="d02cd-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d02cd-141">RELATED LINKS</span></span>

[<span data-ttu-id="d02cd-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="d02cd-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="d02cd-143">Anfang-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="d02cd-143">Start-AzureStorSimpleDeviceBackupJob</span></span>](./Start-AzureStorSimpleDeviceBackupJob.md)


