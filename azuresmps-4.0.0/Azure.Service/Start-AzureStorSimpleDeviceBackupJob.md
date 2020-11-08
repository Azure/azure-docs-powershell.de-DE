---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 76826524-480F-458E-A996-A9DBACB8BA9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa220334c75d3e6832698ec10fbad71896473d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006233"
---
# <span data-ttu-id="61cc6-101">Start-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="61cc6-101">Start-AzureStorSimpleDeviceBackupJob</span></span>

## <span data-ttu-id="61cc6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="61cc6-103">Startet einen neuen Auftrag, mit dem eine Sicherung aus einer vorhandenen Sicherungsrichtlinie erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="61cc6-103">Starts a new job that creates a backup from an existing backup policy.</span></span>

## <span data-ttu-id="61cc6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61cc6-104">SYNTAX</span></span>

### <span data-ttu-id="61cc6-105">Leer (Standard)</span><span class="sxs-lookup"><span data-stu-id="61cc6-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="61cc6-106">BackupTypeGiven</span><span class="sxs-lookup"><span data-stu-id="61cc6-106">BackupTypeGiven</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> -BackupType <String>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="61cc6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61cc6-107">DESCRIPTION</span></span>
<span data-ttu-id="61cc6-108">Mit dem Cmdlet **Start-AzureStorSimpleDeviceBackupJob** wird ein neuer Auftrag gestartet, der eine Sicherung aus einer vorhandenen Sicherungsrichtlinie auf einem StorSimple-Gerät erstellt.</span><span class="sxs-lookup"><span data-stu-id="61cc6-108">The **Start-AzureStorSimpleDeviceBackupJob** cmdlet starts a new job that creates a backup from an existing backup policy on a StorSimple device.</span></span>
<span data-ttu-id="61cc6-109">Standardmäßig wird mit diesem Cmdlet eine lokale Snapshot-Sicherung erstellt.</span><span class="sxs-lookup"><span data-stu-id="61cc6-109">By default, this cmdlet creates a local snapshot backup.</span></span>
<span data-ttu-id="61cc6-110">Um eine Cloud-Sicherung zu erstellen, geben Sie einen Wert von CloudSnapshot für den *backuptype* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="61cc6-110">To create a cloud backup, specify a value of CloudSnapshot for the *BackupType* parameter.</span></span>

## <span data-ttu-id="61cc6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61cc6-111">EXAMPLES</span></span>

### <span data-ttu-id="61cc6-112">Beispiel 1: Erstellen einer lokalen Snapshot-Sicherung</span><span class="sxs-lookup"><span data-stu-id="61cc6-112">Example 1: Create a local snapshot backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f"
JobId                                                                StatusCode RequestId
-----                                                                ---------- ---------
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08                                 Accepted   456cf6bafd427103b71c07145e26d35c

VERBOSE: Your backup operation has been submitted for processing. Use commandlet "Get-AzureStorSimpleJob -JobId
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08" to track status.
```

<span data-ttu-id="61cc6-113">Dieser Befehl erstellt eine lokale Snapshot-Sicherung für die angegebene Richtlinien-ID.</span><span class="sxs-lookup"><span data-stu-id="61cc6-113">This command creates a local snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="61cc6-114">Mit diesem Befehl wird der Auftrag gestartet, und dann wird ein **TaskResponse** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="61cc6-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="61cc6-115">Verwenden Sie das Cmdlet " **Get-AzureStorSimpleTask** ", um den Status des Auftrags anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="61cc6-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="61cc6-116">Beispiel 2: Erstellen einer Cloud-Snapshot-Sicherung und warten auf die Fertigstellung</span><span class="sxs-lookup"><span data-stu-id="61cc6-116">Example 2: Create a cloud snapshot backup and wait to finish</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -BackupType CloudSnapshot -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f28ecf6cf75a7f128ca18e6ae14f9003
```

<span data-ttu-id="61cc6-117">Mit diesem Befehl wird eine Cloud-Snapshot-Sicherung für die angegebene Richtlinien-ID erstellt.</span><span class="sxs-lookup"><span data-stu-id="61cc6-117">This command creates a cloud snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="61cc6-118">Dieser Befehl gibt den *WaitForComplete* -Parameter an, sodass der Befehl die Aufgabe ausführt und dann ein **TaskStatusInfo** -Objekt für den Auftrag zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="61cc6-118">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the job.</span></span>

## <span data-ttu-id="61cc6-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="61cc6-119">PARAMETERS</span></span>

### <span data-ttu-id="61cc6-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="61cc6-120">-BackupPolicyId</span></span>
<span data-ttu-id="61cc6-121">Gibt die ID der Sicherungsrichtlinie an, die zum Erstellen der Sicherung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="61cc6-121">Specifies the ID of the backup policy to use to create the backup.</span></span>

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

### <span data-ttu-id="61cc6-122">-Backuptype</span><span class="sxs-lookup"><span data-stu-id="61cc6-122">-BackupType</span></span>
<span data-ttu-id="61cc6-123">Gibt den Sicherungstyp an.</span><span class="sxs-lookup"><span data-stu-id="61cc6-123">Specifies the backup type.</span></span>
<span data-ttu-id="61cc6-124">Gültige Werte sind: LocalSnapshot und CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="61cc6-124">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: BackupTypeGiven
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61cc6-125">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="61cc6-125">-DeviceName</span></span>
<span data-ttu-id="61cc6-126">Gibt den Namen des StorSimple-Geräts an, auf dem der Backup-Auftrag gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="61cc6-126">Specifies the name of the StorSimple device on which to start the backup job.</span></span>

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

### <span data-ttu-id="61cc6-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="61cc6-127">-Profile</span></span>
<span data-ttu-id="61cc6-128">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="61cc6-128">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="61cc6-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="61cc6-129">-WaitForComplete</span></span>
<span data-ttu-id="61cc6-130">Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="61cc6-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="61cc6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61cc6-131">CommonParameters</span></span>
<span data-ttu-id="61cc6-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61cc6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61cc6-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61cc6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61cc6-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61cc6-134">INPUTS</span></span>

### <span data-ttu-id="61cc6-135">Keine</span><span class="sxs-lookup"><span data-stu-id="61cc6-135">None</span></span>

## <span data-ttu-id="61cc6-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61cc6-136">OUTPUTS</span></span>

### <span data-ttu-id="61cc6-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="61cc6-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="61cc6-138">Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="61cc6-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="61cc6-139">Wenn Sie diesen Parameter nicht angeben, wird ein **TaskResponse** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="61cc6-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="61cc6-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="61cc6-140">NOTES</span></span>

## <span data-ttu-id="61cc6-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61cc6-141">RELATED LINKS</span></span>

[<span data-ttu-id="61cc6-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="61cc6-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="61cc6-143">Anfang-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="61cc6-143">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>](./Start-AzureStorSimpleDeviceBackupRestoreJob.md)


