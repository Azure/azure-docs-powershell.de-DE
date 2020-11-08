---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 049201C9-590F-47EB-9030-25F80CD8DFA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f3337556a9d7bd52e5800af5cdbd65b71ab9818
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005729"
---
# <span data-ttu-id="64a89-101">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="64a89-101">New-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="64a89-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64a89-102">SYNOPSIS</span></span>
<span data-ttu-id="64a89-103">Erstellt ein Volume in einem angegebenen Volumen Container.</span><span class="sxs-lookup"><span data-stu-id="64a89-103">Creates a volume in a specified volume container.</span></span>

## <span data-ttu-id="64a89-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64a89-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer> -VolumeName <String>
 -VolumeSizeInBytes <Int64>
 -AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>
 -VolumeAppType <AppType> -Online <Boolean> -EnableDefaultBackup <Boolean> -EnableMonitoring <Boolean>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="64a89-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64a89-105">DESCRIPTION</span></span>
<span data-ttu-id="64a89-106">Das Cmdlet **New-AzureStorSimpleDeviceVolume** erstellt ein Volume in einem angegebenen Volumen Container.</span><span class="sxs-lookup"><span data-stu-id="64a89-106">The **New-AzureStorSimpleDeviceVolume** cmdlet creates a volume in a specified volume container.</span></span>
<span data-ttu-id="64a89-107">Mit diesem Cmdlet werden die einzelnen Volumes mit mindestens einem Zugriffssteuerungseintrag verknüpft.</span><span class="sxs-lookup"><span data-stu-id="64a89-107">This cmdlet associates each volume with one or more access control records.</span></span>
<span data-ttu-id="64a89-108">Verwenden Sie zum Abrufen von **AccessControlRecord** -Objekten das Cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="64a89-108">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="64a89-109">Geben Sie einen Namen, eine Größe und einen AppType für das Volume an.</span><span class="sxs-lookup"><span data-stu-id="64a89-109">Specify a name, size, and AppType for the volume.</span></span>
<span data-ttu-id="64a89-110">Geben Sie außerdem an, ob das Volume online erstellt werden soll, ob die Standardsicherung aktiviert werden soll und ob die Überwachung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="64a89-110">Also, specify whether to create the volume online, whether to enable default backup, and whether to enable monitoring.</span></span>

## <span data-ttu-id="64a89-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64a89-111">EXAMPLES</span></span>

### <span data-ttu-id="64a89-112">Beispiel 1: Erstellen eines Volumes</span><span class="sxs-lookup"><span data-stu-id="64a89-112">Example 1: Create a volume</span></span>
```
PS C:\>$AcrList = Get-AzureStorSimpleAccessControlRecord
PS C:\> Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer07" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Size 2000000000 -AccessControlRecords $AcrList -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False

VERBOSE: ClientRequestId: a29d1a84-1f81-4f20-9130-7adfe45e41fb_PS
VERBOSE: ClientRequestId: 8fa63df1-3f81-4029-a536-b536a70068ad_PS
VERBOSE: ClientRequestId: 964c5744-8bb1-4f70-beda-95ca4c7f3eb6_PS
VERBOSE: ClientRequestId: f09fff3a-54fa-4a0e-93db-b079260ed2dd_PS
VERBOSE: ClientRequestId: 59aa29e3-8044-411a-adae-b64a2681ffed_PS
VERBOSE: ClientRequestId: 0ffd0297-19be-40fe-a64e-6a2947d831b4_PS
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90 for tracking the task's status
VERBOSE: Volume container with name: VolumeContainer07 is found.
```

<span data-ttu-id="64a89-113">Der erste Befehl ruft die Zugriffssteuerungseinträge in der StorSimple-Manager-Dienstkonfiguration mit dem Cmdlet **Get-AzureStorSimpleAccessControlRecord** ab und speichert Sie dann in der $AcrList-Variablen.</span><span class="sxs-lookup"><span data-stu-id="64a89-113">The first command gets the access control records in the StorSimple Manager service configuration by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet, and then stores them in the $AcrList variable.</span></span>

<span data-ttu-id="64a89-114">Der zweite Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** den Volumen Container mit dem Namen VolumeContainer07 für das Gerät mit dem Namen Contoso63-AppVm ab.</span><span class="sxs-lookup"><span data-stu-id="64a89-114">The second command gets the volume container named VolumeContainer07 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="64a89-115">Der Befehl übergibt diesen Container mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64a89-115">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="64a89-116">Mit diesem Cmdlet wird das Volume erstellt.</span><span class="sxs-lookup"><span data-stu-id="64a89-116">This cmdlet creates the volume.</span></span>
<span data-ttu-id="64a89-117">Der Befehl gibt den Namen des Volumes, die Größe und die Zugriffssteuerungseinträge an, die in $AcrList gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="64a89-117">The command specifies the name for the volume, the size, and the access control records stored in $AcrList.</span></span>
<span data-ttu-id="64a89-118">Mit diesem Befehl wird der Auftrag gestartet, und dann wird ein **TaskResponse** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="64a89-118">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="64a89-119">Verwenden Sie das Cmdlet " **Get-AzureStorSimpleTask** ", um den Status des Auftrags anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="64a89-119">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="64a89-120">Beispiel 2: Erstellen eines Volumes ohne Access Controlaccess Control recordsaccess-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="64a89-120">Example 2: Create a volume without Access Controlaccess control recordsaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer01" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume22" -Size 2000000000 -AccessControlRecords @() -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False -WaitForComplete
VERBOSE: ClientRequestId: 3f359790-7e1f-48e7-acf8-ecabba850966_PS
VERBOSE: ClientRequestId: 2723ebcf-cd72-47bb-99b5-0c099d45641b_PS
VERBOSE: ClientRequestId: e605091f-dd63-42a7-bda2-24753cbc1f9a_PS
VERBOSE: ClientRequestId: b3fd08c3-67c5-4309-9591-15d92c360469_PS
VERBOSE: ClientRequestId: 15a024a3-b0c9-4f83-9c34-0ed8b95d024b_PS
VERBOSE: ClientRequestId: c13f92f9-aea1-40dd-af80-3affe273adbe_PS


TaskId       : ceef657e-390e-4f7a-aab7-669a29c29e7f
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 1d79febf-f752-4255-af2d-230d40773bc6_PS
AccessType             : NoAccess
AcrIdList              : {}
AcrList                : {}
AppType                : PrimaryVolume
DataContainer          : Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainer
DataContainerId        : 68b63d15-6aa5-4e69-9f9d-4a0bc607d6e9
InstanceId             : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd
InternalInstanceId     : 
IsBackupEnabled        : False
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
Name                   : Volume22
Online                 : True
OperationInProgress    : None
SizeInBytes            : 2000000000
VSN                    : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd

VERBOSE: Volume container with name: VolumeContainer01 is found.
```

<span data-ttu-id="64a89-121">Dieser Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** den Volumen Container mit dem Namen VolumeContainer01 für das Gerät mit dem Namen Contoso63-AppVm ab.</span><span class="sxs-lookup"><span data-stu-id="64a89-121">This command gets the volume container named VolumeContainer01 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="64a89-122">Der Befehl übergibt diesen Container mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64a89-122">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="64a89-123">Mit diesem Cmdlet wird das Volume erstellt.</span><span class="sxs-lookup"><span data-stu-id="64a89-123">This cmdlet creates the volume.</span></span>
<span data-ttu-id="64a89-124">Der Befehl gibt den Namen des Volumes, die Größe und einen leeren Wert für die Zugriffssteuerungsdaten Sätze an.</span><span class="sxs-lookup"><span data-stu-id="64a89-124">The command specifies the name for the volume, the size, and an empty value for access control records.</span></span>
<span data-ttu-id="64a89-125">Dieser Befehl gibt den *WaitForComplete* -Parameter an, sodass nach dem Erstellen des Volumes ein **TaskStatusInfo** -Wert zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="64a89-125">This command specifies the *WaitForComplete* parameter, so it returns a **TaskStatusInfo** after it creates the volume.</span></span>

<span data-ttu-id="64a89-126">Da der Befehl keine Zugriffssteuerungseinträge angibt, kann auf dieses Volume nicht zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="64a89-126">Because the command specifies no access control records, this volume cannot be accessed.</span></span>
<span data-ttu-id="64a89-127">Sie können später mithilfe des Cmdlets " **Satz-AzureStorSimpleDeviceVolume** " Zugriff hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="64a89-127">You can add access, later, by using **Set-AzureStorSimpleDeviceVolume** cmdlet.</span></span>

## <span data-ttu-id="64a89-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="64a89-128">PARAMETERS</span></span>

### <span data-ttu-id="64a89-129">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="64a89-129">-AccessControlRecords</span></span>
<span data-ttu-id="64a89-130">Gibt eine Liste der Zugriffssteuerungseinträge an, die dem Datenträger zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64a89-130">Specifies a list of access control records to associate with the volume.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64a89-131">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="64a89-131">-DeviceName</span></span>
<span data-ttu-id="64a89-132">Gibt den Namen des StorSimple-Geräts an, auf dem das Volume erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64a89-132">Specifies the name of the StorSimple device on which to create the volume.</span></span>

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

### <span data-ttu-id="64a89-133">-EnableDefaultBackup</span><span class="sxs-lookup"><span data-stu-id="64a89-133">-EnableDefaultBackup</span></span>
<span data-ttu-id="64a89-134">Gibt an, ob die Standardsicherung für das Volume aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="64a89-134">Specifies whether to enable default backup for the volume.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a89-135">-EnableMonitoring</span><span class="sxs-lookup"><span data-stu-id="64a89-135">-EnableMonitoring</span></span>
<span data-ttu-id="64a89-136">Gibt an, ob die Überwachung des Volumes aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="64a89-136">Specifies whether to enable monitoring for the volume.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a89-137">-Online</span><span class="sxs-lookup"><span data-stu-id="64a89-137">-Online</span></span>
<span data-ttu-id="64a89-138">Gibt an, ob das Volume online erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64a89-138">Specifies whether to create the volume online.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a89-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="64a89-139">-Profile</span></span>
<span data-ttu-id="64a89-140">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="64a89-140">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="64a89-141">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="64a89-141">-VolumeAppType</span></span>
<span data-ttu-id="64a89-142">Gibt an, ob ein primäres oder Archiv Volume erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64a89-142">Specifies whether to create a primary or archive volume.</span></span>
<span data-ttu-id="64a89-143">Gültige Werte sind: PrimaryVolume und ArchiveVolume.</span><span class="sxs-lookup"><span data-stu-id="64a89-143">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a89-144">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="64a89-144">-VolumeContainer</span></span>
<span data-ttu-id="64a89-145">Gibt den Container als **DataContainer-Objekt an** , in dem das Volume erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64a89-145">Specifies the container, as a **DataContainer** object, in which to create the volume.</span></span>
<span data-ttu-id="64a89-146">Verwenden Sie das Cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** , um ein **VirtualDisk** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="64a89-146">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64a89-147">-Volumename</span><span class="sxs-lookup"><span data-stu-id="64a89-147">-VolumeName</span></span>
<span data-ttu-id="64a89-148">Gibt einen Namen für das neue Volume an.</span><span class="sxs-lookup"><span data-stu-id="64a89-148">Specifies a name for the new volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a89-149">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="64a89-149">-VolumeSizeInBytes</span></span>
<span data-ttu-id="64a89-150">Gibt die Datenträgergröße in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="64a89-150">Specifies the volume size in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a89-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="64a89-151">-WaitForComplete</span></span>
<span data-ttu-id="64a89-152">Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="64a89-152">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="64a89-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a89-153">CommonParameters</span></span>
<span data-ttu-id="64a89-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a89-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a89-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64a89-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a89-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64a89-156">INPUTS</span></span>

### <span data-ttu-id="64a89-157">DataContainer, Liste\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="64a89-157">DataContainer, List\<AccessControlRecord\></span></span>
<span data-ttu-id="64a89-158">Dieses Cmdlet akzeptiert ein **DataContainer** -Objekt und eine Liste von **AccessControlRecord** -Objekten für das neue Volume.</span><span class="sxs-lookup"><span data-stu-id="64a89-158">This cmdlet accepts a **DataContainer** object and a list of **AccessControlRecord** objects for the new volume.</span></span>

## <span data-ttu-id="64a89-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64a89-159">OUTPUTS</span></span>

### <span data-ttu-id="64a89-160">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="64a89-160">TaskStatusInfo</span></span>
<span data-ttu-id="64a89-161">Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="64a89-161">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="64a89-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="64a89-162">NOTES</span></span>

## <span data-ttu-id="64a89-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64a89-163">RELATED LINKS</span></span>

[<span data-ttu-id="64a89-164">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="64a89-164">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="64a89-165">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="64a89-165">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="64a89-166">Satz-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="64a89-166">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="64a89-167">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="64a89-167">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="64a89-168">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="64a89-168">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="64a89-169">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="64a89-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


