---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: 837def99279905e3c647ecd8805ed0284840f5a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932032"
---
# <span data-ttu-id="d8bb2-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="d8bb2-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="d8bb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="d8bb2-103">Deaktiviert benutzerdefinierte Domäne HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d8bb2-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="d8bb2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8bb2-104">SYNTAX</span></span>

### <span data-ttu-id="d8bb2-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d8bb2-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8bb2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8bb2-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8bb2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8bb2-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8bb2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8bb2-108">DESCRIPTION</span></span>
<span data-ttu-id="d8bb2-109">Das **Cmdlet Disable-AzCdnCustomDomainHttps** deaktiviert die sichere HTTPS-Übermittlung einer benutzerdefinierten CDN-Domäne.</span><span class="sxs-lookup"><span data-stu-id="d8bb2-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="d8bb2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d8bb2-110">EXAMPLES</span></span>

### <span data-ttu-id="d8bb2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d8bb2-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="d8bb2-112">Deaktivieren Sie die sichere Zustellung der benutzerdefinierten Domäne.</span><span class="sxs-lookup"><span data-stu-id="d8bb2-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="d8bb2-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d8bb2-113">PARAMETERS</span></span>

### <span data-ttu-id="d8bb2-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d8bb2-114">-CustomDomainName</span></span>
<span data-ttu-id="d8bb2-115">Anzeigename der benutzerdefinierten Azure CDN-Domäne.</span><span class="sxs-lookup"><span data-stu-id="d8bb2-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="d8bb2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8bb2-116">-DefaultProfile</span></span>
<span data-ttu-id="d8bb2-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8bb2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8bb2-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d8bb2-118">-EndpointName</span></span>
<span data-ttu-id="d8bb2-119">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="d8bb2-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="d8bb2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8bb2-120">-InputObject</span></span>
<span data-ttu-id="d8bb2-121">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="d8bb2-121">The custom domain object.</span></span>

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

### <span data-ttu-id="d8bb2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8bb2-122">-PassThru</span></span>
<span data-ttu-id="d8bb2-123">Rückgabeobjekt, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="d8bb2-123">Return object if specified.</span></span>

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

### <span data-ttu-id="d8bb2-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d8bb2-124">-ProfileName</span></span>
<span data-ttu-id="d8bb2-125">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="d8bb2-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="d8bb2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8bb2-126">-ResourceGroupName</span></span>
<span data-ttu-id="d8bb2-127">Die Ressourcengruppe des Azure CDN-Profils</span><span class="sxs-lookup"><span data-stu-id="d8bb2-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="d8bb2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8bb2-128">-ResourceId</span></span>
<span data-ttu-id="d8bb2-129">ResourceId der benutzerdefinierten Domäne</span><span class="sxs-lookup"><span data-stu-id="d8bb2-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="d8bb2-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d8bb2-130">-Confirm</span></span>
<span data-ttu-id="d8bb2-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8bb2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8bb2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8bb2-132">-WhatIf</span></span>
<span data-ttu-id="d8bb2-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8bb2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8bb2-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8bb2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8bb2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8bb2-135">CommonParameters</span></span>
<span data-ttu-id="d8bb2-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8bb2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8bb2-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8bb2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8bb2-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d8bb2-138">INPUTS</span></span>

### <span data-ttu-id="d8bb2-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d8bb2-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="d8bb2-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d8bb2-140">System.String</span></span>

## <span data-ttu-id="d8bb2-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d8bb2-141">OUTPUTS</span></span>

### <span data-ttu-id="d8bb2-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8bb2-142">System.Boolean</span></span>

## <span data-ttu-id="d8bb2-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d8bb2-143">NOTES</span></span>

## <span data-ttu-id="d8bb2-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d8bb2-144">RELATED LINKS</span></span>
