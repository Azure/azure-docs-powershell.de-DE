---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: ff2e1a820a2a1cc664969c1872aebe6b88fc415b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003484"
---
# <span data-ttu-id="817c4-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="817c4-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="817c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="817c4-102">SYNOPSIS</span></span>
<span data-ttu-id="817c4-103">Ruft ein virtuelles Netzwerk in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="817c4-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="817c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="817c4-104">SYNTAX</span></span>

### <span data-ttu-id="817c4-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="817c4-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="817c4-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="817c4-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="817c4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="817c4-107">DESCRIPTION</span></span>
<span data-ttu-id="817c4-108">Das Cmdlet " **Get-AzVirtualNetwork** " ruft mindestens ein virtuelles Netzwerk n einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="817c4-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="817c4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="817c4-109">EXAMPLES</span></span>

### <span data-ttu-id="817c4-110">1: Abrufen eines virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="817c4-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="817c4-111">Dieser Befehl ruft das virtuelle Netzwerk mit dem Namen MyVirtualNetwork in der Ressourcengruppe auf TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="817c4-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="817c4-112">2: Auflisten virtueller Netzwerke mithilfe von Filter</span><span class="sxs-lookup"><span data-stu-id="817c4-112">2: List virtual networks using filter</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork*

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="817c4-113">Dieser Befehl ruft alle virtuellen Netzwerke ab, die mit "MyVirtualNetwork" beginnen.</span><span class="sxs-lookup"><span data-stu-id="817c4-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="817c4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="817c4-114">PARAMETERS</span></span>

### <span data-ttu-id="817c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="817c4-115">-DefaultProfile</span></span>
<span data-ttu-id="817c4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="817c4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="817c4-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="817c4-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="817c4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="817c4-118">-Name</span></span>
<span data-ttu-id="817c4-119">Gibt den Namen des virtuellen Netzwerks an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="817c4-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="817c4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="817c4-120">-ResourceGroupName</span></span>
<span data-ttu-id="817c4-121">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerk gehört.</span><span class="sxs-lookup"><span data-stu-id="817c4-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="817c4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="817c4-122">CommonParameters</span></span>
<span data-ttu-id="817c4-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="817c4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="817c4-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="817c4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="817c4-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="817c4-125">INPUTS</span></span>

### <span data-ttu-id="817c4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="817c4-126">System.String</span></span>

## <span data-ttu-id="817c4-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="817c4-127">OUTPUTS</span></span>

### <span data-ttu-id="817c4-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="817c4-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="817c4-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="817c4-129">NOTES</span></span>

## <span data-ttu-id="817c4-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="817c4-130">RELATED LINKS</span></span>

[<span data-ttu-id="817c4-131">Neu – AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="817c4-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="817c4-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="817c4-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="817c4-133">Satz-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="817c4-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


