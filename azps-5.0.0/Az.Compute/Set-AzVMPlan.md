---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 93837ff6618523f71fdd2b0a3b933b50892af429
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177700"
---
# <span data-ttu-id="78c21-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="78c21-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="78c21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78c21-102">SYNOPSIS</span></span>
<span data-ttu-id="78c21-103">Legt die Informationen zum Marktplatz Plan auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="78c21-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="78c21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78c21-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78c21-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78c21-105">DESCRIPTION</span></span>
<span data-ttu-id="78c21-106">Das Cmdlet " **Set-AzVMPlan** " legt die Azure Marketplace-Planinformationen für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="78c21-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="78c21-107">Bevor Sie ein Marketplace-Abbild über die Befehlszeile bereitstellen können, muss der programmgesteuerte Zugriff aktiviert sein, oder der virtuelle Computer muss mithilfe des Azure-Portals bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="78c21-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="78c21-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78c21-108">EXAMPLES</span></span>

## <span data-ttu-id="78c21-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="78c21-109">PARAMETERS</span></span>

### <span data-ttu-id="78c21-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78c21-110">-DefaultProfile</span></span>
<span data-ttu-id="78c21-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78c21-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78c21-112">-Name</span><span class="sxs-lookup"><span data-stu-id="78c21-112">-Name</span></span>
<span data-ttu-id="78c21-113">Gibt den Namen des Bilds vom Marketplace an.</span><span class="sxs-lookup"><span data-stu-id="78c21-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="78c21-114">Dies ist derselbe Wert, der vom Get-AzVMImageSku-Cmdlet zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="78c21-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="78c21-115">Weitere Informationen zum Auffinden von Bildinformationen finden Sie unter Navigieren und Auswählen von Bildern für Azure Virtual Machine mit PowerShell und Azure CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in der Microsoft Azure-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="78c21-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c21-116">-Product</span><span class="sxs-lookup"><span data-stu-id="78c21-116">-Product</span></span>
<span data-ttu-id="78c21-117">Gibt das Produkt des Bilds vom Marktplatz an.</span><span class="sxs-lookup"><span data-stu-id="78c21-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="78c21-118">Hierbei handelt es sich um dieselben Informationen wie der **Angebots** Wert des **imagereference** -Elements.</span><span class="sxs-lookup"><span data-stu-id="78c21-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c21-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="78c21-119">-PromotionCode</span></span>
<span data-ttu-id="78c21-120">Gibt einen Promotionscode an.</span><span class="sxs-lookup"><span data-stu-id="78c21-120">Specifies a promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c21-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="78c21-121">-Publisher</span></span>
<span data-ttu-id="78c21-122">Gibt den Herausgeber des Bilds an.</span><span class="sxs-lookup"><span data-stu-id="78c21-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="78c21-123">Sie finden diese Informationen unter Verwendung des Get-AzVMImagePublisher-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="78c21-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c21-124">-VM</span><span class="sxs-lookup"><span data-stu-id="78c21-124">-VM</span></span>
<span data-ttu-id="78c21-125">Gibt das Objekt des virtuellen Computers an, für das ein Marktplatz Plan festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="78c21-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="78c21-126">Sie können das Get-AzVM-Cmdlet verwenden, um ein Objekt eines virtuellen Computers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="78c21-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="78c21-127">Sie können das New-AzVMConfig-Cmdlet verwenden, um ein Objekt eines virtuellen Computers zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="78c21-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="78c21-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c21-128">CommonParameters</span></span>
<span data-ttu-id="78c21-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78c21-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c21-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78c21-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c21-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78c21-131">INPUTS</span></span>

### <span data-ttu-id="78c21-132">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="78c21-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="78c21-133">System. String</span><span class="sxs-lookup"><span data-stu-id="78c21-133">System.String</span></span>

## <span data-ttu-id="78c21-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78c21-134">OUTPUTS</span></span>

### <span data-ttu-id="78c21-135">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="78c21-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="78c21-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="78c21-136">NOTES</span></span>

## <span data-ttu-id="78c21-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78c21-137">RELATED LINKS</span></span>

[<span data-ttu-id="78c21-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="78c21-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="78c21-139">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="78c21-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="78c21-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="78c21-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="78c21-141">Neu – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="78c21-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
