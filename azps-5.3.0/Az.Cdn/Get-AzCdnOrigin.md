---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: e5e27dba4519d16ebc304f3d6cca99f32f23e341
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473201"
---
# <span data-ttu-id="1ebc1-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="1ebc1-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="1ebc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ebc1-102">SYNOPSIS</span></span>
<span data-ttu-id="1ebc1-103">Ruft einen CDN-Origin-Server ab.</span><span class="sxs-lookup"><span data-stu-id="1ebc1-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="1ebc1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ebc1-104">SYNTAX</span></span>

### <span data-ttu-id="1ebc1-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1ebc1-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ebc1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ebc1-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ebc1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ebc1-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ebc1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ebc1-108">DESCRIPTION</span></span>
<span data-ttu-id="1ebc1-109">Das **Cmdlet "Get-AzCdnOrigin"** ruft einen Azure Content Delivery Network (CDN)-Ursprungserver und dessen Konfigurationsdaten ab.</span><span class="sxs-lookup"><span data-stu-id="1ebc1-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="1ebc1-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1ebc1-110">EXAMPLES</span></span>

## <span data-ttu-id="1ebc1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ebc1-111">PARAMETERS</span></span>

### <span data-ttu-id="1ebc1-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ebc1-112">-CdnEndpoint</span></span>
<span data-ttu-id="1ebc1-113">Gibt das CDN-Endpunkt-Objekt an, zu dem der Ursprung gehört.</span><span class="sxs-lookup"><span data-stu-id="1ebc1-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ebc1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ebc1-114">-DefaultProfile</span></span>
<span data-ttu-id="1ebc1-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1ebc1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ebc1-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1ebc1-116">-EndpointName</span></span>
<span data-ttu-id="1ebc1-117">Gibt den Namen des Endpunkts an, zu dem der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="1ebc1-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="1ebc1-118">-OriginName</span><span class="sxs-lookup"><span data-stu-id="1ebc1-118">-OriginName</span></span>
<span data-ttu-id="1ebc1-119">Gibt den Namen des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="1ebc1-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="1ebc1-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1ebc1-120">-ProfileName</span></span>
<span data-ttu-id="1ebc1-121">Gibt den Namen des Profils an, zu dem der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="1ebc1-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="1ebc1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ebc1-122">-ResourceGroupName</span></span>
<span data-ttu-id="1ebc1-123">Gibt den Namen der Ressourcengruppe an, zu der der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="1ebc1-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="1ebc1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ebc1-124">-ResourceId</span></span>
<span data-ttu-id="1ebc1-125">Die Ressourcen-ID des Azure CDN-Ursprungs.</span><span class="sxs-lookup"><span data-stu-id="1ebc1-125">The resource id of the Azure CDN origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ebc1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ebc1-126">CommonParameters</span></span>
<span data-ttu-id="1ebc1-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ebc1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ebc1-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ebc1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ebc1-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1ebc1-129">INPUTS</span></span>

### <span data-ttu-id="1ebc1-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ebc1-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="1ebc1-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1ebc1-131">OUTPUTS</span></span>

### <span data-ttu-id="1ebc1-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="1ebc1-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="1ebc1-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1ebc1-133">NOTES</span></span>

## <span data-ttu-id="1ebc1-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1ebc1-134">RELATED LINKS</span></span>

[<span data-ttu-id="1ebc1-135">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="1ebc1-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


