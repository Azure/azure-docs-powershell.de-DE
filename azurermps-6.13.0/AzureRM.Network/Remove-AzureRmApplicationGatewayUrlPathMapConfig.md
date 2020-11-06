---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 68676c05757a58f2c1094e36338d17a52de6b040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479478"
---
# <span data-ttu-id="827e4-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="827e4-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="827e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="827e4-102">SYNOPSIS</span></span>
<span data-ttu-id="827e4-103">Entfernt URL-Pfad Zuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="827e4-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="827e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="827e4-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="827e4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="827e4-105">DESCRIPTION</span></span>
<span data-ttu-id="827e4-106">Das Cmdlet **Remove-AzureRmApplicationGatewayUrlPathMapConfig** entfernt URL-Pfad Zuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="827e4-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="827e4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="827e4-107">EXAMPLES</span></span>

## <span data-ttu-id="827e4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="827e4-108">PARAMETERS</span></span>

### <span data-ttu-id="827e4-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="827e4-109">-ApplicationGateway</span></span>
<span data-ttu-id="827e4-110">Gibt das Anwendungsgateway an, auf das dieses Cmdlet die URL-Pfad Zuordnungskonfiguration entfernt.</span><span class="sxs-lookup"><span data-stu-id="827e4-110">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="827e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="827e4-111">-DefaultProfile</span></span>
<span data-ttu-id="827e4-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="827e4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="827e4-113">-Name</span><span class="sxs-lookup"><span data-stu-id="827e4-113">-Name</span></span>
<span data-ttu-id="827e4-114">Gibt den URL-Pfad Zuordnungsnamen an, den dieses Cmdlet vom Back-End-Server entfernt.</span><span class="sxs-lookup"><span data-stu-id="827e4-114">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="827e4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="827e4-115">CommonParameters</span></span>
<span data-ttu-id="827e4-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="827e4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="827e4-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="827e4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="827e4-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="827e4-118">INPUTS</span></span>

### <span data-ttu-id="827e4-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="827e4-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="827e4-120">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="827e4-120">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="827e4-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="827e4-121">OUTPUTS</span></span>

### <span data-ttu-id="827e4-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="827e4-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="827e4-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="827e4-123">NOTES</span></span>

## <span data-ttu-id="827e4-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="827e4-124">RELATED LINKS</span></span>

[<span data-ttu-id="827e4-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="827e4-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="827e4-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="827e4-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="827e4-127">Neu – AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="827e4-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="827e4-128">Satz-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="827e4-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


