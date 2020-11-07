---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
ms.openlocfilehash: 1daa68e021646d91a2ab1b45382b137771411325
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664544"
---
# <span data-ttu-id="ba93f-101">Remove-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="ba93f-101">Remove-AzureRmDelegation</span></span>

## <span data-ttu-id="ba93f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba93f-102">SYNOPSIS</span></span>
<span data-ttu-id="ba93f-103">Entfernt eine Dienst Delegierung aus dem bereitgestellten Subnetz.</span><span class="sxs-lookup"><span data-stu-id="ba93f-103">Removes a service delegation from the provided subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba93f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba93f-104">SYNTAX</span></span>

```
Remove-AzureRmDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba93f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba93f-105">DESCRIPTION</span></span>
<span data-ttu-id="ba93f-106">Das Cmdlet **Remove-AzureRmDelegation** übernimmt ein Subnetz mit Delegierungen und entfernt die benannte Delegierung aus diesem Subnetz.</span><span class="sxs-lookup"><span data-stu-id="ba93f-106">The **Remove-AzureRmDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="ba93f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba93f-107">EXAMPLES</span></span>

### <span data-ttu-id="ba93f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ba93f-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzureRmDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="ba93f-109">In diesem Beispiel ist die erste Hälfte (gefunden unter _"Hinzufügen einer Delegierung zu einem vorhandenen Subnetz"_ ) identisch mit [Add-AzureRmDelegation](./Add-AzureRmDelegation.md).</span><span class="sxs-lookup"><span data-stu-id="ba93f-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzureRmDelegation](./Add-AzureRmDelegation.md).</span></span> <span data-ttu-id="ba93f-110">In der zweiten Hälfte rufen die ersten beiden Cmdlets das Subnetz von Interesse ab, wobei die lokale Kopie auf dem Server aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ba93f-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="ba93f-111">Das dritte Cmdlet entfernt die in der ersten Hälfte von _mysubnet_ erstellte Delegierung und speichert das aktualisierte Subnetz in _$Subnet_.</span><span class="sxs-lookup"><span data-stu-id="ba93f-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="ba93f-112">Das endgültige Cmdlet aktualisiert den Server mit der deinstallierten Delegierung.</span><span class="sxs-lookup"><span data-stu-id="ba93f-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="ba93f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba93f-113">PARAMETERS</span></span>

### <span data-ttu-id="ba93f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba93f-114">-DefaultProfile</span></span>
<span data-ttu-id="ba93f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba93f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba93f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ba93f-116">-Name</span></span>
<span data-ttu-id="ba93f-117">Der Name der Delegierung</span><span class="sxs-lookup"><span data-stu-id="ba93f-117">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba93f-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ba93f-118">-ServiceName</span></span>
<span data-ttu-id="ba93f-119">Der Name des Diensts, an den das Subnetz delegiert werden soll</span><span class="sxs-lookup"><span data-stu-id="ba93f-119">The name of the service to which the subnet should be delegated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba93f-120">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="ba93f-120">-Subnet</span></span>
<span data-ttu-id="ba93f-121">Das Subnetz, aus dem die Delegierung entfernt werden soll</span><span class="sxs-lookup"><span data-stu-id="ba93f-121">The subnet from which to remove the delegation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba93f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba93f-122">CommonParameters</span></span>
<span data-ttu-id="ba93f-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba93f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba93f-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba93f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba93f-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba93f-125">INPUTS</span></span>

### <span data-ttu-id="ba93f-126">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="ba93f-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
### <span data-ttu-id="ba93f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ba93f-127">System.String</span></span>
## <span data-ttu-id="ba93f-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba93f-128">OUTPUTS</span></span>

### <span data-ttu-id="ba93f-129">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="ba93f-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
## <span data-ttu-id="ba93f-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba93f-130">NOTES</span></span>

## <span data-ttu-id="ba93f-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba93f-131">RELATED LINKS</span></span>

<span data-ttu-id="ba93f-132">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md) 
 [Neu – AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Satz-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="ba93f-132">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
