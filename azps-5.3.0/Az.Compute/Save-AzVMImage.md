---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: 0d2a4ade662ec23a4a139460bce8fe5387683120
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472977"
---
# <span data-ttu-id="9e481-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9e481-101">Save-AzVMImage</span></span>

## <span data-ttu-id="9e481-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e481-102">SYNOPSIS</span></span>
<span data-ttu-id="9e481-103">Speichert einen virtuellen Computer als VMImage.</span><span class="sxs-lookup"><span data-stu-id="9e481-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="9e481-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e481-104">SYNTAX</span></span>

### <span data-ttu-id="9e481-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e481-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e481-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9e481-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e481-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e481-107">DESCRIPTION</span></span>
<span data-ttu-id="9e481-108">Das **Cmdlet Save-AzVMImage** speichert einen virtuellen Computer als VMImage.</span><span class="sxs-lookup"><span data-stu-id="9e481-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="9e481-109">Bevor Sie ein Bild für einen virtuellen Computer erstellen, sollten Sie den virtuellen Computer sysprepieren und dann mit dem cmdlet Set-AzVM als generalisiert markieren.</span><span class="sxs-lookup"><span data-stu-id="9e481-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="9e481-110">Die Ausgabe dieses Cmdlets ist eine JavaScript Object Notation (JSON)-Vorlage.</span><span class="sxs-lookup"><span data-stu-id="9e481-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="9e481-111">Sie können virtuelle Computer aus dem aufgenommenen Bild bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9e481-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="9e481-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e481-112">EXAMPLES</span></span>

### <span data-ttu-id="9e481-113">Beispiel 1: Erfassen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="9e481-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="9e481-114">Der erste Befehl kennzeichnet den virtuellen Computer mit dem Namen "VirtualMachine07" als generalisiert.</span><span class="sxs-lookup"><span data-stu-id="9e481-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="9e481-115">Der zweite Befehl erfasst einen virtuellen Computer namens "VirtualMachine07" als VMImage.</span><span class="sxs-lookup"><span data-stu-id="9e481-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="9e481-116">Die **Eigenschaft "Output"** gibt eine JSON-Vorlage zurück.</span><span class="sxs-lookup"><span data-stu-id="9e481-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="9e481-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e481-117">PARAMETERS</span></span>

### <span data-ttu-id="9e481-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e481-118">-AsJob</span></span>
<span data-ttu-id="9e481-119">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="9e481-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9e481-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e481-120">-DefaultProfile</span></span>
<span data-ttu-id="9e481-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e481-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e481-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="9e481-122">-DestinationContainerName</span></span>
<span data-ttu-id="9e481-123">Gibt den Namen eines Containers innerhalb des "System"-Containers an, der die Bilder enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="9e481-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="9e481-124">Wenn der Container nicht vorhanden ist, wird er für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="9e481-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="9e481-125">Die virtuellen Festplatten (VHDs), die das VMImage bilden, befinden sich im Container, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9e481-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="9e481-126">Wenn die VHDs auf mehrere Speicherkonten verteilt sind, erstellt dieses Cmdlet einen Container mit diesem Namen in jedem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="9e481-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="9e481-127">Die URL des gespeicherten Bilds ähnelt: https:// \<storageAccountName\> .blob.core.windows.net/system/Microsoft.Compute/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> .xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span><span class="sxs-lookup"><span data-stu-id="9e481-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="9e481-128">-ID</span><span class="sxs-lookup"><span data-stu-id="9e481-128">-Id</span></span>
<span data-ttu-id="9e481-129">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="9e481-129">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="9e481-130">-Name</span><span class="sxs-lookup"><span data-stu-id="9e481-130">-Name</span></span>
<span data-ttu-id="9e481-131">Gibt einen Namen an.</span><span class="sxs-lookup"><span data-stu-id="9e481-131">Specifies a name.</span></span>

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

### <span data-ttu-id="9e481-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="9e481-132">-Overwrite</span></span>
<span data-ttu-id="9e481-133">Gibt an, dass dieses Cmdlet alle VHDs mit demselben Präfix im Zielcontainer überschreibt.</span><span class="sxs-lookup"><span data-stu-id="9e481-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="9e481-134">-Path</span><span class="sxs-lookup"><span data-stu-id="9e481-134">-Path</span></span>
<span data-ttu-id="9e481-135">Der Dateipfad, in dem die Vorlage des aufgenommenen Bilds gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="9e481-135">The file path in which the template of the captured image is stored.</span></span>

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

### <span data-ttu-id="9e481-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e481-136">-ResourceGroupName</span></span>
<span data-ttu-id="9e481-137">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="9e481-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9e481-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="9e481-138">-VHDNamePrefix</span></span>
<span data-ttu-id="9e481-139">Gibt das Präfix im Namen der BLOBS an, die das Speicherprofil des VMImage bilden.</span><span class="sxs-lookup"><span data-stu-id="9e481-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="9e481-140">Beispielsweise führt ein Präfix vhdPrefix für einen Betriebssystemdatenträger zum Namen "vhdPrefix-osdisk". \<guid\> vhd.</span><span class="sxs-lookup"><span data-stu-id="9e481-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="9e481-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e481-141">CommonParameters</span></span>
<span data-ttu-id="9e481-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e481-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e481-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e481-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e481-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e481-144">INPUTS</span></span>

### <span data-ttu-id="9e481-145">System.String</span><span class="sxs-lookup"><span data-stu-id="9e481-145">System.String</span></span>

### <span data-ttu-id="9e481-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9e481-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9e481-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e481-147">OUTPUTS</span></span>

### <span data-ttu-id="9e481-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="9e481-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="9e481-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9e481-149">NOTES</span></span>

## <span data-ttu-id="9e481-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9e481-150">RELATED LINKS</span></span>

[<span data-ttu-id="9e481-151">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9e481-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="9e481-152">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9e481-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="9e481-153">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9e481-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="9e481-154">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9e481-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="9e481-155">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e481-155">Set-AzVM</span></span>](./Set-AzVM.md)


