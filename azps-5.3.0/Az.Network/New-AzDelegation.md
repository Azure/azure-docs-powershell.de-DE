---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 05ed0d27dc1d004c2d9a1c5221795af708b812d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459963"
---
# <span data-ttu-id="5f47f-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="5f47f-101">New-AzDelegation</span></span>

## <span data-ttu-id="5f47f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f47f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f47f-103">Erstellt eine Dienstdelegierung.</span><span class="sxs-lookup"><span data-stu-id="5f47f-103">Creates a service delegation.</span></span>

## <span data-ttu-id="5f47f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f47f-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f47f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f47f-105">DESCRIPTION</span></span>
<span data-ttu-id="5f47f-106">Das **Cmdlet "New-AzDelegation"** erstellt eine Dienstdelegierung, die einem Subnetz hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5f47f-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="5f47f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5f47f-107">EXAMPLES</span></span>

### <span data-ttu-id="5f47f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5f47f-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="5f47f-109">Das erste Cmdlet erstellt eine Delegierung, die einem Subnetz hinzugefügt werden kann, und speichert sie in $delegation Variable.</span><span class="sxs-lookup"><span data-stu-id="5f47f-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="5f47f-110">Das zweite und dritte Cmdlets rufen das zu delegierte Subnetz ab.</span><span class="sxs-lookup"><span data-stu-id="5f47f-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="5f47f-111">Das vierte Cmdlet fügt die erstellte Delegierung dem von Interesse öffentlichen Subnetz hinzu, und das letzte Cmdlet sendet die aktualisierte Konfiguration an den Server.</span><span class="sxs-lookup"><span data-stu-id="5f47f-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="5f47f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f47f-112">PARAMETERS</span></span>

### <span data-ttu-id="5f47f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f47f-113">-DefaultProfile</span></span>
<span data-ttu-id="5f47f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f47f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f47f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5f47f-115">-Name</span></span>
<span data-ttu-id="5f47f-116">Der Name der Legierung</span><span class="sxs-lookup"><span data-stu-id="5f47f-116">The name of the delegation</span></span>

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

### <span data-ttu-id="5f47f-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5f47f-117">-ServiceName</span></span>
<span data-ttu-id="5f47f-118">Der Name des Diensts, an den das Subnetz delegiert werden soll</span><span class="sxs-lookup"><span data-stu-id="5f47f-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="5f47f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f47f-119">CommonParameters</span></span>
<span data-ttu-id="5f47f-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f47f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f47f-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f47f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f47f-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5f47f-122">INPUTS</span></span>

### <span data-ttu-id="5f47f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="5f47f-123">System.String</span></span>

## <span data-ttu-id="5f47f-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5f47f-124">OUTPUTS</span></span>

### <span data-ttu-id="5f47f-125">Microsoft.Azure.Commands.Network.Models.PSDElegation</span><span class="sxs-lookup"><span data-stu-id="5f47f-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="5f47f-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5f47f-126">NOTES</span></span>

## <span data-ttu-id="5f47f-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5f47f-127">RELATED LINKS</span></span>

<span data-ttu-id="5f47f-128">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="5f47f-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>