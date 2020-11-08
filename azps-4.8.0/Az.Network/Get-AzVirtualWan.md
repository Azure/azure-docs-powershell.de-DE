---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
ms.openlocfilehash: d017ef97d7c8a1834a8cab2de979e017251adf7f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008367"
---
# <span data-ttu-id="43cce-101">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="43cce-101">Get-AzVirtualWan</span></span>

## <span data-ttu-id="43cce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43cce-102">SYNOPSIS</span></span>
<span data-ttu-id="43cce-103">Ruft ein virtuelles WAN oder alle virtuellen WANs in einer Ressourcengruppe oder einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="43cce-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="43cce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43cce-104">SYNTAX</span></span>

### <span data-ttu-id="43cce-105">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="43cce-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43cce-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43cce-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualWan [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43cce-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43cce-107">DESCRIPTION</span></span>
<span data-ttu-id="43cce-108">Ruft ein virtuelles WAN oder alle virtuellen WANs in einer Ressourcengruppe oder einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="43cce-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="43cce-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43cce-109">EXAMPLES</span></span>

### <span data-ttu-id="43cce-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43cce-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : myVirtualWAN
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="43cce-111">Dieser Befehl ruft das virtuelle WAN mit dem Namen myVirtualWAN in der Ressourcengruppe testRG.</span><span class="sxs-lookup"><span data-stu-id="43cce-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

### <span data-ttu-id="43cce-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="43cce-112">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualWan -Name test*

Name                       : test1
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test1
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded

Name                       : test2
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test2
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="43cce-113">Dieser Befehl ruft alle virtuellen WANs ab, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="43cce-113">This command gets all Virtual WANs starting with "test".</span></span>

## <span data-ttu-id="43cce-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="43cce-114">PARAMETERS</span></span>

### <span data-ttu-id="43cce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43cce-115">-DefaultProfile</span></span>
<span data-ttu-id="43cce-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43cce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43cce-117">-Name</span><span class="sxs-lookup"><span data-stu-id="43cce-117">-Name</span></span>
<span data-ttu-id="43cce-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="43cce-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="43cce-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43cce-119">-ResourceGroupName</span></span>
<span data-ttu-id="43cce-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="43cce-120">The resource group name.</span></span>

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

### <span data-ttu-id="43cce-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43cce-121">CommonParameters</span></span>
<span data-ttu-id="43cce-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43cce-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43cce-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43cce-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43cce-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43cce-124">INPUTS</span></span>

### <span data-ttu-id="43cce-125">Keine</span><span class="sxs-lookup"><span data-stu-id="43cce-125">None</span></span>

## <span data-ttu-id="43cce-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43cce-126">OUTPUTS</span></span>

### <span data-ttu-id="43cce-127">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="43cce-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="43cce-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="43cce-128">NOTES</span></span>

## <span data-ttu-id="43cce-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43cce-129">RELATED LINKS</span></span>

[<span data-ttu-id="43cce-130">Neu – AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="43cce-130">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="43cce-131">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="43cce-131">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="43cce-132">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="43cce-132">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
