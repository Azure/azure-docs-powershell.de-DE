---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: 9cf4633f464316d41034a0cb2d79384e229bcf4c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995512"
---
# <span data-ttu-id="dad3f-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="dad3f-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="dad3f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dad3f-102">SYNOPSIS</span></span>
<span data-ttu-id="dad3f-103">Aktiviert benutzerdefinierte HTTPS-Domäne (veraltet).</span><span class="sxs-lookup"><span data-stu-id="dad3f-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="dad3f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dad3f-104">SYNTAX</span></span>

### <span data-ttu-id="dad3f-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dad3f-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dad3f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dad3f-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dad3f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dad3f-107">DESCRIPTION</span></span>
<span data-ttu-id="dad3f-108">Das Cmdlet **enable-AzCdnCustomDomain** ermöglicht die sichere HTTPS-Zustellung einer benutzerdefinierten CDN-Domäne.</span><span class="sxs-lookup"><span data-stu-id="dad3f-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="dad3f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dad3f-109">EXAMPLES</span></span>

### <span data-ttu-id="dad3f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dad3f-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="dad3f-111">Aktivieren Sie die HTTPS-Zustellung der benutzerdefinierten Domäne.</span><span class="sxs-lookup"><span data-stu-id="dad3f-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="dad3f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dad3f-112">PARAMETERS</span></span>

### <span data-ttu-id="dad3f-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="dad3f-113">-CustomDomainName</span></span>
<span data-ttu-id="dad3f-114">Benutzerdefinierter Azure CDN-Domänen Anzeigename</span><span class="sxs-lookup"><span data-stu-id="dad3f-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="dad3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad3f-115">-DefaultProfile</span></span>
<span data-ttu-id="dad3f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dad3f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dad3f-117">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="dad3f-117">-EndpointName</span></span>
<span data-ttu-id="dad3f-118">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="dad3f-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="dad3f-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dad3f-119">-InputObject</span></span>
<span data-ttu-id="dad3f-120">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="dad3f-120">The custom domain object.</span></span>

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

### <span data-ttu-id="dad3f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dad3f-121">-PassThru</span></span>
<span data-ttu-id="dad3f-122">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="dad3f-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="dad3f-123">-Profilname</span><span class="sxs-lookup"><span data-stu-id="dad3f-123">-ProfileName</span></span>
<span data-ttu-id="dad3f-124">Azure CDN-Profilname</span><span class="sxs-lookup"><span data-stu-id="dad3f-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="dad3f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dad3f-125">-ResourceGroupName</span></span>
<span data-ttu-id="dad3f-126">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="dad3f-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="dad3f-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dad3f-127">-Confirm</span></span>
<span data-ttu-id="dad3f-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dad3f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dad3f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dad3f-129">-WhatIf</span></span>
<span data-ttu-id="dad3f-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dad3f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dad3f-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dad3f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dad3f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad3f-132">CommonParameters</span></span>
<span data-ttu-id="dad3f-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad3f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad3f-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dad3f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad3f-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dad3f-135">INPUTS</span></span>

### <span data-ttu-id="dad3f-136">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="dad3f-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="dad3f-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dad3f-137">OUTPUTS</span></span>

### <span data-ttu-id="dad3f-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dad3f-138">System.Boolean</span></span>

## <span data-ttu-id="dad3f-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="dad3f-139">NOTES</span></span>

## <span data-ttu-id="dad3f-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dad3f-140">RELATED LINKS</span></span>