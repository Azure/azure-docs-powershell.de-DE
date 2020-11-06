---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: c881232c065f8494b962a0e010865cbefe8bc0eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499969"
---
# <span data-ttu-id="39847-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="39847-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="39847-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39847-102">SYNOPSIS</span></span>
<span data-ttu-id="39847-103">Ruft ein lokales Netzwerk Gateway ab</span><span class="sxs-lookup"><span data-stu-id="39847-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39847-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39847-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39847-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39847-105">DESCRIPTION</span></span>
<span data-ttu-id="39847-106">Das lokale Netzwerk Gateway ist das Objekt, das Ihr VPN-Gerät lokal darstellt.</span><span class="sxs-lookup"><span data-stu-id="39847-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="39847-107">Das Cmdlet " **Get-AzureRmLocalNetworkGateway** " gibt das Objekt zurück, das ihr auf-Prem-Gateway basierend auf Name und Ressourcengruppenname darstellt.</span><span class="sxs-lookup"><span data-stu-id="39847-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="39847-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39847-108">EXAMPLES</span></span>

### <span data-ttu-id="39847-109">1: Abrufen eines lokalen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="39847-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="39847-110">Gibt das Objekt des lokalen Netzwerkgateways mit dem Namen "myLocalGW" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="39847-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="39847-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="39847-111">PARAMETERS</span></span>

### <span data-ttu-id="39847-112">-Name</span><span class="sxs-lookup"><span data-stu-id="39847-112">-Name</span></span>
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

### <span data-ttu-id="39847-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39847-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="39847-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39847-114">-DefaultProfile</span></span>
<span data-ttu-id="39847-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39847-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39847-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39847-116">CommonParameters</span></span>
<span data-ttu-id="39847-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39847-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39847-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39847-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39847-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39847-119">INPUTS</span></span>

## <span data-ttu-id="39847-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39847-120">OUTPUTS</span></span>

### <span data-ttu-id="39847-121">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="39847-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="39847-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="39847-122">NOTES</span></span>

## <span data-ttu-id="39847-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39847-123">RELATED LINKS</span></span>

