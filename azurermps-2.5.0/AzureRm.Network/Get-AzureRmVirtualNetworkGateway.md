---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 1700ec112767397653201ff16608afbfb4af8f3e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849204"
---
# <span data-ttu-id="768f7-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="768f7-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="768f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="768f7-102">SYNOPSIS</span></span>
<span data-ttu-id="768f7-103">Ruft ein virtuelles Netzwerk Gateway ab</span><span class="sxs-lookup"><span data-stu-id="768f7-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="768f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="768f7-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="768f7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="768f7-105">DESCRIPTION</span></span>
<span data-ttu-id="768f7-106">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="768f7-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="768f7-107">Das Cmdlet " **Get-AzureRmVirtualNetworkGateway** " gibt das Objekt Ihres Gateways in Azure basierend auf Name und Ressourcengruppennamen zurück.</span><span class="sxs-lookup"><span data-stu-id="768f7-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="768f7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="768f7-108">EXAMPLES</span></span>

### <span data-ttu-id="768f7-109">1: Abrufen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="768f7-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="768f7-110">Gibt das Objekt des virtuellen Netzwerkgateways mit dem Namen "mygateway" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="768f7-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="768f7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="768f7-111">PARAMETERS</span></span>

### <span data-ttu-id="768f7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="768f7-112">-DefaultProfile</span></span>
<span data-ttu-id="768f7-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="768f7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="768f7-114">-Name</span><span class="sxs-lookup"><span data-stu-id="768f7-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="768f7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="768f7-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="768f7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="768f7-116">CommonParameters</span></span>
<span data-ttu-id="768f7-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="768f7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="768f7-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="768f7-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="768f7-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="768f7-119">INPUTS</span></span>

## <span data-ttu-id="768f7-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="768f7-120">OUTPUTS</span></span>

### <span data-ttu-id="768f7-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="768f7-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="768f7-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="768f7-122">NOTES</span></span>

## <span data-ttu-id="768f7-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="768f7-123">RELATED LINKS</span></span>

