---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 39E9BB88-6AD8-4B05-9498-35393E22BA30
online version: ''
schema: 2.0.0
ms.openlocfilehash: 234b1f7fa2719cc1b34e6bcd0b8e8fd340acc4af
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006624"
---
# <span data-ttu-id="670a9-101">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="670a9-101">Set-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="670a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="670a9-102">SYNOPSIS</span></span>
<span data-ttu-id="670a9-103">Aktualisiert die Eigenschaften eines vorhandenen Volumes.</span><span class="sxs-lookup"><span data-stu-id="670a9-103">Updates the properties of an existing volume.</span></span>

## <span data-ttu-id="670a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="670a9-104">SYNTAX</span></span>

### <span data-ttu-id="670a9-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="670a9-105">IdentifyByName</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="670a9-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="670a9-106">IdentifyByObject</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="670a9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="670a9-107">DESCRIPTION</span></span>
<span data-ttu-id="670a9-108">Das Cmdlet " **Satz-AzureStorSimpleDeviceVolume** " aktualisiert die Eigenschaften eines vorhandenen Volumes.</span><span class="sxs-lookup"><span data-stu-id="670a9-108">The **Set-AzureStorSimpleDeviceVolume** cmdlet updates the properties of an existing volume.</span></span>
<span data-ttu-id="670a9-109">Dieses Cmdlet ordnet ein Volume einem oder mehreren Zugriffssteuerungseinträgen zu.</span><span class="sxs-lookup"><span data-stu-id="670a9-109">This cmdlet associates a volume with one or more access control records.</span></span>
<span data-ttu-id="670a9-110">Verwenden Sie zum Abrufen von **AccessControlRecord** -Objekten das Cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="670a9-110">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="670a9-111">Aktualisieren Sie die Größe oder den Typ des Volumes.</span><span class="sxs-lookup"><span data-stu-id="670a9-111">Update the size or type for the volume.</span></span>
<span data-ttu-id="670a9-112">Aktualisieren Sie außerdem, ob das Volume online erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="670a9-112">Also, update whether to create the volume online.</span></span>

## <span data-ttu-id="670a9-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="670a9-113">EXAMPLES</span></span>

### <span data-ttu-id="670a9-114">Beispiel 1: Online-Wert für ein Volume aktualisieren</span><span class="sxs-lookup"><span data-stu-id="670a9-114">Example 1: Update online value for a volume</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $False
VERBOSE: ClientRequestId: f2869570-ea47-4be7-801e-9c0f22f2600d_PS
VERBOSE: ClientRequestId: c70bb86a-51d3-4390-be17-4d0847641dc3_PS
VERBOSE: ClientRequestId: d20cb5b2-6b3c-4e06-af99-cada28c5e50a_PS
VERBOSE: ClientRequestId: ab6d533e-b55b-4cfb-9c58-9153295e0547_PS
de7000f1-29c7-4102-a375-b52432f9e67e
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
de7000f1-29c7-4102-a375-b52432f9e67e for tracking the task's status
```

<span data-ttu-id="670a9-115">Dieser Befehl aktualisiert das Volume mit dem Namen Volume18, um einen Online-Wert von $false zu haben.</span><span class="sxs-lookup"><span data-stu-id="670a9-115">This command updates the volume named Volume18 to have an online value of $False.</span></span>
<span data-ttu-id="670a9-116">Mit diesem Befehl wird die Aufgabe gestartet, und dann wird ein **TaskResponse** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="670a9-116">This command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="670a9-117">Verwenden Sie das Cmdlet **Get-AzureStorSimpleTask** , um den Status der Aufgabe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="670a9-117">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="670a9-118">Beispiel 2: Ändern des Online Werts und des Typs</span><span class="sxs-lookup"><span data-stu-id="670a9-118">Example 2: Modify online value and type</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $True -VolumeAppType ArchiveVolume 
VERBOSE: ClientRequestId: af42b02a-645e-4801-a2d7-4197511c68cf_PS
VERBOSE: ClientRequestId: 7cb4f3b4-548e-42dc-a38c-0df0911c5206_PS
VERBOSE: ClientRequestId: 7cc706ad-a58f-4939-8e78-cabae8379a51_PS
VERBOSE: ClientRequestId: 6bed21d5-12fc-4a12-a89c-120bdb5636b1_PS
aa977225-af78-4c93-b754-72704afc928f
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
aa977225-af78-4c93-b754-72704afc928f for tracking the task's status
```

<span data-ttu-id="670a9-119">Mit diesem Befehl wird das Volume mit dem Namen Volume18 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="670a9-119">This command updates the volume named Volume18.</span></span>
<span data-ttu-id="670a9-120">Sie ändert den Typ und ändert den Wert des *Online-* Parameters in $true.</span><span class="sxs-lookup"><span data-stu-id="670a9-120">It modifies the type and changes the value of the *Online* parameter to $True.</span></span>

## <span data-ttu-id="670a9-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="670a9-121">PARAMETERS</span></span>

### <span data-ttu-id="670a9-122">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="670a9-122">-AccessControlRecords</span></span>
<span data-ttu-id="670a9-123">Gibt eine Liste der Zugriffssteuerungseinträge an, die dem Datenträger zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="670a9-123">Specifies a list of access control records to associate with the volume.</span></span>

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

### <span data-ttu-id="670a9-124">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="670a9-124">-DeviceName</span></span>
<span data-ttu-id="670a9-125">Gibt den Namen des StorSimple-Geräts an, auf dem das Volume aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="670a9-125">Specifies the name of the StorSimple device on which to update the volume exists.</span></span>

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

### <span data-ttu-id="670a9-126">-Information</span><span class="sxs-lookup"><span data-stu-id="670a9-126">-InformationAction</span></span>
<span data-ttu-id="670a9-127">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="670a9-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="670a9-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="670a9-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="670a9-129">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="670a9-129">Continue</span></span>
- <span data-ttu-id="670a9-130">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="670a9-130">Ignore</span></span>
- <span data-ttu-id="670a9-131">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="670a9-131">Inquire</span></span>
- <span data-ttu-id="670a9-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="670a9-132">SilentlyContinue</span></span>
- <span data-ttu-id="670a9-133">Beenden</span><span class="sxs-lookup"><span data-stu-id="670a9-133">Stop</span></span>
- <span data-ttu-id="670a9-134">Anhalten</span><span class="sxs-lookup"><span data-stu-id="670a9-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670a9-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="670a9-135">-InformationVariable</span></span>
<span data-ttu-id="670a9-136">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="670a9-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670a9-137">-Name</span><span class="sxs-lookup"><span data-stu-id="670a9-137">-NewName</span></span>
<span data-ttu-id="670a9-138">Gibt einen neuen Namen für das StorSimple-Gerät an.</span><span class="sxs-lookup"><span data-stu-id="670a9-138">Specifies a new name for the StorSimple device.</span></span>

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

### <span data-ttu-id="670a9-139">-Online</span><span class="sxs-lookup"><span data-stu-id="670a9-139">-Online</span></span>
<span data-ttu-id="670a9-140">Gibt an, ob das Volume online ist.</span><span class="sxs-lookup"><span data-stu-id="670a9-140">Specifies whether the volume is online.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670a9-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="670a9-141">-Profile</span></span>
<span data-ttu-id="670a9-142">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="670a9-142">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="670a9-143">-Lautstärke</span><span class="sxs-lookup"><span data-stu-id="670a9-143">-Volume</span></span>
<span data-ttu-id="670a9-144">Gibt den Namen des Volumes an, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="670a9-144">Specifies the name of the volume to update.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="670a9-145">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="670a9-145">-VolumeAppType</span></span>
<span data-ttu-id="670a9-146">Gibt an, ob das Volume als primäres oder Archivierungs Volume aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="670a9-146">Specifies whether to update the volume to be a primary or archive volume.</span></span>
<span data-ttu-id="670a9-147">Gültige Werte sind: PrimaryVolume und ArchiveVolume.</span><span class="sxs-lookup"><span data-stu-id="670a9-147">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670a9-148">-Volumename</span><span class="sxs-lookup"><span data-stu-id="670a9-148">-VolumeName</span></span>
<span data-ttu-id="670a9-149">Gibt den Namen des Volumes an, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="670a9-149">Specifies the name of the volume to update.</span></span>

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

### <span data-ttu-id="670a9-150">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="670a9-150">-VolumeSizeInBytes</span></span>
<span data-ttu-id="670a9-151">Gibt die aktualisierte Größe des Volumes in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="670a9-151">Specifies the updated size, in bytes, for the volume.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670a9-152">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="670a9-152">-WaitForComplete</span></span>
<span data-ttu-id="670a9-153">Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="670a9-153">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="670a9-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670a9-154">CommonParameters</span></span>
<span data-ttu-id="670a9-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="670a9-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670a9-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="670a9-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670a9-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="670a9-157">INPUTS</span></span>

### <span data-ttu-id="670a9-158">Liste\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="670a9-158">List\<AccessControlRecord\></span></span>
<span data-ttu-id="670a9-159">Dieses Cmdlet akzeptiert eine Liste von **AccessControlRecord** -Objekten, die einem Datenträger zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="670a9-159">This cmdlet accepts a list of **AccessControlRecord** objects to associate to a volume.</span></span>

## <span data-ttu-id="670a9-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="670a9-160">OUTPUTS</span></span>

### <span data-ttu-id="670a9-161">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="670a9-161">TaskStatusInfo</span></span>
<span data-ttu-id="670a9-162">Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="670a9-162">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="670a9-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="670a9-163">NOTES</span></span>

## <span data-ttu-id="670a9-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="670a9-164">RELATED LINKS</span></span>

[<span data-ttu-id="670a9-165">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="670a9-165">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="670a9-166">Neu – AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="670a9-166">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="670a9-167">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="670a9-167">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="670a9-168">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="670a9-168">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="670a9-169">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="670a9-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


