---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: eebc75ba8f8f1a55fb4c1db2e7929ce233d93a23
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162417"
---
# <span data-ttu-id="4e282-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4e282-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="4e282-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e282-102">SYNOPSIS</span></span>
<span data-ttu-id="4e282-103">Aktiviert HTTPS der benutzerdefinierten Domäne (veraltet).</span><span class="sxs-lookup"><span data-stu-id="4e282-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="4e282-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e282-104">SYNTAX</span></span>

### <span data-ttu-id="4e282-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4e282-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e282-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e282-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e282-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e282-107">DESCRIPTION</span></span>
<span data-ttu-id="4e282-108">Das **Cmdlet "Enable-AzCdnCustomDomain"** ermöglicht die sichere Bereitstellung einer benutzerdefinierten CDN-Domäne.</span><span class="sxs-lookup"><span data-stu-id="4e282-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="4e282-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4e282-109">EXAMPLES</span></span>

### <span data-ttu-id="4e282-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4e282-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="4e282-111">Aktivieren Sie die Https-Übermittlung der benutzerdefinierten Domäne.</span><span class="sxs-lookup"><span data-stu-id="4e282-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="4e282-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e282-112">PARAMETERS</span></span>

### <span data-ttu-id="4e282-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="4e282-113">-CustomDomainName</span></span>
<span data-ttu-id="4e282-114">Anzeigename der benutzerdefinierten Azure CDN-Domäne.</span><span class="sxs-lookup"><span data-stu-id="4e282-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="4e282-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e282-115">-DefaultProfile</span></span>
<span data-ttu-id="4e282-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e282-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e282-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4e282-117">-EndpointName</span></span>
<span data-ttu-id="4e282-118">Name des Azure CDN-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="4e282-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="4e282-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e282-119">-InputObject</span></span>
<span data-ttu-id="4e282-120">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="4e282-120">The custom domain object.</span></span>

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

### <span data-ttu-id="4e282-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e282-121">-PassThru</span></span>
<span data-ttu-id="4e282-122">Rückgabeobjekt (sofern angegeben)</span><span class="sxs-lookup"><span data-stu-id="4e282-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="4e282-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4e282-123">-ProfileName</span></span>
<span data-ttu-id="4e282-124">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="4e282-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="4e282-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e282-125">-ResourceGroupName</span></span>
<span data-ttu-id="4e282-126">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="4e282-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="4e282-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e282-127">-Confirm</span></span>
<span data-ttu-id="4e282-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4e282-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e282-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4e282-129">-WhatIf</span></span>
<span data-ttu-id="4e282-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e282-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e282-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e282-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e282-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e282-132">CommonParameters</span></span>
<span data-ttu-id="4e282-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e282-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e282-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e282-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e282-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4e282-135">INPUTS</span></span>

### <span data-ttu-id="4e282-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4e282-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="4e282-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4e282-137">OUTPUTS</span></span>

### <span data-ttu-id="4e282-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4e282-138">System.Boolean</span></span>

## <span data-ttu-id="4e282-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4e282-139">NOTES</span></span>

## <span data-ttu-id="4e282-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4e282-140">RELATED LINKS</span></span>
