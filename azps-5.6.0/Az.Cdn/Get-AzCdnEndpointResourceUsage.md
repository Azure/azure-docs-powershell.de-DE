---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: d39bd2d3a10f1ff8512b54cdf45902fb10f6810d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950320"
---
# <span data-ttu-id="ec180-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="ec180-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="ec180-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec180-102">SYNOPSIS</span></span>
<span data-ttu-id="ec180-103">Ruft die Ressourcennutzung eines CDN-Endpunkts ab.</span><span class="sxs-lookup"><span data-stu-id="ec180-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="ec180-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec180-104">SYNTAX</span></span>

### <span data-ttu-id="ec180-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ec180-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec180-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec180-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec180-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec180-107">DESCRIPTION</span></span>
<span data-ttu-id="ec180-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="ec180-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ec180-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ec180-109">EXAMPLES</span></span>

### <span data-ttu-id="ec180-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ec180-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ec180-111">{{ Beispielbeschreibung hier hinzufügen }}</span><span class="sxs-lookup"><span data-stu-id="ec180-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="ec180-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ec180-112">PARAMETERS</span></span>

### <span data-ttu-id="ec180-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec180-113">-CdnEndpoint</span></span>
<span data-ttu-id="ec180-114">Das CDN-Endpunktobjekt.</span><span class="sxs-lookup"><span data-stu-id="ec180-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="ec180-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec180-115">-DefaultProfile</span></span>
<span data-ttu-id="ec180-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ec180-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec180-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ec180-117">-EndpointName</span></span>
<span data-ttu-id="ec180-118">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="ec180-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="ec180-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ec180-119">-ProfileName</span></span>
<span data-ttu-id="ec180-120">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="ec180-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="ec180-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec180-121">-ResourceGroupName</span></span>
<span data-ttu-id="ec180-122">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="ec180-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="ec180-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec180-123">CommonParameters</span></span>
<span data-ttu-id="ec180-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec180-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec180-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec180-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec180-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ec180-126">INPUTS</span></span>

### <span data-ttu-id="ec180-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec180-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="ec180-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ec180-128">OUTPUTS</span></span>

### <span data-ttu-id="ec180-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="ec180-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="ec180-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ec180-130">NOTES</span></span>

## <span data-ttu-id="ec180-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ec180-131">RELATED LINKS</span></span>
