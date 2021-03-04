---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: 38f7d6780b598606d0a0938178309ed67e602315
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926576"
---
# <span data-ttu-id="935fe-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="935fe-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="935fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="935fe-102">SYNOPSIS</span></span>
<span data-ttu-id="935fe-103">Ruft die effektive Netzwerksicherheitsgruppe einer Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="935fe-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="935fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="935fe-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="935fe-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="935fe-105">DESCRIPTION</span></span>
<span data-ttu-id="935fe-106">Das **Get-AzEffectiveNetworkSecurityGroup-Cmdlet** gibt die effektive Netzwerksicherheitsgruppe zurück, die auf eine Netzwerkschnittstelle angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="935fe-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="935fe-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="935fe-107">EXAMPLES</span></span>

### <span data-ttu-id="935fe-108">Beispiel 1: Erhalten der effektiven Netzwerksicherheitsgruppe auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="935fe-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="935fe-109">Dieser Befehl ruft alle effektiven Netzwerksicherheitsregeln ab, die der Netzwerkschnittstelle "MyNetworkInterface" in der Ressourcengruppe "myResourceGroup" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="935fe-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="935fe-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="935fe-110">PARAMETERS</span></span>

### <span data-ttu-id="935fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935fe-111">-DefaultProfile</span></span>
<span data-ttu-id="935fe-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="935fe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="935fe-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="935fe-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="935fe-114">Hat den Namen einer Netzwerkschnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="935fe-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="935fe-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="935fe-115">-ResourceGroupName</span></span>
<span data-ttu-id="935fe-116">Gibt die Ressourcengruppe einer Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="935fe-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="935fe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935fe-117">CommonParameters</span></span>
<span data-ttu-id="935fe-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="935fe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935fe-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="935fe-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935fe-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="935fe-120">INPUTS</span></span>

### <span data-ttu-id="935fe-121">System.String</span><span class="sxs-lookup"><span data-stu-id="935fe-121">System.String</span></span>

## <span data-ttu-id="935fe-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="935fe-122">OUTPUTS</span></span>

### <span data-ttu-id="935fe-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="935fe-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="935fe-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="935fe-124">NOTES</span></span>

## <span data-ttu-id="935fe-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="935fe-125">RELATED LINKS</span></span>

[<span data-ttu-id="935fe-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="935fe-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


