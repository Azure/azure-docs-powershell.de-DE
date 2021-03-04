---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: f82882a4975c2f873362ece62f6eac9e6b7a53a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940267"
---
# <span data-ttu-id="5ec4e-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5ec4e-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="5ec4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ec4e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec4e-103">Ruft ein Array von URL-Pfadzuordnungen zu einem Back-End-Serverpool ab.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5ec4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ec4e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ec4e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ec4e-105">DESCRIPTION</span></span>
<span data-ttu-id="5ec4e-106">Das **Get-AzApplicationGatewayURLPathMapConfig-Cmdlet** ruft ein Array von URL-Pfadzuordnungen zu einem Back-End-Serverpool ab.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5ec4e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5ec4e-107">EXAMPLES</span></span>

### <span data-ttu-id="5ec4e-108">Beispiel 1: Erstellen einer Urlpfadzuordnungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="5ec4e-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="5ec4e-109">Dieser Befehl ruft die Konfigurationen der URL-Pfadzuordnung vom Back-End-Server ab, der sich auf dem Anwendungsgateway mit dem Namen Gateway befindet.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="5ec4e-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5ec4e-110">PARAMETERS</span></span>

### <span data-ttu-id="5ec4e-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ec4e-111">-ApplicationGateway</span></span>
<span data-ttu-id="5ec4e-112">Gibt das Anwendungsgateway an, zu dem dieses Cmdlet eine URL-Pfadzuordnungskonfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="5ec4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ec4e-113">-DefaultProfile</span></span>
<span data-ttu-id="5ec4e-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ec4e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5ec4e-115">-Name</span></span>
<span data-ttu-id="5ec4e-116">Gibt den Namen der URL-Pfadzuordnung an, in dem dieses Cmdlet die Pfadzuordnungskonfiguration erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ec4e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec4e-117">CommonParameters</span></span>
<span data-ttu-id="5ec4e-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ec4e-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ec4e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec4e-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5ec4e-120">INPUTS</span></span>

### <span data-ttu-id="5ec4e-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ec4e-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ec4e-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5ec4e-122">OUTPUTS</span></span>

### <span data-ttu-id="5ec4e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="5ec4e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="5ec4e-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5ec4e-124">NOTES</span></span>

## <span data-ttu-id="5ec4e-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5ec4e-125">RELATED LINKS</span></span>

[<span data-ttu-id="5ec4e-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5ec4e-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5ec4e-127">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5ec4e-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5ec4e-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5ec4e-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5ec4e-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5ec4e-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


