---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: 58e4d922d74f36f6f472cf3bfef8e0d0d45155d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948011"
---
# <span data-ttu-id="bee76-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bee76-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="bee76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bee76-102">SYNOPSIS</span></span>
<span data-ttu-id="bee76-103">Erstellt eine benutzerdefinierte Domäne für einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="bee76-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="bee76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bee76-104">SYNTAX</span></span>

### <span data-ttu-id="bee76-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bee76-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bee76-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bee76-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bee76-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bee76-107">DESCRIPTION</span></span>
<span data-ttu-id="bee76-108">Das **Cmdlet New-AzCdnCustomDomain** erstellt eine benutzerdefinierte Domäne für den Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="bee76-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="bee76-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bee76-109">EXAMPLES</span></span>

## <span data-ttu-id="bee76-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bee76-110">PARAMETERS</span></span>

### <span data-ttu-id="bee76-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bee76-111">-CdnEndpoint</span></span>
<span data-ttu-id="bee76-112">Gibt das CDN-Endpunktobjekt an, dem die benutzerdefinierte Domäne hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="bee76-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="bee76-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="bee76-113">-CustomDomainName</span></span>
<span data-ttu-id="bee76-114">Gibt den Ressourcennamen der benutzerdefinierten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="bee76-114">Specifies the resource name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bee76-115">-DefaultProfile</span></span>
<span data-ttu-id="bee76-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bee76-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bee76-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bee76-117">-EndpointName</span></span>
<span data-ttu-id="bee76-118">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="bee76-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="bee76-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="bee76-119">-HostName</span></span>
<span data-ttu-id="bee76-120">Gibt den Hostnamen der benutzerdefinierten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="bee76-120">Specifies the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee76-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="bee76-121">-ProfileName</span></span>
<span data-ttu-id="bee76-122">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="bee76-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="bee76-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bee76-123">-ResourceGroupName</span></span>
<span data-ttu-id="bee76-124">Gibt den Namen der Ressourcengruppe an, zu der die benutzerdefinierte Domäne gehört.</span><span class="sxs-lookup"><span data-stu-id="bee76-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="bee76-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bee76-125">-Confirm</span></span>
<span data-ttu-id="bee76-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bee76-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee76-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bee76-127">-WhatIf</span></span>
<span data-ttu-id="bee76-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bee76-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bee76-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bee76-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee76-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee76-130">CommonParameters</span></span>
<span data-ttu-id="bee76-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bee76-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee76-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bee76-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee76-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bee76-133">INPUTS</span></span>

### <span data-ttu-id="bee76-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="bee76-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="bee76-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bee76-135">OUTPUTS</span></span>

### <span data-ttu-id="bee76-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bee76-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="bee76-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bee76-137">NOTES</span></span>

## <span data-ttu-id="bee76-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bee76-138">RELATED LINKS</span></span>

[<span data-ttu-id="bee76-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bee76-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="bee76-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bee76-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="bee76-141">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bee76-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


