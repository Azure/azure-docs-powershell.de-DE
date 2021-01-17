---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: 6a0a90657ee76401117971a29dc03a78a7330afc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365754"
---
# <span data-ttu-id="e587a-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e587a-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="e587a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e587a-102">SYNOPSIS</span></span>
<span data-ttu-id="e587a-103">Erstellt eine benutzerdefinierte Domäne für einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="e587a-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="e587a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e587a-104">SYNTAX</span></span>

### <span data-ttu-id="e587a-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e587a-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e587a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e587a-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e587a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e587a-107">DESCRIPTION</span></span>
<span data-ttu-id="e587a-108">Das **Cmdlet "New-AzCdnCustomDomain"** erstellt eine benutzerdefinierte Domäne für den Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="e587a-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e587a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e587a-109">EXAMPLES</span></span>

## <span data-ttu-id="e587a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e587a-110">PARAMETERS</span></span>

### <span data-ttu-id="e587a-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e587a-111">-CdnEndpoint</span></span>
<span data-ttu-id="e587a-112">Gibt das CDN-Endpunktobjekt an, dem die benutzerdefinierte Domäne hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e587a-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="e587a-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="e587a-113">-CustomDomainName</span></span>
<span data-ttu-id="e587a-114">Gibt den Ressourcennamen der benutzerdefinierten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="e587a-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="e587a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e587a-115">-DefaultProfile</span></span>
<span data-ttu-id="e587a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e587a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e587a-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e587a-117">-EndpointName</span></span>
<span data-ttu-id="e587a-118">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="e587a-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="e587a-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="e587a-119">-HostName</span></span>
<span data-ttu-id="e587a-120">Gibt den Hostnamen der benutzerdefinierten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="e587a-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="e587a-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e587a-121">-ProfileName</span></span>
<span data-ttu-id="e587a-122">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="e587a-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="e587a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e587a-123">-ResourceGroupName</span></span>
<span data-ttu-id="e587a-124">Gibt den Namen der Ressourcengruppe an, zu der die benutzerdefinierte Domäne gehört.</span><span class="sxs-lookup"><span data-stu-id="e587a-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="e587a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e587a-125">-Confirm</span></span>
<span data-ttu-id="e587a-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e587a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e587a-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e587a-127">-WhatIf</span></span>
<span data-ttu-id="e587a-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e587a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e587a-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e587a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e587a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e587a-130">CommonParameters</span></span>
<span data-ttu-id="e587a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e587a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e587a-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e587a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e587a-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e587a-133">INPUTS</span></span>

### <span data-ttu-id="e587a-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e587a-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="e587a-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e587a-135">OUTPUTS</span></span>

### <span data-ttu-id="e587a-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e587a-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="e587a-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e587a-137">NOTES</span></span>

## <span data-ttu-id="e587a-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e587a-138">RELATED LINKS</span></span>

[<span data-ttu-id="e587a-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e587a-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="e587a-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e587a-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="e587a-141">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e587a-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


