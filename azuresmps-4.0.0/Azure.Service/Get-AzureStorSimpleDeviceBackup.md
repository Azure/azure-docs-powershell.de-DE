---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A40879D2-371B-4CF1-BF1F-9E5C896EB89C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5ffe0a6e5a2d6ae181f4396eae2b5732f527843
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006496"
---
# <span data-ttu-id="a81bc-101">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="a81bc-101">Get-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="a81bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a81bc-102">SYNOPSIS</span></span>
<span data-ttu-id="a81bc-103">Ruft Sicherungen von einem Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="a81bc-103">Gets backups from a device.</span></span>

## <span data-ttu-id="a81bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a81bc-104">SYNTAX</span></span>

### <span data-ttu-id="a81bc-105">Leer (Standard)</span><span class="sxs-lookup"><span data-stu-id="a81bc-105">Empty (Default)</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> [-From <String>] [-To <String>] [-First <Int32>]
 [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a81bc-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="a81bc-106">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicyId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a81bc-107">IdentifyById2</span><span class="sxs-lookup"><span data-stu-id="a81bc-107">IdentifyById2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -VolumeId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a81bc-108">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="a81bc-108">IdentifyByObject</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-From <String>]
 [-To <String>] [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a81bc-109">IdentifyByObject2</span><span class="sxs-lookup"><span data-stu-id="a81bc-109">IdentifyByObject2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -Volume <VirtualDisk> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a81bc-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a81bc-110">DESCRIPTION</span></span>
<span data-ttu-id="a81bc-111">Das Cmdlet " **Get-AzureStorSimpleDeviceBackup** " ruft Sicherungen von einem Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="a81bc-111">The **Get-AzureStorSimpleDeviceBackup** cmdlet gets backups from a device.</span></span>
<span data-ttu-id="a81bc-112">Sie können die Sicherungsrichtlinie, das Volume und die Erstellungszeit für Sicherungen angeben.</span><span class="sxs-lookup"><span data-stu-id="a81bc-112">You can specify the backup policy, volume, and creation time for backups.</span></span>

<span data-ttu-id="a81bc-113">Dieses Cmdlet kann auf der ersten Seite maximal 100-Sicherungen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a81bc-113">This cmdlet can return a maximum of 100 backups in the first page.</span></span>
<span data-ttu-id="a81bc-114">Wenn mehr als 100-Sicherungen vorhanden sind, rufen Sie nachfolgende Seiten mithilfe des *First* -und *Skip* -Parameters ab.</span><span class="sxs-lookup"><span data-stu-id="a81bc-114">If more than 100 backups exist, retrieve subsequent pages by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="a81bc-115">Wenn Sie einen Wert von 100 für *Skip* und 50 für *First* angeben, gibt dieses Cmdlet nicht die ersten 100 Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="a81bc-115">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="a81bc-116">Nach dem 100 werden die nächsten 50-Ergebnisse zurückgegeben, die übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="a81bc-116">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="a81bc-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a81bc-117">EXAMPLES</span></span>

### <span data-ttu-id="a81bc-118">Beispiel 1: Abrufen aller Sicherungen auf einem Gerät</span><span class="sxs-lookup"><span data-stu-id="a81bc-118">Example 1: Get all backups on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
InstanceId                           Name                               Type          BackupJobCreationType              CreatedOn                          SizeInBytes                       Snapshots                         SSMHostName                      
----------                           ----                               ----          ---------------------              ---------                          -----------                       ---------                         -----------                      
85074062-ef6a-408a-b6c9-2a0904bb99ca Snapshot_vg-all                    LocalSnapshot BySchedule                         4/15/2015 1:30:02 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
ebd87fa3-a9e2-49c9-a7e6-dada47071544 Cloud_Snapshot_vg-all              CloudSnapshot BySchedule                         4/15/2015 11:30:02 AM              9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
9f7a03be-8c39-474c-bf88-b2c7b54e833c Cloud_Snapshot_Vol3_clone VG       CloudSnapshot BySchedule                         4/15/2015 9:00:03 AM               1717986918400                     {Volume 3 Clone}                                                   
177b2dad-c0b2-42d6-b7bb-16926e54e9c6 VG Clones                          CloudSnapshot BySchedule                         4/15/2015 8:30:02 AM               5016521801728                     {Volume 1 Clone, Volume 3 Clone}                                   
49c470c0-eadb-40ac-9928-94018a8edcd4 Cloud_Snapshot_Vol1_clone VG       CloudSnapshot BySchedule                         4/15/2015 7:30:02 AM               3298534883328                     {Volume 1 Clone}                                                   
45dfd283-f924-4b45-93eb-b20650cadf43 vg-all                             LocalSnapshot Adhoc                              3/27/2015 9:12:15 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
2c3dd48d-824c-4298-82b5-fb44abb67a1e Test Group                         LocalSnapshot Adhoc                              3/27/2015 1:47:00 AM               5016521801728                     {Volume 1, Volume 3}
```

<span data-ttu-id="a81bc-119">Dieser Befehl ruft alle Sicherungen ab, die auf dem Gerät mit dem Namen Contoso63-AppVm vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a81bc-119">This command gets all backups that exist on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="a81bc-120">Wenn für die erste Seite mehr als maximal 100-Sicherungen zulässig sind, verwenden Sie die Parameter *First* und *Skip* , um weitere Ergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a81bc-120">If there are more than the maximum of 100 backups allowed for the first page, use the *First* and *Skip* parameters to view additional results.</span></span>

### <span data-ttu-id="a81bc-121">Beispiel 2: Abrufen von Sicherungen, die zwischen zwei Datumsangaben erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="a81bc-121">Example 2: Get backups created between two dates</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -From "9/7/2014" -To "10/7/2014" -First 2 -Skip 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/5/2014 11:00:04 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : ec2fdf5c-c807-4f7b-a942-d4c4a9b68c44
Name                  : ContosoTSQA_Default
BackupJobCreationType : BySchedule
CreatedOn             : 10/4/2014 11:00:06 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 5ac4f947-f4c6-4770-9000-2242e72fc6d3
Name                  : ContosoTSQA_DefaultVERBOSE: # of backups returned : 2
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 2 -Skip 3\" in
your commandlet
```

<span data-ttu-id="a81bc-122">Dieser Befehl ruft Sicherungen auf dem Gerät mit dem Namen Contoso63-AppVm ab, die am oder nach 10/7/2014 und vor 10/8/2014 erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="a81bc-122">This command gets backups on the device named Contoso63-AppVm that were created on or after 10/7/2014 and on or before 10/8/2014.</span></span>
<span data-ttu-id="a81bc-123">Dieses Cmdlet überspringt das erste Ergebnis und gibt die ersten beiden Ergebnisse nach dem ersten Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="a81bc-123">This cmdlet skips the first result and returns the first two results after that first result.</span></span>
<span data-ttu-id="a81bc-124">Ändern Sie die Werte für *First* , und *überspringen* Sie, um andere Ergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a81bc-124">Modify values for *First* and *Skip* to view other results.</span></span>

### <span data-ttu-id="a81bc-125">Beispiel 3: Abrufen von Sicherungen für eine Sicherungsrichtlinien-ID</span><span class="sxs-lookup"><span data-stu-id="a81bc-125">Example 3: Get backups for a backup policy ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="a81bc-126">Dieser Befehl ruft Sicherungen auf dem Gerät mit dem Namen Contoso63-AppVm ab, die am oder vor dem angegebenen Datum erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="a81bc-126">This command gets backups on the device named Contoso63-AppVm created on or before the specified date.</span></span>
<span data-ttu-id="a81bc-127">Der Befehl ruft Sicherungen ab, die mit der Sicherungsrichtlinie erstellt wurden, die die angegebene ID aufweist.</span><span class="sxs-lookup"><span data-stu-id="a81bc-127">The command gets backups that were created by using the backup policy that has the specified ID.</span></span>
<span data-ttu-id="a81bc-128">Dieser Befehl gibt den *ersten* Parameter an, sodass nur die ersten 10 Ergebnisse zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a81bc-128">This command specifies the *First* parameter, so it returns only the first 10 results.</span></span>

### <span data-ttu-id="a81bc-129">Beispiel 4: Abrufen von Sicherungen für ein sicherungsrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="a81bc-129">Example 4: Get backups for a backup policy object</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQATest_Default" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="a81bc-130">Dieser Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** ein **BackupPolicyDetails** -Objekt ab und übergibt dieses Objekt dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a81bc-130">This command gets a **BackupPolicyDetails** object by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a81bc-131">Dieses Cmdlet ruft Sicherungen für das Gerät mit dem Namen Contoso63-AppVm ab, das mithilfe der Sicherungsrichtlinie aus dem ersten Teil des Befehls erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a81bc-131">That cmdlet gets backups for the device named Contoso63-AppVm created by using the backup policy from the first part of the command.</span></span>
<span data-ttu-id="a81bc-132">Der Befehl ruft Sicherungen ab, die am oder vor dem angegebenen Datum erstellt wurden, genau wie im vorherigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="a81bc-132">The command gets backups created on or before the specified date, just as in the previous example.</span></span>
<span data-ttu-id="a81bc-133">Dieser Befehl gibt nur die ersten 10 Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="a81bc-133">This command returns only the first 10 results.</span></span>

### <span data-ttu-id="a81bc-134">Beispiel 5: Abrufen einer Sicherung für eine Volumen-ID</span><span class="sxs-lookup"><span data-stu-id="a81bc-134">Example 5: Get a backup for a volume ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -VolumeId "SS-VOL-246b9df1-11bb-4071-8043-f955cc406446" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="a81bc-135">Dieser Befehl ruft eine Sicherung auf dem Gerät ab, die auf dem Datenträger mit der angegebenen Instanz-ID erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a81bc-135">This command gets a backup on the device that is created on the volume that has the specified instance ID.</span></span>
<span data-ttu-id="a81bc-136">Dieser Befehl gibt den *ersten* Parameter an, sodass nur das erste Ergebnis zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a81bc-136">This command specifies the *First* parameter, so it returns only the first one result.</span></span>

### <span data-ttu-id="a81bc-137">Beispiel 6: Abrufen einer Sicherung für einen Datenträgernamen</span><span class="sxs-lookup"><span data-stu-id="a81bc-137">Example 6: Get a backup for a volume name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "TSQATest03" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="a81bc-138">Dieser Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceVolume** ein **VirtualDisk** -Objekt ab und übergibt dieses Objekt dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a81bc-138">This command gets a **VirtualDisk** object by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a81bc-139">Dieses Cmdlet ruft Sicherungen für das Gerät mit dem Namen Contoso63-AppVm ab, das auf dem Volume aus dem ersten Teil des Befehls erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a81bc-139">That cmdlet gets backups for the device named Contoso63-AppVm created on the volume from the first part of the command.</span></span>
<span data-ttu-id="a81bc-140">Dieser Befehl gibt nur das erste Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="a81bc-140">This command returns only the first result.</span></span>

## <span data-ttu-id="a81bc-141">Parameter</span><span class="sxs-lookup"><span data-stu-id="a81bc-141">PARAMETERS</span></span>

### <span data-ttu-id="a81bc-142">-BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="a81bc-142">-BackupPolicy</span></span>
<span data-ttu-id="a81bc-143">Gibt ein **BackupPolicyDetails** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a81bc-143">Specifies a **BackupPolicyDetails** object.</span></span>
<span data-ttu-id="a81bc-144">Dieses Cmdlet verwendet die **InstanceId** dieses Objekts, um zu ermitteln, welche Sicherungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a81bc-144">This cmdlet uses the **InstanceId** of this object to determine which backups to get.</span></span>
<span data-ttu-id="a81bc-145">Verwenden Sie das Cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** , um ein **BackupPolicyDetails** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a81bc-145">To obtain a **BackupPolicyDetails** object, use the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: BackupPolicyDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a81bc-146">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="a81bc-146">-BackupPolicyId</span></span>
<span data-ttu-id="a81bc-147">Gibt eine Instanz-ID einer Sicherungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="a81bc-147">Specifies an instance ID of a backup policy.</span></span>
<span data-ttu-id="a81bc-148">Dieses Cmdlet ruft Gerätesicherungen für Richtlinien ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a81bc-148">This cmdlet gets device backups for policy that this parameter specifies.</span></span>

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

### <span data-ttu-id="a81bc-149">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a81bc-149">-DeviceName</span></span>
<span data-ttu-id="a81bc-150">Gibt den Namen des StorSimple-Geräts an, für das Sicherungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a81bc-150">Specifies the name of the StorSimple device for which to get backups.</span></span>

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

### <span data-ttu-id="a81bc-151">-First</span><span class="sxs-lookup"><span data-stu-id="a81bc-151">-First</span></span>
<span data-ttu-id="a81bc-152">Ruft nur die angegebene Anzahl von Objekten ab.</span><span class="sxs-lookup"><span data-stu-id="a81bc-152">Gets only the specified number of objects.</span></span>
<span data-ttu-id="a81bc-153">Geben Sie die Anzahl der abzurufenden Objekte ein.</span><span class="sxs-lookup"><span data-stu-id="a81bc-153">Enter the number of objects to get.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a81bc-154">-Ab</span><span class="sxs-lookup"><span data-stu-id="a81bc-154">-From</span></span>
<span data-ttu-id="a81bc-155">Gibt das Startdatum und die Startzeit für die Sicherungen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="a81bc-155">Specifies the start date and time for the backups that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a81bc-156">-Profil</span><span class="sxs-lookup"><span data-stu-id="a81bc-156">-Profile</span></span>
<span data-ttu-id="a81bc-157">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="a81bc-157">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="a81bc-158">-Skip</span><span class="sxs-lookup"><span data-stu-id="a81bc-158">-Skip</span></span>
<span data-ttu-id="a81bc-159">Ignoriert die angegebene Anzahl von Objekten und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="a81bc-159">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="a81bc-160">Geben Sie die Anzahl der zu überspringenden Objekte ein.</span><span class="sxs-lookup"><span data-stu-id="a81bc-160">Enter the number of objects to skip.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a81bc-161">-To</span><span class="sxs-lookup"><span data-stu-id="a81bc-161">-To</span></span>
<span data-ttu-id="a81bc-162">Gibt das Enddatum und die Endzeit für die Sicherungen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="a81bc-162">Specifies the end date and time for the backups that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a81bc-163">-Lautstärke</span><span class="sxs-lookup"><span data-stu-id="a81bc-163">-Volume</span></span>
<span data-ttu-id="a81bc-164">Gibt ein **VirtualDisk** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a81bc-164">Specifies a **VirtualDisk** object.</span></span>
<span data-ttu-id="a81bc-165">Dieses Cmdlet verwendet die **InstanceId** dieses Objekts, um das Volume zu ermitteln, in dem Sicherungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a81bc-165">This cmdlet uses the **InstanceId** of this object to determine the volume in which backups exist.</span></span>
<span data-ttu-id="a81bc-166">Verwenden Sie zum Abrufen eines **VirtualDisk** -Objekts den **Get-AzureStorSimpleDeviceVolume-** Parameter.</span><span class="sxs-lookup"><span data-stu-id="a81bc-166">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolume** parameter.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject2
Aliases: VirtualDiskInfo

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a81bc-167">-Volumen-Nr.</span><span class="sxs-lookup"><span data-stu-id="a81bc-167">-VolumeId</span></span>
<span data-ttu-id="a81bc-168">Gibt die Instanz-ID des Volumes an, in dem Sicherungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a81bc-168">Specifies the instance ID of the volume in which backups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById2
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a81bc-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a81bc-169">CommonParameters</span></span>
<span data-ttu-id="a81bc-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a81bc-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a81bc-171">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a81bc-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a81bc-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a81bc-172">INPUTS</span></span>

### <span data-ttu-id="a81bc-173">BackupPolicyDetails, VirtualDisk</span><span class="sxs-lookup"><span data-stu-id="a81bc-173">BackupPolicyDetails, VirtualDisk</span></span>
<span data-ttu-id="a81bc-174">Dieses Cmdlet akzeptiert **BackupPolicyDetails** -und **VirtualDisk** -Objekte.</span><span class="sxs-lookup"><span data-stu-id="a81bc-174">This cmdlet accepts **BackupPolicyDetails** and **VirtualDisk** objects.</span></span>

## <span data-ttu-id="a81bc-175">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a81bc-175">OUTPUTS</span></span>

### <span data-ttu-id="a81bc-176">IList\<Backup\></span><span class="sxs-lookup"><span data-stu-id="a81bc-176">IList\<Backup\></span></span>
<span data-ttu-id="a81bc-177">Dieses Cmdlet gibt eine Liste von **Sicherungs** Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="a81bc-177">This cmdlet returns a list of **Backup** objects.</span></span>

## <span data-ttu-id="a81bc-178">Notizen</span><span class="sxs-lookup"><span data-stu-id="a81bc-178">NOTES</span></span>

## <span data-ttu-id="a81bc-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a81bc-179">RELATED LINKS</span></span>

[<span data-ttu-id="a81bc-180">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="a81bc-180">Remove-AzureStorSimpleDeviceBackup</span></span>](./Remove-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="a81bc-181">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="a81bc-181">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="a81bc-182">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="a81bc-182">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)


