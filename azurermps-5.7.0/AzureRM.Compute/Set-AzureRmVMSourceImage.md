---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
ms.openlocfilehash: d96d583f871e0d037c72018339d44952562bac35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478562"
---
# <span data-ttu-id="43c67-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="43c67-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="43c67-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43c67-102">SYNOPSIS</span></span>
<span data-ttu-id="43c67-103">Gibt das Bild für einen virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="43c67-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43c67-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43c67-104">SYNTAX</span></span>

### <span data-ttu-id="43c67-105">ImageReferenceSkuParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="43c67-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [<CommonParameters>]
```

### <span data-ttu-id="43c67-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43c67-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [<CommonParameters>]
```

## <span data-ttu-id="43c67-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43c67-107">DESCRIPTION</span></span>
<span data-ttu-id="43c67-108">Das Cmdlet " **Satz-AzureRmVMSourceImage** " gibt das Platt Form Bild an, das für einen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43c67-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="43c67-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43c67-109">EXAMPLES</span></span>

### <span data-ttu-id="43c67-110">Beispiel 1: Setzen von Werten für ein Bild</span><span class="sxs-lookup"><span data-stu-id="43c67-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="43c67-111">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="43c67-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="43c67-112">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="43c67-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="43c67-113">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="43c67-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="43c67-114">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="43c67-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="43c67-115">Der endgültige Befehl legt Werte für den Herausgebernamen, das Angebot, die SKU und die Version fest.</span><span class="sxs-lookup"><span data-stu-id="43c67-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="43c67-116">Die Cmdlets **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** und **Get-AzureRmVMImage** können diese Einstellungen ermitteln.</span><span class="sxs-lookup"><span data-stu-id="43c67-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="43c67-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="43c67-117">PARAMETERS</span></span>

### <span data-ttu-id="43c67-118">-ID</span><span class="sxs-lookup"><span data-stu-id="43c67-118">-Id</span></span>
<span data-ttu-id="43c67-119">Gibt die ID an.</span><span class="sxs-lookup"><span data-stu-id="43c67-119">Specifies the ID.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceIdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c67-120">-Angebot</span><span class="sxs-lookup"><span data-stu-id="43c67-120">-Offer</span></span>
<span data-ttu-id="43c67-121">Gibt den Typ des VMImage-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="43c67-121">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="43c67-122">Verwenden Sie das Get-AzureRmVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="43c67-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c67-123">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="43c67-123">-PublisherName</span></span>
<span data-ttu-id="43c67-124">Gibt den Namen des Herausgebers eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="43c67-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="43c67-125">Verwenden Sie zum Abrufen eines Verlegers das Get-AzureRmVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43c67-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c67-126">-SKUs</span><span class="sxs-lookup"><span data-stu-id="43c67-126">-Skus</span></span>
<span data-ttu-id="43c67-127">Gibt eine VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="43c67-127">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="43c67-128">Verwenden Sie zum Abrufen von SKUs das Get-AzureRmVMImageSku-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43c67-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c67-129">-Version</span><span class="sxs-lookup"><span data-stu-id="43c67-129">-Version</span></span>
<span data-ttu-id="43c67-130">Gibt eine Version eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="43c67-130">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="43c67-131">Wenn Sie die neueste Version verwenden möchten, geben Sie einen Wert von Latest anstelle einer bestimmten Version an.</span><span class="sxs-lookup"><span data-stu-id="43c67-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c67-132">-VM</span><span class="sxs-lookup"><span data-stu-id="43c67-132">-VM</span></span>
<span data-ttu-id="43c67-133">Gibt das zu konfigurierende Objekt des lokalen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="43c67-133">Specifies the local virtual machine object to configure.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43c67-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c67-134">CommonParameters</span></span>
<span data-ttu-id="43c67-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43c67-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c67-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43c67-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c67-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43c67-137">INPUTS</span></span>

### <span data-ttu-id="43c67-138">Keine</span><span class="sxs-lookup"><span data-stu-id="43c67-138">None</span></span>
<span data-ttu-id="43c67-139">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="43c67-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43c67-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43c67-140">OUTPUTS</span></span>

## <span data-ttu-id="43c67-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="43c67-141">NOTES</span></span>

## <span data-ttu-id="43c67-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43c67-142">RELATED LINKS</span></span>

[<span data-ttu-id="43c67-143">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="43c67-143">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="43c67-144">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="43c67-144">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="43c67-145">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="43c67-145">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="43c67-146">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="43c67-146">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="43c67-147">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="43c67-147">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="43c67-148">Neu – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="43c67-148">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


