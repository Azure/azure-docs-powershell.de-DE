---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 9d3897b52d59c85caac3f68b9904878f14014606
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945293"
---
# <span data-ttu-id="07033-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="07033-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="07033-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07033-102">SYNOPSIS</span></span>
<span data-ttu-id="07033-103">Legt die Informationen zum Marketplace-Plan auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="07033-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="07033-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07033-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07033-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07033-105">DESCRIPTION</span></span>
<span data-ttu-id="07033-106">Das **Cmdlet Set-AzVMPlan** legt die Azure Marketplace-Planinformationen für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="07033-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="07033-107">Bevor Sie ein Marketplace-Bild über die Befehlszeile bereitstellen können, muss der programmgesteuerte Zugriff aktiviert oder der virtuelle Computer über das Azure-Portal bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="07033-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="07033-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="07033-108">EXAMPLES</span></span>

## <span data-ttu-id="07033-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="07033-109">PARAMETERS</span></span>

### <span data-ttu-id="07033-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07033-110">-DefaultProfile</span></span>
<span data-ttu-id="07033-111">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07033-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07033-112">-Name</span><span class="sxs-lookup"><span data-stu-id="07033-112">-Name</span></span>
<span data-ttu-id="07033-113">Gibt den Namen des Bilds aus dem Marketplace an.</span><span class="sxs-lookup"><span data-stu-id="07033-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="07033-114">Dies ist derselbe Wert, der vom cmdlet Get-AzVMImageSku wird.</span><span class="sxs-lookup"><span data-stu-id="07033-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="07033-115">Weitere Informationen zum Suchen nach Bildinformationen finden Sie unter Navigieren und Auswählen von Azure Virtual Machine-Bildern mit PowerShell und der Azure CLI (in der https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) Microsoft Azure-Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="07033-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="07033-116">-Produkt</span><span class="sxs-lookup"><span data-stu-id="07033-116">-Product</span></span>
<span data-ttu-id="07033-117">Gibt das Produkt des Bilds aus dem Marketplace an.</span><span class="sxs-lookup"><span data-stu-id="07033-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="07033-118">Dies sind dieselben Informationen wie der **Offer-Wert** des **imageReference-Elements.**</span><span class="sxs-lookup"><span data-stu-id="07033-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="07033-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="07033-119">-PromotionCode</span></span>
<span data-ttu-id="07033-120">Gibt einen Werbecode an.</span><span class="sxs-lookup"><span data-stu-id="07033-120">Specifies a promotion code.</span></span>

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

### <span data-ttu-id="07033-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="07033-121">-Publisher</span></span>
<span data-ttu-id="07033-122">Gibt den Herausgeber des Bilds an.</span><span class="sxs-lookup"><span data-stu-id="07033-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="07033-123">Sie können diese Informationen über das cmdlet Get-AzVMImagePublisher finden.</span><span class="sxs-lookup"><span data-stu-id="07033-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="07033-124">-VM</span><span class="sxs-lookup"><span data-stu-id="07033-124">-VM</span></span>
<span data-ttu-id="07033-125">Gibt das Objekt des virtuellen Computers an, für das ein Marketplace-Plan festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="07033-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="07033-126">Sie können das cmdlet Get-AzVM verwenden, um ein Objekt für einen virtuellen Computer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="07033-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="07033-127">Sie können das cmdlet New-AzVMConfig verwenden, um ein Objekt für einen virtuellen Computer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="07033-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="07033-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07033-128">CommonParameters</span></span>
<span data-ttu-id="07033-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07033-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07033-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07033-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07033-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="07033-131">INPUTS</span></span>

### <span data-ttu-id="07033-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="07033-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="07033-133">System.String</span><span class="sxs-lookup"><span data-stu-id="07033-133">System.String</span></span>

## <span data-ttu-id="07033-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="07033-134">OUTPUTS</span></span>

### <span data-ttu-id="07033-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="07033-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="07033-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="07033-136">NOTES</span></span>

## <span data-ttu-id="07033-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="07033-137">RELATED LINKS</span></span>

[<span data-ttu-id="07033-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="07033-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="07033-139">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="07033-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="07033-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="07033-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="07033-141">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="07033-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
