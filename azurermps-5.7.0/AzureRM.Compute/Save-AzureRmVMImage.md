---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: 8f3aebe1e9e79423d7251fa79084d6fa85407b9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503833"
---
# <span data-ttu-id="20c55-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="20c55-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="20c55-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20c55-102">SYNOPSIS</span></span>
<span data-ttu-id="20c55-103">Speichert einen virtuellen Computer als VMImage.</span><span class="sxs-lookup"><span data-stu-id="20c55-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20c55-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20c55-104">SYNTAX</span></span>

### <span data-ttu-id="20c55-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="20c55-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [<CommonParameters>]
```

### <span data-ttu-id="20c55-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="20c55-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [<CommonParameters>]
```

## <span data-ttu-id="20c55-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20c55-107">DESCRIPTION</span></span>
<span data-ttu-id="20c55-108">Das Cmdlet **Save-AzureRmVMImage** speichert einen virtuellen Computer als VMImage.</span><span class="sxs-lookup"><span data-stu-id="20c55-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="20c55-109">Bevor Sie ein Bild für einen virtuellen Computer erstellen, müssen Sie den virtuellen Computer Sysprep durchführen und dann mithilfe des Set-AzureRmVM-Cmdlets als generalisiert kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="20c55-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="20c55-110">Die Ausgabe dieses Cmdlets ist eine JSON-Vorlage (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="20c55-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="20c55-111">Sie können virtuelle Computer aus dem aufgenommenen Bild bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="20c55-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="20c55-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20c55-112">EXAMPLES</span></span>

### <span data-ttu-id="20c55-113">Beispiel 1: Aufzeichnen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="20c55-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="20c55-114">Der erste Befehl kennzeichnet den virtuellen Computer mit dem Namen "VirtualMachine07" als "generalisiert".</span><span class="sxs-lookup"><span data-stu-id="20c55-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="20c55-115">Der zweite Befehl zeichnet einen virtuellen Computer mit dem Namen "VirtualMachine07" als VMImage auf.</span><span class="sxs-lookup"><span data-stu-id="20c55-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="20c55-116">Die **Output** -Eigenschaft gibt eine JSON-Vorlage zurück.</span><span class="sxs-lookup"><span data-stu-id="20c55-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="20c55-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="20c55-117">PARAMETERS</span></span>

### <span data-ttu-id="20c55-118">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="20c55-118">-DestinationContainerName</span></span>
<span data-ttu-id="20c55-119">Gibt den Namen eines Containers im Container "System" an, in dem die Bilder enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="20c55-119">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="20c55-120">Wenn der Container nicht vorhanden ist, wird er für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="20c55-120">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="20c55-121">Die virtuellen Festplatten (VHD), die die VMImage bilden, befinden sich in dem Container, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="20c55-121">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="20c55-122">Wenn die virtuellen Festplatten über mehrere Speicherkonten verteilt sind, erstellt dieses Cmdlet einen Container mit diesem Namen in jedem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="20c55-122">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="20c55-123">Die URL des gespeicherten Bilds ähnelt:</span><span class="sxs-lookup"><span data-stu-id="20c55-123">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="20c55-124"> https:// \<storageAccountName\> . BLOB.Core.Windows.NET/System/Microsoft.Compute/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="20c55-124">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20c55-125">-ID</span><span class="sxs-lookup"><span data-stu-id="20c55-125">-Id</span></span>
<span data-ttu-id="20c55-126">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="20c55-126">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20c55-127">-Name</span><span class="sxs-lookup"><span data-stu-id="20c55-127">-Name</span></span>
<span data-ttu-id="20c55-128">Gibt einen Namen an.</span><span class="sxs-lookup"><span data-stu-id="20c55-128">Specifies a name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20c55-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="20c55-129">-Overwrite</span></span>
<span data-ttu-id="20c55-130">Gibt an, dass mit diesem Cmdlet alle virtuellen Festplatten überschrieben werden, die das gleiche Präfix im Zielcontainer aufweisen.</span><span class="sxs-lookup"><span data-stu-id="20c55-130">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20c55-131">-Path</span><span class="sxs-lookup"><span data-stu-id="20c55-131">-Path</span></span>
<span data-ttu-id="20c55-132">Gibt den Pfad der VHD an.</span><span class="sxs-lookup"><span data-stu-id="20c55-132">Specifies the path of the VHD.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20c55-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20c55-133">-ResourceGroupName</span></span>
<span data-ttu-id="20c55-134">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="20c55-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20c55-135">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="20c55-135">-VHDNamePrefix</span></span>
<span data-ttu-id="20c55-136">Gibt das Präfix im Namen der Blobs an, die das Speicherprofil des VMImage darstellen.</span><span class="sxs-lookup"><span data-stu-id="20c55-136">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="20c55-137">Beispielsweise führt ein Präfix vhdPrefix für einen Betriebssystemdatenträger zu dem Namen vhdPrefix- \<guid\> osdisk. VHD.</span><span class="sxs-lookup"><span data-stu-id="20c55-137">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20c55-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c55-138">CommonParameters</span></span>
<span data-ttu-id="20c55-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20c55-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c55-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20c55-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c55-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20c55-141">INPUTS</span></span>

### <span data-ttu-id="20c55-142">Keine</span><span class="sxs-lookup"><span data-stu-id="20c55-142">None</span></span>
<span data-ttu-id="20c55-143">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="20c55-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="20c55-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20c55-144">OUTPUTS</span></span>

## <span data-ttu-id="20c55-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="20c55-145">NOTES</span></span>

## <span data-ttu-id="20c55-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20c55-146">RELATED LINKS</span></span>

[<span data-ttu-id="20c55-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="20c55-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="20c55-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="20c55-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="20c55-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="20c55-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="20c55-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="20c55-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="20c55-151">Satz-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="20c55-151">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


