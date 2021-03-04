---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: 80a1c21b118bf8bcc5a613fef2cdfbe382b117a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928584"
---
# <span data-ttu-id="7aa29-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7aa29-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="7aa29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7aa29-102">SYNOPSIS</span></span>
<span data-ttu-id="7aa29-103">Ruft ein virtuelles Netzwerk in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="7aa29-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="7aa29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7aa29-104">SYNTAX</span></span>

### <span data-ttu-id="7aa29-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="7aa29-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7aa29-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="7aa29-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7aa29-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7aa29-107">DESCRIPTION</span></span>
<span data-ttu-id="7aa29-108">Das **Get-AzVirtualNetwork-Cmdlet** ruft mindestens ein virtuelles Netzwerk n einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="7aa29-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="7aa29-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7aa29-109">EXAMPLES</span></span>

### <span data-ttu-id="7aa29-110">1: Abrufen eines virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="7aa29-110">1: Retrieve a virtual network</span></span>
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

<span data-ttu-id="7aa29-111">Dieser Befehl ruft das virtuelle Netzwerk mit dem Namen MyVirtualNetwork in der Ressourcengruppe TestResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="7aa29-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="7aa29-112">2: Auflisten virtueller Netzwerke mithilfe von Filter</span><span class="sxs-lookup"><span data-stu-id="7aa29-112">2: List virtual networks using filter</span></span>
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

<span data-ttu-id="7aa29-113">Dieser Befehl ruft alle virtuellen Netzwerke ab, die mit "MyVirtualNetwork" beginnen.</span><span class="sxs-lookup"><span data-stu-id="7aa29-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="7aa29-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7aa29-114">PARAMETERS</span></span>

### <span data-ttu-id="7aa29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aa29-115">-DefaultProfile</span></span>
<span data-ttu-id="7aa29-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7aa29-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7aa29-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="7aa29-117">-ExpandResource</span></span>
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

### <span data-ttu-id="7aa29-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7aa29-118">-Name</span></span>
<span data-ttu-id="7aa29-119">Gibt den Namen des virtuellen Netzwerks an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="7aa29-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7aa29-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aa29-120">-ResourceGroupName</span></span>
<span data-ttu-id="7aa29-121">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerk gehört.</span><span class="sxs-lookup"><span data-stu-id="7aa29-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="7aa29-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aa29-122">CommonParameters</span></span>
<span data-ttu-id="7aa29-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aa29-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aa29-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7aa29-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aa29-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7aa29-125">INPUTS</span></span>

### <span data-ttu-id="7aa29-126">System.String</span><span class="sxs-lookup"><span data-stu-id="7aa29-126">System.String</span></span>

## <span data-ttu-id="7aa29-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7aa29-127">OUTPUTS</span></span>

### <span data-ttu-id="7aa29-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7aa29-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="7aa29-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7aa29-129">NOTES</span></span>

## <span data-ttu-id="7aa29-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7aa29-130">RELATED LINKS</span></span>

[<span data-ttu-id="7aa29-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7aa29-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="7aa29-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7aa29-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="7aa29-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7aa29-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


