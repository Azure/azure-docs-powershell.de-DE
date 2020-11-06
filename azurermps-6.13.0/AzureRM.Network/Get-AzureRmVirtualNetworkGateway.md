---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: af925c1de08a5a615f5435bb20377582fedc0089
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505741"
---
# <span data-ttu-id="9737d-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9737d-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="9737d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9737d-102">SYNOPSIS</span></span>
<span data-ttu-id="9737d-103">Ruft ein virtuelles Netzwerk Gateway ab</span><span class="sxs-lookup"><span data-stu-id="9737d-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9737d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9737d-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9737d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9737d-105">DESCRIPTION</span></span>
<span data-ttu-id="9737d-106">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="9737d-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="9737d-107">Das Cmdlet " **Get-AzureRmVirtualNetworkGateway** " gibt das Objekt Ihres Gateways in Azure basierend auf Name und Ressourcengruppennamen zurück.</span><span class="sxs-lookup"><span data-stu-id="9737d-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="9737d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9737d-108">EXAMPLES</span></span>

### <span data-ttu-id="9737d-109">1: Abrufen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="9737d-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="9737d-110">Gibt das Objekt des virtuellen Netzwerkgateways mit dem Namen "mygateway" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="9737d-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="9737d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9737d-111">PARAMETERS</span></span>

### <span data-ttu-id="9737d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9737d-112">-DefaultProfile</span></span>
<span data-ttu-id="9737d-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9737d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9737d-114">-Name</span><span class="sxs-lookup"><span data-stu-id="9737d-114">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9737d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9737d-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="9737d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9737d-116">CommonParameters</span></span>
<span data-ttu-id="9737d-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9737d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9737d-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9737d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9737d-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9737d-119">INPUTS</span></span>

### <span data-ttu-id="9737d-120">System. String</span><span class="sxs-lookup"><span data-stu-id="9737d-120">System.String</span></span>

## <span data-ttu-id="9737d-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9737d-121">OUTPUTS</span></span>

### <span data-ttu-id="9737d-122">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9737d-122">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="9737d-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="9737d-123">NOTES</span></span>

## <span data-ttu-id="9737d-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9737d-124">RELATED LINKS</span></span>
