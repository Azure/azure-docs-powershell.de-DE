---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: a1ed1fa266638891507b6853199bff23d23aa1b3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294862"
---
# <span data-ttu-id="38527-101">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="38527-101">Set-AzVMSourceImage</span></span>

## <span data-ttu-id="38527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38527-102">SYNOPSIS</span></span>
<span data-ttu-id="38527-103">Gibt das Bild für einen virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="38527-103">Specifies the image for a virtual machine.</span></span>

## <span data-ttu-id="38527-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38527-104">SYNTAX</span></span>

### <span data-ttu-id="38527-105">ImageReferenceSkuParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="38527-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38527-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38527-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38527-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38527-107">DESCRIPTION</span></span>
<span data-ttu-id="38527-108">Das **Cmdlet "Set-AzVMSourceImage"** gibt das Plattformbild an, das für einen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="38527-108">The **Set-AzVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="38527-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38527-109">EXAMPLES</span></span>

### <span data-ttu-id="38527-110">Beispiel 1: Festlegen von Werten für ein Bild</span><span class="sxs-lookup"><span data-stu-id="38527-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="38527-111">Der erste Befehl ruft den Verfügbarkeitssatz namens "AvailabilitySet03" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $AvailabilitySet Variable.</span><span class="sxs-lookup"><span data-stu-id="38527-111">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="38527-112">Der zweite Befehl erstellt ein Objekt des virtuellen Computers und speichert es dann in der $VirtualMachine Variable.</span><span class="sxs-lookup"><span data-stu-id="38527-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="38527-113">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="38527-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="38527-114">Der virtuelle Computer gehört zu dem Verfügbarkeitssatz, der auf der $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="38527-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="38527-115">Der endgültige Befehl legt Werte für den Herausgebernamen, das Angebot, die SKU und die Version fest.</span><span class="sxs-lookup"><span data-stu-id="38527-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="38527-116">Die **Cmdlets "Get-AzVMImagePublisher",** **"Get-AzVMImageOffer",** **"Get-AzVMImageSku"** und **"Get-AzVMImage"** können diese Einstellungen ermitteln.</span><span class="sxs-lookup"><span data-stu-id="38527-116">The **Get-AzVMImagePublisher**, **Get-AzVMImageOffer**, **Get-AzVMImageSku**, and **Get-AzVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="38527-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38527-117">PARAMETERS</span></span>

### <span data-ttu-id="38527-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38527-118">-DefaultProfile</span></span>
<span data-ttu-id="38527-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38527-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38527-120">-ID</span><span class="sxs-lookup"><span data-stu-id="38527-120">-Id</span></span>
<span data-ttu-id="38527-121">Gibt die ID an.</span><span class="sxs-lookup"><span data-stu-id="38527-121">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38527-122">-Offer</span><span class="sxs-lookup"><span data-stu-id="38527-122">-Offer</span></span>
<span data-ttu-id="38527-123">Gibt den Typ des Angebots "VMImage" an.</span><span class="sxs-lookup"><span data-stu-id="38527-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="38527-124">Um ein Bildangebot zu erhalten, verwenden Sie das Get-AzVMImageOffer Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38527-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38527-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="38527-125">-PublisherName</span></span>
<span data-ttu-id="38527-126">Gibt den Namen eines Herausgebers eines VMImages an.</span><span class="sxs-lookup"><span data-stu-id="38527-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="38527-127">Verwenden Sie zum Abrufen eines Herausgebers das Get-AzVMImagePublisher Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38527-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38527-128">-SKUS</span><span class="sxs-lookup"><span data-stu-id="38527-128">-Skus</span></span>
<span data-ttu-id="38527-129">Gibt eine VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="38527-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="38527-130">Verwenden Sie zum Abrufen von SKUs das Get-AzVMImageSku Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38527-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38527-131">-Version</span><span class="sxs-lookup"><span data-stu-id="38527-131">-Version</span></span>
<span data-ttu-id="38527-132">Gibt eine Version eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="38527-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="38527-133">Wenn Sie die neueste Version verwenden möchten, geben Sie den Wert "Neueste Version" anstelle einer bestimmten Version an.</span><span class="sxs-lookup"><span data-stu-id="38527-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38527-134">-VM</span><span class="sxs-lookup"><span data-stu-id="38527-134">-VM</span></span>
<span data-ttu-id="38527-135">Gibt das zu konfigurierende Objekt des lokalen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="38527-135">Specifies the local virtual machine object to configure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38527-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38527-136">CommonParameters</span></span>
<span data-ttu-id="38527-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38527-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38527-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38527-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38527-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38527-139">INPUTS</span></span>

### <span data-ttu-id="38527-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="38527-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="38527-141">System.String</span><span class="sxs-lookup"><span data-stu-id="38527-141">System.String</span></span>

## <span data-ttu-id="38527-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38527-142">OUTPUTS</span></span>

### <span data-ttu-id="38527-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="38527-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="38527-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="38527-144">NOTES</span></span>

## <span data-ttu-id="38527-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="38527-145">RELATED LINKS</span></span>

[<span data-ttu-id="38527-146">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="38527-146">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="38527-147">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="38527-147">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="38527-148">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="38527-148">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="38527-149">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="38527-149">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="38527-150">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="38527-150">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="38527-151">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="38527-151">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


