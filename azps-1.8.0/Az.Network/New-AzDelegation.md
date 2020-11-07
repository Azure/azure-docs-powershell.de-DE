---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 32398b235ef28872730f5839cef52023fe0f4ee9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660566"
---
# <span data-ttu-id="178c7-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="178c7-101">New-AzDelegation</span></span>

## <span data-ttu-id="178c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="178c7-102">SYNOPSIS</span></span>
<span data-ttu-id="178c7-103">Erstellt eine Dienst Delegierung.</span><span class="sxs-lookup"><span data-stu-id="178c7-103">Creates a service delegation.</span></span>

## <span data-ttu-id="178c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="178c7-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="178c7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="178c7-105">DESCRIPTION</span></span>
<span data-ttu-id="178c7-106">Das Cmdlet **New-AzDelegation** erstellt eine Dienst Delegierung, die einem Subnetz hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="178c7-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="178c7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="178c7-107">EXAMPLES</span></span>

### <span data-ttu-id="178c7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="178c7-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="178c7-109">Das erste Cmdlet erstellt eine Delegierung, die einem Subnetz hinzugefügt werden kann, und speichert Sie in der $Delegation-Variablen.</span><span class="sxs-lookup"><span data-stu-id="178c7-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="178c7-110">Das zweite und dritte Cmdlets rufen das Subnetz ab, das delegiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="178c7-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="178c7-111">Das vierte Cmdlet fügt die erstellte Delegierung dem Subnetz von Interesse hinzu, und das endgültige Cmdlet sendet die aktualisierte Konfiguration an den Server.</span><span class="sxs-lookup"><span data-stu-id="178c7-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="178c7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="178c7-112">PARAMETERS</span></span>

### <span data-ttu-id="178c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="178c7-113">-DefaultProfile</span></span>
<span data-ttu-id="178c7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="178c7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="178c7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="178c7-115">-Name</span></span>
<span data-ttu-id="178c7-116">Der Name der Delegierung</span><span class="sxs-lookup"><span data-stu-id="178c7-116">The name of the delegation</span></span>

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

### <span data-ttu-id="178c7-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="178c7-117">-ServiceName</span></span>
<span data-ttu-id="178c7-118">Der Name des Diensts, an den das Subnetz delegiert werden soll</span><span class="sxs-lookup"><span data-stu-id="178c7-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="178c7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178c7-119">CommonParameters</span></span>
<span data-ttu-id="178c7-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="178c7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178c7-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="178c7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178c7-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="178c7-122">INPUTS</span></span>

### <span data-ttu-id="178c7-123">System. String</span><span class="sxs-lookup"><span data-stu-id="178c7-123">System.String</span></span>

## <span data-ttu-id="178c7-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="178c7-124">OUTPUTS</span></span>

### <span data-ttu-id="178c7-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="178c7-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="178c7-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="178c7-126">NOTES</span></span>

## <span data-ttu-id="178c7-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="178c7-127">RELATED LINKS</span></span>

<span data-ttu-id="178c7-128">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Satz-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="178c7-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>