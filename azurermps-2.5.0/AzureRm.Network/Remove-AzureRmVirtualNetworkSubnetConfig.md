---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: 4020f6aa32a7dda31f97831badf9f7916f3db10f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850611"
---
# <span data-ttu-id="f492c-101">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f492c-101">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="f492c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f492c-102">SYNOPSIS</span></span>
<span data-ttu-id="f492c-103">Entfernt eine Subnetz-Konfiguration aus einem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f492c-103">Removes a subnet configuration from a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f492c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f492c-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f492c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f492c-105">DESCRIPTION</span></span>
<span data-ttu-id="f492c-106">Das Cmdlet **Remove-AzureRmVirtualNetworkSubnetConfig** entfernt ein Subnetz aus einem virtuellen Azure-Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f492c-106">The **Remove-AzureRmVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="f492c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f492c-107">EXAMPLES</span></span>

### <span data-ttu-id="f492c-108">1: Entfernen eines Subnets aus einem virtuellen Netzwerk und Aktualisieren des virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="f492c-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="f492c-109">In diesem Beispiel werden eine Ressourcengruppe und ein virtuelles Netzwerk mit zwei Subnetzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="f492c-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="f492c-110">Anschließend wird der Befehl Remove-AzureRmVirtualNetworkSubnetConfig verwendet, um das Back-End-Subnetz aus der speicherinternen Darstellung des virtuellen Netzwerks zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f492c-110">It then uses the Remove-AzureRmVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="f492c-111">Set-AzureRmVirtualNetwork wird dann aufgerufen, um das virtuelle Netzwerk auf der Serverseite zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f492c-111">Set-AzureRmVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="f492c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f492c-112">PARAMETERS</span></span>

### <span data-ttu-id="f492c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f492c-113">-DefaultProfile</span></span>
<span data-ttu-id="f492c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f492c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f492c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f492c-115">-Name</span></span>
<span data-ttu-id="f492c-116">Gibt den Namen der zu entfernenden Subnet-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="f492c-116">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="f492c-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f492c-117">-VirtualNetwork</span></span>
<span data-ttu-id="f492c-118">Gibt das **VirtualNetwork** -Objekt an, das die zu entfernende Subnet-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="f492c-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="f492c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f492c-119">CommonParameters</span></span>
<span data-ttu-id="f492c-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f492c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f492c-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f492c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f492c-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f492c-122">INPUTS</span></span>

### <span data-ttu-id="f492c-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f492c-123">PSVirtualNetwork</span></span>
<span data-ttu-id="f492c-124">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f492c-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="f492c-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f492c-125">OUTPUTS</span></span>

### <span data-ttu-id="f492c-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f492c-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="f492c-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="f492c-127">NOTES</span></span>

## <span data-ttu-id="f492c-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f492c-128">RELATED LINKS</span></span>

[<span data-ttu-id="f492c-129">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f492c-129">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f492c-130">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f492c-130">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f492c-131">Neu – AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f492c-131">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f492c-132">Satz-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f492c-132">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


