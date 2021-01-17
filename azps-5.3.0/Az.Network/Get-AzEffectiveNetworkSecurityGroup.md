---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: c0f7d2692472316d018d4a11b6843264c8666fe2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380189"
---
# <span data-ttu-id="45b24-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="45b24-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="45b24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45b24-102">SYNOPSIS</span></span>
<span data-ttu-id="45b24-103">Ruft die effektive Netzwerksicherheitsgruppe einer Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="45b24-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="45b24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45b24-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45b24-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45b24-105">DESCRIPTION</span></span>
<span data-ttu-id="45b24-106">Das **Cmdlet "Get-AzEffectiveNetworkSecurityGroup"** gibt die effektive Netzwerksicherheitsgruppe zurück, die auf eine Netzwerkschnittstelle angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="45b24-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="45b24-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="45b24-107">EXAMPLES</span></span>

### <span data-ttu-id="45b24-108">Beispiel 1: Herstellen der effektiven Netzwerksicherheitsgruppe auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="45b24-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="45b24-109">Dieser Befehl ruft alle effektiven Netzwerksicherheitsregeln ab, die der Netzwerkschnittstelle "MyNetworkInterface" in der Ressourcengruppe mit dem Namen "myResourceGroup" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="45b24-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="45b24-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45b24-110">PARAMETERS</span></span>

### <span data-ttu-id="45b24-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b24-111">-DefaultProfile</span></span>
<span data-ttu-id="45b24-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45b24-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45b24-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="45b24-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="45b24-114">Der Name einer Netzwerkschnittstelle wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="45b24-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="45b24-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45b24-115">-ResourceGroupName</span></span>
<span data-ttu-id="45b24-116">Gibt die Ressourcengruppe einer Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="45b24-116">Specifies the resource group of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45b24-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b24-117">CommonParameters</span></span>
<span data-ttu-id="45b24-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b24-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b24-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45b24-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b24-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="45b24-120">INPUTS</span></span>

### <span data-ttu-id="45b24-121">System.String</span><span class="sxs-lookup"><span data-stu-id="45b24-121">System.String</span></span>

## <span data-ttu-id="45b24-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="45b24-122">OUTPUTS</span></span>

### <span data-ttu-id="45b24-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="45b24-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="45b24-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="45b24-124">NOTES</span></span>

## <span data-ttu-id="45b24-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="45b24-125">RELATED LINKS</span></span>

[<span data-ttu-id="45b24-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="45b24-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


