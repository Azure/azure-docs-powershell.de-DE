---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: d479c66b899637f2dc12061b7499fc65b7d59d66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497821"
---
# <span data-ttu-id="5ae3e-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5ae3e-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="5ae3e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ae3e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ae3e-103">Ruft die effektive Netzwerksicherheitsgruppe einer Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="5ae3e-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ae3e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ae3e-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ae3e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ae3e-105">DESCRIPTION</span></span>
<span data-ttu-id="5ae3e-106">Das Cmdlet " **Get-AzureRmEffectiveNetworkSecurityGroup** " gibt die effektive Netzwerksicherheitsgruppe zurück, die auf einer Netzwerkschnittstelle angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ae3e-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="5ae3e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ae3e-107">EXAMPLES</span></span>

### <span data-ttu-id="5ae3e-108">Beispiel 1: Abrufen der effektiven Netzwerksicherheitsgruppe auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="5ae3e-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="5ae3e-109">Dieser Befehl ruft alle effektiven Netzwerksicherheitsregeln ab, die mit der Netzwerkschnittstelle mit dem Namen MyNetworkInterface in der Ressourcengruppe myresourcegroup verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="5ae3e-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="5ae3e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ae3e-110">PARAMETERS</span></span>

### <span data-ttu-id="5ae3e-111">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="5ae3e-111">-NetworkInterfaceName</span></span>
<span data-ttu-id="5ae3e-112">Hat den Namen einer Netzwerkschnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="5ae3e-112">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="5ae3e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ae3e-113">-ResourceGroupName</span></span>
<span data-ttu-id="5ae3e-114">Gibt die Ressourcengruppe einer Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="5ae3e-114">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="5ae3e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ae3e-115">-DefaultProfile</span></span>
<span data-ttu-id="5ae3e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5ae3e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ae3e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ae3e-117">CommonParameters</span></span>
<span data-ttu-id="5ae3e-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ae3e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ae3e-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ae3e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ae3e-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ae3e-120">INPUTS</span></span>

## <span data-ttu-id="5ae3e-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ae3e-121">OUTPUTS</span></span>

### <span data-ttu-id="5ae3e-122">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5ae3e-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="5ae3e-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ae3e-123">NOTES</span></span>

## <span data-ttu-id="5ae3e-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ae3e-124">RELATED LINKS</span></span>

[<span data-ttu-id="5ae3e-125">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="5ae3e-125">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


