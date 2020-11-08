---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: C50959BB-7481-4898-BF4B-C5ABF8758473
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2c06455004afbd15235f59164034abc2147964b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006659"
---
# <span data-ttu-id="8c815-101">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="8c815-101">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="8c815-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c815-102">SYNOPSIS</span></span>
<span data-ttu-id="8c815-103">Entfernt einen Volumen Container von einem StorSimple-Gerät.</span><span class="sxs-lookup"><span data-stu-id="8c815-103">Removes a volume container from a StorSimple device.</span></span>

## <span data-ttu-id="8c815-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c815-104">SYNTAX</span></span>

```
Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainer <DataContainer>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8c815-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c815-105">DESCRIPTION</span></span>
<span data-ttu-id="8c815-106">Das Cmdlet **Remove-AzureStorSimpleDeviceVolumeContainer** entfernt ein Volumen Containerobjekt von einem StorSimple-Gerät.</span><span class="sxs-lookup"><span data-stu-id="8c815-106">The **Remove-AzureStorSimpleDeviceVolumeContainer** cmdlet removes a volume container object from a StorSimple device.</span></span>
<span data-ttu-id="8c815-107">Dieses Cmdlet fordert Sie zur Bestätigung auf, es sei denn, Sie geben den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="8c815-107">This cmdlet prompts you for confirmation unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="8c815-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c815-108">EXAMPLES</span></span>

### <span data-ttu-id="8c815-109">Beispiel 1: Entfernen eines Containers mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="8c815-109">Example 1: Remove a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" | Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -Force
VERBOSE: ClientRequestId: 0efbb4fc-ceb0-4311-bc49-0e08161d0a37_PS
VERBOSE: ClientRequestId: bf5b615f-47e3-4868-91b6-f2d12217a302_PS
VERBOSE: ClientRequestId: 5590c87e-0602-4197-b6c3-cf58b0e7a7b3_PS
VERBOSE: ClientRequestId: b33c71ac-c345-44ff-8213-d7fdf9f8480a_PS
VERBOSE: ClientRequestId: 903d42ef-58f4-4e89-ba7f-5f234262356d_PS
VERBOSE: About to create a job to remove your Volume container! 
VERBOSE: ClientRequestId: 2279575f-5115-4344-9c6f-9ef599bd203e_PS
e9ddec89-67ac-4e2e-a2ed-820de3547bb0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
e9ddec89-67ac-4e2e-a2ed-820de3547bb0 for tracking the task's status
VERBOSE: Volume container with name: Container08 is found.
```

<span data-ttu-id="8c815-110">Dieser Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** den Volumen Container mit dem Namen Container08 auf dem Gerät mit dem Namen Contoso63-AppVm ab.</span><span class="sxs-lookup"><span data-stu-id="8c815-110">This command gets the volume container named Container08 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="8c815-111">Der Befehl übergibt den Volumen Container mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c815-111">The command passes the volume container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8c815-112">Mit diesem Befehl wird die Aufgabe gestartet, um den Container zu entfernen, und es wird ein **TaskResponse** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8c815-112">This command starts the task to remove the container, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="8c815-113">Verwenden Sie das Cmdlet **Get-AzureStorSimpleTask** , um den Status der Aufgabe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8c815-113">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="8c815-114">Dieser Befehl gibt den *Force* -Parameter an, sodass Sie nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="8c815-114">This command specifies the *Force* parameter, so it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8c815-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c815-115">PARAMETERS</span></span>

### <span data-ttu-id="8c815-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8c815-116">-DeviceName</span></span>
<span data-ttu-id="8c815-117">Gibt den Namen des StorSimple-Geräts an, auf dem der zu entfernende Volumen Container vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8c815-117">Specifies the name of the StorSimple device on which to the volume container to remove exists.</span></span>

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

### <span data-ttu-id="8c815-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8c815-118">-Force</span></span>
<span data-ttu-id="8c815-119">Gibt an, dass Sie von diesem Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="8c815-119">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="8c815-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="8c815-120">-Profile</span></span>
<span data-ttu-id="8c815-121">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="8c815-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="8c815-122">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="8c815-122">-VolumeContainer</span></span>
<span data-ttu-id="8c815-123">Gibt den zu entfernenden Volumen Container als **DataContainer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8c815-123">Specifies the volume container to remove, as a **DataContainer** object.</span></span>
<span data-ttu-id="8c815-124">Verwenden Sie das Cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** , um ein **DataContainer** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8c815-124">To obtain a **DataContainer** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c815-125">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="8c815-125">-WaitForComplete</span></span>
<span data-ttu-id="8c815-126">Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8c815-126">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="8c815-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c815-127">CommonParameters</span></span>
<span data-ttu-id="8c815-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c815-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c815-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c815-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c815-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c815-130">INPUTS</span></span>

### <span data-ttu-id="8c815-131">DataContainer</span><span class="sxs-lookup"><span data-stu-id="8c815-131">DataContainer</span></span>
<span data-ttu-id="8c815-132">Dieses Cmdlet akzeptiert ein **DataContainer** -Objekt, das entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c815-132">This cmdlet accepts a **DataContainer** object to remove.</span></span>

## <span data-ttu-id="8c815-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c815-133">OUTPUTS</span></span>

### <span data-ttu-id="8c815-134">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="8c815-134">TaskStatusInfo</span></span>
<span data-ttu-id="8c815-135">Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="8c815-135">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="8c815-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c815-136">NOTES</span></span>

## <span data-ttu-id="8c815-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c815-137">RELATED LINKS</span></span>

[<span data-ttu-id="8c815-138">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="8c815-138">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="8c815-139">Neu – AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="8c815-139">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


