---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: b663087437097b3e059f9d88c7720696222134e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820575"
---
# <span data-ttu-id="0c3dd-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0c3dd-101">Save-AzVMImage</span></span>

## <span data-ttu-id="0c3dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3dd-103">Speichert einen virtuellen Computer als VMImage.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="0c3dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c3dd-104">SYNTAX</span></span>

### <span data-ttu-id="0c3dd-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0c3dd-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c3dd-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="0c3dd-106">IdParameterSetName</span></span>
```
Save-AzVMImage [[-Name] <String>] [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c3dd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c3dd-107">DESCRIPTION</span></span>
<span data-ttu-id="0c3dd-108">Das Cmdlet **Save-AzVMImage** speichert einen virtuellen Computer als VMImage.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="0c3dd-109">Bevor Sie ein Bild für einen virtuellen Computer erstellen, müssen Sie den virtuellen Computer Sysprep durchführen und dann mithilfe des Set-AzVM-Cmdlets als generalisiert kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="0c3dd-110">Die Ausgabe dieses Cmdlets ist eine JSON-Vorlage (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="0c3dd-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="0c3dd-111">Sie können virtuelle Computer aus dem aufgenommenen Bild bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="0c3dd-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c3dd-112">EXAMPLES</span></span>

### <span data-ttu-id="0c3dd-113">Beispiel 1: Aufzeichnen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="0c3dd-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="0c3dd-114">Der erste Befehl kennzeichnet den virtuellen Computer mit dem Namen "VirtualMachine07" als "generalisiert".</span><span class="sxs-lookup"><span data-stu-id="0c3dd-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="0c3dd-115">Der zweite Befehl zeichnet einen virtuellen Computer mit dem Namen "VirtualMachine07" als VMImage auf.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="0c3dd-116">Die **Output** -Eigenschaft gibt eine JSON-Vorlage zurück.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="0c3dd-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c3dd-117">PARAMETERS</span></span>

### <span data-ttu-id="0c3dd-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c3dd-118">-AsJob</span></span>
<span data-ttu-id="0c3dd-119">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-119">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3dd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3dd-120">-DefaultProfile</span></span>
<span data-ttu-id="0c3dd-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3dd-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="0c3dd-122">-DestinationContainerName</span></span>
<span data-ttu-id="0c3dd-123">Gibt den Namen eines Containers im Container "System" an, in dem die Bilder enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="0c3dd-124">Wenn der Container nicht vorhanden ist, wird er für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="0c3dd-125">Die virtuellen Festplatten (VHD), die die VMImage bilden, befinden sich in dem Container, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="0c3dd-126">Wenn die virtuellen Festplatten über mehrere Speicherkonten verteilt sind, erstellt dieses Cmdlet einen Container mit diesem Namen in jedem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="0c3dd-127">Die URL des gespeicherten Bilds ähnelt: https:// \< storageAccountName \> . BLOB.Core.Windows.NET/System/Microsoft.Compute/Images/ \< imagesContainer \> / \< vhdPrefix-osDisk \> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3dd-128">-ID</span><span class="sxs-lookup"><span data-stu-id="0c3dd-128">-Id</span></span>
<span data-ttu-id="0c3dd-129">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-129">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3dd-130">-Name</span><span class="sxs-lookup"><span data-stu-id="0c3dd-130">-Name</span></span>
<span data-ttu-id="0c3dd-131">Gibt einen Namen an.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-131">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3dd-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="0c3dd-132">-Overwrite</span></span>
<span data-ttu-id="0c3dd-133">Gibt an, dass mit diesem Cmdlet alle virtuellen Festplatten überschrieben werden, die das gleiche Präfix im Zielcontainer aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3dd-134">-Path</span><span class="sxs-lookup"><span data-stu-id="0c3dd-134">-Path</span></span>
<span data-ttu-id="0c3dd-135">Der Dateipfad, in dem die Vorlage des aufgenommenen Bilds gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-135">The file path in which the template of the captured image is stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3dd-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c3dd-136">-ResourceGroupName</span></span>
<span data-ttu-id="0c3dd-137">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3dd-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="0c3dd-138">-VHDNamePrefix</span></span>
<span data-ttu-id="0c3dd-139">Gibt das Präfix im Namen der Blobs an, die das Speicherprofil des VMImage darstellen.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="0c3dd-140">Beispielsweise führt ein Präfix vhdPrefix für einen Betriebssystemdatenträger zu dem Namen vhdPrefix-osdisk. \< GUID \> . vhd.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3dd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3dd-141">CommonParameters</span></span>
<span data-ttu-id="0c3dd-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c3dd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3dd-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c3dd-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3dd-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c3dd-144">INPUTS</span></span>

### <span data-ttu-id="0c3dd-145">System. String</span><span class="sxs-lookup"><span data-stu-id="0c3dd-145">System.String</span></span>

### <span data-ttu-id="0c3dd-146">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="0c3dd-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0c3dd-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c3dd-147">OUTPUTS</span></span>

### <span data-ttu-id="0c3dd-148">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="0c3dd-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="0c3dd-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c3dd-149">NOTES</span></span>

## <span data-ttu-id="0c3dd-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c3dd-150">RELATED LINKS</span></span>

[<span data-ttu-id="0c3dd-151">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0c3dd-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="0c3dd-152">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="0c3dd-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="0c3dd-153">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="0c3dd-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="0c3dd-154">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="0c3dd-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="0c3dd-155">Satz-AzVM</span><span class="sxs-lookup"><span data-stu-id="0c3dd-155">Set-AzVM</span></span>](./Set-AzVM.md)


