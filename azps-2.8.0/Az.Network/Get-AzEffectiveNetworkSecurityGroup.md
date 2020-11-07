---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: c9dd7695e195386b9dd0921b4a9161a5fb175c6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821875"
---
# <span data-ttu-id="65e94-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="65e94-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="65e94-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65e94-102">SYNOPSIS</span></span>
<span data-ttu-id="65e94-103">Ruft die effektive Netzwerksicherheitsgruppe einer Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="65e94-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="65e94-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65e94-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65e94-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65e94-105">DESCRIPTION</span></span>
<span data-ttu-id="65e94-106">Das Cmdlet " **Get-AzEffectiveNetworkSecurityGroup** " gibt die effektive Netzwerksicherheitsgruppe zurück, die auf einer Netzwerkschnittstelle angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="65e94-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="65e94-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65e94-107">EXAMPLES</span></span>

### <span data-ttu-id="65e94-108">Beispiel 1: Abrufen der effektiven Netzwerksicherheitsgruppe auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="65e94-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="65e94-109">Dieser Befehl ruft alle effektiven Netzwerksicherheitsregeln ab, die mit der Netzwerkschnittstelle mit dem Namen MyNetworkInterface in der Ressourcengruppe myresourcegroup verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="65e94-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="65e94-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="65e94-110">PARAMETERS</span></span>

### <span data-ttu-id="65e94-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65e94-111">-DefaultProfile</span></span>
<span data-ttu-id="65e94-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65e94-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65e94-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="65e94-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="65e94-114">Hat den Namen einer Netzwerkschnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="65e94-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="65e94-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65e94-115">-ResourceGroupName</span></span>
<span data-ttu-id="65e94-116">Gibt die Ressourcengruppe einer Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="65e94-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="65e94-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e94-117">CommonParameters</span></span>
<span data-ttu-id="65e94-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65e94-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65e94-119">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65e94-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e94-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65e94-120">INPUTS</span></span>

### <span data-ttu-id="65e94-121">System. String</span><span class="sxs-lookup"><span data-stu-id="65e94-121">System.String</span></span>

## <span data-ttu-id="65e94-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65e94-122">OUTPUTS</span></span>

### <span data-ttu-id="65e94-123">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="65e94-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="65e94-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="65e94-124">NOTES</span></span>

## <span data-ttu-id="65e94-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65e94-125">RELATED LINKS</span></span>

[<span data-ttu-id="65e94-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="65e94-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


