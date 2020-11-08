---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: 3352991d73bcef2e4f5b6475c9c71d5f48eaa526
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179421"
---
# <span data-ttu-id="16755-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="16755-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="16755-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16755-102">SYNOPSIS</span></span>
<span data-ttu-id="16755-103">Deaktiviert benutzerdefinierte Domänen-HTTPS (veraltet).</span><span class="sxs-lookup"><span data-stu-id="16755-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="16755-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16755-104">SYNTAX</span></span>

### <span data-ttu-id="16755-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="16755-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16755-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16755-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16755-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16755-107">DESCRIPTION</span></span>
<span data-ttu-id="16755-108">Das Cmdlet **Disable-AzCdnCustomDomain** deaktiviert die gesicherte HTTPS-Zustellung einer benutzerdefinierten CDN-Domäne.</span><span class="sxs-lookup"><span data-stu-id="16755-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="16755-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16755-109">EXAMPLES</span></span>

### <span data-ttu-id="16755-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16755-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="16755-111">Deaktivieren Sie die HTTPS-Zustellung der benutzerdefinierten Domäne.</span><span class="sxs-lookup"><span data-stu-id="16755-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="16755-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="16755-112">PARAMETERS</span></span>

### <span data-ttu-id="16755-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="16755-113">-CustomDomainName</span></span>
<span data-ttu-id="16755-114">Benutzerdefinierter Azure CDN-Domänen Anzeigename</span><span class="sxs-lookup"><span data-stu-id="16755-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="16755-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16755-115">-DefaultProfile</span></span>
<span data-ttu-id="16755-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16755-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16755-117">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="16755-117">-EndpointName</span></span>
<span data-ttu-id="16755-118">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="16755-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="16755-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="16755-119">-InputObject</span></span>
<span data-ttu-id="16755-120">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="16755-120">The custom domain object.</span></span>

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

### <span data-ttu-id="16755-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16755-121">-PassThru</span></span>
<span data-ttu-id="16755-122">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="16755-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="16755-123">-Profilname</span><span class="sxs-lookup"><span data-stu-id="16755-123">-ProfileName</span></span>
<span data-ttu-id="16755-124">Azure CDN-Profilname</span><span class="sxs-lookup"><span data-stu-id="16755-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="16755-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16755-125">-ResourceGroupName</span></span>
<span data-ttu-id="16755-126">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="16755-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="16755-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="16755-127">-Confirm</span></span>
<span data-ttu-id="16755-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16755-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16755-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16755-129">-WhatIf</span></span>
<span data-ttu-id="16755-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16755-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16755-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16755-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16755-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16755-132">CommonParameters</span></span>
<span data-ttu-id="16755-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16755-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16755-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16755-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16755-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16755-135">INPUTS</span></span>

### <span data-ttu-id="16755-136">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="16755-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="16755-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16755-137">OUTPUTS</span></span>

### <span data-ttu-id="16755-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="16755-138">System.Boolean</span></span>

## <span data-ttu-id="16755-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="16755-139">NOTES</span></span>

## <span data-ttu-id="16755-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16755-140">RELATED LINKS</span></span>
