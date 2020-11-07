---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: dd7ad8110afad4302c393295599ed1ef9d6fd4bf
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848464"
---
# <span data-ttu-id="8b0f4-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8b0f4-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="8b0f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b0f4-102">SYNOPSIS</span></span>
<span data-ttu-id="8b0f4-103">Ruft ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool ab.</span><span class="sxs-lookup"><span data-stu-id="8b0f4-103">Gets an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b0f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b0f4-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b0f4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b0f4-105">DESCRIPTION</span></span>
<span data-ttu-id="8b0f4-106">Das Cmdlet " **Get-AzureRmApplicationGatewayURLPathMapConfig** " Ruft ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool ab.</span><span class="sxs-lookup"><span data-stu-id="8b0f4-106">The **Get-AzureRmApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="8b0f4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b0f4-107">EXAMPLES</span></span>

### <span data-ttu-id="8b0f4-108">Beispiel 1: Abrufen einer URL-Pfad Zuordnungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="8b0f4-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="8b0f4-109">Dieser Befehl ruft die URL-Pfad Zuordnungs Konfigurationen vom Back-End-Server ab, der sich auf dem Application Gateway mit dem Namen Gateway befindet.</span><span class="sxs-lookup"><span data-stu-id="8b0f4-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="8b0f4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b0f4-110">PARAMETERS</span></span>

### <span data-ttu-id="8b0f4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b0f4-111">-ApplicationGateway</span></span>
<span data-ttu-id="8b0f4-112">Gibt das Anwendungsgateway an, für das dieses Cmdlet eine URL-Pfad Zuordnungskonfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="8b0f4-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="8b0f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b0f4-113">-DefaultProfile</span></span>
<span data-ttu-id="8b0f4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b0f4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b0f4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8b0f4-115">-Name</span></span>
<span data-ttu-id="8b0f4-116">Gibt den URL-Pfad Zuordnungsnamen an, in dem dieses Cmdlet die Pfad Zuordnungskonfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="8b0f4-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0f4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b0f4-117">CommonParameters</span></span>
<span data-ttu-id="8b0f4-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b0f4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b0f4-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b0f4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b0f4-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b0f4-120">INPUTS</span></span>

### <span data-ttu-id="8b0f4-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b0f4-121">PSApplicationGateway</span></span>
<span data-ttu-id="8b0f4-122">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8b0f4-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="8b0f4-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b0f4-123">OUTPUTS</span></span>

### <span data-ttu-id="8b0f4-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="8b0f4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="8b0f4-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap]</span><span class="sxs-lookup"><span data-stu-id="8b0f4-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="8b0f4-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b0f4-126">NOTES</span></span>

## <span data-ttu-id="8b0f4-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b0f4-127">RELATED LINKS</span></span>

[<span data-ttu-id="8b0f4-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8b0f4-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="8b0f4-129">Neu – AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8b0f4-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="8b0f4-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8b0f4-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="8b0f4-131">Satz-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8b0f4-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


