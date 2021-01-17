---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: 3352991d73bcef2e4f5b6475c9c71d5f48eaa526
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471024"
---
# <span data-ttu-id="3ee51-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3ee51-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="3ee51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ee51-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee51-103">Deaktiviert HTTPS der benutzerdefinierten Domäne (veraltet).</span><span class="sxs-lookup"><span data-stu-id="3ee51-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="3ee51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ee51-104">SYNTAX</span></span>

### <span data-ttu-id="3ee51-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3ee51-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ee51-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ee51-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ee51-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ee51-107">DESCRIPTION</span></span>
<span data-ttu-id="3ee51-108">Das **Cmdlet "Disable-AzCdnCustomDomain"** deaktiviert die sichere BEREITSTELLUNG einer benutzerdefinierten CDN-Domäne.</span><span class="sxs-lookup"><span data-stu-id="3ee51-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="3ee51-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ee51-109">EXAMPLES</span></span>

### <span data-ttu-id="3ee51-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3ee51-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="3ee51-111">Deaktivieren Sie die Übermittlung der benutzerdefinierten Domäne durch https.</span><span class="sxs-lookup"><span data-stu-id="3ee51-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="3ee51-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ee51-112">PARAMETERS</span></span>

### <span data-ttu-id="3ee51-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="3ee51-113">-CustomDomainName</span></span>
<span data-ttu-id="3ee51-114">Anzeigename der benutzerdefinierten Azure CDN-Domäne.</span><span class="sxs-lookup"><span data-stu-id="3ee51-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="3ee51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee51-115">-DefaultProfile</span></span>
<span data-ttu-id="3ee51-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ee51-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ee51-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3ee51-117">-EndpointName</span></span>
<span data-ttu-id="3ee51-118">Name des Azure CDN-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="3ee51-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="3ee51-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ee51-119">-InputObject</span></span>
<span data-ttu-id="3ee51-120">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="3ee51-120">The custom domain object.</span></span>

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

### <span data-ttu-id="3ee51-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ee51-121">-PassThru</span></span>
<span data-ttu-id="3ee51-122">Rückgabeobjekt (sofern angegeben)</span><span class="sxs-lookup"><span data-stu-id="3ee51-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="3ee51-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="3ee51-123">-ProfileName</span></span>
<span data-ttu-id="3ee51-124">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="3ee51-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="3ee51-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ee51-125">-ResourceGroupName</span></span>
<span data-ttu-id="3ee51-126">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="3ee51-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="3ee51-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ee51-127">-Confirm</span></span>
<span data-ttu-id="3ee51-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ee51-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ee51-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3ee51-129">-WhatIf</span></span>
<span data-ttu-id="3ee51-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ee51-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ee51-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ee51-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ee51-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee51-132">CommonParameters</span></span>
<span data-ttu-id="3ee51-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ee51-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee51-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ee51-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee51-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ee51-135">INPUTS</span></span>

### <span data-ttu-id="3ee51-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3ee51-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="3ee51-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ee51-137">OUTPUTS</span></span>

### <span data-ttu-id="3ee51-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3ee51-138">System.Boolean</span></span>

## <span data-ttu-id="3ee51-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3ee51-139">NOTES</span></span>

## <span data-ttu-id="3ee51-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3ee51-140">RELATED LINKS</span></span>
