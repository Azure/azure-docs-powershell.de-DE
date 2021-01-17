---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 93837ff6618523f71fdd2b0a3b933b50892af429
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362338"
---
# <span data-ttu-id="be0a0-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="be0a0-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="be0a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be0a0-102">SYNOPSIS</span></span>
<span data-ttu-id="be0a0-103">Legt die Informationen zum Marketplace-Plan auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="be0a0-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="be0a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be0a0-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be0a0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be0a0-105">DESCRIPTION</span></span>
<span data-ttu-id="be0a0-106">Das **Cmdlet Set-AzVMPlan** legt die Azure Marketplace-Planinformationen für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="be0a0-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="be0a0-107">Bevor Sie ein Marketplace-Bild über die Befehlszeile bereitstellen können, muss der programmgesteuerte Zugriff aktiviert oder der virtuelle Computer über das Azure-Portal bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="be0a0-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="be0a0-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="be0a0-108">EXAMPLES</span></span>

## <span data-ttu-id="be0a0-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be0a0-109">PARAMETERS</span></span>

### <span data-ttu-id="be0a0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be0a0-110">-DefaultProfile</span></span>
<span data-ttu-id="be0a0-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be0a0-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be0a0-112">-Name</span><span class="sxs-lookup"><span data-stu-id="be0a0-112">-Name</span></span>
<span data-ttu-id="be0a0-113">Gibt den Namen des Bilds aus dem Marketplace an.</span><span class="sxs-lookup"><span data-stu-id="be0a0-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="be0a0-114">Dies ist derselbe Wert, der vom cmdlet Get-AzVMImageSku zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="be0a0-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="be0a0-115">Weitere Informationen zum Suchen nach Bildinformationen finden Sie in der Microsoft Azure-Dokumentation zum Navigieren und Auswählen von Bildern für den virtuellen Azure-Computer mit PowerShell und der https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) Azure-CLI.</span><span class="sxs-lookup"><span data-stu-id="be0a0-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="be0a0-116">-Produkt</span><span class="sxs-lookup"><span data-stu-id="be0a0-116">-Product</span></span>
<span data-ttu-id="be0a0-117">Gibt das Produkt des Bilds aus dem Marketplace an.</span><span class="sxs-lookup"><span data-stu-id="be0a0-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="be0a0-118">Dies sind die gleichen Informationen wie der **Angebotswert** des **imageReference-Elements.**</span><span class="sxs-lookup"><span data-stu-id="be0a0-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="be0a0-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="be0a0-119">-PromotionCode</span></span>
<span data-ttu-id="be0a0-120">Gibt einen Werbecode an.</span><span class="sxs-lookup"><span data-stu-id="be0a0-120">Specifies a promotion code.</span></span>

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

### <span data-ttu-id="be0a0-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="be0a0-121">-Publisher</span></span>
<span data-ttu-id="be0a0-122">Gibt den Herausgeber des Bilds an.</span><span class="sxs-lookup"><span data-stu-id="be0a0-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="be0a0-123">Sie finden diese Informationen mithilfe des Get-AzVMImagePublisher Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="be0a0-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="be0a0-124">-VM</span><span class="sxs-lookup"><span data-stu-id="be0a0-124">-VM</span></span>
<span data-ttu-id="be0a0-125">Gibt das Objekt des virtuellen Computers an, für das ein Marketplace-Plan festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="be0a0-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="be0a0-126">Sie können das Get-AzVM cmdlet verwenden, um ein Objekt des virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="be0a0-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="be0a0-127">Sie können das New-AzVMConfig cmdlet verwenden, um ein Objekt für einen virtuellen Computer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="be0a0-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="be0a0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be0a0-128">CommonParameters</span></span>
<span data-ttu-id="be0a0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be0a0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be0a0-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be0a0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be0a0-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="be0a0-131">INPUTS</span></span>

### <span data-ttu-id="be0a0-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="be0a0-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="be0a0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="be0a0-133">System.String</span></span>

## <span data-ttu-id="be0a0-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="be0a0-134">OUTPUTS</span></span>

### <span data-ttu-id="be0a0-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="be0a0-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="be0a0-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="be0a0-136">NOTES</span></span>

## <span data-ttu-id="be0a0-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="be0a0-137">RELATED LINKS</span></span>

[<span data-ttu-id="be0a0-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="be0a0-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="be0a0-139">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="be0a0-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="be0a0-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="be0a0-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="be0a0-141">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="be0a0-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
