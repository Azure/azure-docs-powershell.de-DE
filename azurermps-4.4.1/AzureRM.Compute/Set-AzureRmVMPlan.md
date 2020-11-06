---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
ms.openlocfilehash: 9fc5da6afd281f68329274ae62a67d888aa13260
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505609"
---
# <span data-ttu-id="63e34-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="63e34-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="63e34-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63e34-102">SYNOPSIS</span></span>
<span data-ttu-id="63e34-103">Legt die Informationen zum Marktplatz Plan auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="63e34-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63e34-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63e34-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63e34-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63e34-105">DESCRIPTION</span></span>
<span data-ttu-id="63e34-106">Das Cmdlet " **Set-AzureRmVMPlan** " legt die Azure Marketplace-Planinformationen für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="63e34-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="63e34-107">Bevor Sie ein Marketplace-Abbild über die Befehlszeile bereitstellen können, muss der programmgesteuerte Zugriff aktiviert sein, oder der virtuelle Computer muss mithilfe des Azure-Portals bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="63e34-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="63e34-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63e34-108">EXAMPLES</span></span>

## <span data-ttu-id="63e34-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="63e34-109">PARAMETERS</span></span>

### <span data-ttu-id="63e34-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e34-110">-DefaultProfile</span></span>
<span data-ttu-id="63e34-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="63e34-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63e34-112">-Name</span><span class="sxs-lookup"><span data-stu-id="63e34-112">-Name</span></span>
<span data-ttu-id="63e34-113">Gibt den Namen des Bilds vom Marketplace an.</span><span class="sxs-lookup"><span data-stu-id="63e34-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="63e34-114">Dies ist derselbe Wert, der vom Get-AzureRmVMImageSku-Cmdlet zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="63e34-114">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="63e34-115">Weitere Informationen zum Auffinden von Bildinformationen finden Sie unter Navigieren und Auswählen von Bildern für Azure Virtual Machine mit PowerShell und Azure CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in der Microsoft Azure-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="63e34-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="63e34-116">-Product</span><span class="sxs-lookup"><span data-stu-id="63e34-116">-Product</span></span>
<span data-ttu-id="63e34-117">Gibt das Produkt des Bilds vom Marktplatz an.</span><span class="sxs-lookup"><span data-stu-id="63e34-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="63e34-118">Hierbei handelt es sich um dieselben Informationen wie der **Angebots** Wert des **imagereference** -Elements.</span><span class="sxs-lookup"><span data-stu-id="63e34-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="63e34-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="63e34-119">-PromotionCode</span></span>
<span data-ttu-id="63e34-120">Gibt einen Promotionscode an.</span><span class="sxs-lookup"><span data-stu-id="63e34-120">Specifies a promotion code.</span></span>

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

### <span data-ttu-id="63e34-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="63e34-121">-Publisher</span></span>
<span data-ttu-id="63e34-122">Gibt den Herausgeber des Bilds an.</span><span class="sxs-lookup"><span data-stu-id="63e34-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="63e34-123">Sie finden diese Informationen unter Verwendung des Get-AzureRmVMImagePublisher-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="63e34-123">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="63e34-124">-VM</span><span class="sxs-lookup"><span data-stu-id="63e34-124">-VM</span></span>
<span data-ttu-id="63e34-125">Gibt das Objekt des virtuellen Computers an, für das ein Marktplatz Plan festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="63e34-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="63e34-126">Sie können das Get-AzureRmVM-Cmdlet verwenden, um ein Objekt eines virtuellen Computers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="63e34-126">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="63e34-127">Sie können das New-AzureRmVMConfig-Cmdlet verwenden, um ein Objekt eines virtuellen Computers zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="63e34-127">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="63e34-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e34-128">CommonParameters</span></span>
<span data-ttu-id="63e34-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63e34-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e34-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63e34-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e34-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63e34-131">INPUTS</span></span>

## <span data-ttu-id="63e34-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63e34-132">OUTPUTS</span></span>

## <span data-ttu-id="63e34-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="63e34-133">NOTES</span></span>

## <span data-ttu-id="63e34-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63e34-134">RELATED LINKS</span></span>

[<span data-ttu-id="63e34-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="63e34-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="63e34-136">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="63e34-136">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="63e34-137">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="63e34-137">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="63e34-138">Neu – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="63e34-138">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
