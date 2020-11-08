---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: 5f65ec635c71e64fb0e16d6a7391f188c6e2582c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003490"
---
# <span data-ttu-id="a1e5e-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a1e5e-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="a1e5e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a1e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e5e-103">Ruft eine Azure VirtualHub nach Name und ResourceGroupName ab oder listet alle virtuellen Hubs nach ResourceGroupName/Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="a1e5e-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="a1e5e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1e5e-104">SYNTAX</span></span>

### <span data-ttu-id="a1e5e-105">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1e5e-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1e5e-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e5e-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1e5e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1e5e-107">DESCRIPTION</span></span>
<span data-ttu-id="a1e5e-108">Ruft eine Azure VirtualHub nach Name und ResourceGroupName ab oder listet alle virtuellen Hubs nach ResourceGroupName/Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="a1e5e-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="a1e5e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1e5e-109">EXAMPLES</span></span>

### <span data-ttu-id="a1e5e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a1e5e-110">Example 1</span></span>

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

<span data-ttu-id="a1e5e-111">Das oben beschriebene erstellt eine Ressourcengruppe "testRG", ein virtuelles WAN und einen virtuellen Hub in West-USA in dieser Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="a1e5e-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="a1e5e-112">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="a1e5e-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="a1e5e-113">Anschließend wird der virtuelle Hub mithilfe von ResourceGroupName und resourceName abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a1e5e-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="a1e5e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a1e5e-114">Example 2</span></span>

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

<span data-ttu-id="a1e5e-115">Dieses Cmdlet ruft den virtuellen Hub mithilfe von Filtern ab.</span><span class="sxs-lookup"><span data-stu-id="a1e5e-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="a1e5e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1e5e-116">PARAMETERS</span></span>

### <span data-ttu-id="a1e5e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e5e-117">-DefaultProfile</span></span>
<span data-ttu-id="a1e5e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a1e5e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1e5e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a1e5e-119">-Name</span></span>
<span data-ttu-id="a1e5e-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="a1e5e-120">The resource name.</span></span>

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

### <span data-ttu-id="a1e5e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e5e-121">-ResourceGroupName</span></span>
<span data-ttu-id="a1e5e-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a1e5e-122">The resource group name.</span></span>

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

### <span data-ttu-id="a1e5e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e5e-123">CommonParameters</span></span>
<span data-ttu-id="a1e5e-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1e5e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e5e-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1e5e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e5e-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a1e5e-126">INPUTS</span></span>

### <span data-ttu-id="a1e5e-127">Keine</span><span class="sxs-lookup"><span data-stu-id="a1e5e-127">None</span></span>

## <span data-ttu-id="a1e5e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a1e5e-128">OUTPUTS</span></span>

### <span data-ttu-id="a1e5e-129">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a1e5e-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="a1e5e-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="a1e5e-130">NOTES</span></span>

## <span data-ttu-id="a1e5e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a1e5e-131">RELATED LINKS</span></span>

[<span data-ttu-id="a1e5e-132">Neu – AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a1e5e-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="a1e5e-133">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a1e5e-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="a1e5e-134">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a1e5e-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
