---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: b01f8d356d83cb111441cf911750056033422fe8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844315"
---
# <span data-ttu-id="a0514-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a0514-101">Save-AzVMImage</span></span>

## <span data-ttu-id="a0514-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0514-102">SYNOPSIS</span></span>
<span data-ttu-id="a0514-103">Speichert einen virtuellen Computer als VMImage.</span><span class="sxs-lookup"><span data-stu-id="a0514-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="a0514-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0514-104">SYNTAX</span></span>

### <span data-ttu-id="a0514-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0514-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0514-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a0514-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0514-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0514-107">DESCRIPTION</span></span>
<span data-ttu-id="a0514-108">Das Cmdlet **Save-AzVMImage** speichert einen virtuellen Computer als VMImage.</span><span class="sxs-lookup"><span data-stu-id="a0514-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="a0514-109">Bevor Sie ein Bild für einen virtuellen Computer erstellen, müssen Sie den virtuellen Computer Sysprep durchführen und dann mithilfe des Set-AzVM-Cmdlets als generalisiert kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="a0514-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>

<span data-ttu-id="a0514-110">Die Ausgabe dieses Cmdlets ist eine JSON-Vorlage (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="a0514-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="a0514-111">Sie können virtuelle Computer aus dem aufgenommenen Bild bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a0514-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="a0514-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0514-112">EXAMPLES</span></span>

### <span data-ttu-id="a0514-113">Beispiel 1: Aufzeichnen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="a0514-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="a0514-114">Der erste Befehl kennzeichnet den virtuellen Computer mit dem Namen "VirtualMachine07" als "generalisiert".</span><span class="sxs-lookup"><span data-stu-id="a0514-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="a0514-115">Der zweite Befehl zeichnet einen virtuellen Computer mit dem Namen "VirtualMachine07" als VMImage auf.</span><span class="sxs-lookup"><span data-stu-id="a0514-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="a0514-116">Die **Output** -Eigenschaft gibt eine JSON-Vorlage zurück.</span><span class="sxs-lookup"><span data-stu-id="a0514-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="a0514-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0514-117">PARAMETERS</span></span>

### <span data-ttu-id="a0514-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0514-118">-AsJob</span></span>
<span data-ttu-id="a0514-119">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="a0514-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a0514-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0514-120">-DefaultProfile</span></span>
<span data-ttu-id="a0514-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a0514-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0514-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="a0514-122">-DestinationContainerName</span></span>
<span data-ttu-id="a0514-123">Gibt den Namen eines Containers im Container "System" an, in dem die Bilder enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="a0514-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="a0514-124">Wenn der Container nicht vorhanden ist, wird er für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="a0514-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="a0514-125">Die virtuellen Festplatten (VHD), die die VMImage bilden, befinden sich in dem Container, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a0514-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="a0514-126">Wenn die virtuellen Festplatten über mehrere Speicherkonten verteilt sind, erstellt dieses Cmdlet einen Container mit diesem Namen in jedem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="a0514-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="a0514-127">Die URL des gespeicherten Bilds ähnelt:</span><span class="sxs-lookup"><span data-stu-id="a0514-127">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="a0514-128"> https:// \< storageAccountName \> . BLOB.Core.Windows.NET/System/Microsoft.Compute/Images/ \< imagesContainer \> / \< vhdPrefix-osDisk \> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="a0514-128">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="a0514-129">-ID</span><span class="sxs-lookup"><span data-stu-id="a0514-129">-Id</span></span>
<span data-ttu-id="a0514-130">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="a0514-130">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="a0514-131">-Name</span><span class="sxs-lookup"><span data-stu-id="a0514-131">-Name</span></span>
<span data-ttu-id="a0514-132">Gibt einen Namen an.</span><span class="sxs-lookup"><span data-stu-id="a0514-132">Specifies a name.</span></span>

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

### <span data-ttu-id="a0514-133">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="a0514-133">-Overwrite</span></span>
<span data-ttu-id="a0514-134">Gibt an, dass mit diesem Cmdlet alle virtuellen Festplatten überschrieben werden, die das gleiche Präfix im Zielcontainer aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a0514-134">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="a0514-135">-Path</span><span class="sxs-lookup"><span data-stu-id="a0514-135">-Path</span></span>
<span data-ttu-id="a0514-136">Gibt den Pfad der VHD an.</span><span class="sxs-lookup"><span data-stu-id="a0514-136">Specifies the path of the VHD.</span></span>

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

### <span data-ttu-id="a0514-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0514-137">-ResourceGroupName</span></span>
<span data-ttu-id="a0514-138">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="a0514-138">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a0514-139">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="a0514-139">-VHDNamePrefix</span></span>
<span data-ttu-id="a0514-140">Gibt das Präfix im Namen der Blobs an, die das Speicherprofil des VMImage darstellen.</span><span class="sxs-lookup"><span data-stu-id="a0514-140">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="a0514-141">Beispielsweise führt ein Präfix vhdPrefix für einen Betriebssystemdatenträger zu dem Namen vhdPrefix-osdisk. \< GUID \> . vhd.</span><span class="sxs-lookup"><span data-stu-id="a0514-141">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="a0514-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0514-142">CommonParameters</span></span>
<span data-ttu-id="a0514-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0514-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0514-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0514-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0514-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0514-145">INPUTS</span></span>

### <span data-ttu-id="a0514-146">Keine</span><span class="sxs-lookup"><span data-stu-id="a0514-146">None</span></span>
<span data-ttu-id="a0514-147">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a0514-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0514-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0514-148">OUTPUTS</span></span>

### <span data-ttu-id="a0514-149">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="a0514-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="a0514-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0514-150">NOTES</span></span>

## <span data-ttu-id="a0514-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0514-151">RELATED LINKS</span></span>

[<span data-ttu-id="a0514-152">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a0514-152">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="a0514-153">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="a0514-153">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="a0514-154">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a0514-154">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="a0514-155">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="a0514-155">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="a0514-156">Satz-AzVM</span><span class="sxs-lookup"><span data-stu-id="a0514-156">Set-AzVM</span></span>](./Set-AzVM.md)


