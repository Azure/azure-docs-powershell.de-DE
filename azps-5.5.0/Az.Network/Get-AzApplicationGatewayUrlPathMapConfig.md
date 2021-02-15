---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 50f80f8c7a191c43bb9e8b6b4aed5f44d1ecb85a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159228"
---
# <span data-ttu-id="38635-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="38635-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="38635-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38635-102">SYNOPSIS</span></span>
<span data-ttu-id="38635-103">Ruft ein Array von URL-Pfadzuordnungen zu einem Back-End-Server-Pool ab.</span><span class="sxs-lookup"><span data-stu-id="38635-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="38635-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38635-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38635-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38635-105">DESCRIPTION</span></span>
<span data-ttu-id="38635-106">Das **Cmdlet "Get-AzApplicationGatewayURLPathMapConfig"** ruft ein Array von URL-Pfadzuordnungen zu einem Back-End-Serverpool ab.</span><span class="sxs-lookup"><span data-stu-id="38635-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="38635-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38635-107">EXAMPLES</span></span>

### <span data-ttu-id="38635-108">Beispiel 1: Erhalten der Konfiguration einer URL-Pfadzuordnung</span><span class="sxs-lookup"><span data-stu-id="38635-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="38635-109">Dieser Befehl ruft die Konfigurationen der URL-Pfadzuordnung vom Back-End-Server ab, der sich auf dem Anwendungsgateway namens Gateway befindet.</span><span class="sxs-lookup"><span data-stu-id="38635-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="38635-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38635-110">PARAMETERS</span></span>

### <span data-ttu-id="38635-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38635-111">-ApplicationGateway</span></span>
<span data-ttu-id="38635-112">Gibt das Anwendungsgateway an, zu dem dieses Cmdlet eine Konfiguration der URL-Pfadzuordnung erhält.</span><span class="sxs-lookup"><span data-stu-id="38635-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="38635-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38635-113">-DefaultProfile</span></span>
<span data-ttu-id="38635-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38635-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38635-115">-Name</span><span class="sxs-lookup"><span data-stu-id="38635-115">-Name</span></span>
<span data-ttu-id="38635-116">Gibt den Namen der URL-Pfadzuordnung an, in der dieses Cmdlet die Pfadzuordnungskonfiguration abbekommt.</span><span class="sxs-lookup"><span data-stu-id="38635-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="38635-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38635-117">CommonParameters</span></span>
<span data-ttu-id="38635-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38635-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38635-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38635-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38635-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38635-120">INPUTS</span></span>

### <span data-ttu-id="38635-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38635-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="38635-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38635-122">OUTPUTS</span></span>

### <span data-ttu-id="38635-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="38635-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="38635-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="38635-124">NOTES</span></span>

## <span data-ttu-id="38635-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="38635-125">RELATED LINKS</span></span>

[<span data-ttu-id="38635-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="38635-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="38635-127">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="38635-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="38635-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="38635-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="38635-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="38635-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


