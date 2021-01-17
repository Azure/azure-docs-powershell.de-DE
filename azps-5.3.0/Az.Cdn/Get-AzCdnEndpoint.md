---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 5f137543d694ee9d470a1e24d1ba6d52b22cd2e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471015"
---
# <span data-ttu-id="95982-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="95982-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="95982-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95982-102">SYNOPSIS</span></span>
<span data-ttu-id="95982-103">Ruft einen CDN-Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="95982-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="95982-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95982-104">SYNTAX</span></span>

### <span data-ttu-id="95982-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="95982-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95982-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95982-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95982-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95982-107">DESCRIPTION</span></span>
<span data-ttu-id="95982-108">Das **Get-AzCdnEndpoint-Cmdlet** ruft einen Azure Content Delivery Network (CDN)-Endpunkt und die zugehörigen Konfigurationsdaten ab.</span><span class="sxs-lookup"><span data-stu-id="95982-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="95982-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95982-109">EXAMPLES</span></span>

## <span data-ttu-id="95982-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95982-110">PARAMETERS</span></span>

### <span data-ttu-id="95982-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="95982-111">-CdnProfile</span></span>
<span data-ttu-id="95982-112">Gibt das CDN-Profilobjekt an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="95982-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95982-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95982-113">-DefaultProfile</span></span>
<span data-ttu-id="95982-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="95982-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95982-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="95982-115">-EndpointName</span></span>
<span data-ttu-id="95982-116">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="95982-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="95982-117">Der Name des Endpunkts ist nicht der Hostname des Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="95982-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="95982-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="95982-118">-ProfileName</span></span>
<span data-ttu-id="95982-119">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="95982-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95982-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95982-120">-ResourceGroupName</span></span>
<span data-ttu-id="95982-121">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="95982-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95982-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95982-122">CommonParameters</span></span>
<span data-ttu-id="95982-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95982-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95982-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95982-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95982-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95982-125">INPUTS</span></span>

### <span data-ttu-id="95982-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="95982-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="95982-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95982-127">OUTPUTS</span></span>

### <span data-ttu-id="95982-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="95982-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="95982-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="95982-129">NOTES</span></span>

## <span data-ttu-id="95982-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="95982-130">RELATED LINKS</span></span>

[<span data-ttu-id="95982-131">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="95982-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="95982-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="95982-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="95982-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="95982-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="95982-134">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="95982-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="95982-135">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="95982-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


