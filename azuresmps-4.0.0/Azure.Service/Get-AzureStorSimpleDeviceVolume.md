---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 79EE846E-D5BE-4808-BC6F-E3B16A308AB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9d0cd7ef0eacc7ff3e38c4619b60a0bd61f24f1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005772"
---
# <span data-ttu-id="d73ce-101">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="d73ce-101">Get-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="d73ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d73ce-102">SYNOPSIS</span></span>
<span data-ttu-id="d73ce-103">Ruft Volumes auf einem Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="d73ce-103">Gets volumes on a device.</span></span>

## <span data-ttu-id="d73ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d73ce-104">SYNTAX</span></span>

### <span data-ttu-id="d73ce-105">IdentifyByParentObject</span><span class="sxs-lookup"><span data-stu-id="d73ce-105">IdentifyByParentObject</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d73ce-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="d73ce-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d73ce-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d73ce-107">DESCRIPTION</span></span>
<span data-ttu-id="d73ce-108">Das Cmdlet " **Get-AzureStorSimpleDeviceVolume** " Ruft eine Liste der Volumes für einen angegebenen Volumen Container oder Volume mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="d73ce-108">The **Get-AzureStorSimpleDeviceVolume** cmdlet gets a list of volumes for a specified volume container, or volume that has the specified name.</span></span>
<span data-ttu-id="d73ce-109">Das zurückgegebene Objekt enthält die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d73ce-109">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="d73ce-110">**Access Type**</span><span class="sxs-lookup"><span data-stu-id="d73ce-110">**AccessType**</span></span>
- <span data-ttu-id="d73ce-111">**AcrList**</span><span class="sxs-lookup"><span data-stu-id="d73ce-111">**AcrList**</span></span>
- <span data-ttu-id="d73ce-112">**AppType**</span><span class="sxs-lookup"><span data-stu-id="d73ce-112">**AppType**</span></span>
- <span data-ttu-id="d73ce-113">**DataContainer**</span><span class="sxs-lookup"><span data-stu-id="d73ce-113">**DataContainer**</span></span>
- <span data-ttu-id="d73ce-114">**DataContainer-Nr**</span><span class="sxs-lookup"><span data-stu-id="d73ce-114">**DataContainerId**</span></span>
- <span data-ttu-id="d73ce-115">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="d73ce-115">**InstanceId**</span></span>
- <span data-ttu-id="d73ce-116">**IsBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="d73ce-116">**IsBackupEnabled**</span></span>
- <span data-ttu-id="d73ce-117">**IsDefaultBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="d73ce-117">**IsDefaultBackupEnabled**</span></span>
- <span data-ttu-id="d73ce-118">**IsMonitoringEnabled**</span><span class="sxs-lookup"><span data-stu-id="d73ce-118">**IsMonitoringEnabled**</span></span>
- <span data-ttu-id="d73ce-119">**Namen**</span><span class="sxs-lookup"><span data-stu-id="d73ce-119">**Name**</span></span>
- <span data-ttu-id="d73ce-120">**Online**</span><span class="sxs-lookup"><span data-stu-id="d73ce-120">**Online**</span></span>
- <span data-ttu-id="d73ce-121">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="d73ce-121">**OperationInProgress**</span></span>
- <span data-ttu-id="d73ce-122">**SizeInBytes**</span><span class="sxs-lookup"><span data-stu-id="d73ce-122">**SizeInBytes**</span></span>
- <span data-ttu-id="d73ce-123">**VSN**</span><span class="sxs-lookup"><span data-stu-id="d73ce-123">**VSN**</span></span>

## <span data-ttu-id="d73ce-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d73ce-124">EXAMPLES</span></span>

### <span data-ttu-id="d73ce-125">Beispiel 1: Abrufen von Volumes in einem angegebenen Container</span><span class="sxs-lookup"><span data-stu-id="d73ce-125">Example 1: Get volumes in a specified container</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container03" | Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
InstanceId             : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c
Name                   : Volume 1 Clone
Online                 : True
SizeInBytes            : 3298534883328
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c

InstanceId             : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe
Name                   : Volume 3 Clone
Online                 : True
SizeInBytes            : 1717986918400
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe

InstanceId             : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
Name                   : Volume 4
Online                 : True
SizeInBytes            : 1610612736000
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
```

<span data-ttu-id="d73ce-126">Dieser Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** den Volumen Container mit dem Namen Container03 auf dem Gerät mit dem Namen Contoso63-AppVm ab.</span><span class="sxs-lookup"><span data-stu-id="d73ce-126">This command gets the volume container named Container03 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="d73ce-127">Der Befehl übergibt diesen Container an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d73ce-127">The command uses the pipeline operator to pass that container to the current cmdlet.</span></span>
<span data-ttu-id="d73ce-128">Dieses Cmdlet ruft alle Volumes in diesem Container für das Gerät mit dem Namen Contoso63-AppVm ab.</span><span class="sxs-lookup"><span data-stu-id="d73ce-128">That cmdlet gets all the volumes in that container for the device named Contoso63-AppVm.</span></span>

### <span data-ttu-id="d73ce-129">Beispiel 2: Abrufen eines Volumes mithilfe des Namens</span><span class="sxs-lookup"><span data-stu-id="d73ce-129">Example 2: Get a volume by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18"
InstanceId             : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
Name                   : Volume18
Online                 : True
SizeInBytes            : 2748779069440
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
```

<span data-ttu-id="d73ce-130">Dieser Befehl ruft das Volume mit dem Namen Volume18 auf dem Gerät mit dem Namen Contoso63-AppVm ab.</span><span class="sxs-lookup"><span data-stu-id="d73ce-130">This command gets the volume named Volume18 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="d73ce-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="d73ce-131">PARAMETERS</span></span>

### <span data-ttu-id="d73ce-132">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d73ce-132">-DeviceName</span></span>
<span data-ttu-id="d73ce-133">Gibt den Namen des StorSimple-Geräts an, aus dem Volumes abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d73ce-133">Specifies the name of the StorSimple device from which to get volumes.</span></span>

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

### <span data-ttu-id="d73ce-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="d73ce-134">-Profile</span></span>
<span data-ttu-id="d73ce-135">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="d73ce-135">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="d73ce-136">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="d73ce-136">-VolumeContainer</span></span>
<span data-ttu-id="d73ce-137">Gibt den Volumen Container als **DataContainer-Objekt an** , das die abzurufenden Volumes enthält.</span><span class="sxs-lookup"><span data-stu-id="d73ce-137">Specifies the volume container, as a **DataContainer** object, that includes the volumes to get.</span></span>
<span data-ttu-id="d73ce-138">Verwenden Sie zum Abrufen eines **datacontainers** das Cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="d73ce-138">To obtain a **DataContainer** , use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: IdentifyByParentObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d73ce-139">-Volumename</span><span class="sxs-lookup"><span data-stu-id="d73ce-139">-VolumeName</span></span>
<span data-ttu-id="d73ce-140">Gibt den Namen des abzurufenden Volumes an.</span><span class="sxs-lookup"><span data-stu-id="d73ce-140">Specifies the name of the volume to get.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d73ce-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d73ce-141">CommonParameters</span></span>
<span data-ttu-id="d73ce-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d73ce-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d73ce-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d73ce-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d73ce-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d73ce-144">INPUTS</span></span>

### <span data-ttu-id="d73ce-145">DataContainer</span><span class="sxs-lookup"><span data-stu-id="d73ce-145">DataContainer</span></span>
<span data-ttu-id="d73ce-146">Dieses Cmdlet akzeptiert ein **DataContainer** -Objekt, das das abzurufende Volume enthält.</span><span class="sxs-lookup"><span data-stu-id="d73ce-146">This cmdlet accepts a **DataContainer** object that contains the volume to get.</span></span>

## <span data-ttu-id="d73ce-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d73ce-147">OUTPUTS</span></span>

### <span data-ttu-id="d73ce-148">VirtualDisk, IList\<VirtualDisk\></span><span class="sxs-lookup"><span data-stu-id="d73ce-148">VirtualDisk, IList\<VirtualDisk\></span></span>
<span data-ttu-id="d73ce-149">Dieses Cmdlet gibt ein **VirtualDisk** -Objekt zurück, wenn Sie den *Volumename* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="d73ce-149">This cmdlet returns a **VirtualDisk** object if you specify the *VolumeName* parameter.</span></span>
<span data-ttu-id="d73ce-150">Wenn Sie die *VolumeContainer* angeben, gibt dieses Cmdlet ein **IList \<VirtualDisk\>** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="d73ce-150">If you specify the *VolumeContainer* , this cmdlet returns an **IList\<VirtualDisk\>** object.</span></span>

## <span data-ttu-id="d73ce-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="d73ce-151">NOTES</span></span>

## <span data-ttu-id="d73ce-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d73ce-152">RELATED LINKS</span></span>

[<span data-ttu-id="d73ce-153">Neu – AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="d73ce-153">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="d73ce-154">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="d73ce-154">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="d73ce-155">Satz-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="d73ce-155">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="d73ce-156">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="d73ce-156">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


