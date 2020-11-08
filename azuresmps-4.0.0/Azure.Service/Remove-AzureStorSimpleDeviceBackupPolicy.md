---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5AB916CB-A141-4662-8220-6C1FBB58FC69
online version: ''
schema: 2.0.0
ms.openlocfilehash: aab5e0f3ef432333eeb4aff68673c0d5c2219521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006670"
---
# <span data-ttu-id="24c9e-101">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="24c9e-101">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="24c9e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24c9e-102">SYNOPSIS</span></span>
<span data-ttu-id="24c9e-103">Entfernt eine vorhandene Sicherungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="24c9e-103">Removes an existing backup policy.</span></span>

## <span data-ttu-id="24c9e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24c9e-104">SYNTAX</span></span>

### <span data-ttu-id="24c9e-105">IdentifyById (Standard)</span><span class="sxs-lookup"><span data-stu-id="24c9e-105">IdentifyById (Default)</span></span>
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="24c9e-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="24c9e-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="24c9e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24c9e-107">DESCRIPTION</span></span>
<span data-ttu-id="24c9e-108">Das Cmdlet **Remove-AzureStorSimpleDeviceBackupPolicy** entfernt ein vorhandenes **BackupPolicy** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="24c9e-108">The **Remove-AzureStorSimpleDeviceBackupPolicy** cmdlet removes an existing **BackupPolicy** object.</span></span>
<span data-ttu-id="24c9e-109">Nachdem Sie eine Sicherungsrichtlinie entfernt haben, erfolgen keine weiteren Sicherungen auf Grundlage dieser Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="24c9e-109">After you remove a backup policy, no further backups take place based on that policy.</span></span>
<span data-ttu-id="24c9e-110">Mit diesem Cmdlet werden auch alle Zeitpläne gelöscht, die der gelöschten Richtlinie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="24c9e-110">This cmdlet also deletes all schedules associated with the deleted policy.</span></span>

## <span data-ttu-id="24c9e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24c9e-111">EXAMPLES</span></span>

### <span data-ttu-id="24c9e-112">Beispiel 1: Entfernen einer Sicherungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="24c9e-112">Example 1: Remove a backup policy</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "03710b4c-82c1-40ca-be5c-40289dc49642" -Force
VERBOSE: ClientRequestId: b3e4d485-eae4-4cf4-a43b-815f3abcd2dd_PS
VERBOSE: ClientRequestId: a260ee98-46aa-49e0-91ac-31d4155f4cae_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: 92a9c264-90df-4345-a495-92767dd266f2_PS
695be190-ac81-4cf2-b1c5-03ef6b08d005
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
695be190-ac81-4cf2-b1c5-03ef6b08d005 for tracking the task's status
```

<span data-ttu-id="24c9e-113">Mit diesem Befehl wird der **BackupPolicy** mit der Instanz-ID 03710b4c-82c1-40ca-be5c-40289dc49642 entfernt, sodass keine weiteren Sicherungen auf Grundlage dieser Richtlinie durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="24c9e-113">This command removes the **BackupPolicy** that has the instance ID 03710b4c-82c1-40ca-be5c-40289dc49642, so that no more backups are made based on this policy.</span></span>
<span data-ttu-id="24c9e-114">Der Befehl löscht auch alle Zeitpläne, die dieser Richtlinie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="24c9e-114">The command also deletes all schedules associated with this policy.</span></span>
<span data-ttu-id="24c9e-115">Der Befehl startet den Vorgang, der das **BackupPolicy** -Objekt entfernt, und gibt dann ein **TaskResponse** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="24c9e-115">The command starts the operation that removes the **BackupPolicy** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="24c9e-116">Verwenden Sie das Cmdlet **Get-AzureStorSimpleTask** , um den Status der Aufgabe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="24c9e-116">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="24c9e-117">Beispiel 2: Entfernen der ersten Sicherungsrichtlinien für ein Gerät</span><span class="sxs-lookup"><span data-stu-id="24c9e-117">Example 2: Remove the first of the backup policies for a device</span></span>
```
PS C:\>$Policies = Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId $Policies[0].InstanceId -Force -WaitForComplete
VERBOSE: ClientRequestId: db3b49fa-cffa-446d-ba52-daa6802e00f7_PS
VERBOSE: ClientRequestId: 70e2b56f-c2df-40d0-a1e5-d7a4d7e25962_PS
VERBOSE: About to run a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: f8eb3d4d-2c57-4fc9-9f40-79d0f2ea1b6a_PS


JobId        : 820a246e-54b6-41a9-bdd5-15d5daea9b0a
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your remove operation has completed successfully.
```

<span data-ttu-id="24c9e-118">Der erste Befehl ruft die Sicherungsrichtlinien für das Gerät mit dem Namen Contoso63-AppVm ab und speichert Sie dann in der $Policies Variablen.</span><span class="sxs-lookup"><span data-stu-id="24c9e-118">The first command gets the backup policies for the device named Contoso63-AppVm, and then stores them in the $Policies variable.</span></span>

<span data-ttu-id="24c9e-119">Der zweite Befehl entfernt die erste Sicherungsrichtlinie aus Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="24c9e-119">The second command removes the first backup policy from Contoso63-AppVm.</span></span>
<span data-ttu-id="24c9e-120">Der Befehl verwendet die standardmäßige Punktsyntax, um die **InstanceId** -Eigenschaft des ersten Elements in $Policies zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="24c9e-120">The command uses standard dot syntax to identify the **InstanceId** property of the first item in $Policies.</span></span>
<span data-ttu-id="24c9e-121">Dieser Befehl gibt den *WaitForComplete* -Parameter an, sodass der Befehl die Aufgabe ausführt und dann ein **TaskStatusInfo** -Objekt für die Aufgabe zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="24c9e-121">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the task.</span></span>

### <span data-ttu-id="24c9e-122">Beispiel 3: Entfernen einer Sicherungsrichtlinie mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="24c9e-122">Example 3: Remove a backup policy by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQAVolume01_Default" | Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -Force -WaitForComplete
VERBOSE: ClientRequestId: 60080fb1-2f88-4c17-bfd7-21aa73440a9c_PS
VERBOSE: ClientRequestId: 04c91121-50d7-4796-9af6-fc6a7d6b6a0e_PS
VERBOSE: ClientRequestId: 47ceb37c-672f-42e8-bd19-1190925c46cd_PS
VERBOSE: ClientRequestId: cbc39757-f2cc-4cc5-93ea-4ec0fbfb0ca8_PS
VERBOSE: ClientRequestId: 3614d47a-51fc-4500-a5f1-5401301ca4e3_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: dbd7166e-1888-4b11-9af9-8d49712a8c8b_PS
702ad240-5730-4015-b051-56055bd2c2d3
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
702ad240-5730-4015-b051-56055bd2c2d3 for tracking the task's status
VERBOSE: BackupPolicy with id bfe0bf8a-2d09-4690-93da-38a4f24e9f4f found!
```

<span data-ttu-id="24c9e-123">Dieser Befehl ruft mithilfe von **Get-AzureStorSimpleDeviceBackupPolicy** ein **BackupPolicyDetails** -Objekt ab und übergibt es dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24c9e-123">This command gets a **BackupPolicyDetails** object by using **Get-AzureStorSimpleDeviceBackupPolicy** , and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="24c9e-124">Das aktuelle Cmdlet entfernt die Sicherungsrichtlinie mit dem Namen TSQAVolume01_Default.</span><span class="sxs-lookup"><span data-stu-id="24c9e-124">The current cmdlet removes the backup policy named TSQAVolume01_Default.</span></span>

## <span data-ttu-id="24c9e-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="24c9e-125">PARAMETERS</span></span>

### <span data-ttu-id="24c9e-126">-BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="24c9e-126">-BackupPolicy</span></span>
<span data-ttu-id="24c9e-127">Gibt das **BackupPolicyDetails** -Objekt an, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="24c9e-127">Specifies the **BackupPolicyDetails** object to delete.</span></span>
<span data-ttu-id="24c9e-128">Verwenden Sie das Cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** , um ein **BackupPolicyDetails** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="24c9e-128">To obtain a **BackupPolicyDetails** object, use the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24c9e-129">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="24c9e-129">-BackupPolicyId</span></span>
<span data-ttu-id="24c9e-130">Gibt die Instanz-ID des zu löschenden **BackupPolicy** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="24c9e-130">Specifies the instance ID of the **BackupPolicy** object to delete.</span></span>

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

### <span data-ttu-id="24c9e-131">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="24c9e-131">-DeviceName</span></span>
<span data-ttu-id="24c9e-132">Gibt den Namen des StorSimple-Geräts an, auf dem die Sicherungsrichtlinie gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="24c9e-132">Specifies the name of the StorSimple device on which to delete the backup policy.</span></span>

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

### <span data-ttu-id="24c9e-133">-Force</span><span class="sxs-lookup"><span data-stu-id="24c9e-133">-Force</span></span>
<span data-ttu-id="24c9e-134">Gibt an, dass Sie von diesem Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="24c9e-134">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="24c9e-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="24c9e-135">-Profile</span></span>
<span data-ttu-id="24c9e-136">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="24c9e-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="24c9e-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="24c9e-137">-WaitForComplete</span></span>
<span data-ttu-id="24c9e-138">Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="24c9e-138">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="24c9e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c9e-139">CommonParameters</span></span>
<span data-ttu-id="24c9e-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24c9e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c9e-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c9e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c9e-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24c9e-142">INPUTS</span></span>

### <span data-ttu-id="24c9e-143">BackupPolicyDetails</span><span class="sxs-lookup"><span data-stu-id="24c9e-143">BackupPolicyDetails</span></span>
<span data-ttu-id="24c9e-144">Dieses Cmdlet akzeptiert ein zu löschendes **BackupPolicyDetails** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="24c9e-144">This cmdlet accepts a **BackupPolicyDetails** object to delete.</span></span>

## <span data-ttu-id="24c9e-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24c9e-145">OUTPUTS</span></span>

### <span data-ttu-id="24c9e-146">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="24c9e-146">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="24c9e-147">Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="24c9e-147">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="24c9e-148">Wenn Sie diesen Parameter nicht angeben, wird ein **TaskResponse** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="24c9e-148">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="24c9e-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="24c9e-149">NOTES</span></span>

## <span data-ttu-id="24c9e-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24c9e-150">RELATED LINKS</span></span>

[<span data-ttu-id="24c9e-151">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="24c9e-151">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="24c9e-152">Neu – AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="24c9e-152">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="24c9e-153">Satz-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="24c9e-153">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="24c9e-154">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="24c9e-154">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


