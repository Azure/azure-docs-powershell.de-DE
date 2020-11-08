---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006673"
---
# <span data-ttu-id="75281-101">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="75281-101">Remove-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="75281-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75281-102">SYNOPSIS</span></span>
<span data-ttu-id="75281-103">Löscht ein Sicherungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="75281-103">Deletes a backup object.</span></span>

## <span data-ttu-id="75281-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75281-104">SYNTAX</span></span>

### <span data-ttu-id="75281-105">IdentifyById (Standard)</span><span class="sxs-lookup"><span data-stu-id="75281-105">IdentifyById (Default)</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="75281-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="75281-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="75281-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75281-107">DESCRIPTION</span></span>
<span data-ttu-id="75281-108">Das Cmdlet **Remove-AzureStorSimpleDeviceBackup** löscht ein einzelnes Sicherungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="75281-108">The **Remove-AzureStorSimpleDeviceBackup** cmdlet deletes a single backup object.</span></span>
<span data-ttu-id="75281-109">Wenn Sie versuchen, eine bereits gelöschte Sicherung zu löschen, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="75281-109">If you attempt to delete a backup that has already been deleted, this cmdlet returns an error.</span></span>

## <span data-ttu-id="75281-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75281-110">EXAMPLES</span></span>

### <span data-ttu-id="75281-111">Beispiel 1: Entfernen einer Sicherung für ein Gerät</span><span class="sxs-lookup"><span data-stu-id="75281-111">Example 1: Remove a backup for a device</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

<span data-ttu-id="75281-112">Dieser Befehl entfernt die Sicherung mit der angegebenen ID für das Gerät mit dem Namen Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="75281-112">This command removes the backup that has the specified ID for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="75281-113">Der Befehl startet den Vorgang, der das **Sicherungs** Objekt entfernt, und gibt dann ein **TaskResponse** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="75281-113">The command starts the operation that removes the **Backup** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="75281-114">Verwenden Sie das Cmdlet **Get-AzureStorSimpleTask** , um den Status der Aufgabe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="75281-114">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="75281-115">Beispiel 2: Entfernen der ersten Sicherung für ein Gerät mithilfe der ID</span><span class="sxs-lookup"><span data-stu-id="75281-115">Example 2: Remove the first backup for a device by using its ID</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

<span data-ttu-id="75281-116">Der erste Befehl ruft die Sicherungen für das Gerät mit dem Namen Contoso63-AppVm ab und speichert Sie dann in der $Backup Variablen.</span><span class="sxs-lookup"><span data-stu-id="75281-116">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="75281-117">Der zweite Befehl löscht eine Sicherung vom Gerät mit dem Namen Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="75281-117">The second command deletes a backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="75281-118">Der Befehl verwendet die standardmäßige Punktnotation, um auf die **InstanceId** -Eigenschaft des ersten Elements des $Backup-Arrays zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="75281-118">The command uses standard dot notation to refer to the **InstanceId** property of the first element of the $Backup array.</span></span>
<span data-ttu-id="75281-119">Dieser Befehl gibt den *WaitForComplete* -Parameter an, und der Befehl wartet daher, bis der Vorgang abgeschlossen ist, und gibt dann ein **TaskStatusInfo** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="75281-119">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="75281-120">Beispiel 3: Entfernen der ersten Sicherung für ein Gerät mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="75281-120">Example 3: Remove the first backup for a device by using the pipeline</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

<span data-ttu-id="75281-121">Der erste Befehl ruft die Sicherungen für das Gerät mit dem Namen Contoso63-AppVm ab und speichert Sie dann in der $Backup Variablen.</span><span class="sxs-lookup"><span data-stu-id="75281-121">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="75281-122">Der zweite Befehl übergibt das erste im $Backup-Array gespeicherte Objekt an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75281-122">The second command passes the first object stored in the $Backup array to the current cmdlet.</span></span>
<span data-ttu-id="75281-123">Dieses Cmdlet löscht diese Sicherung vom Gerät mit dem Namen Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="75281-123">That cmdlet deletes that backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="75281-124">Dieser Befehl gibt den *WaitForComplete* -Parameter an, und der Befehl wartet daher, bis der Vorgang abgeschlossen ist, und gibt dann ein **TaskStatusInfo** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="75281-124">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="75281-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="75281-125">PARAMETERS</span></span>

### <span data-ttu-id="75281-126">-Backup</span><span class="sxs-lookup"><span data-stu-id="75281-126">-Backup</span></span>
<span data-ttu-id="75281-127">Gibt das zu löschende **Sicherungs** Objekt an.</span><span class="sxs-lookup"><span data-stu-id="75281-127">Specifies the **Backup** object to delete.</span></span>
<span data-ttu-id="75281-128">Wenn Sie ein **Sicherungs** Objekt abrufen möchten, verwenden Sie das Cmdlet **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="75281-128">To obtain a **Backup** object, use the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75281-129">-Backup-Nr.</span><span class="sxs-lookup"><span data-stu-id="75281-129">-BackupId</span></span>
<span data-ttu-id="75281-130">Gibt die Instanz-ID einer zu löschenden Sicherung an.</span><span class="sxs-lookup"><span data-stu-id="75281-130">Specifies the instance ID of a backup to delete.</span></span>

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

### <span data-ttu-id="75281-131">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="75281-131">-DeviceName</span></span>
<span data-ttu-id="75281-132">Gibt den Namen des StorSimple-Geräts an, auf dem eine Sicherung gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="75281-132">Specifies the name of the StorSimple device on which to delete a backup.</span></span>

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

### <span data-ttu-id="75281-133">-Force</span><span class="sxs-lookup"><span data-stu-id="75281-133">-Force</span></span>
<span data-ttu-id="75281-134">Gibt an, dass Sie von diesem Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="75281-134">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="75281-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="75281-135">-Profile</span></span>
<span data-ttu-id="75281-136">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="75281-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="75281-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="75281-137">-WaitForComplete</span></span>
<span data-ttu-id="75281-138">Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="75281-138">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="75281-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75281-139">CommonParameters</span></span>
<span data-ttu-id="75281-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75281-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75281-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75281-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75281-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75281-142">INPUTS</span></span>

### <span data-ttu-id="75281-143">Backup</span><span class="sxs-lookup"><span data-stu-id="75281-143">Backup</span></span>

## <span data-ttu-id="75281-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75281-144">OUTPUTS</span></span>

### <span data-ttu-id="75281-145">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="75281-145">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="75281-146">Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben, wenn Sie diesen Parameter nicht angeben, wird ein **TaskResponse** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75281-146">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="75281-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="75281-147">NOTES</span></span>

## <span data-ttu-id="75281-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75281-148">RELATED LINKS</span></span>

[<span data-ttu-id="75281-149">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="75281-149">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)


