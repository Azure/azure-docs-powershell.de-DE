---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: cb11377c4ee18278dee2a3dc97c16bb58a02f5d5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165918"
---
# <span data-ttu-id="a00cb-101">Enable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="a00cb-101">Enable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="a00cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a00cb-102">SYNOPSIS</span></span>
<span data-ttu-id="a00cb-103">Aktiviert benutzerdefiniertes HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a00cb-103">Enables custom HTTPS.</span></span>

## <span data-ttu-id="a00cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a00cb-104">SYNTAX</span></span>

### <span data-ttu-id="a00cb-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a00cb-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a00cb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a00cb-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a00cb-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a00cb-107">ByResourceIdParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a00cb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a00cb-108">DESCRIPTION</span></span>
<span data-ttu-id="a00cb-109">Das Cmdlet **enable-AzCdnCustomDomainHttps** ermöglicht die sichere HTTPS-Zustellung einer benutzerdefinierten CDN-Domäne.</span><span class="sxs-lookup"><span data-stu-id="a00cb-109">The **Enable-AzCdnCustomDomainHttps** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="a00cb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a00cb-110">EXAMPLES</span></span>

### <span data-ttu-id="a00cb-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a00cb-111">Example 1</span></span>
```powershell
PS C:\> Enable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="a00cb-112">Aktivieren Sie die sichere Zustellung der benutzerdefinierten Domäne.</span><span class="sxs-lookup"><span data-stu-id="a00cb-112">Enable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="a00cb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a00cb-113">PARAMETERS</span></span>

### <span data-ttu-id="a00cb-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="a00cb-114">-CustomDomainName</span></span>
<span data-ttu-id="a00cb-115">Benutzerdefinierter Azure CDN-Domänen Anzeigename</span><span class="sxs-lookup"><span data-stu-id="a00cb-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="a00cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a00cb-116">-DefaultProfile</span></span>
<span data-ttu-id="a00cb-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a00cb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a00cb-118">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="a00cb-118">-EndpointName</span></span>
<span data-ttu-id="a00cb-119">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="a00cb-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="a00cb-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a00cb-120">-InputObject</span></span>
<span data-ttu-id="a00cb-121">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="a00cb-121">The custom domain object.</span></span>

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

### <span data-ttu-id="a00cb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a00cb-122">-PassThru</span></span>
<span data-ttu-id="a00cb-123">Gibt das Objekt zurück, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="a00cb-123">Return object if specified.</span></span>

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

### <span data-ttu-id="a00cb-124">-Profilname</span><span class="sxs-lookup"><span data-stu-id="a00cb-124">-ProfileName</span></span>
<span data-ttu-id="a00cb-125">Azure CDN-Profilname</span><span class="sxs-lookup"><span data-stu-id="a00cb-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="a00cb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a00cb-126">-ResourceGroupName</span></span>
<span data-ttu-id="a00cb-127">Die Ressourcengruppe des Azure CDN-Profils</span><span class="sxs-lookup"><span data-stu-id="a00cb-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="a00cb-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a00cb-128">-ResourceId</span></span>
<span data-ttu-id="a00cb-129">Resourcen-Nr der benutzerdefinierten Domäne</span><span class="sxs-lookup"><span data-stu-id="a00cb-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="a00cb-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a00cb-130">-Confirm</span></span>
<span data-ttu-id="a00cb-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a00cb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a00cb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a00cb-132">-WhatIf</span></span>
<span data-ttu-id="a00cb-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a00cb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a00cb-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a00cb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a00cb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a00cb-135">CommonParameters</span></span>
<span data-ttu-id="a00cb-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a00cb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a00cb-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a00cb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a00cb-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a00cb-138">INPUTS</span></span>

### <span data-ttu-id="a00cb-139">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a00cb-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="a00cb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a00cb-140">System.String</span></span>

## <span data-ttu-id="a00cb-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a00cb-141">OUTPUTS</span></span>

### <span data-ttu-id="a00cb-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a00cb-142">System.Boolean</span></span>

## <span data-ttu-id="a00cb-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="a00cb-143">NOTES</span></span>

## <span data-ttu-id="a00cb-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a00cb-144">RELATED LINKS</span></span>
