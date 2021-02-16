---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 5f137543d694ee9d470a1e24d1ba6d52b22cd2e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168060"
---
# <span data-ttu-id="52689-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52689-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="52689-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52689-102">SYNOPSIS</span></span>
<span data-ttu-id="52689-103">Ruft einen CDN-Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="52689-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="52689-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52689-104">SYNTAX</span></span>

### <span data-ttu-id="52689-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="52689-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52689-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52689-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52689-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52689-107">DESCRIPTION</span></span>
<span data-ttu-id="52689-108">Das **Get-AzCdnEndpoint-Cmdlet** ruft einen Azure Content Delivery Network (CDN)-Endpunkt und die zugehörigen Konfigurationsdaten ab.</span><span class="sxs-lookup"><span data-stu-id="52689-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="52689-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="52689-109">EXAMPLES</span></span>

## <span data-ttu-id="52689-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52689-110">PARAMETERS</span></span>

### <span data-ttu-id="52689-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="52689-111">-CdnProfile</span></span>
<span data-ttu-id="52689-112">Gibt das CDN-Profilobjekt an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="52689-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="52689-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52689-113">-DefaultProfile</span></span>
<span data-ttu-id="52689-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="52689-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52689-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="52689-115">-EndpointName</span></span>
<span data-ttu-id="52689-116">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="52689-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="52689-117">Der Name des Endpunkts ist nicht der Hostname des Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="52689-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="52689-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="52689-118">-ProfileName</span></span>
<span data-ttu-id="52689-119">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="52689-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="52689-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52689-120">-ResourceGroupName</span></span>
<span data-ttu-id="52689-121">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="52689-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="52689-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52689-122">CommonParameters</span></span>
<span data-ttu-id="52689-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52689-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52689-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52689-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52689-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="52689-125">INPUTS</span></span>

### <span data-ttu-id="52689-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="52689-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="52689-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="52689-127">OUTPUTS</span></span>

### <span data-ttu-id="52689-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="52689-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="52689-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="52689-129">NOTES</span></span>

## <span data-ttu-id="52689-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="52689-130">RELATED LINKS</span></span>

[<span data-ttu-id="52689-131">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52689-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="52689-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52689-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="52689-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52689-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="52689-134">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52689-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="52689-135">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52689-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


