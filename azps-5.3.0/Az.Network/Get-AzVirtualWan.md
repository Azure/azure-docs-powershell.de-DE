---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
ms.openlocfilehash: d017ef97d7c8a1834a8cab2de979e017251adf7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379769"
---
# <span data-ttu-id="0364d-101">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0364d-101">Get-AzVirtualWan</span></span>

## <span data-ttu-id="0364d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0364d-102">SYNOPSIS</span></span>
<span data-ttu-id="0364d-103">Ruft ein virtuelles WAN oder alle virtuellen WANs in einer Ressourcengruppe oder einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="0364d-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="0364d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0364d-104">SYNTAX</span></span>

### <span data-ttu-id="0364d-105">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="0364d-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0364d-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0364d-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualWan [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0364d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0364d-107">DESCRIPTION</span></span>
<span data-ttu-id="0364d-108">Ruft ein virtuelles WAN oder alle virtuellen WANs in einer Ressourcengruppe oder einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="0364d-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="0364d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0364d-109">EXAMPLES</span></span>

### <span data-ttu-id="0364d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0364d-110">Example 1</span></span>

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

<span data-ttu-id="0364d-111">Dieser Befehl ruft das virtuelle WAN namens myVirtualWAN in der Ressourcengruppe testRG ab.</span><span class="sxs-lookup"><span data-stu-id="0364d-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

### <span data-ttu-id="0364d-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0364d-112">Example 2</span></span>

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

<span data-ttu-id="0364d-113">Dieser Befehl ruft alle virtuellen WANs ab "test" ab.</span><span class="sxs-lookup"><span data-stu-id="0364d-113">This command gets all Virtual WANs starting with "test".</span></span>

## <span data-ttu-id="0364d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0364d-114">PARAMETERS</span></span>

### <span data-ttu-id="0364d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0364d-115">-DefaultProfile</span></span>
<span data-ttu-id="0364d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0364d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0364d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0364d-117">-Name</span></span>
<span data-ttu-id="0364d-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="0364d-118">The resource name.</span></span>

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

### <span data-ttu-id="0364d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0364d-119">-ResourceGroupName</span></span>
<span data-ttu-id="0364d-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0364d-120">The resource group name.</span></span>

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

### <span data-ttu-id="0364d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0364d-121">CommonParameters</span></span>
<span data-ttu-id="0364d-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0364d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0364d-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0364d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0364d-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0364d-124">INPUTS</span></span>

### <span data-ttu-id="0364d-125">Keine</span><span class="sxs-lookup"><span data-stu-id="0364d-125">None</span></span>

## <span data-ttu-id="0364d-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0364d-126">OUTPUTS</span></span>

### <span data-ttu-id="0364d-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0364d-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="0364d-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0364d-128">NOTES</span></span>

## <span data-ttu-id="0364d-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0364d-129">RELATED LINKS</span></span>

[<span data-ttu-id="0364d-130">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0364d-130">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="0364d-131">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0364d-131">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="0364d-132">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0364d-132">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
