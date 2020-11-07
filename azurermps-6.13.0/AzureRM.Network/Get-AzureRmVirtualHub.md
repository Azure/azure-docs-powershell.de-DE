---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHub.md
ms.openlocfilehash: f758197a0d2b3f6a62071a139e8a5fc67acc50c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665145"
---
# <span data-ttu-id="98509-101">Get-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="98509-101">Get-AzureRmVirtualHub</span></span>

## <span data-ttu-id="98509-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="98509-102">SYNOPSIS</span></span>
<span data-ttu-id="98509-103">Ruft eine Azure VirtualHub nach Name und ResourceGroupName ab oder listet alle virtuellen Hubs nach ResourceGroupName/Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="98509-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98509-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="98509-104">SYNTAX</span></span>

### <span data-ttu-id="98509-105">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="98509-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98509-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98509-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVirtualHub -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98509-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98509-107">DESCRIPTION</span></span>
<span data-ttu-id="98509-108">Ruft eine Azure VirtualHub nach Name und ResourceGroupName ab oder listet alle virtuellen Hubs nach ResourceGroupName/Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="98509-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="98509-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="98509-109">EXAMPLES</span></span>

### <span data-ttu-id="98509-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="98509-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub"

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

<span data-ttu-id="98509-111">Das oben beschriebene erstellt eine Ressourcengruppe "testRG", ein virtuelles WAN und einen virtuellen Hub in West-USA in dieser Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="98509-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="98509-112">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="98509-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="98509-113">Anschließend wird der virtuelle Hub mithilfe von ResourceGroupName und resourceName abgerufen.</span><span class="sxs-lookup"><span data-stu-id="98509-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

## <span data-ttu-id="98509-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="98509-114">PARAMETERS</span></span>

### <span data-ttu-id="98509-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98509-115">-DefaultProfile</span></span>
<span data-ttu-id="98509-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="98509-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98509-117">-Name</span><span class="sxs-lookup"><span data-stu-id="98509-117">-Name</span></span>
<span data-ttu-id="98509-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="98509-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98509-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98509-119">-ResourceGroupName</span></span>
<span data-ttu-id="98509-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="98509-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98509-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98509-121">CommonParameters</span></span>
<span data-ttu-id="98509-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98509-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98509-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98509-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98509-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="98509-124">INPUTS</span></span>

### <span data-ttu-id="98509-125">Keine</span><span class="sxs-lookup"><span data-stu-id="98509-125">None</span></span>

## <span data-ttu-id="98509-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="98509-126">OUTPUTS</span></span>

### <span data-ttu-id="98509-127">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="98509-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="98509-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="98509-128">NOTES</span></span>

## <span data-ttu-id="98509-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="98509-129">RELATED LINKS</span></span>
