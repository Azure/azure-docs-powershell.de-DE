---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A62D1A9D-C0EF-4305-B1F9-3AE68A79222D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a5023abffae6bbc2b70b7400e604ffabb1d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006666"
---
# <span data-ttu-id="f042d-101">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="f042d-101">Remove-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="f042d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f042d-102">SYNOPSIS</span></span>
<span data-ttu-id="f042d-103">Entfernt ein Volume von einem StorSimple-Gerät.</span><span class="sxs-lookup"><span data-stu-id="f042d-103">Removes a volume from a StorSimple device.</span></span>

## <span data-ttu-id="f042d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f042d-104">SYNTAX</span></span>

### <span data-ttu-id="f042d-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="f042d-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f042d-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="f042d-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f042d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f042d-107">DESCRIPTION</span></span>
<span data-ttu-id="f042d-108">Das Cmdlet **Remove-AzureStorSimpleDeviceVolume** entfernt ein Volume von einem StorSimple-Gerät.</span><span class="sxs-lookup"><span data-stu-id="f042d-108">The **Remove-AzureStorSimpleDeviceVolume** cmdlet removes a volume from a StorSimple device.</span></span>
<span data-ttu-id="f042d-109">Dieses Cmdlet fordert Sie zur Bestätigung auf, es sei denn, Sie geben den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="f042d-109">This cmdlet prompts you for confirmation unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="f042d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f042d-110">EXAMPLES</span></span>

### <span data-ttu-id="f042d-111">Beispiel 1: Entfernen eines Volumes mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="f042d-111">Example 1: Remove a volume by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" | Remove-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: 2933e24d-9564-42b5-9053-5f0bc4f59ea8_PS
VERBOSE: ClientRequestId: 7c2d854b-537a-4253-bb0c-c15bc8aa2b49_PS
VERBOSE: ClientRequestId: 4bf749ac-517c-49e7-8027-a8f62e272014_PS
VERBOSE: ClientRequestId: 7d9ec87a-616d-4ca9-bfb8-158859174d59_PS

Confirm
Are you sure you want to remove the volume? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 67a38e28-a015-44b1-8159-c1a6604f4d81_PS
VERBOSE: About to run a job to remove your volume! 
VERBOSE: ClientRequestId: 56101c10-07ca-40f4-8f19-c6fdd895e3a5_PS
32925451-4451-4478-89f7-d8930505d3fb
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
32925451-4451-4478-89f7-d8930505d3fb for tracking the task's status
VERBOSE: Volume with name: Volume18 is found.
```

<span data-ttu-id="f042d-112">Dieser Befehl ruft das Volume mit dem Namen Volume18 auf dem Gerät mit dem Namen Contoso63-AppVm ab und übergibt dann das Volume mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f042d-112">This command gets the volume named Volume18 on the device named Contoso63-AppVm, and then passes that volume to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f042d-113">Das aktuelle Cmdlet startet die Aufgabe, die das Volume entfernt, und gibt dann ein **TaskResponse** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f042d-113">The current cmdlet starts the task that removes the volume, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="f042d-114">Verwenden Sie das Cmdlet **Get-AzureStorSimpleTask** , um den Status der Aufgabe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f042d-114">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="f042d-115">Der Befehl gibt keinen *Force* -Parameter an, sodass Sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f042d-115">The command does not specify the *Force* parameter, so the cmdlet prompts you for confirmation.</span></span>

### <span data-ttu-id="f042d-116">Beispiel 2: Entfernen eines Volumes ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="f042d-116">Example 2: Remove a volume without confirmation</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Force
VERBOSE: ClientRequestId: 72f13290-41eb-4ac4-9535-da1a42d0fa0b_PS
VERBOSE: ClientRequestId: ae0c1d99-1a66-4a69-9260-f2c8c12546bd_PS
VERBOSE: ClientRequestId: 9610744f-d031-488f-87e6-3ecddb305e13_PS
VERBOSE: About to run a job to remove your volume! 
VERBOSE: ClientRequestId: d33525d8-7276-4d2a-942d-d10f8078f1f7_PS
483f8cb4-ebc3-46a9-a9e6-0989e25738a0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
483f8cb4-ebc3-46a9-a9e6-0989e25738a0 for tracking the task's status
```

<span data-ttu-id="f042d-117">Dieser Befehl entfernt das Volume mit dem Namen Volume18 aus dem Gerät namens Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="f042d-117">This command removes the volume named Volume18 from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="f042d-118">Der Befehl gibt den Parameter *Force* an, sodass Sie vom Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f042d-118">The command specifies the *Force* parameter, so the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f042d-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="f042d-119">PARAMETERS</span></span>

### <span data-ttu-id="f042d-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f042d-120">-DeviceName</span></span>
<span data-ttu-id="f042d-121">Gibt den Namen des StorSimple-Geräts an, auf dem das zu entfernende Volume vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f042d-121">Specifies the name of the StorSimple device on which to the volume to remove exists.</span></span>

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

### <span data-ttu-id="f042d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f042d-122">-Force</span></span>
<span data-ttu-id="f042d-123">Gibt an, dass Sie von diesem Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f042d-123">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="f042d-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="f042d-124">-Profile</span></span>
<span data-ttu-id="f042d-125">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="f042d-125">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="f042d-126">-Lautstärke</span><span class="sxs-lookup"><span data-stu-id="f042d-126">-Volume</span></span>
<span data-ttu-id="f042d-127">Gibt das zu entfernende Volume als **VirtualDisk** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f042d-127">Specifies the volume to remove, as a **VirtualDisk** object.</span></span>
<span data-ttu-id="f042d-128">Verwenden Sie das Cmdlet **Get-AzureStorSimpleDeviceVolume** , um ein **VirtualDisk** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f042d-128">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolume** cmdlet.</span></span>

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

### <span data-ttu-id="f042d-129">-Volumename</span><span class="sxs-lookup"><span data-stu-id="f042d-129">-VolumeName</span></span>
<span data-ttu-id="f042d-130">Gibt den Namen des zu entfernenden Volumes an.</span><span class="sxs-lookup"><span data-stu-id="f042d-130">Specifies the name of the volume to remove.</span></span>

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

### <span data-ttu-id="f042d-131">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="f042d-131">-WaitForComplete</span></span>
<span data-ttu-id="f042d-132">Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f042d-132">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="f042d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f042d-133">CommonParameters</span></span>
<span data-ttu-id="f042d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f042d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f042d-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f042d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f042d-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f042d-136">INPUTS</span></span>

### <span data-ttu-id="f042d-137">VirtualDisk</span><span class="sxs-lookup"><span data-stu-id="f042d-137">VirtualDisk</span></span>
<span data-ttu-id="f042d-138">Dieses Cmdlet akzeptiert entweder das zu löschende **VirtualDisk** -Objekt oder den volumennamen des zu löschenden **VirtualDisk** .</span><span class="sxs-lookup"><span data-stu-id="f042d-138">This cmdlet accepts either the **VirtualDisk** object to delete or the volume name of the **VirtualDisk** to delete.</span></span>

## <span data-ttu-id="f042d-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f042d-139">OUTPUTS</span></span>

### <span data-ttu-id="f042d-140">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="f042d-140">TaskStatusInfo</span></span>
<span data-ttu-id="f042d-141">Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="f042d-141">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="f042d-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="f042d-142">NOTES</span></span>

## <span data-ttu-id="f042d-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f042d-143">RELATED LINKS</span></span>

[<span data-ttu-id="f042d-144">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="f042d-144">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="f042d-145">Neu – AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="f042d-145">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="f042d-146">Satz-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="f042d-146">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="f042d-147">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="f042d-147">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


