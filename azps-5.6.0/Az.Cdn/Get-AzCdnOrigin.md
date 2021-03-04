---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: 5c2aa677bd2f197cfae262ed54372d5172fe2a4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947248"
---
# <span data-ttu-id="bdd7f-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="bdd7f-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="bdd7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdd7f-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd7f-103">Ruft einen CDN-Ursprungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="bdd7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdd7f-104">SYNTAX</span></span>

### <span data-ttu-id="bdd7f-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bdd7f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdd7f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdd7f-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bdd7f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdd7f-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bdd7f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bdd7f-108">DESCRIPTION</span></span>
<span data-ttu-id="bdd7f-109">Das **Get-AzCdnOrigin-Cmdlet** ruft einen Azure Content Delivery Network (CDN)-Ursprungsserver und seine Konfigurationsdaten ab.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="bdd7f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bdd7f-110">EXAMPLES</span></span>

## <span data-ttu-id="bdd7f-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bdd7f-111">PARAMETERS</span></span>

### <span data-ttu-id="bdd7f-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bdd7f-112">-CdnEndpoint</span></span>
<span data-ttu-id="bdd7f-113">Gibt das CDN-Endpunktobjekt an, zu dem der Ursprung gehört.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="bdd7f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd7f-114">-DefaultProfile</span></span>
<span data-ttu-id="bdd7f-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bdd7f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdd7f-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bdd7f-116">-EndpointName</span></span>
<span data-ttu-id="bdd7f-117">Gibt den Namen des Endpunkts an, zu dem der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="bdd7f-118">-OriginName</span><span class="sxs-lookup"><span data-stu-id="bdd7f-118">-OriginName</span></span>
<span data-ttu-id="bdd7f-119">Gibt den Namen des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="bdd7f-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="bdd7f-120">-ProfileName</span></span>
<span data-ttu-id="bdd7f-121">Gibt den Namen des Profils an, dem der Ursprungsserver angehört.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="bdd7f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdd7f-122">-ResourceGroupName</span></span>
<span data-ttu-id="bdd7f-123">Gibt den Namen der Ressourcengruppe an, zu der der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="bdd7f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdd7f-124">-ResourceId</span></span>
<span data-ttu-id="bdd7f-125">Die Ressourcen-ID des Azure CDN-Ursprungs.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-125">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="bdd7f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd7f-126">CommonParameters</span></span>
<span data-ttu-id="bdd7f-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdd7f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd7f-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdd7f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd7f-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bdd7f-129">INPUTS</span></span>

### <span data-ttu-id="bdd7f-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="bdd7f-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="bdd7f-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bdd7f-131">OUTPUTS</span></span>

### <span data-ttu-id="bdd7f-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="bdd7f-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="bdd7f-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bdd7f-133">NOTES</span></span>

## <span data-ttu-id="bdd7f-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bdd7f-134">RELATED LINKS</span></span>

[<span data-ttu-id="bdd7f-135">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="bdd7f-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


