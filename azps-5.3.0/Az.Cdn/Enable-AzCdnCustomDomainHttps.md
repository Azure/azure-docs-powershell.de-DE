---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: cb11377c4ee18278dee2a3dc97c16bb58a02f5d5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473207"
---
# <span data-ttu-id="e907e-101">Enable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="e907e-101">Enable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="e907e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e907e-102">SYNOPSIS</span></span>
<span data-ttu-id="e907e-103">Aktiviert benutzerdefiniertes HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e907e-103">Enables custom HTTPS.</span></span>

## <span data-ttu-id="e907e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e907e-104">SYNTAX</span></span>

### <span data-ttu-id="e907e-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e907e-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e907e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e907e-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e907e-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e907e-107">ByResourceIdParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e907e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e907e-108">DESCRIPTION</span></span>
<span data-ttu-id="e907e-109">Das **Cmdlet "Enable-AzCdnCustomDomainHttps"** ermöglicht die sichere Bereitstellung einer benutzerdefinierten CDN-Domäne.</span><span class="sxs-lookup"><span data-stu-id="e907e-109">The **Enable-AzCdnCustomDomainHttps** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="e907e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e907e-110">EXAMPLES</span></span>

### <span data-ttu-id="e907e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e907e-111">Example 1</span></span>
```powershell
PS C:\> Enable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="e907e-112">Aktivieren Sie die sichere Übermittlung der benutzerdefinierten Domäne.</span><span class="sxs-lookup"><span data-stu-id="e907e-112">Enable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="e907e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e907e-113">PARAMETERS</span></span>

### <span data-ttu-id="e907e-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="e907e-114">-CustomDomainName</span></span>
<span data-ttu-id="e907e-115">Anzeigename der benutzerdefinierten Azure CDN-Domäne.</span><span class="sxs-lookup"><span data-stu-id="e907e-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="e907e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e907e-116">-DefaultProfile</span></span>
<span data-ttu-id="e907e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e907e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e907e-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e907e-118">-EndpointName</span></span>
<span data-ttu-id="e907e-119">Name des Azure CDN-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="e907e-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="e907e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e907e-120">-InputObject</span></span>
<span data-ttu-id="e907e-121">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="e907e-121">The custom domain object.</span></span>

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

### <span data-ttu-id="e907e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e907e-122">-PassThru</span></span>
<span data-ttu-id="e907e-123">Rückgabeobjekt bei Angabe</span><span class="sxs-lookup"><span data-stu-id="e907e-123">Return object if specified.</span></span>

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

### <span data-ttu-id="e907e-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e907e-124">-ProfileName</span></span>
<span data-ttu-id="e907e-125">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="e907e-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="e907e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e907e-126">-ResourceGroupName</span></span>
<span data-ttu-id="e907e-127">Die Ressourcengruppe des Azure CDN-Profils</span><span class="sxs-lookup"><span data-stu-id="e907e-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="e907e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e907e-128">-ResourceId</span></span>
<span data-ttu-id="e907e-129">ResourceId der benutzerdefinierten Domäne</span><span class="sxs-lookup"><span data-stu-id="e907e-129">ResourceId of the Custom Domain</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e907e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e907e-130">-Confirm</span></span>
<span data-ttu-id="e907e-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e907e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e907e-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e907e-132">-WhatIf</span></span>
<span data-ttu-id="e907e-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e907e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e907e-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e907e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e907e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e907e-135">CommonParameters</span></span>
<span data-ttu-id="e907e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e907e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e907e-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e907e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e907e-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e907e-138">INPUTS</span></span>

### <span data-ttu-id="e907e-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e907e-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="e907e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e907e-140">System.String</span></span>

## <span data-ttu-id="e907e-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e907e-141">OUTPUTS</span></span>

### <span data-ttu-id="e907e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e907e-142">System.Boolean</span></span>

## <span data-ttu-id="e907e-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e907e-143">NOTES</span></span>

## <span data-ttu-id="e907e-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e907e-144">RELATED LINKS</span></span>
