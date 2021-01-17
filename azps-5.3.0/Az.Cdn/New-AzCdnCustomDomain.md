---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: 6a0a90657ee76401117971a29dc03a78a7330afc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471005"
---
# <span data-ttu-id="2663b-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2663b-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="2663b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2663b-102">SYNOPSIS</span></span>
<span data-ttu-id="2663b-103">Erstellt eine benutzerdefinierte Domäne für einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="2663b-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="2663b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2663b-104">SYNTAX</span></span>

### <span data-ttu-id="2663b-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2663b-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2663b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2663b-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2663b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2663b-107">DESCRIPTION</span></span>
<span data-ttu-id="2663b-108">Das **Cmdlet "New-AzCdnCustomDomain"** erstellt eine benutzerdefinierte Domäne für den Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="2663b-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="2663b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2663b-109">EXAMPLES</span></span>

## <span data-ttu-id="2663b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2663b-110">PARAMETERS</span></span>

### <span data-ttu-id="2663b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2663b-111">-CdnEndpoint</span></span>
<span data-ttu-id="2663b-112">Gibt das CDN-Endpunktobjekt an, dem die benutzerdefinierte Domäne hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2663b-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="2663b-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="2663b-113">-CustomDomainName</span></span>
<span data-ttu-id="2663b-114">Gibt den Ressourcennamen der benutzerdefinierten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="2663b-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="2663b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2663b-115">-DefaultProfile</span></span>
<span data-ttu-id="2663b-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2663b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2663b-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2663b-117">-EndpointName</span></span>
<span data-ttu-id="2663b-118">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="2663b-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="2663b-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="2663b-119">-HostName</span></span>
<span data-ttu-id="2663b-120">Gibt den Hostnamen der benutzerdefinierten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="2663b-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="2663b-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2663b-121">-ProfileName</span></span>
<span data-ttu-id="2663b-122">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="2663b-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="2663b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2663b-123">-ResourceGroupName</span></span>
<span data-ttu-id="2663b-124">Gibt den Namen der Ressourcengruppe an, zu der die benutzerdefinierte Domäne gehört.</span><span class="sxs-lookup"><span data-stu-id="2663b-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="2663b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2663b-125">-Confirm</span></span>
<span data-ttu-id="2663b-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2663b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2663b-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2663b-127">-WhatIf</span></span>
<span data-ttu-id="2663b-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2663b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2663b-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2663b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2663b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2663b-130">CommonParameters</span></span>
<span data-ttu-id="2663b-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2663b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2663b-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2663b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2663b-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2663b-133">INPUTS</span></span>

### <span data-ttu-id="2663b-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2663b-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="2663b-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2663b-135">OUTPUTS</span></span>

### <span data-ttu-id="2663b-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2663b-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="2663b-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2663b-137">NOTES</span></span>

## <span data-ttu-id="2663b-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2663b-138">RELATED LINKS</span></span>

[<span data-ttu-id="2663b-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2663b-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="2663b-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2663b-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="2663b-141">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2663b-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


