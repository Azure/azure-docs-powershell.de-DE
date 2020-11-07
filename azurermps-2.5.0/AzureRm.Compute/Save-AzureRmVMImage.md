---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvmimage
schema: 2.0.0
ms.openlocfilehash: b781023b424dd23d3d0874893b724744ecb33bda
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850908"
---
# <span data-ttu-id="c6304-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c6304-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="c6304-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6304-102">SYNOPSIS</span></span>
<span data-ttu-id="c6304-103">Speichert einen virtuellen Computer als VMImage.</span><span class="sxs-lookup"><span data-stu-id="c6304-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6304-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6304-104">SYNTAX</span></span>

### <span data-ttu-id="c6304-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c6304-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6304-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c6304-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6304-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6304-107">DESCRIPTION</span></span>
<span data-ttu-id="c6304-108">Das Cmdlet **Save-AzureRmVMImage** speichert einen virtuellen Computer als VMImage.</span><span class="sxs-lookup"><span data-stu-id="c6304-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="c6304-109">Bevor Sie ein Bild für einen virtuellen Computer erstellen, müssen Sie den virtuellen Computer Sysprep durchführen und dann mithilfe des Set-AzureRmVM-Cmdlets als generalisiert kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="c6304-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="c6304-110">Die Ausgabe dieses Cmdlets ist eine JSON-Vorlage (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="c6304-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="c6304-111">Sie können virtuelle Computer aus dem aufgenommenen Bild bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c6304-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="c6304-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6304-112">EXAMPLES</span></span>

### <span data-ttu-id="c6304-113">Beispiel 1: Aufzeichnen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="c6304-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="c6304-114">Der erste Befehl kennzeichnet den virtuellen Computer mit dem Namen "VirtualMachine07" als "generalisiert".</span><span class="sxs-lookup"><span data-stu-id="c6304-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="c6304-115">Der zweite Befehl zeichnet einen virtuellen Computer mit dem Namen "VirtualMachine07" als VMImage auf.</span><span class="sxs-lookup"><span data-stu-id="c6304-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="c6304-116">Die **Output** -Eigenschaft gibt eine JSON-Vorlage zurück.</span><span class="sxs-lookup"><span data-stu-id="c6304-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="c6304-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6304-117">PARAMETERS</span></span>

### <span data-ttu-id="c6304-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6304-118">-AsJob</span></span>
<span data-ttu-id="c6304-119">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="c6304-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c6304-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6304-120">-DefaultProfile</span></span>
<span data-ttu-id="c6304-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c6304-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6304-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="c6304-122">-DestinationContainerName</span></span>
<span data-ttu-id="c6304-123">Gibt den Namen eines Containers im Container "System" an, in dem die Bilder enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="c6304-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="c6304-124">Wenn der Container nicht vorhanden ist, wird er für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="c6304-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="c6304-125">Die virtuellen Festplatten (VHD), die die VMImage bilden, befinden sich in dem Container, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c6304-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="c6304-126">Wenn die virtuellen Festplatten über mehrere Speicherkonten verteilt sind, erstellt dieses Cmdlet einen Container mit diesem Namen in jedem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="c6304-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="c6304-127">Die URL des gespeicherten Bilds ähnelt:</span><span class="sxs-lookup"><span data-stu-id="c6304-127">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="c6304-128"> https:// \<storageAccountName\> . BLOB.Core.Windows.NET/System/Microsoft.Compute/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="c6304-128">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="c6304-129">-ID</span><span class="sxs-lookup"><span data-stu-id="c6304-129">-Id</span></span>
<span data-ttu-id="c6304-130">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="c6304-130">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="c6304-131">-Name</span><span class="sxs-lookup"><span data-stu-id="c6304-131">-Name</span></span>
<span data-ttu-id="c6304-132">Gibt einen Namen an.</span><span class="sxs-lookup"><span data-stu-id="c6304-132">Specifies a name.</span></span>

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

### <span data-ttu-id="c6304-133">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="c6304-133">-Overwrite</span></span>
<span data-ttu-id="c6304-134">Gibt an, dass mit diesem Cmdlet alle virtuellen Festplatten überschrieben werden, die das gleiche Präfix im Zielcontainer aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c6304-134">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="c6304-135">-Path</span><span class="sxs-lookup"><span data-stu-id="c6304-135">-Path</span></span>
<span data-ttu-id="c6304-136">Gibt den Pfad der VHD an.</span><span class="sxs-lookup"><span data-stu-id="c6304-136">Specifies the path of the VHD.</span></span>

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

### <span data-ttu-id="c6304-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6304-137">-ResourceGroupName</span></span>
<span data-ttu-id="c6304-138">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="c6304-138">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c6304-139">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="c6304-139">-VHDNamePrefix</span></span>
<span data-ttu-id="c6304-140">Gibt das Präfix im Namen der Blobs an, die das Speicherprofil des VMImage darstellen.</span><span class="sxs-lookup"><span data-stu-id="c6304-140">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="c6304-141">Beispielsweise führt ein Präfix vhdPrefix für einen Betriebssystemdatenträger zu dem Namen vhdPrefix- \<guid\> osdisk. VHD.</span><span class="sxs-lookup"><span data-stu-id="c6304-141">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="c6304-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6304-142">CommonParameters</span></span>
<span data-ttu-id="c6304-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6304-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6304-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6304-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6304-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6304-145">INPUTS</span></span>

### <span data-ttu-id="c6304-146">Keine</span><span class="sxs-lookup"><span data-stu-id="c6304-146">None</span></span>
<span data-ttu-id="c6304-147">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c6304-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c6304-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6304-148">OUTPUTS</span></span>

### <span data-ttu-id="c6304-149">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="c6304-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="c6304-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6304-150">NOTES</span></span>

## <span data-ttu-id="c6304-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6304-151">RELATED LINKS</span></span>

[<span data-ttu-id="c6304-152">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c6304-152">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="c6304-153">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="c6304-153">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="c6304-154">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c6304-154">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="c6304-155">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="c6304-155">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="c6304-156">Satz-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c6304-156">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


