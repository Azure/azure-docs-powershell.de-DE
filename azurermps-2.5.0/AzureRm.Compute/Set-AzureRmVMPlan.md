---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmplan
schema: 2.0.0
ms.openlocfilehash: ce0101140bc353eb52ee8d1af7f2878735da73db
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850903"
---
# <span data-ttu-id="d2890-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="d2890-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="d2890-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2890-102">SYNOPSIS</span></span>
<span data-ttu-id="d2890-103">Legt die Informationen zum Marktplatz Plan auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="d2890-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2890-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2890-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2890-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2890-105">DESCRIPTION</span></span>
<span data-ttu-id="d2890-106">Das Cmdlet " **Set-AzureRmVMPlan** " legt die Azure Marketplace-Planinformationen für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="d2890-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="d2890-107">Bevor Sie ein Marketplace-Abbild über die Befehlszeile bereitstellen können, muss der programmgesteuerte Zugriff aktiviert sein, oder der virtuelle Computer muss mithilfe des Azure-Portals bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d2890-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="d2890-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2890-108">EXAMPLES</span></span>

## <span data-ttu-id="d2890-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2890-109">PARAMETERS</span></span>

### <span data-ttu-id="d2890-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2890-110">-DefaultProfile</span></span>
<span data-ttu-id="d2890-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2890-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2890-112">-Name</span><span class="sxs-lookup"><span data-stu-id="d2890-112">-Name</span></span>
<span data-ttu-id="d2890-113">Gibt den Namen des Bilds vom Marketplace an.</span><span class="sxs-lookup"><span data-stu-id="d2890-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="d2890-114">Dies ist derselbe Wert, der vom Get-AzureRmVMImageSku-Cmdlet zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d2890-114">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="d2890-115">Weitere Informationen zum Auffinden von Bildinformationen finden Sie unter Navigieren und Auswählen von Bildern für Azure Virtual Machine mit PowerShell und Azure CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in der Microsoft Azure-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="d2890-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2890-116">-Product</span><span class="sxs-lookup"><span data-stu-id="d2890-116">-Product</span></span>
<span data-ttu-id="d2890-117">Gibt das Produkt des Bilds vom Marktplatz an.</span><span class="sxs-lookup"><span data-stu-id="d2890-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="d2890-118">Hierbei handelt es sich um dieselben Informationen wie der **Angebots** Wert des **imagereference** -Elements.</span><span class="sxs-lookup"><span data-stu-id="d2890-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2890-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="d2890-119">-PromotionCode</span></span>
<span data-ttu-id="d2890-120">Gibt einen Promotionscode an.</span><span class="sxs-lookup"><span data-stu-id="d2890-120">Specifies a promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2890-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d2890-121">-Publisher</span></span>
<span data-ttu-id="d2890-122">Gibt den Herausgeber des Bilds an.</span><span class="sxs-lookup"><span data-stu-id="d2890-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="d2890-123">Sie finden diese Informationen unter Verwendung des Get-AzureRmVMImagePublisher-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d2890-123">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2890-124">-VM</span><span class="sxs-lookup"><span data-stu-id="d2890-124">-VM</span></span>
<span data-ttu-id="d2890-125">Gibt das Objekt des virtuellen Computers an, für das ein Marktplatz Plan festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2890-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="d2890-126">Sie können das Get-AzureRmVM-Cmdlet verwenden, um ein Objekt eines virtuellen Computers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d2890-126">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="d2890-127">Sie können das New-AzureRmVMConfig-Cmdlet verwenden, um ein Objekt eines virtuellen Computers zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d2890-127">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="d2890-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2890-128">CommonParameters</span></span>
<span data-ttu-id="d2890-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2890-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2890-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2890-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2890-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2890-131">INPUTS</span></span>

### <span data-ttu-id="d2890-132">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d2890-132">PSVirtualMachine</span></span>
<span data-ttu-id="d2890-133">Der Parameter "VM" akzeptiert den Wert vom Typ "PSVirtualMachine" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d2890-133">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="d2890-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2890-134">OUTPUTS</span></span>

### <span data-ttu-id="d2890-135">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d2890-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d2890-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2890-136">NOTES</span></span>

## <span data-ttu-id="d2890-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2890-137">RELATED LINKS</span></span>

[<span data-ttu-id="d2890-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d2890-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="d2890-139">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d2890-139">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="d2890-140">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="d2890-140">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="d2890-141">Neu – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="d2890-141">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
