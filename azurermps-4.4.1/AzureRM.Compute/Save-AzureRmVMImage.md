---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: cadcaccc2bb93dee5298ca92561c5bef36b5d9ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505146"
---
# <span data-ttu-id="b7733-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="b7733-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="b7733-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7733-102">SYNOPSIS</span></span>
<span data-ttu-id="b7733-103">Speichert einen virtuellen Computer als VMImage.</span><span class="sxs-lookup"><span data-stu-id="b7733-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7733-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7733-104">SYNTAX</span></span>

### <span data-ttu-id="b7733-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b7733-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7733-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b7733-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7733-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7733-107">DESCRIPTION</span></span>
<span data-ttu-id="b7733-108">Das Cmdlet **Save-AzureRmVMImage** speichert einen virtuellen Computer als VMImage.</span><span class="sxs-lookup"><span data-stu-id="b7733-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="b7733-109">Bevor Sie ein Bild für einen virtuellen Computer erstellen, müssen Sie den virtuellen Computer Sysprep durchführen und dann mithilfe des Set-AzureRmVM-Cmdlets als generalisiert kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="b7733-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="b7733-110">Die Ausgabe dieses Cmdlets ist eine JSON-Vorlage (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="b7733-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="b7733-111">Sie können virtuelle Computer aus dem aufgenommenen Bild bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b7733-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="b7733-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7733-112">EXAMPLES</span></span>

### <span data-ttu-id="b7733-113">Beispiel 1: Aufzeichnen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="b7733-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="b7733-114">Der erste Befehl kennzeichnet den virtuellen Computer mit dem Namen "VirtualMachine07" als "generalisiert".</span><span class="sxs-lookup"><span data-stu-id="b7733-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="b7733-115">Der zweite Befehl zeichnet einen virtuellen Computer mit dem Namen "VirtualMachine07" als VMImage auf.</span><span class="sxs-lookup"><span data-stu-id="b7733-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="b7733-116">Die **Output** -Eigenschaft gibt eine JSON-Vorlage zurück.</span><span class="sxs-lookup"><span data-stu-id="b7733-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="b7733-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7733-117">PARAMETERS</span></span>

### <span data-ttu-id="b7733-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7733-118">-DefaultProfile</span></span>
<span data-ttu-id="b7733-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b7733-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7733-120">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="b7733-120">-DestinationContainerName</span></span>
<span data-ttu-id="b7733-121">Gibt den Namen eines Containers im Container "System" an, in dem die Bilder enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="b7733-121">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="b7733-122">Wenn der Container nicht vorhanden ist, wird er für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="b7733-122">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="b7733-123">Die virtuellen Festplatten (VHD), die die VMImage bilden, befinden sich in dem Container, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b7733-123">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="b7733-124">Wenn die virtuellen Festplatten über mehrere Speicherkonten verteilt sind, erstellt dieses Cmdlet einen Container mit diesem Namen in jedem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="b7733-124">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="b7733-125">Die URL des gespeicherten Bilds ähnelt:</span><span class="sxs-lookup"><span data-stu-id="b7733-125">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="b7733-126"> https:// \<storageAccountName\> . BLOB.Core.Windows.NET/System/Microsoft.Compute/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="b7733-126">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="b7733-127">-ID</span><span class="sxs-lookup"><span data-stu-id="b7733-127">-Id</span></span>
<span data-ttu-id="b7733-128">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="b7733-128">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="b7733-129">-Name</span><span class="sxs-lookup"><span data-stu-id="b7733-129">-Name</span></span>
<span data-ttu-id="b7733-130">Gibt einen Namen an.</span><span class="sxs-lookup"><span data-stu-id="b7733-130">Specifies a name.</span></span>

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

### <span data-ttu-id="b7733-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="b7733-131">-Overwrite</span></span>
<span data-ttu-id="b7733-132">Gibt an, dass mit diesem Cmdlet alle virtuellen Festplatten überschrieben werden, die das gleiche Präfix im Zielcontainer aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b7733-132">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="b7733-133">-Path</span><span class="sxs-lookup"><span data-stu-id="b7733-133">-Path</span></span>
<span data-ttu-id="b7733-134">Gibt den Pfad der VHD an.</span><span class="sxs-lookup"><span data-stu-id="b7733-134">Specifies the path of the VHD.</span></span>

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

### <span data-ttu-id="b7733-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7733-135">-ResourceGroupName</span></span>
<span data-ttu-id="b7733-136">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="b7733-136">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b7733-137">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="b7733-137">-VHDNamePrefix</span></span>
<span data-ttu-id="b7733-138">Gibt das Präfix im Namen der Blobs an, die das Speicherprofil des VMImage darstellen.</span><span class="sxs-lookup"><span data-stu-id="b7733-138">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="b7733-139">Beispielsweise führt ein Präfix vhdPrefix für einen Betriebssystemdatenträger zu dem Namen vhdPrefix- \<guid\> osdisk. VHD.</span><span class="sxs-lookup"><span data-stu-id="b7733-139">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="b7733-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7733-140">CommonParameters</span></span>
<span data-ttu-id="b7733-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7733-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7733-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7733-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7733-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7733-143">INPUTS</span></span>

## <span data-ttu-id="b7733-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7733-144">OUTPUTS</span></span>

## <span data-ttu-id="b7733-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7733-145">NOTES</span></span>

## <span data-ttu-id="b7733-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7733-146">RELATED LINKS</span></span>

[<span data-ttu-id="b7733-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="b7733-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="b7733-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="b7733-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="b7733-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="b7733-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="b7733-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="b7733-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="b7733-151">Satz-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b7733-151">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


