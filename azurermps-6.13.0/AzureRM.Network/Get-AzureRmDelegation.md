---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
ms.openlocfilehash: f3e8ef97ab618df37ba7d5adae107d65676ed29f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501125"
---
# <span data-ttu-id="d17ab-101">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="d17ab-101">Get-AzureRmDelegation</span></span>

## <span data-ttu-id="d17ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d17ab-102">SYNOPSIS</span></span>
<span data-ttu-id="d17ab-103">Besorgen Sie sich eine Delegation (oder alle Delegationen) in einem bestimmten Subnetz.</span><span class="sxs-lookup"><span data-stu-id="d17ab-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d17ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d17ab-104">SYNTAX</span></span>

```
Get-AzureRmDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d17ab-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d17ab-105">DESCRIPTION</span></span>
<span data-ttu-id="d17ab-106">Das Cmdlet " **Get-AzureRmDelegation** " Ruft die benannte Delegierung aus einem Subnetz ab.</span><span class="sxs-lookup"><span data-stu-id="d17ab-106">The **Get-AzureRmDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="d17ab-107">Wenn keine Delegierung benannt wird, gibt Sie alle Delegierungen im bereitgestellten Subnetz zurück.</span><span class="sxs-lookup"><span data-stu-id="d17ab-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="d17ab-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d17ab-108">EXAMPLES</span></span>

### <span data-ttu-id="d17ab-109">1: Abrufen einer bestimmten Delegierung</span><span class="sxs-lookup"><span data-stu-id="d17ab-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzureRmDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="d17ab-110">Die erste Zeile Ruft das Subnetz von Interesse ab.</span><span class="sxs-lookup"><span data-stu-id="d17ab-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="d17ab-111">Die zweite Zeile zeigt die Delegations Informationen für die Delegation mit dem Namen "mydelegation".</span><span class="sxs-lookup"><span data-stu-id="d17ab-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="d17ab-112">2: Abrufen aller Subnet-Delegierungen</span><span class="sxs-lookup"><span data-stu-id="d17ab-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzureRmDelegation -Subnet $subnet
```

<span data-ttu-id="d17ab-113">Die erste Zeile Ruft das Subnetz von Interesse ab.</span><span class="sxs-lookup"><span data-stu-id="d17ab-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="d17ab-114">In der zweiten Zeile wird eine Liste aller Delegierungen in _mysubnet_ in der $Delegations-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d17ab-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="d17ab-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d17ab-115">PARAMETERS</span></span>

### <span data-ttu-id="d17ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d17ab-116">-DefaultProfile</span></span>
<span data-ttu-id="d17ab-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d17ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d17ab-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d17ab-118">-Name</span></span>
<span data-ttu-id="d17ab-119">Der Name der Delegierung</span><span class="sxs-lookup"><span data-stu-id="d17ab-119">The name of the delegation</span></span>

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

### <span data-ttu-id="d17ab-120">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="d17ab-120">-Subnet</span></span>
<span data-ttu-id="d17ab-121">Das Subnetz</span><span class="sxs-lookup"><span data-stu-id="d17ab-121">The subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d17ab-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d17ab-122">CommonParameters</span></span>
<span data-ttu-id="d17ab-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d17ab-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d17ab-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d17ab-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d17ab-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d17ab-125">INPUTS</span></span>

### <span data-ttu-id="d17ab-126">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="d17ab-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="d17ab-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d17ab-127">OUTPUTS</span></span>

### <span data-ttu-id="d17ab-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="d17ab-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="d17ab-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="d17ab-129">NOTES</span></span>

## <span data-ttu-id="d17ab-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d17ab-130">RELATED LINKS</span></span>
<span data-ttu-id="d17ab-131">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Neu – AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="d17ab-131">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span></span>
