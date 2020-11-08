---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F420A47F-D036-4B31-AA59-97CFC9C79E75
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a53d0821832b29f0f1f6a0b2ab5f1353e3331a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006404"
---
# <span data-ttu-id="e6b35-101">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="e6b35-101">New-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="e6b35-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6b35-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b35-103">Erstellt ein Festplatten-Konfigurationssatz Objekt.</span><span class="sxs-lookup"><span data-stu-id="e6b35-103">Creates a disk configuration set object.</span></span>

## <span data-ttu-id="e6b35-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6b35-104">SYNTAX</span></span>

```
New-AzureVMImageDiskConfigSet [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6b35-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6b35-105">DESCRIPTION</span></span>
<span data-ttu-id="e6b35-106">Das Cmdlet **New-AzureVMImageDiskConfigSet** erstellt ein Festplatten-Konfigurationssatz Objekt, das an das Image Update-Cmdlet übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e6b35-106">The **New-AzureVMImageDiskConfigSet** cmdlet creates a disk configuration set object that is passed to the image update cmdlet.</span></span>
<span data-ttu-id="e6b35-107">Sie kapselt die OSDiskConfig und das DataDiskConfig-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e6b35-107">It encapsulates the OSDiskConfig and the DataDiskConfig object.</span></span>
<span data-ttu-id="e6b35-108">Verwenden Sie die Cmdlets " **Satz-AzureVMImageOSDiskConfig** " und " **AzureVMImageDataDiskConfig** ", um die Eigenschaften des Betriebssystems festzulegen und die Datenträgereigenschaften für das Bild des virtuellen Computers festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e6b35-108">Use the **Set-AzureVMImageOSDiskConfig** and **Set-AzureVMImageDataDiskConfig** cmdlets to set the OS Disk and Data Disk properties for the virtual machine image.</span></span>

## <span data-ttu-id="e6b35-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6b35-109">EXAMPLES</span></span>

### <span data-ttu-id="e6b35-110">Beispiel 1: Erstellen eines Festplatten-Konfigurationssatz Objekts</span><span class="sxs-lookup"><span data-stu-id="e6b35-110">Example 1: Create a disk configuration set object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="e6b35-111">Mit diesem Befehl wird ein Festplatten-Konfigurationssatz Objekt erstellt, und die Ergebnisse werden in der Variablen mit dem Namen $Disk gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e6b35-111">This command creates a disk configuration set object and stores the results in the variable named $Disk.</span></span>
<span data-ttu-id="e6b35-112">Nachdem die Datenträgerkonfiguration erstellt wurde, wird Sie verwendet, um die OSDiskConfig und DataDiskConfig festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e6b35-112">After the disk configuration is created, it is used to set the OSDiskConfig and DataDiskConfig.</span></span>
<span data-ttu-id="e6b35-113">Anschließend wird der virtuelle Computer mit der Konfiguration aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e6b35-113">Then the virtual machine is updated with the configuration.</span></span>

## <span data-ttu-id="e6b35-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6b35-114">PARAMETERS</span></span>

### <span data-ttu-id="e6b35-115">-Information</span><span class="sxs-lookup"><span data-stu-id="e6b35-115">-InformationAction</span></span>
<span data-ttu-id="e6b35-116">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="e6b35-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e6b35-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e6b35-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6b35-118">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="e6b35-118">Continue</span></span>
- <span data-ttu-id="e6b35-119">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="e6b35-119">Ignore</span></span>
- <span data-ttu-id="e6b35-120">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="e6b35-120">Inquire</span></span>
- <span data-ttu-id="e6b35-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e6b35-121">SilentlyContinue</span></span>
- <span data-ttu-id="e6b35-122">Beenden</span><span class="sxs-lookup"><span data-stu-id="e6b35-122">Stop</span></span>
- <span data-ttu-id="e6b35-123">Anhalten</span><span class="sxs-lookup"><span data-stu-id="e6b35-123">Suspend</span></span>

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

### <span data-ttu-id="e6b35-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e6b35-124">-InformationVariable</span></span>
<span data-ttu-id="e6b35-125">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="e6b35-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e6b35-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b35-126">CommonParameters</span></span>
<span data-ttu-id="e6b35-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6b35-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b35-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6b35-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b35-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6b35-129">INPUTS</span></span>

## <span data-ttu-id="e6b35-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6b35-130">OUTPUTS</span></span>

### <span data-ttu-id="e6b35-131">Microsoft. WindowsAzure. Commands. Servicemanagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="e6b35-131">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="e6b35-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6b35-132">NOTES</span></span>

## <span data-ttu-id="e6b35-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6b35-133">RELATED LINKS</span></span>

[<span data-ttu-id="e6b35-134">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="e6b35-134">Get-AzureVMImageDiskConfigSet</span></span>](./Get-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="e6b35-135">Satz-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="e6b35-135">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="e6b35-136">Satz-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="e6b35-136">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


