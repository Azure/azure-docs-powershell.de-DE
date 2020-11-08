---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 05ed0d27dc1d004c2d9a1c5221795af708b812d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004961"
---
# <span data-ttu-id="a942a-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="a942a-101">New-AzDelegation</span></span>

## <span data-ttu-id="a942a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a942a-102">SYNOPSIS</span></span>
<span data-ttu-id="a942a-103">Erstellt eine Dienst Delegierung.</span><span class="sxs-lookup"><span data-stu-id="a942a-103">Creates a service delegation.</span></span>

## <span data-ttu-id="a942a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a942a-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a942a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a942a-105">DESCRIPTION</span></span>
<span data-ttu-id="a942a-106">Das Cmdlet **New-AzDelegation** erstellt eine Dienst Delegierung, die einem Subnetz hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a942a-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="a942a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a942a-107">EXAMPLES</span></span>

### <span data-ttu-id="a942a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a942a-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="a942a-109">Das erste Cmdlet erstellt eine Delegierung, die einem Subnetz hinzugefügt werden kann, und speichert Sie in der $Delegation-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a942a-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="a942a-110">Das zweite und dritte Cmdlets rufen das Subnetz ab, das delegiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a942a-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="a942a-111">Das vierte Cmdlet fügt die erstellte Delegierung dem Subnetz von Interesse hinzu, und das endgültige Cmdlet sendet die aktualisierte Konfiguration an den Server.</span><span class="sxs-lookup"><span data-stu-id="a942a-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="a942a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a942a-112">PARAMETERS</span></span>

### <span data-ttu-id="a942a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a942a-113">-DefaultProfile</span></span>
<span data-ttu-id="a942a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a942a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a942a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a942a-115">-Name</span></span>
<span data-ttu-id="a942a-116">Der Name der Delegierung</span><span class="sxs-lookup"><span data-stu-id="a942a-116">The name of the delegation</span></span>

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

### <span data-ttu-id="a942a-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a942a-117">-ServiceName</span></span>
<span data-ttu-id="a942a-118">Der Name des Diensts, an den das Subnetz delegiert werden soll</span><span class="sxs-lookup"><span data-stu-id="a942a-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="a942a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a942a-119">CommonParameters</span></span>
<span data-ttu-id="a942a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a942a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a942a-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a942a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a942a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a942a-122">INPUTS</span></span>

### <span data-ttu-id="a942a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a942a-123">System.String</span></span>

## <span data-ttu-id="a942a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a942a-124">OUTPUTS</span></span>

### <span data-ttu-id="a942a-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="a942a-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="a942a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="a942a-126">NOTES</span></span>

## <span data-ttu-id="a942a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a942a-127">RELATED LINKS</span></span>

<span data-ttu-id="a942a-128">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Satz-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="a942a-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>