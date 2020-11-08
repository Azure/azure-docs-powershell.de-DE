---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9CD39F1C-D858-4275-A6DE-10901DC962FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cb2557b411d46ce718f97ba7939efb4571ce025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005650"
---
# <span data-ttu-id="77173-101">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="77173-101">Set-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="77173-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77173-102">SYNOPSIS</span></span>
<span data-ttu-id="77173-103">Legt die Datenträgereigenschaften des Betriebssystems auf einem Bild eines virtuellen Computers fest.</span><span class="sxs-lookup"><span data-stu-id="77173-103">Sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="77173-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77173-104">SYNTAX</span></span>

### <span data-ttu-id="77173-105">UpdateAzureVMImageParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="77173-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="77173-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="77173-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-MediaLink] <Uri> [-OSState] <String> [-OS] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="77173-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77173-107">DESCRIPTION</span></span>
<span data-ttu-id="77173-108">Das Cmdlet " **Set-AzureVMImageOSDiskConfig** " legt die Eigenschaften des Betriebssystemdatenträgers für ein Bild eines virtuellen Computers fest.</span><span class="sxs-lookup"><span data-stu-id="77173-108">The **Set-AzureVMImageOSDiskConfig** cmdlet sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="77173-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77173-109">EXAMPLES</span></span>

### <span data-ttu-id="77173-110">Beispiel 1: Einrichten der Festplatten Eigenschaften des Betriebssystems auf einem virtuellen Computer Bild</span><span class="sxs-lookup"><span data-stu-id="77173-110">Example 1: Set the operating system disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="77173-111">In diesem Beispiel werden die Datenträgereigenschaften des Betriebssystems auf einem Bild eines virtuellen Computers festgelegt.</span><span class="sxs-lookup"><span data-stu-id="77173-111">This example sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="77173-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="77173-112">PARAMETERS</span></span>

### <span data-ttu-id="77173-113">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="77173-113">-DiskConfig</span></span>
<span data-ttu-id="77173-114">Gibt das Datenträger Konfigurationsobjekt an, das die Datenträgerobjekte des Betriebssystems kapselt.</span><span class="sxs-lookup"><span data-stu-id="77173-114">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

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

### <span data-ttu-id="77173-115">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="77173-115">-HostCaching</span></span>
<span data-ttu-id="77173-116">Gibt das Host Cache Attribut für den Betriebssystemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="77173-116">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="77173-117">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="77173-117">Valid values are:</span></span>

<span data-ttu-id="77173-118">--ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="77173-118">--ReadOnly --ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77173-119">-Information</span><span class="sxs-lookup"><span data-stu-id="77173-119">-InformationAction</span></span>
<span data-ttu-id="77173-120">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="77173-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="77173-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="77173-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="77173-122">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="77173-122">Continue</span></span>
- <span data-ttu-id="77173-123">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="77173-123">Ignore</span></span>
- <span data-ttu-id="77173-124">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="77173-124">Inquire</span></span>
- <span data-ttu-id="77173-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="77173-125">SilentlyContinue</span></span>
- <span data-ttu-id="77173-126">Beenden</span><span class="sxs-lookup"><span data-stu-id="77173-126">Stop</span></span>
- <span data-ttu-id="77173-127">Anhalten</span><span class="sxs-lookup"><span data-stu-id="77173-127">Suspend</span></span>

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

### <span data-ttu-id="77173-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="77173-128">-InformationVariable</span></span>
<span data-ttu-id="77173-129">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="77173-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="77173-130">-MediaLINK</span><span class="sxs-lookup"><span data-stu-id="77173-130">-MediaLink</span></span>
<span data-ttu-id="77173-131">Gibt den URI des Speicherorts an, an dem die neue virtuelle Festplatte erstellt wird, wenn der neue Daten Datenträger hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="77173-131">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77173-132">-OS</span><span class="sxs-lookup"><span data-stu-id="77173-132">-OS</span></span>
<span data-ttu-id="77173-133">Gibt das Betriebssystem der Datenträgerkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="77173-133">Specifies the operating system of the disk configuration.</span></span>

<span data-ttu-id="77173-134">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="77173-134">Valid values are:</span></span>

- <span data-ttu-id="77173-135">Windows</span><span class="sxs-lookup"><span data-stu-id="77173-135">Windows</span></span>
- <span data-ttu-id="77173-136">Linux</span><span class="sxs-lookup"><span data-stu-id="77173-136">Linux</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77173-137">-OSState</span><span class="sxs-lookup"><span data-stu-id="77173-137">-OSState</span></span>
<span data-ttu-id="77173-138">Gibt den Betriebssystemstatus für das Bild eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="77173-138">Specifies the operating system state for virtual machine image</span></span>

<span data-ttu-id="77173-139">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="77173-139">Valid values are:</span></span>

- <span data-ttu-id="77173-140">Generalisierten</span><span class="sxs-lookup"><span data-stu-id="77173-140">Generalized</span></span>
- <span data-ttu-id="77173-141">Spezielle</span><span class="sxs-lookup"><span data-stu-id="77173-141">Specialized</span></span>

<span data-ttu-id="77173-142">Die Verwendung dieses Parameters gibt an, dass Sie beabsichtigen, das Bild des virtuellen Computers in Azure zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="77173-142">The use of this parameter indicates your intent to capture the virtual machine image to Azure.</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77173-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77173-143">CommonParameters</span></span>
<span data-ttu-id="77173-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77173-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77173-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77173-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77173-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77173-146">INPUTS</span></span>

## <span data-ttu-id="77173-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77173-147">OUTPUTS</span></span>

### <span data-ttu-id="77173-148">Microsoft. WindowsAzure. Commands. Servicemanagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="77173-148">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="77173-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="77173-149">NOTES</span></span>

## <span data-ttu-id="77173-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77173-150">RELATED LINKS</span></span>

[<span data-ttu-id="77173-151">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="77173-151">Remove-AzureVMImageOSDiskConfig</span></span>](./Remove-AzureVMImageOSDiskConfig.md)


