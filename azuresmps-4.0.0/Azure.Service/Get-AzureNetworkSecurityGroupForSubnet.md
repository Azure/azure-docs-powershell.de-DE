---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4D75240C-F2B5-4273-848C-107308DD6837
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d56de5b27565f7bfdd90198ad45e2766da521f4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005844"
---
# <span data-ttu-id="f16e6-101">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="f16e6-101">Get-AzureNetworkSecurityGroupForSubnet</span></span>

## <span data-ttu-id="f16e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f16e6-102">SYNOPSIS</span></span>
<span data-ttu-id="f16e6-103">Ruft die Netzwerksicherheitsgruppe für ein Subnetz ab.</span><span class="sxs-lookup"><span data-stu-id="f16e6-103">Gets the network security group for a subnet.</span></span>

## <span data-ttu-id="f16e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f16e6-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupForSubnet -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f16e6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f16e6-105">DESCRIPTION</span></span>
<span data-ttu-id="f16e6-106">Das Cmdlet " **Get-AzureNetworkSecurityGroupForSubnet** " Ruft die Netzwerksicherheitsgruppe ab, die einem Subnetz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f16e6-106">The **Get-AzureNetworkSecurityGroupForSubnet** cmdlet gets the network security group that is associated to a subnet.</span></span>

## <span data-ttu-id="f16e6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f16e6-107">EXAMPLES</span></span>

## <span data-ttu-id="f16e6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f16e6-108">PARAMETERS</span></span>

### <span data-ttu-id="f16e6-109">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="f16e6-109">-Detailed</span></span>
<span data-ttu-id="f16e6-110">Gibt an, dass dieses Cmdlet die Netzwerksicherheitsregeln anzeigt.</span><span class="sxs-lookup"><span data-stu-id="f16e6-110">Indicates that this cmdlet displays the network security rules.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f16e6-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="f16e6-111">-Profile</span></span>
<span data-ttu-id="f16e6-112">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f16e6-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f16e6-113">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f16e6-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f16e6-114">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f16e6-114">-SubnetName</span></span>
<span data-ttu-id="f16e6-115">Gibt den Namen eines Subnets an, für das dieses Cmdlet eine Netzwerksicherheitsgruppe erhält.</span><span class="sxs-lookup"><span data-stu-id="f16e6-115">Specifies the name of a subnet for which this cmdlet gets a network security group.</span></span>

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

### <span data-ttu-id="f16e6-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f16e6-116">-VirtualNetworkName</span></span>
<span data-ttu-id="f16e6-117">Gibt den Namen eines virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="f16e6-117">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="f16e6-118">Dieses Cmdlet ruft eine Netzwerksicherheitsgruppe für ein Subnetz im virtuellen Netzwerk ab, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f16e6-118">This cmdlet gets a network security group for a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="f16e6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f16e6-119">CommonParameters</span></span>
<span data-ttu-id="f16e6-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f16e6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f16e6-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f16e6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f16e6-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f16e6-122">INPUTS</span></span>

## <span data-ttu-id="f16e6-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f16e6-123">OUTPUTS</span></span>

## <span data-ttu-id="f16e6-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="f16e6-124">NOTES</span></span>

## <span data-ttu-id="f16e6-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f16e6-125">RELATED LINKS</span></span>

[<span data-ttu-id="f16e6-126">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="f16e6-126">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)

[<span data-ttu-id="f16e6-127">Satz-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="f16e6-127">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)
