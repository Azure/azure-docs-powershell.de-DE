---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 403AD2BF-5D03-4B48-A635-E08216FFFC0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07df96f59b2278d804312d1076965ffed43c2569
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005954"
---
# <span data-ttu-id="70411-101">Start-AzureStorSimpleBackupCloneJob</span><span class="sxs-lookup"><span data-stu-id="70411-101">Start-AzureStorSimpleBackupCloneJob</span></span>

## <span data-ttu-id="70411-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70411-102">SYNOPSIS</span></span>
<span data-ttu-id="70411-103">Startet einen Auftrag, der eine Sicherung auf einem Gerät klont.</span><span class="sxs-lookup"><span data-stu-id="70411-103">Starts a job that clones a backup on a device.</span></span>

## <span data-ttu-id="70411-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70411-104">SYNTAX</span></span>

### <span data-ttu-id="70411-105">Leer (Standard)</span><span class="sxs-lookup"><span data-stu-id="70411-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleBackupCloneJob -BackupId <String> -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="70411-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="70411-106">IdentifyByName</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceName <String> -TargetDeviceName <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="70411-107">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="70411-107">IdentifyById</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceId <String> -TargetDeviceId <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="70411-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70411-108">DESCRIPTION</span></span>
<span data-ttu-id="70411-109">Mit dem Cmdlet **Start-AzureStorSimpleBackupCloneJob** wird ein Auftrag gestartet, der eine vorhandene Sicherung auf einem StorSimple-Gerät klont.</span><span class="sxs-lookup"><span data-stu-id="70411-109">The **Start-AzureStorSimpleBackupCloneJob** cmdlet starts a job that clones an existing backup on a StorSimple device.</span></span>

## <span data-ttu-id="70411-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70411-110">EXAMPLES</span></span>

### <span data-ttu-id="70411-111">Beispiel 1: Klonen einer Sicherung auf ein anderes Volume mithilfe von Gerätenamen</span><span class="sxs-lookup"><span data-stu-id="70411-111">Example 1: Clone a backup to a different volume by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07 -TargetDeviceName "ContosoDev07" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="70411-112">Der erste Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceBackup** die erste Sicherung für das Gerät mit dem Namen ContosoDev07 ab.</span><span class="sxs-lookup"><span data-stu-id="70411-112">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="70411-113">Der Befehl speichert diese Sicherung in der $Backup-Variablen.</span><span class="sxs-lookup"><span data-stu-id="70411-113">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="70411-114">Der zweite Befehl ruft Zugriffssteuerungseinträge mit dem Cmdlet **Get-AzureStorSimpleAccessControlRecord** ab.</span><span class="sxs-lookup"><span data-stu-id="70411-114">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="70411-115">Der Befehl speichert das Ergebnis in der $ACRS-Variablen.</span><span class="sxs-lookup"><span data-stu-id="70411-115">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="70411-116">Mit dem letzten Befehl wird ein Auftrag gestartet, der eine angegebene Sicherung eines Volumes auf einem Gerät auf ein anderes Volume auf dem gleichen Gerät klont.</span><span class="sxs-lookup"><span data-stu-id="70411-116">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="70411-117">In diesem Beispiel wird der Name des Geräts angegeben.</span><span class="sxs-lookup"><span data-stu-id="70411-117">This example specifies the device by name.</span></span>
<span data-ttu-id="70411-118">Der Befehl verwendet die Werte, die in $Backup und $ACRS gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="70411-118">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="70411-119">Der Befehl gibt die ID des Auftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="70411-119">The command returns the ID of the job.</span></span>

### <span data-ttu-id="70411-120">Beispiel 2: Klonen einer Sicherung auf ein anderes Volume mithilfe von Geräte-IDs</span><span class="sxs-lookup"><span data-stu-id="70411-120">Example 2: Clone a backup to a different volume by using device IDs</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev07 -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -TargetDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="70411-121">Der erste Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceBackup** die erste Sicherung für das Gerät mit dem Namen ContosoDev07 ab.</span><span class="sxs-lookup"><span data-stu-id="70411-121">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="70411-122">Der Befehl speichert diese Sicherung in der $Backup-Variablen.</span><span class="sxs-lookup"><span data-stu-id="70411-122">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="70411-123">Der zweite Befehl ruft Zugriffssteuerungseinträge mit dem Cmdlet **Get-AzureStorSimpleAccessControlRecord** ab.</span><span class="sxs-lookup"><span data-stu-id="70411-123">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="70411-124">Der Befehl speichert das Ergebnis in der $ACRS-Variablen.</span><span class="sxs-lookup"><span data-stu-id="70411-124">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="70411-125">Mit dem letzten Befehl wird ein Auftrag gestartet, der eine angegebene Sicherung eines Volumes auf einem Gerät auf ein anderes Volume auf dem gleichen Gerät klont.</span><span class="sxs-lookup"><span data-stu-id="70411-125">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="70411-126">In diesem Beispiel wird das Gerät nach Geräte-ID angegeben.</span><span class="sxs-lookup"><span data-stu-id="70411-126">This example specifies the device by device ID.</span></span>
<span data-ttu-id="70411-127">Der Befehl verwendet die Werte, die in $Backup und $ACRS gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="70411-127">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="70411-128">Der Befehl gibt die ID des Auftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="70411-128">The command returns the ID of the job.</span></span>

### <span data-ttu-id="70411-129">Beispiel 3: Klonen einer Sicherung auf ein Volume auf einem anderen Gerät mithilfe von Gerätenamen</span><span class="sxs-lookup"><span data-stu-id="70411-129">Example 3: Clone a backup to a volume on a different device by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07" -TargetDeviceName "ContosoDev12" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="70411-130">Der erste Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceBackup** die erste Sicherung für das Gerät mit dem Namen ContosoDev07 ab.</span><span class="sxs-lookup"><span data-stu-id="70411-130">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="70411-131">Der Befehl speichert diese Sicherung in der $Backup-Variablen.</span><span class="sxs-lookup"><span data-stu-id="70411-131">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="70411-132">Der zweite Befehl ruft Zugriffssteuerungseinträge mit dem Cmdlet **Get-AzureStorSimpleAccessControlRecord** ab.</span><span class="sxs-lookup"><span data-stu-id="70411-132">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="70411-133">Der Befehl speichert das Ergebnis in der $ACRS-Variablen.</span><span class="sxs-lookup"><span data-stu-id="70411-133">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="70411-134">Mit dem letzten Befehl wird ein Auftrag gestartet, der eine angegebene Sicherung eines Volumes auf einem Gerät auf ein Volume auf einem anderen Gerät klont.</span><span class="sxs-lookup"><span data-stu-id="70411-134">The final command begins a job that clones a specified backup of a volume on a device to a volume on a different device.</span></span>
<span data-ttu-id="70411-135">In diesem Beispiel werden die Geräte nach Namen angegeben.</span><span class="sxs-lookup"><span data-stu-id="70411-135">This example specifies the devices by name.</span></span>
<span data-ttu-id="70411-136">Der Befehl verwendet die Werte, die in $Backup und $ACRS gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="70411-136">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="70411-137">Der Befehl gibt die ID des Auftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="70411-137">The command returns the ID of the job.</span></span>

### <span data-ttu-id="70411-138">Beispiel 4: Klonen einer Sicherung auf ein anderes Volume mithilfe von Gerätenamen und dem Pipelineoperator</span><span class="sxs-lookup"><span data-stu-id="70411-138">Example 4: Clone a backup to a different volume by using device names and the pipeline operator</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev1 -First 1
PS C:\> Get-AzureStorSimpleAccessControlRecord -ACRName acr1 | Start-AzureStorSimpleBackupCloneJob -SourceDeviceName ContosoDev1 -TargetDeviceName ContosoDev1 -BackupId $backup.InstanceId -Snapshot $backup.Snapshots[0] -CloneVolumeName "cloned_vol1" 
VERBOSE: ClientRequestId: 1183a29d-63a9-408a-9065-032c92d317ee_PS
VERBOSE: ClientRequestId: e195717c-5920-4133-bdf0-c1201ebabf6f_PS
VERBOSE: ClientRequestId: ac16644d-bfd8-4edf-b1ad-f5df4ceb4df7_PS
VERBOSE: ClientRequestId: dcdcab7f-2aaa-496d-8a18-2e7449a70227_PS
VERBOSE: ClientRequestId: 6f92e422-eda9-4087-aefb-2257a49f5beb_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 646b280c-b51c-4812-b5c5-b7ca215f1c90_PS
a747d2dc-2876-474e-aea6-6546b255427e
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId a747d2dc-2876-474e-aea6-6546b255427e for tracking the job's status
VERBOSE: Access Control Record with given name acr11 is found!
```

<span data-ttu-id="70411-139">Der erste Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceBackup** die erste Sicherung für das Gerät mit dem Namen ContosoDev07 ab.</span><span class="sxs-lookup"><span data-stu-id="70411-139">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="70411-140">Der Befehl speichert diese Sicherung in der $Backup-Variablen.</span><span class="sxs-lookup"><span data-stu-id="70411-140">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="70411-141">Der zweite Befehl ruft Zugriffssteuerungseinträge mit dem Cmdlet **Get-AzureStorSimpleAccessControlRecord** ab.</span><span class="sxs-lookup"><span data-stu-id="70411-141">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="70411-142">Der Befehl übergibt seine Ergebnisse mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70411-142">The command passes its results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="70411-143">Das aktuelle Cmdlet beginnt einen Auftrag, der eine angegebene Sicherung eines Volumes auf einem Gerät auf ein anderes Volume auf demselben Gerät klont.</span><span class="sxs-lookup"><span data-stu-id="70411-143">The current cmdlet begins a job that clones a specified backup of a volume on a device, to a different volume on the same device.</span></span>
<span data-ttu-id="70411-144">In diesem Beispiel wird der Name des Geräts angegeben.</span><span class="sxs-lookup"><span data-stu-id="70411-144">This example specifies the device by name.</span></span>
<span data-ttu-id="70411-145">Der Befehl verwendet den in $Backup gespeicherten Wert.</span><span class="sxs-lookup"><span data-stu-id="70411-145">The command uses the value stored in $Backup.</span></span>
<span data-ttu-id="70411-146">Der Befehl übernimmt den Wert des *TargetAccessControlRecords* -Parameters aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="70411-146">The command takes the value of the *TargetAccessControlRecords* parameter from the pipeline.</span></span>
<span data-ttu-id="70411-147">Der Befehl gibt die ID des Auftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="70411-147">The command returns the ID of the job.</span></span>

## <span data-ttu-id="70411-148">Parameter</span><span class="sxs-lookup"><span data-stu-id="70411-148">PARAMETERS</span></span>

### <span data-ttu-id="70411-149">-Backup-Nr.</span><span class="sxs-lookup"><span data-stu-id="70411-149">-BackupId</span></span>
<span data-ttu-id="70411-150">Gibt die Instanz-ID des zu klonenden Backups an.</span><span class="sxs-lookup"><span data-stu-id="70411-150">Specifies the instance ID of the backup to clone.</span></span>

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

### <span data-ttu-id="70411-151">-CloneVolumeName</span><span class="sxs-lookup"><span data-stu-id="70411-151">-CloneVolumeName</span></span>
<span data-ttu-id="70411-152">Gibt den Namen des neuen geklonten Volumes auf dem Zielgerät an.</span><span class="sxs-lookup"><span data-stu-id="70411-152">Specifies the name for the new cloned volume on the target device.</span></span>

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

### <span data-ttu-id="70411-153">-Force</span><span class="sxs-lookup"><span data-stu-id="70411-153">-Force</span></span>
<span data-ttu-id="70411-154">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="70411-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="70411-155">-Profil</span><span class="sxs-lookup"><span data-stu-id="70411-155">-Profile</span></span>
<span data-ttu-id="70411-156">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="70411-156">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="70411-157">-Schnappschuss</span><span class="sxs-lookup"><span data-stu-id="70411-157">-Snapshot</span></span>
<span data-ttu-id="70411-158">Gibt das Snapshot-Objekt an, das dieses Cmdlet klont.</span><span class="sxs-lookup"><span data-stu-id="70411-158">Specifies the snapshot object that this cmdlet clones.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70411-159">-SourceDeviceId</span><span class="sxs-lookup"><span data-stu-id="70411-159">-SourceDeviceId</span></span>
<span data-ttu-id="70411-160">Gibt die Instanz-ID des Quellgeräts an.</span><span class="sxs-lookup"><span data-stu-id="70411-160">Specifies the instance ID of the source device.</span></span>
<span data-ttu-id="70411-161">Dieses Cmdlet klont die Rückseite des Quellgeräts.</span><span class="sxs-lookup"><span data-stu-id="70411-161">This cmdlet clones the back from the source device.</span></span>

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

### <span data-ttu-id="70411-162">-SourceDeviceName</span><span class="sxs-lookup"><span data-stu-id="70411-162">-SourceDeviceName</span></span>
<span data-ttu-id="70411-163">Gibt den Namen des Quellgeräts an.</span><span class="sxs-lookup"><span data-stu-id="70411-163">Specifies the name of the source device.</span></span>
<span data-ttu-id="70411-164">Dieses Cmdlet klont die Rückseite des Quellgeräts.</span><span class="sxs-lookup"><span data-stu-id="70411-164">This cmdlet clones the back from the source device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70411-165">-TargetAccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="70411-165">-TargetAccessControlRecords</span></span>
<span data-ttu-id="70411-166">Gibt die Zugriffssteuerungsdaten Sätze an.</span><span class="sxs-lookup"><span data-stu-id="70411-166">Specifies the access control records.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70411-167">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="70411-167">-TargetDeviceId</span></span>
<span data-ttu-id="70411-168">Gibt die Instanz-ID des Zielgeräts an.</span><span class="sxs-lookup"><span data-stu-id="70411-168">Specifies the instance ID of the target device.</span></span>

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

### <span data-ttu-id="70411-169">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="70411-169">-TargetDeviceName</span></span>
<span data-ttu-id="70411-170">Gibt den Namen des Geräts an, auf das dieses Cmdlet die Sicherung klont.</span><span class="sxs-lookup"><span data-stu-id="70411-170">Specifies the name of the device to which this cmdlet clones the backup.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70411-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70411-171">CommonParameters</span></span>
<span data-ttu-id="70411-172">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70411-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70411-173">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70411-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70411-174">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70411-174">INPUTS</span></span>

### <span data-ttu-id="70411-175">Schnappschuss, Liste der AccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="70411-175">Snapshot, List of AccessControlRecord</span></span>
<span data-ttu-id="70411-176">Sie können **Snapshot** -Objekte oder eine Liste von **AccessControlRecord** -Objekten an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="70411-176">You can pipe **Snapshot** objects or a list of **AccessControlRecord** objects to this cmdlet.</span></span>

## <span data-ttu-id="70411-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70411-177">OUTPUTS</span></span>

## <span data-ttu-id="70411-178">Notizen</span><span class="sxs-lookup"><span data-stu-id="70411-178">NOTES</span></span>

## <span data-ttu-id="70411-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70411-179">RELATED LINKS</span></span>

[<span data-ttu-id="70411-180">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="70411-180">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="70411-181">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="70411-181">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


