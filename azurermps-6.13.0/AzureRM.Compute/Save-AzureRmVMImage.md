---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: b6d8d21eea863683912e204403ebe5a75ac40fc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476189"
---
# <span data-ttu-id="f4d18-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f4d18-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="f4d18-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4d18-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d18-103">Speichert einen virtuellen Computer als VMImage.</span><span class="sxs-lookup"><span data-stu-id="f4d18-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4d18-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4d18-104">SYNTAX</span></span>

### <span data-ttu-id="f4d18-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4d18-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4d18-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f4d18-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4d18-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4d18-107">DESCRIPTION</span></span>
<span data-ttu-id="f4d18-108">Das Cmdlet **Save-AzureRmVMImage** speichert einen virtuellen Computer als VMImage.</span><span class="sxs-lookup"><span data-stu-id="f4d18-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="f4d18-109">Bevor Sie ein Bild für einen virtuellen Computer erstellen, müssen Sie den virtuellen Computer Sysprep durchführen und dann mithilfe des Set-AzureRmVM-Cmdlets als generalisiert kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="f4d18-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="f4d18-110">Die Ausgabe dieses Cmdlets ist eine JSON-Vorlage (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="f4d18-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="f4d18-111">Sie können virtuelle Computer aus dem aufgenommenen Bild bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f4d18-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="f4d18-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4d18-112">EXAMPLES</span></span>

### <span data-ttu-id="f4d18-113">Beispiel 1: Aufzeichnen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="f4d18-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="f4d18-114">Der erste Befehl kennzeichnet den virtuellen Computer mit dem Namen "VirtualMachine07" als "generalisiert".</span><span class="sxs-lookup"><span data-stu-id="f4d18-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="f4d18-115">Der zweite Befehl zeichnet einen virtuellen Computer mit dem Namen "VirtualMachine07" als VMImage auf.</span><span class="sxs-lookup"><span data-stu-id="f4d18-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="f4d18-116">Die **Output** -Eigenschaft gibt eine JSON-Vorlage zurück.</span><span class="sxs-lookup"><span data-stu-id="f4d18-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="f4d18-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4d18-117">PARAMETERS</span></span>

### <span data-ttu-id="f4d18-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4d18-118">-AsJob</span></span>
<span data-ttu-id="f4d18-119">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="f4d18-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f4d18-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d18-120">-DefaultProfile</span></span>
<span data-ttu-id="f4d18-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4d18-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d18-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="f4d18-122">-DestinationContainerName</span></span>
<span data-ttu-id="f4d18-123">Gibt den Namen eines Containers im Container "System" an, in dem die Bilder enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="f4d18-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="f4d18-124">Wenn der Container nicht vorhanden ist, wird er für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="f4d18-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="f4d18-125">Die virtuellen Festplatten (VHD), die die VMImage bilden, befinden sich in dem Container, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f4d18-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="f4d18-126">Wenn die virtuellen Festplatten über mehrere Speicherkonten verteilt sind, erstellt dieses Cmdlet einen Container mit diesem Namen in jedem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="f4d18-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="f4d18-127">Die URL des gespeicherten Bilds ähnelt: https:// \<storageAccountName\> . BLOB.Core.Windows.NET/System/Microsoft.Compute/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="f4d18-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="f4d18-128">-ID</span><span class="sxs-lookup"><span data-stu-id="f4d18-128">-Id</span></span>
<span data-ttu-id="f4d18-129">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="f4d18-129">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="f4d18-130">-Name</span><span class="sxs-lookup"><span data-stu-id="f4d18-130">-Name</span></span>
<span data-ttu-id="f4d18-131">Gibt einen Namen an.</span><span class="sxs-lookup"><span data-stu-id="f4d18-131">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d18-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f4d18-132">-Overwrite</span></span>
<span data-ttu-id="f4d18-133">Gibt an, dass mit diesem Cmdlet alle virtuellen Festplatten überschrieben werden, die das gleiche Präfix im Zielcontainer aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f4d18-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="f4d18-134">-Path</span><span class="sxs-lookup"><span data-stu-id="f4d18-134">-Path</span></span>
<span data-ttu-id="f4d18-135">Der Dateipfad, in dem die Vorlage des aufgenommenen Bilds gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f4d18-135">The file path in which the template of the captured image is stored.</span></span>

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

### <span data-ttu-id="f4d18-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d18-136">-ResourceGroupName</span></span>
<span data-ttu-id="f4d18-137">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="f4d18-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f4d18-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="f4d18-138">-VHDNamePrefix</span></span>
<span data-ttu-id="f4d18-139">Gibt das Präfix im Namen der Blobs an, die das Speicherprofil des VMImage darstellen.</span><span class="sxs-lookup"><span data-stu-id="f4d18-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="f4d18-140">Beispielsweise führt ein Präfix vhdPrefix für einen Betriebssystemdatenträger zu dem Namen vhdPrefix- \<guid\> osdisk. VHD.</span><span class="sxs-lookup"><span data-stu-id="f4d18-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="f4d18-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d18-141">CommonParameters</span></span>
<span data-ttu-id="f4d18-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4d18-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d18-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4d18-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d18-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4d18-144">INPUTS</span></span>

### <span data-ttu-id="f4d18-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f4d18-145">System.String</span></span>

### <span data-ttu-id="f4d18-146">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="f4d18-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f4d18-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4d18-147">OUTPUTS</span></span>

### <span data-ttu-id="f4d18-148">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="f4d18-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="f4d18-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4d18-149">NOTES</span></span>

## <span data-ttu-id="f4d18-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4d18-150">RELATED LINKS</span></span>

[<span data-ttu-id="f4d18-151">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f4d18-151">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="f4d18-152">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f4d18-152">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="f4d18-153">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f4d18-153">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="f4d18-154">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f4d18-154">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="f4d18-155">Satz-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f4d18-155">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


