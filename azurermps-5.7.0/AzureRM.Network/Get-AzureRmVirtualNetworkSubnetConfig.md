---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 531eab9d8b1405b34a4676cd3e06430cfeda0680
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496422"
---
# <span data-ttu-id="749a1-101">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="749a1-101">Get-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="749a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="749a1-102">SYNOPSIS</span></span>
<span data-ttu-id="749a1-103">Ruft ein Subnetz in einem virtuellen Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="749a1-103">Gets a subnet in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="749a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="749a1-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="749a1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="749a1-105">DESCRIPTION</span></span>
<span data-ttu-id="749a1-106">Das Cmdlet " **Get-AzureRmVirtualNetworkSubnetConfig** " ruft mindestens eine Subnetz-Konfiguration in einem virtuellen Azure-Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="749a1-106">The **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="749a1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="749a1-107">EXAMPLES</span></span>

### <span data-ttu-id="749a1-108">1: Abrufen eines Subnetzes in einem virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="749a1-108">1: Get a subnet in a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="749a1-109">In diesem Beispiel werden eine Ressourcengruppe und ein virtuelles Netzwerk mit einem einzelnen Subnetz in dieser Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="749a1-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="749a1-110">Anschließend werden Daten zu diesem Subnetz abgerufen.</span><span class="sxs-lookup"><span data-stu-id="749a1-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="749a1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="749a1-111">PARAMETERS</span></span>

### <span data-ttu-id="749a1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="749a1-112">-DefaultProfile</span></span>
<span data-ttu-id="749a1-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="749a1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="749a1-114">-Name</span><span class="sxs-lookup"><span data-stu-id="749a1-114">-Name</span></span>
<span data-ttu-id="749a1-115">Gibt den Namen der Subnet-Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="749a1-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="749a1-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="749a1-116">-VirtualNetwork</span></span>
<span data-ttu-id="749a1-117">Gibt das **VirtualNetwork** -Objekt an, das die Subnet-Konfiguration enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="749a1-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="749a1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="749a1-118">CommonParameters</span></span>
<span data-ttu-id="749a1-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="749a1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="749a1-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="749a1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="749a1-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="749a1-121">INPUTS</span></span>

### <span data-ttu-id="749a1-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="749a1-122">PSVirtualNetwork</span></span>
<span data-ttu-id="749a1-123">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="749a1-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="749a1-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="749a1-124">OUTPUTS</span></span>

### <span data-ttu-id="749a1-125">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="749a1-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="749a1-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="749a1-126">NOTES</span></span>

## <span data-ttu-id="749a1-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="749a1-127">RELATED LINKS</span></span>

[<span data-ttu-id="749a1-128">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="749a1-128">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="749a1-129">Neu – AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="749a1-129">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="749a1-130">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="749a1-130">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="749a1-131">Satz-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="749a1-131">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


