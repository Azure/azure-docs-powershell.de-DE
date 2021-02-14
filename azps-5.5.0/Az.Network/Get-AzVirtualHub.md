---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: 5f65ec635c71e64fb0e16d6a7391f188c6e2582c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169979"
---
# <span data-ttu-id="9f8f8-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9f8f8-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="9f8f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f8f8-102">SYNOPSIS</span></span>
<span data-ttu-id="9f8f8-103">Ruft einen Azure VirtualHub nach Name und ResourceGroupName ab oder listet alle virtuellen Hubs nach ResourceGroupName/Subscription auf.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="9f8f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f8f8-104">SYNTAX</span></span>

### <span data-ttu-id="9f8f8-105">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="9f8f8-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f8f8-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f8f8-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f8f8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f8f8-107">DESCRIPTION</span></span>
<span data-ttu-id="9f8f8-108">Ruft einen Azure VirtualHub nach Name und ResourceGroupName ab oder listet alle virtuellen Hubs nach ResourceGroupName/Subscription auf.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="9f8f8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9f8f8-109">EXAMPLES</span></span>

### <span data-ttu-id="9f8f8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9f8f8-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="9f8f8-111">Im vorstehenden Beispiel wird eine Ressourcengruppe "testRG", ein virtuelles WAN und ein virtueller Hub in West US in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="9f8f8-112">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="9f8f8-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="9f8f8-113">Anschließend ruft sie den virtuellen Hub mit "ResourceGroupName" und "ResourceName" ab.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="9f8f8-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9f8f8-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualHub -Name westushub*

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub1
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub1
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub2
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub2
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="9f8f8-115">Dieses Cmdlet ruft den virtuellen Hub mithilfe von Filterung ab.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="9f8f8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f8f8-116">PARAMETERS</span></span>

### <span data-ttu-id="9f8f8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f8f8-117">-DefaultProfile</span></span>
<span data-ttu-id="9f8f8-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f8f8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9f8f8-119">-Name</span></span>
<span data-ttu-id="9f8f8-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="9f8f8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f8f8-121">-ResourceGroupName</span></span>
<span data-ttu-id="9f8f8-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="9f8f8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f8f8-123">CommonParameters</span></span>
<span data-ttu-id="9f8f8-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f8f8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f8f8-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f8f8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f8f8-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9f8f8-126">INPUTS</span></span>

### <span data-ttu-id="9f8f8-127">Keine</span><span class="sxs-lookup"><span data-stu-id="9f8f8-127">None</span></span>

## <span data-ttu-id="9f8f8-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9f8f8-128">OUTPUTS</span></span>

### <span data-ttu-id="9f8f8-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9f8f8-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="9f8f8-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9f8f8-130">NOTES</span></span>

## <span data-ttu-id="9f8f8-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9f8f8-131">RELATED LINKS</span></span>

[<span data-ttu-id="9f8f8-132">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9f8f8-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="9f8f8-133">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9f8f8-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="9f8f8-134">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9f8f8-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
