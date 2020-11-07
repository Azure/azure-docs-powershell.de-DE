---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: a0885534311dfef4498c9fc71be7f82d16b05277
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848736"
---
# <span data-ttu-id="46ca5-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="46ca5-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="46ca5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="46ca5-103">Entfernt URL-Pfad Zuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="46ca5-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46ca5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46ca5-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46ca5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46ca5-105">DESCRIPTION</span></span>
<span data-ttu-id="46ca5-106">Das Cmdlet **Remove-AzureRmApplicationGatewayUrlPathMapConfig** entfernt URL-Pfad Zuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="46ca5-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="46ca5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46ca5-107">EXAMPLES</span></span>

### <span data-ttu-id="46ca5-108">1:</span><span class="sxs-lookup"><span data-stu-id="46ca5-108">1:</span></span>
```

```

## <span data-ttu-id="46ca5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="46ca5-109">PARAMETERS</span></span>

### <span data-ttu-id="46ca5-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="46ca5-110">-ApplicationGateway</span></span>
<span data-ttu-id="46ca5-111">Gibt das Anwendungsgateway an, auf das dieses Cmdlet die URL-Pfad Zuordnungskonfiguration entfernt.</span><span class="sxs-lookup"><span data-stu-id="46ca5-111">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46ca5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ca5-112">-DefaultProfile</span></span>
<span data-ttu-id="46ca5-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46ca5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46ca5-114">-Name</span><span class="sxs-lookup"><span data-stu-id="46ca5-114">-Name</span></span>
<span data-ttu-id="46ca5-115">Gibt den URL-Pfad Zuordnungsnamen an, den dieses Cmdlet vom Back-End-Server entfernt.</span><span class="sxs-lookup"><span data-stu-id="46ca5-115">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ca5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ca5-116">CommonParameters</span></span>
<span data-ttu-id="46ca5-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46ca5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ca5-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46ca5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ca5-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46ca5-119">INPUTS</span></span>

### <span data-ttu-id="46ca5-120">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="46ca5-120">PSApplicationGateway</span></span>
<span data-ttu-id="46ca5-121">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="46ca5-121">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="46ca5-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46ca5-122">OUTPUTS</span></span>

### <span data-ttu-id="46ca5-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="46ca5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="46ca5-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="46ca5-124">NOTES</span></span>

## <span data-ttu-id="46ca5-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46ca5-125">RELATED LINKS</span></span>

[<span data-ttu-id="46ca5-126">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="46ca5-126">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="46ca5-127">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="46ca5-127">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="46ca5-128">Neu – AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="46ca5-128">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="46ca5-129">Satz-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="46ca5-129">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


