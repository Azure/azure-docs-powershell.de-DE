---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMSourceImage.md
ms.openlocfilehash: c164d352256f84ea18c09b775c9a9639dbde7866
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496293"
---
# <span data-ttu-id="e3896-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="e3896-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="e3896-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3896-102">SYNOPSIS</span></span>
<span data-ttu-id="e3896-103">Gibt das Bild für einen virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="e3896-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3896-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3896-104">SYNTAX</span></span>

### <span data-ttu-id="e3896-105">ImageReferenceSkuParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e3896-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3896-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3896-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3896-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3896-107">DESCRIPTION</span></span>
<span data-ttu-id="e3896-108">Das Cmdlet " **Satz-AzureRmVMSourceImage** " gibt das Platt Form Bild an, das für einen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3896-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="e3896-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3896-109">EXAMPLES</span></span>

### <span data-ttu-id="e3896-110">Beispiel 1: Setzen von Werten für ein Bild</span><span class="sxs-lookup"><span data-stu-id="e3896-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="e3896-111">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="e3896-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="e3896-112">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e3896-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e3896-113">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="e3896-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e3896-114">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="e3896-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="e3896-115">Der endgültige Befehl legt Werte für den Herausgebernamen, das Angebot, die SKU und die Version fest.</span><span class="sxs-lookup"><span data-stu-id="e3896-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="e3896-116">Die Cmdlets **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** und **Get-AzureRmVMImage** können diese Einstellungen ermitteln.</span><span class="sxs-lookup"><span data-stu-id="e3896-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="e3896-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3896-117">PARAMETERS</span></span>

### <span data-ttu-id="e3896-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3896-118">-DefaultProfile</span></span>
<span data-ttu-id="e3896-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e3896-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3896-120">-ID</span><span class="sxs-lookup"><span data-stu-id="e3896-120">-Id</span></span>
<span data-ttu-id="e3896-121">Gibt die ID an.</span><span class="sxs-lookup"><span data-stu-id="e3896-121">Specifies the ID.</span></span>

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

### <span data-ttu-id="e3896-122">-Angebot</span><span class="sxs-lookup"><span data-stu-id="e3896-122">-Offer</span></span>
<span data-ttu-id="e3896-123">Gibt den Typ des VMImage-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="e3896-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="e3896-124">Verwenden Sie das Get-AzureRmVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e3896-124">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="e3896-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="e3896-125">-PublisherName</span></span>
<span data-ttu-id="e3896-126">Gibt den Namen des Herausgebers eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="e3896-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="e3896-127">Verwenden Sie zum Abrufen eines Verlegers das Get-AzureRmVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3896-127">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="e3896-128">-SKUs</span><span class="sxs-lookup"><span data-stu-id="e3896-128">-Skus</span></span>
<span data-ttu-id="e3896-129">Gibt eine VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="e3896-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="e3896-130">Verwenden Sie zum Abrufen von SKUs das Get-AzureRmVMImageSku-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3896-130">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="e3896-131">-Version</span><span class="sxs-lookup"><span data-stu-id="e3896-131">-Version</span></span>
<span data-ttu-id="e3896-132">Gibt eine Version eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="e3896-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="e3896-133">Wenn Sie die neueste Version verwenden möchten, geben Sie einen Wert von Latest anstelle einer bestimmten Version an.</span><span class="sxs-lookup"><span data-stu-id="e3896-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="e3896-134">-VM</span><span class="sxs-lookup"><span data-stu-id="e3896-134">-VM</span></span>
<span data-ttu-id="e3896-135">Gibt das zu konfigurierende Objekt des lokalen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="e3896-135">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="e3896-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3896-136">CommonParameters</span></span>
<span data-ttu-id="e3896-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3896-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3896-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3896-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3896-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3896-139">INPUTS</span></span>

### <span data-ttu-id="e3896-140">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e3896-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="e3896-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e3896-141">System.String</span></span>

## <span data-ttu-id="e3896-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3896-142">OUTPUTS</span></span>

### <span data-ttu-id="e3896-143">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e3896-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e3896-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3896-144">NOTES</span></span>

## <span data-ttu-id="e3896-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3896-145">RELATED LINKS</span></span>

[<span data-ttu-id="e3896-146">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e3896-146">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="e3896-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e3896-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="e3896-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="e3896-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="e3896-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e3896-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="e3896-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="e3896-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="e3896-151">Neu – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="e3896-151">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


