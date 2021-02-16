---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: c98ec2ebee71188ddbc5760dbbd3d1528da3c770
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162404"
---
# <span data-ttu-id="831bc-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="831bc-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="831bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="831bc-102">SYNOPSIS</span></span>
<span data-ttu-id="831bc-103">Ruft eine benutzerdefinierte CDN-Domäne ab.</span><span class="sxs-lookup"><span data-stu-id="831bc-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="831bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="831bc-104">SYNTAX</span></span>

### <span data-ttu-id="831bc-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="831bc-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="831bc-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="831bc-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="831bc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="831bc-107">DESCRIPTION</span></span>
<span data-ttu-id="831bc-108">Das **Cmdlet "Get-AzCdnCustomDomain"** ruft eine benutzerdefinierte Azure Content Delivery Network (CDN)-Domäne und die zugehörigen Einstellungen ab.</span><span class="sxs-lookup"><span data-stu-id="831bc-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="831bc-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="831bc-109">EXAMPLES</span></span>

## <span data-ttu-id="831bc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="831bc-110">PARAMETERS</span></span>

### <span data-ttu-id="831bc-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="831bc-111">-CdnEndpoint</span></span>
<span data-ttu-id="831bc-112">Gibt das CDN-Endpunktobjekt an, dessen Mitglied die benutzerdefinierte Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="831bc-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="831bc-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="831bc-113">-CustomDomainName</span></span>
<span data-ttu-id="831bc-114">Gibt den Namen der benutzerdefinierten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="831bc-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="831bc-115">Der Name der benutzerdefinierten Domäne unterscheidet sich vom Hostnamen der benutzerdefinierten Domäne.</span><span class="sxs-lookup"><span data-stu-id="831bc-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="831bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="831bc-116">-DefaultProfile</span></span>
<span data-ttu-id="831bc-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="831bc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="831bc-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="831bc-118">-EndpointName</span></span>
<span data-ttu-id="831bc-119">Gibt den Namen des Endpunkts an, zu dem die benutzerdefinierte Domäne gehört.</span><span class="sxs-lookup"><span data-stu-id="831bc-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="831bc-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="831bc-120">-ProfileName</span></span>
<span data-ttu-id="831bc-121">Gibt den Namen des Profils an, zu dem die benutzerdefinierte Domäne gehört.</span><span class="sxs-lookup"><span data-stu-id="831bc-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="831bc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="831bc-122">-ResourceGroupName</span></span>
<span data-ttu-id="831bc-123">Gibt den Namen der Ressourcengruppe an, zu der die benutzerdefinierte Domäne gehört.</span><span class="sxs-lookup"><span data-stu-id="831bc-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="831bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="831bc-124">CommonParameters</span></span>
<span data-ttu-id="831bc-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="831bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="831bc-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="831bc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="831bc-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="831bc-127">INPUTS</span></span>

### <span data-ttu-id="831bc-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="831bc-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="831bc-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="831bc-129">OUTPUTS</span></span>

### <span data-ttu-id="831bc-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="831bc-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="831bc-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="831bc-131">NOTES</span></span>

## <span data-ttu-id="831bc-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="831bc-132">RELATED LINKS</span></span>

[<span data-ttu-id="831bc-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="831bc-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="831bc-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="831bc-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


