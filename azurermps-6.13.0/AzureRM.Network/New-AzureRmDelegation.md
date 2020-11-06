---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
ms.openlocfilehash: 9912d41cd9e2600c55d378fbb88510a0defaaa85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500193"
---
# <span data-ttu-id="22136-101">New-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="22136-101">New-AzureRmDelegation</span></span>

## <span data-ttu-id="22136-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22136-102">SYNOPSIS</span></span>
<span data-ttu-id="22136-103">Erstellt eine Dienst Delegierung.</span><span class="sxs-lookup"><span data-stu-id="22136-103">Creates a service delegation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22136-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22136-104">SYNTAX</span></span>

```
New-AzureRmDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22136-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22136-105">DESCRIPTION</span></span>
<span data-ttu-id="22136-106">Das Cmdlet **New-AzureRmDelegation** erstellt eine Dienst Delegierung, die einem Subnetz hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="22136-106">The **New-AzureRmDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="22136-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22136-107">EXAMPLES</span></span>

### <span data-ttu-id="22136-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="22136-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="22136-109">Das erste Cmdlet erstellt eine Delegierung, die einem Subnetz hinzugefügt werden kann, und speichert Sie in der $Delegation-Variablen.</span><span class="sxs-lookup"><span data-stu-id="22136-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="22136-110">Das zweite und dritte Cmdlets rufen das Subnetz ab, das delegiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="22136-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="22136-111">Das vierte Cmdlet fügt die erstellte Delegierung dem Subnetz von Interesse hinzu, und das endgültige Cmdlet sendet die aktualisierte Konfiguration an den Server.</span><span class="sxs-lookup"><span data-stu-id="22136-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="22136-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="22136-112">PARAMETERS</span></span>

### <span data-ttu-id="22136-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22136-113">-DefaultProfile</span></span>
<span data-ttu-id="22136-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="22136-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22136-115">-Name</span><span class="sxs-lookup"><span data-stu-id="22136-115">-Name</span></span>
<span data-ttu-id="22136-116">Der Name der Delegierung</span><span class="sxs-lookup"><span data-stu-id="22136-116">The name of the delegation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22136-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="22136-117">-ServiceName</span></span>
<span data-ttu-id="22136-118">Der Name des Diensts, an den das Subnetz delegiert werden soll</span><span class="sxs-lookup"><span data-stu-id="22136-118">The name of the service to which the subnet should be delegated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22136-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22136-119">CommonParameters</span></span>
<span data-ttu-id="22136-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22136-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="22136-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22136-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22136-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22136-122">INPUTS</span></span>

### <span data-ttu-id="22136-123">System. String</span><span class="sxs-lookup"><span data-stu-id="22136-123">System.String</span></span>

## <span data-ttu-id="22136-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22136-124">OUTPUTS</span></span>

### <span data-ttu-id="22136-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="22136-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="22136-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="22136-126">NOTES</span></span>

## <span data-ttu-id="22136-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22136-127">RELATED LINKS</span></span>
<span data-ttu-id="22136-128">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Satz-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="22136-128">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
