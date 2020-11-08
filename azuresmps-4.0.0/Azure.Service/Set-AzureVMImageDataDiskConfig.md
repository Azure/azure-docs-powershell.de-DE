---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6C7CB0AE-C788-4E6F-AD48-E30B547A2269
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7512ef446227742c2a3564c5f3e5f38f1e2ccce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005642"
---
# <span data-ttu-id="30609-101">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="30609-101">Set-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="30609-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="30609-102">SYNOPSIS</span></span>
<span data-ttu-id="30609-103">Legt die Datenträgereigenschaften auf dem Bild des virtuellen Computers fest.</span><span class="sxs-lookup"><span data-stu-id="30609-103">Sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="30609-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="30609-104">SYNTAX</span></span>

### <span data-ttu-id="30609-105">UpdateAzureVMImageParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="30609-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-Lun] <Int32> [-HostCaching] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="30609-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="30609-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-HostCaching] <String> [-MediaLink] <Uri> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="30609-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30609-107">DESCRIPTION</span></span>
<span data-ttu-id="30609-108">Das Cmdlet " **Set-AzureVMImageDataDiskConfig** " legt die Daten Datenträgereigenschaften auf dem Bild des virtuellen Computers fest.</span><span class="sxs-lookup"><span data-stu-id="30609-108">The **Set-AzureVMImageDataDiskConfig** cmdlet sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="30609-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30609-109">EXAMPLES</span></span>

### <span data-ttu-id="30609-110">Beispiel 1: Einrichten von Datenträgereigenschaften auf einem virtuellen Computer Bild</span><span class="sxs-lookup"><span data-stu-id="30609-110">Example 1: Set Data Disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="30609-111">Mit diesem Befehl werden Datenträgereigenschaften auf einem virtuellen Computer festgelegt und dann das Bild des virtuellen Computers aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="30609-111">This command sets data disk properties on a virtual machine then updates the virtual machine image.</span></span>

## <span data-ttu-id="30609-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="30609-112">PARAMETERS</span></span>

### <span data-ttu-id="30609-113">-Datadiskname</span><span class="sxs-lookup"><span data-stu-id="30609-113">-DataDiskName</span></span>
<span data-ttu-id="30609-114">Gibt den Namen des Daten Datenträgers an, den dieses Cmdlet konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="30609-114">Specifies the name of the data disk that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: UpdateAzureVMImageParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30609-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="30609-115">-DiskConfig</span></span>
<span data-ttu-id="30609-116">Gibt das Datenträger Konfigurationsobjekt an, das die Datenträgerobjekte des Betriebssystems kapselt.</span><span class="sxs-lookup"><span data-stu-id="30609-116">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30609-117">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="30609-117">-HostCaching</span></span>
<span data-ttu-id="30609-118">Gibt das Host Cache Attribut für den Betriebssystemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="30609-118">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="30609-119">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="30609-119">Valid values are:</span></span>

<span data-ttu-id="30609-120">--ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="30609-120">--ReadOnly --ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30609-121">-Information</span><span class="sxs-lookup"><span data-stu-id="30609-121">-InformationAction</span></span>
<span data-ttu-id="30609-122">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="30609-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="30609-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="30609-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="30609-124">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="30609-124">Continue</span></span>
- <span data-ttu-id="30609-125">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="30609-125">Ignore</span></span>
- <span data-ttu-id="30609-126">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="30609-126">Inquire</span></span>
- <span data-ttu-id="30609-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="30609-127">SilentlyContinue</span></span>
- <span data-ttu-id="30609-128">Beenden</span><span class="sxs-lookup"><span data-stu-id="30609-128">Stop</span></span>
- <span data-ttu-id="30609-129">Anhalten</span><span class="sxs-lookup"><span data-stu-id="30609-129">Suspend</span></span>

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

### <span data-ttu-id="30609-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="30609-130">-InformationVariable</span></span>
<span data-ttu-id="30609-131">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="30609-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="30609-132">-LUN</span><span class="sxs-lookup"><span data-stu-id="30609-132">-Lun</span></span>
<span data-ttu-id="30609-133">Gibt den Steckplatz an, in dem das Datenlaufwerk auf dem virtuellen Computer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="30609-133">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30609-134">-MediaLINK</span><span class="sxs-lookup"><span data-stu-id="30609-134">-MediaLink</span></span>
<span data-ttu-id="30609-135">Gibt den URI des Speicherorts an, an dem die neue virtuelle Festplatte erstellt wird, wenn der neue Daten Datenträger hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="30609-135">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30609-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30609-136">CommonParameters</span></span>
<span data-ttu-id="30609-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30609-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30609-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30609-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30609-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="30609-139">INPUTS</span></span>

## <span data-ttu-id="30609-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="30609-140">OUTPUTS</span></span>

### <span data-ttu-id="30609-141">Microsoft. WindowsAzure. Commands. Servicemanagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="30609-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="30609-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="30609-142">NOTES</span></span>

## <span data-ttu-id="30609-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="30609-143">RELATED LINKS</span></span>

[<span data-ttu-id="30609-144">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="30609-144">Remove-AzureVMImageDataDiskConfig</span></span>](./Remove-AzureVMImageDataDiskConfig.md)


