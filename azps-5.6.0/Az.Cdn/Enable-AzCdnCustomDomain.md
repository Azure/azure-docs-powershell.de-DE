---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: 82d980768147bb82332dae2dfa8965d962cc882e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920624"
---
# <span data-ttu-id="95812-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="95812-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="95812-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95812-102">SYNOPSIS</span></span>
<span data-ttu-id="95812-103">Aktiviert benutzerdefinierte Domäne HTTPS (veraltet).</span><span class="sxs-lookup"><span data-stu-id="95812-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="95812-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95812-104">SYNTAX</span></span>

### <span data-ttu-id="95812-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="95812-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95812-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95812-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95812-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95812-107">DESCRIPTION</span></span>
<span data-ttu-id="95812-108">Das **Cmdlet Enable-AzCdnCustomDomain** ermöglicht die sichere HTTPS-Übermittlung einer benutzerdefinierten CDN-Domäne.</span><span class="sxs-lookup"><span data-stu-id="95812-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="95812-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95812-109">EXAMPLES</span></span>

### <span data-ttu-id="95812-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95812-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="95812-111">Aktivieren sie die Https-Übermittlung der benutzerdefinierten Domäne.</span><span class="sxs-lookup"><span data-stu-id="95812-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="95812-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="95812-112">PARAMETERS</span></span>

### <span data-ttu-id="95812-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="95812-113">-CustomDomainName</span></span>
<span data-ttu-id="95812-114">Anzeigename der benutzerdefinierten Azure CDN-Domäne.</span><span class="sxs-lookup"><span data-stu-id="95812-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="95812-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95812-115">-DefaultProfile</span></span>
<span data-ttu-id="95812-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95812-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95812-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="95812-117">-EndpointName</span></span>
<span data-ttu-id="95812-118">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="95812-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="95812-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95812-119">-InputObject</span></span>
<span data-ttu-id="95812-120">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="95812-120">The custom domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95812-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95812-121">-PassThru</span></span>
<span data-ttu-id="95812-122">Rückgabeobjekt (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="95812-122">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95812-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="95812-123">-ProfileName</span></span>
<span data-ttu-id="95812-124">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="95812-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="95812-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95812-125">-ResourceGroupName</span></span>
<span data-ttu-id="95812-126">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="95812-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="95812-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="95812-127">-Confirm</span></span>
<span data-ttu-id="95812-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95812-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95812-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95812-129">-WhatIf</span></span>
<span data-ttu-id="95812-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95812-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95812-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95812-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95812-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95812-132">CommonParameters</span></span>
<span data-ttu-id="95812-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95812-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95812-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95812-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95812-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95812-135">INPUTS</span></span>

### <span data-ttu-id="95812-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="95812-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="95812-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95812-137">OUTPUTS</span></span>

### <span data-ttu-id="95812-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="95812-138">System.Boolean</span></span>

## <span data-ttu-id="95812-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="95812-139">NOTES</span></span>

## <span data-ttu-id="95812-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="95812-140">RELATED LINKS</span></span>
