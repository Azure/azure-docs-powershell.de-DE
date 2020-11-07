---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 88c17626da87608a1086331289cb99f8e7668e5a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841607"
---
# <span data-ttu-id="c951d-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c951d-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="c951d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c951d-102">SYNOPSIS</span></span>
<span data-ttu-id="c951d-103">Ruft ein lokales Netzwerk Gateway ab</span><span class="sxs-lookup"><span data-stu-id="c951d-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="c951d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c951d-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c951d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c951d-105">DESCRIPTION</span></span>
<span data-ttu-id="c951d-106">Das lokale Netzwerk Gateway ist das Objekt, das Ihr VPN-Gerät lokal darstellt.</span><span class="sxs-lookup"><span data-stu-id="c951d-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="c951d-107">Das Cmdlet " **Get-AzLocalNetworkGateway** " gibt das Objekt zurück, das ihr auf-Prem-Gateway basierend auf Name und Ressourcengruppenname darstellt.</span><span class="sxs-lookup"><span data-stu-id="c951d-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="c951d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c951d-108">EXAMPLES</span></span>

### <span data-ttu-id="c951d-109">1: Abrufen eines lokalen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="c951d-109">1: Get a Local Network Gateway</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="c951d-110">Gibt das Objekt des lokalen Netzwerkgateways mit dem Namen "myLocalGW" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="c951d-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="c951d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c951d-111">PARAMETERS</span></span>

### <span data-ttu-id="c951d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c951d-112">-DefaultProfile</span></span>
<span data-ttu-id="c951d-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c951d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c951d-114">-Name</span><span class="sxs-lookup"><span data-stu-id="c951d-114">-Name</span></span>
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

### <span data-ttu-id="c951d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c951d-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c951d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c951d-116">CommonParameters</span></span>
<span data-ttu-id="c951d-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c951d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c951d-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c951d-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c951d-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c951d-119">INPUTS</span></span>

## <span data-ttu-id="c951d-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c951d-120">OUTPUTS</span></span>

### <span data-ttu-id="c951d-121">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c951d-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="c951d-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="c951d-122">NOTES</span></span>

## <span data-ttu-id="c951d-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c951d-123">RELATED LINKS</span></span>

