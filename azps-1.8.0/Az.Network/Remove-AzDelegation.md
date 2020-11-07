---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: de345650553771078c03d728551b4713b5696fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660391"
---
# <span data-ttu-id="ba61c-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="ba61c-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="ba61c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba61c-102">SYNOPSIS</span></span>
<span data-ttu-id="ba61c-103">Entfernt eine Dienst Delegierung aus dem bereitgestellten Subnetz.</span><span class="sxs-lookup"><span data-stu-id="ba61c-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="ba61c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba61c-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba61c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba61c-105">DESCRIPTION</span></span>
<span data-ttu-id="ba61c-106">Das Cmdlet **Remove-AzDelegation** übernimmt ein Subnetz mit Delegierungen und entfernt die benannte Delegierung aus diesem Subnetz.</span><span class="sxs-lookup"><span data-stu-id="ba61c-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="ba61c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba61c-107">EXAMPLES</span></span>

### <span data-ttu-id="ba61c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ba61c-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="ba61c-109">In diesem Beispiel ist die erste Hälfte (gefunden unter _"Hinzufügen einer Delegierung zu einem vorhandenen Subnetz"_ ) identisch mit [Add-AzDelegation](./Add-AzDelegation.md).</span><span class="sxs-lookup"><span data-stu-id="ba61c-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="ba61c-110">In der zweiten Hälfte rufen die ersten beiden Cmdlets das Subnetz von Interesse ab, wobei die lokale Kopie auf dem Server aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ba61c-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="ba61c-111">Das dritte Cmdlet entfernt die in der ersten Hälfte von _mysubnet_ erstellte Delegierung und speichert das aktualisierte Subnetz in _$Subnet_.</span><span class="sxs-lookup"><span data-stu-id="ba61c-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="ba61c-112">Das endgültige Cmdlet aktualisiert den Server mit der deinstallierten Delegierung.</span><span class="sxs-lookup"><span data-stu-id="ba61c-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="ba61c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba61c-113">PARAMETERS</span></span>

### <span data-ttu-id="ba61c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba61c-114">-DefaultProfile</span></span>
<span data-ttu-id="ba61c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba61c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba61c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ba61c-116">-Name</span></span>
<span data-ttu-id="ba61c-117">Der Name der Delegierung</span><span class="sxs-lookup"><span data-stu-id="ba61c-117">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba61c-118">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="ba61c-118">-Subnet</span></span>
<span data-ttu-id="ba61c-119">Das Subnetz, aus dem die Delegierung entfernt werden soll</span><span class="sxs-lookup"><span data-stu-id="ba61c-119">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="ba61c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba61c-120">CommonParameters</span></span>
<span data-ttu-id="ba61c-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba61c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba61c-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba61c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba61c-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba61c-123">INPUTS</span></span>

### <span data-ttu-id="ba61c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ba61c-124">System.String</span></span>

### <span data-ttu-id="ba61c-125">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="ba61c-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="ba61c-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba61c-126">OUTPUTS</span></span>

### <span data-ttu-id="ba61c-127">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="ba61c-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="ba61c-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba61c-128">NOTES</span></span>

## <span data-ttu-id="ba61c-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba61c-129">RELATED LINKS</span></span>

<span data-ttu-id="ba61c-130">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Neu – AzDelegation](./New-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Satz-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="ba61c-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>