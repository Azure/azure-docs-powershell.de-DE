---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: a7c131db8ce5a3489bc2a869e31b0ef7ab89f3c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663220"
---
# <span data-ttu-id="54717-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="54717-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="54717-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54717-102">SYNOPSIS</span></span>
<span data-ttu-id="54717-103">Ruft die effektive Netzwerksicherheitsgruppe einer Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="54717-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54717-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54717-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54717-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54717-105">DESCRIPTION</span></span>
<span data-ttu-id="54717-106">Das Cmdlet " **Get-AzureRmEffectiveNetworkSecurityGroup** " gibt die effektive Netzwerksicherheitsgruppe zurück, die auf einer Netzwerkschnittstelle angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="54717-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="54717-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54717-107">EXAMPLES</span></span>

### <span data-ttu-id="54717-108">Beispiel 1: Abrufen der effektiven Netzwerksicherheitsgruppe auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="54717-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="54717-109">Dieser Befehl ruft alle effektiven Netzwerksicherheitsregeln ab, die mit der Netzwerkschnittstelle mit dem Namen MyNetworkInterface in der Ressourcengruppe myresourcegroup verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="54717-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="54717-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="54717-110">PARAMETERS</span></span>

### <span data-ttu-id="54717-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54717-111">-DefaultProfile</span></span>
<span data-ttu-id="54717-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="54717-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54717-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="54717-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="54717-114">Hat den Namen einer Netzwerkschnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="54717-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="54717-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54717-115">-ResourceGroupName</span></span>
<span data-ttu-id="54717-116">Gibt die Ressourcengruppe einer Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="54717-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="54717-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54717-117">CommonParameters</span></span>
<span data-ttu-id="54717-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54717-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54717-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54717-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54717-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54717-120">INPUTS</span></span>

### <span data-ttu-id="54717-121">Keine</span><span class="sxs-lookup"><span data-stu-id="54717-121">None</span></span>
<span data-ttu-id="54717-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="54717-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="54717-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54717-123">OUTPUTS</span></span>

### <span data-ttu-id="54717-124">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="54717-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="54717-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="54717-125">NOTES</span></span>

## <span data-ttu-id="54717-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54717-126">RELATED LINKS</span></span>

[<span data-ttu-id="54717-127">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="54717-127">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


