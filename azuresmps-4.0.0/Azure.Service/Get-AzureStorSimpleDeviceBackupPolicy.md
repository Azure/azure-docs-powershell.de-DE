---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 8C7551CD-0222-44D1-AA1B-647669B01853
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdb7b8f1b53f7352e3e147c6f203e3a4460e8a05
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006495"
---
# <span data-ttu-id="19c78-101">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="19c78-101">Get-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="19c78-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19c78-102">SYNOPSIS</span></span>
<span data-ttu-id="19c78-103">Ruft Sicherungsrichtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="19c78-103">Gets backup policies.</span></span>

## <span data-ttu-id="19c78-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19c78-104">SYNTAX</span></span>

```
Get-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> [-BackupPolicyName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="19c78-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19c78-105">DESCRIPTION</span></span>
<span data-ttu-id="19c78-106">Das Cmdlet " **Get-AzureStorSimpleDeviceBackupPolicy** " ruft Sicherungsrichtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="19c78-106">The **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet gets backup policies.</span></span>
<span data-ttu-id="19c78-107">Dieses Cmdlet gibt ein **BackupPolicy** -Objekt oder eine Liste aller **BackupPolicy** -Objekte zurück, die zu einem Gerät gehören.</span><span class="sxs-lookup"><span data-stu-id="19c78-107">This cmdlet returns a **BackupPolicy** object or a list of all the **BackupPolicy** objects that belong to a device.</span></span>
<span data-ttu-id="19c78-108">Die Sicherungsrichtlinien Objekte enthalten die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="19c78-108">The backup policy objects contain the following properties:</span></span> 

- <span data-ttu-id="19c78-109">**Namen**</span><span class="sxs-lookup"><span data-stu-id="19c78-109">**Name**</span></span>
- <span data-ttu-id="19c78-110">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="19c78-110">**InstanceId**</span></span>
- <span data-ttu-id="19c78-111">**BackupPolicyCreationType**</span><span class="sxs-lookup"><span data-stu-id="19c78-111">**BackupPolicyCreationType**</span></span>
- <span data-ttu-id="19c78-112">**Last Backup**</span><span class="sxs-lookup"><span data-stu-id="19c78-112">**LastBackup**</span></span>
- <span data-ttu-id="19c78-113">**NextBackup**</span><span class="sxs-lookup"><span data-stu-id="19c78-113">**NextBackup**</span></span>
- <span data-ttu-id="19c78-114">**SchedulesCount**</span><span class="sxs-lookup"><span data-stu-id="19c78-114">**SchedulesCount**</span></span>
- <span data-ttu-id="19c78-115">**SSMHostName**</span><span class="sxs-lookup"><span data-stu-id="19c78-115">**SSMHostName**</span></span>
- <span data-ttu-id="19c78-116">**VolumesCount**</span><span class="sxs-lookup"><span data-stu-id="19c78-116">**VolumesCount**</span></span>

## <span data-ttu-id="19c78-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19c78-117">EXAMPLES</span></span>

### <span data-ttu-id="19c78-118">Beispiel 1: Abrufen von Details für eine Richtlinie</span><span class="sxs-lookup"><span data-stu-id="19c78-118">Example 1: Get details for a policy</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralBackupPolicy07"
VERBOSE: ClientRequestId: 2a878cd6-8432-4646-8be8-a0cb0750958e_PS
VERBOSE: ClientRequestId: 00ea5a6d-8c27-4e22-b182-5969cdbb8033_PS
VERBOSE: ClientRequestId: 39dac9ff-4455-45ae-ae3d-7de1445b9520_PS


BackupSchedules          : {8658e3a2-8a59-4d43-8725-ab0c95665301}
Volumes                  : {testvolume03, testvolume05}
BackupPolicyCreationType : BySaaS
LastBackup               : 
NextBackup               : 16-12-2014 00:30:00
SchedulesCount           : 1
SSMHostName              : 
VolumesCount             : 2
InstanceId               : 84140a6a-9254-4fff-8d09-ae40e9f1bc7d
Name                     : GeneralBackupPolicy07
OperationInProgress      : None

VERBOSE: BackupPolicy with id 84140a6a-9254-4fff-8d09-ae40e9f1bc7d found!
```

<span data-ttu-id="19c78-119">Dieser Befehl ruft ein **BackupPolicyDetails** -Objekt mit dem Namen GeneralBackupPolicy07 auf dem Gerät mit dem Namen Contoso63-AppVm ab.</span><span class="sxs-lookup"><span data-stu-id="19c78-119">This command gets a **BackupPolicyDetails** object named GeneralBackupPolicy07 on the device named Contoso63-AppVm.</span></span>

### <span data-ttu-id="19c78-120">Beispiel 2: Abrufen einer Liste mit Sicherungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="19c78-120">Example 2: Get a list of backup policies</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm"
InstanceId                           Name                               SchedulesCount VolumesCount                       BackupPolicyCreationType          LastBackup                        NextBackup                        SSMHostName                      
----------                           ----                               -------------- ------------                       ------------------------          ----------                        ----------                        -----------                      
13db29a4-bba9-4871-b872-db1fa0506b16 VG Clones                          1              2                                  BySaaS                            4/15/2015 8:30:02 AM              4/15/2015 8:30:00 PM                                               
2dcd3002-13c4-4bdb-a1ef-b35ce0a29416 vg-all                             1              4                                  BySaaS                            3/27/2015 9:12:15 PM              1/1/2010 5:30:00 AM                                                
54828d08-8309-4bd4-828f-21904863fb4c Cloud_Snapshot_Vol3_clone VG       1              1                                  BySaaS                            4/15/2015 9:00:03 AM              4/17/2015 9:00:30 AM                                               
6a51f39e-0ec9-4c57-8ec9-14a9255efa95 Test Group                         0              2                                  BySaaS                            3/27/2015 1:47:00 AM              1/1/2010 5:30:00 AM                                                
81c2db43-38f7-45fc-b2f2-476d1f6039a7 Cloud_Snapshot_Vol1_clone VG       1              1                                  BySaaS                            4/15/2015 7:30:02 AM              4/17/2015 7:30:00 AM                                               
82c4a5be-7473-431f-86e7-9db31ee9a9f8 Cloud_Snapshot_vg-all              1              4                                  BySaaS                            4/15/2015 11:30:02 AM             4/15/2015 3:30:00 PM                                               
cda96e83-3b38-4345-a56d-c8a96a0e57b3 Snapshot_vg-all                    1              4                                  BySaaS                            4/15/2015 1:30:02 PM              4/15/2015 3:30:00 PM
```

<span data-ttu-id="19c78-121">Dieser Befehl listet die **BackupPolicy** -Objekte auf dem Gerät mit dem Namen Contoso63-AppVm auf.</span><span class="sxs-lookup"><span data-stu-id="19c78-121">This command lists the **BackupPolicy** objects on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="19c78-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="19c78-122">PARAMETERS</span></span>

### <span data-ttu-id="19c78-123">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="19c78-123">-BackupPolicyName</span></span>
<span data-ttu-id="19c78-124">Gibt den Namen der abzurufenden Sicherungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="19c78-124">Specifies the name of the backup policy to get.</span></span>
<span data-ttu-id="19c78-125">Wenn Sie diesen Parameter nicht angeben, ruft dieses Cmdlet alle Richtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="19c78-125">If you do not specify this parameter, this cmdlet gets all policies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c78-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="19c78-126">-DeviceName</span></span>
<span data-ttu-id="19c78-127">Gibt den Namen des StorSimple-Geräts an, auf dem die Sicherungsrichtlinie erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="19c78-127">Specifies the name of the StorSimple device on which to create the backup policy.</span></span>

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

### <span data-ttu-id="19c78-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="19c78-128">-Profile</span></span>
<span data-ttu-id="19c78-129">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="19c78-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="19c78-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c78-130">CommonParameters</span></span>
<span data-ttu-id="19c78-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c78-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c78-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c78-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c78-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19c78-133">INPUTS</span></span>

### <span data-ttu-id="19c78-134">Keine</span><span class="sxs-lookup"><span data-stu-id="19c78-134">None</span></span>

## <span data-ttu-id="19c78-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19c78-135">OUTPUTS</span></span>

### <span data-ttu-id="19c78-136">IList \<BackupPolicy\> , BackupPolicyDetails</span><span class="sxs-lookup"><span data-stu-id="19c78-136">IList\<BackupPolicy\>, BackupPolicyDetails</span></span>
<span data-ttu-id="19c78-137">Dieses Cmdlet gibt ein **BackupPolicyDetails** -Objekt zurück, wenn Sie den *BackupPolicyName* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="19c78-137">This cmdlet returns a **BackupPolicyDetails** object, if you specify the *BackupPolicyName* parameter.</span></span>
<span data-ttu-id="19c78-138">Wenn Sie diesen Parameter nicht angeben, wird ein **IList \<BackupPolicy\>** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="19c78-138">If you do not specify that parameter, it returns an **IList\<BackupPolicy\>** object.</span></span>

## <span data-ttu-id="19c78-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="19c78-139">NOTES</span></span>

## <span data-ttu-id="19c78-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19c78-140">RELATED LINKS</span></span>

[<span data-ttu-id="19c78-141">Neu – AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="19c78-141">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="19c78-142">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="19c78-142">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="19c78-143">Satz-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="19c78-143">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)


