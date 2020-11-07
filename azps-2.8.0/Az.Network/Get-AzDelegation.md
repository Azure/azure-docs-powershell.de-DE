---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: 4b6f253da0c2494db49883402be8f39f5ef80ae4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822396"
---
# <span data-ttu-id="537b8-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="537b8-101">Get-AzDelegation</span></span>

## <span data-ttu-id="537b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="537b8-102">SYNOPSIS</span></span>
<span data-ttu-id="537b8-103">Besorgen Sie sich eine Delegation (oder alle Delegationen) in einem bestimmten Subnetz.</span><span class="sxs-lookup"><span data-stu-id="537b8-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="537b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="537b8-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="537b8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="537b8-105">DESCRIPTION</span></span>
<span data-ttu-id="537b8-106">Das Cmdlet " **Get-AzDelegation** " Ruft die benannte Delegierung aus einem Subnetz ab.</span><span class="sxs-lookup"><span data-stu-id="537b8-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="537b8-107">Wenn keine Delegierung benannt wird, gibt Sie alle Delegierungen im bereitgestellten Subnetz zurück.</span><span class="sxs-lookup"><span data-stu-id="537b8-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="537b8-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="537b8-108">EXAMPLES</span></span>

### <span data-ttu-id="537b8-109">1: Abrufen einer bestimmten Delegierung</span><span class="sxs-lookup"><span data-stu-id="537b8-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="537b8-110">Die erste Zeile Ruft das Subnetz von Interesse ab.</span><span class="sxs-lookup"><span data-stu-id="537b8-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="537b8-111">Die zweite Zeile zeigt die Delegations Informationen für die Delegation mit dem Namen "mydelegation".</span><span class="sxs-lookup"><span data-stu-id="537b8-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="537b8-112">2: Abrufen aller Subnet-Delegierungen</span><span class="sxs-lookup"><span data-stu-id="537b8-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="537b8-113">Die erste Zeile Ruft das Subnetz von Interesse ab.</span><span class="sxs-lookup"><span data-stu-id="537b8-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="537b8-114">In der zweiten Zeile wird eine Liste aller Delegierungen in _mysubnet_ in der $Delegations-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="537b8-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="537b8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="537b8-115">PARAMETERS</span></span>

### <span data-ttu-id="537b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="537b8-116">-DefaultProfile</span></span>
<span data-ttu-id="537b8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="537b8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="537b8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="537b8-118">-Name</span></span>
<span data-ttu-id="537b8-119">Der Name der Delegierung</span><span class="sxs-lookup"><span data-stu-id="537b8-119">The name of the delegation</span></span>

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

### <span data-ttu-id="537b8-120">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="537b8-120">-Subnet</span></span>
<span data-ttu-id="537b8-121">Das Subnetz</span><span class="sxs-lookup"><span data-stu-id="537b8-121">The subnet</span></span>

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

### <span data-ttu-id="537b8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="537b8-122">CommonParameters</span></span>
<span data-ttu-id="537b8-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="537b8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="537b8-124">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="537b8-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="537b8-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="537b8-125">INPUTS</span></span>

### <span data-ttu-id="537b8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="537b8-126">System.String</span></span>

### <span data-ttu-id="537b8-127">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="537b8-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="537b8-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="537b8-128">OUTPUTS</span></span>

### <span data-ttu-id="537b8-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="537b8-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="537b8-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="537b8-130">NOTES</span></span>

## <span data-ttu-id="537b8-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="537b8-131">RELATED LINKS</span></span>

<span data-ttu-id="537b8-132">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Neu – AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="537b8-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>