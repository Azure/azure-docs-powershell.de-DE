---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 1a2a8aa8405be5dfc5275a07d253f06f1134e3e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849612"
---
# <span data-ttu-id="723c2-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="723c2-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="723c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="723c2-102">SYNOPSIS</span></span>
<span data-ttu-id="723c2-103">Ruft ein lokales Netzwerk Gateway ab</span><span class="sxs-lookup"><span data-stu-id="723c2-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="723c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="723c2-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="723c2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="723c2-105">DESCRIPTION</span></span>
<span data-ttu-id="723c2-106">Das lokale Netzwerk Gateway ist das Objekt, das Ihr VPN-Gerät lokal darstellt.</span><span class="sxs-lookup"><span data-stu-id="723c2-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="723c2-107">Das Cmdlet " **Get-AzureRmLocalNetworkGateway** " gibt das Objekt zurück, das ihr auf-Prem-Gateway basierend auf Name und Ressourcengruppenname darstellt.</span><span class="sxs-lookup"><span data-stu-id="723c2-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="723c2-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="723c2-108">EXAMPLES</span></span>

### <span data-ttu-id="723c2-109">1: Abrufen eines lokalen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="723c2-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="723c2-110">Gibt das Objekt des lokalen Netzwerkgateways mit dem Namen "myLocalGW" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="723c2-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="723c2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="723c2-111">PARAMETERS</span></span>

### <span data-ttu-id="723c2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="723c2-112">-DefaultProfile</span></span>
<span data-ttu-id="723c2-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="723c2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="723c2-114">-Name</span><span class="sxs-lookup"><span data-stu-id="723c2-114">-Name</span></span>
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

### <span data-ttu-id="723c2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="723c2-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="723c2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="723c2-116">CommonParameters</span></span>
<span data-ttu-id="723c2-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="723c2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="723c2-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="723c2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="723c2-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="723c2-119">INPUTS</span></span>

## <span data-ttu-id="723c2-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="723c2-120">OUTPUTS</span></span>

### <span data-ttu-id="723c2-121">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="723c2-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="723c2-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="723c2-122">NOTES</span></span>

## <span data-ttu-id="723c2-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="723c2-123">RELATED LINKS</span></span>

