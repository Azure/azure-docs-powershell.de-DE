---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: a960d5b2f6daf19fc4e46eb253b596eb88e6bd71
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841683"
---
# <span data-ttu-id="5a240-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5a240-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="5a240-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a240-102">SYNOPSIS</span></span>
<span data-ttu-id="5a240-103">Ruft die effektive Netzwerksicherheitsgruppe einer Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="5a240-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="5a240-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a240-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a240-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a240-105">DESCRIPTION</span></span>
<span data-ttu-id="5a240-106">Das Cmdlet " **Get-AzEffectiveNetworkSecurityGroup** " gibt die effektive Netzwerksicherheitsgruppe zurück, die auf einer Netzwerkschnittstelle angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a240-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="5a240-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a240-107">EXAMPLES</span></span>

### <span data-ttu-id="5a240-108">Beispiel 1: Abrufen der effektiven Netzwerksicherheitsgruppe auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="5a240-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="5a240-109">Dieser Befehl ruft alle effektiven Netzwerksicherheitsregeln ab, die mit der Netzwerkschnittstelle mit dem Namen MyNetworkInterface in der Ressourcengruppe myresourcegroup verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="5a240-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="5a240-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a240-110">PARAMETERS</span></span>

### <span data-ttu-id="5a240-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a240-111">-DefaultProfile</span></span>
<span data-ttu-id="5a240-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a240-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a240-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="5a240-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="5a240-114">Hat den Namen einer Netzwerkschnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="5a240-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="5a240-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a240-115">-ResourceGroupName</span></span>
<span data-ttu-id="5a240-116">Gibt die Ressourcengruppe einer Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="5a240-116">Specifies the resource group of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a240-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a240-117">CommonParameters</span></span>
<span data-ttu-id="5a240-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a240-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a240-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a240-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a240-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a240-120">INPUTS</span></span>

## <span data-ttu-id="5a240-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a240-121">OUTPUTS</span></span>

### <span data-ttu-id="5a240-122">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5a240-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="5a240-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a240-123">NOTES</span></span>

## <span data-ttu-id="5a240-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a240-124">RELATED LINKS</span></span>

[<span data-ttu-id="5a240-125">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="5a240-125">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


