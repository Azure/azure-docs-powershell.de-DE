---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/enable-azurermcdncustomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Enable-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Enable-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 50c1bf02a8952bbbddd2bbb82e55441adacd6a2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476225"
---
# <span data-ttu-id="0779b-101">Enable-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0779b-101">Enable-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="0779b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0779b-102">SYNOPSIS</span></span>
<span data-ttu-id="0779b-103">Aktiviert benutzerdefiniertes HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0779b-103">Enables custom HTTPS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0779b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0779b-104">SYNTAX</span></span>

### <span data-ttu-id="0779b-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0779b-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0779b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0779b-106">ByObjectParameterSet</span></span>
```
Enable-AzureRmCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0779b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0779b-107">DESCRIPTION</span></span>
<span data-ttu-id="0779b-108">Das Cmdlet **enable-AzureRmCdnCustomDomain** ermöglicht die sichere HTTPS-Zustellung einer benutzerdefinierten CDN-Domäne.</span><span class="sxs-lookup"><span data-stu-id="0779b-108">The **Enable-AzureRmCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="0779b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0779b-109">EXAMPLES</span></span>

### <span data-ttu-id="0779b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0779b-110">Example 1</span></span>
```powershell
Enable-AzureRmCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="0779b-111">Aktivieren Sie die HTTPS-Zustellung der benutzerdefinierten Domäne.</span><span class="sxs-lookup"><span data-stu-id="0779b-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="0779b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0779b-112">PARAMETERS</span></span>

### <span data-ttu-id="0779b-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="0779b-113">-CustomDomainName</span></span>
<span data-ttu-id="0779b-114">Benutzerdefinierter Azure CDN-Domänen Anzeigename</span><span class="sxs-lookup"><span data-stu-id="0779b-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="0779b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0779b-115">-DefaultProfile</span></span>
<span data-ttu-id="0779b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0779b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0779b-117">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="0779b-117">-EndpointName</span></span>
<span data-ttu-id="0779b-118">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="0779b-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="0779b-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0779b-119">-InputObject</span></span>
<span data-ttu-id="0779b-120">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="0779b-120">The custom domain object.</span></span>

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

### <span data-ttu-id="0779b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0779b-121">-PassThru</span></span>
<span data-ttu-id="0779b-122">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="0779b-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="0779b-123">-Profilname</span><span class="sxs-lookup"><span data-stu-id="0779b-123">-ProfileName</span></span>
<span data-ttu-id="0779b-124">Azure CDN-Profilname</span><span class="sxs-lookup"><span data-stu-id="0779b-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="0779b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0779b-125">-ResourceGroupName</span></span>
<span data-ttu-id="0779b-126">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="0779b-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="0779b-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0779b-127">-Confirm</span></span>
<span data-ttu-id="0779b-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0779b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0779b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0779b-129">-WhatIf</span></span>
<span data-ttu-id="0779b-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0779b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0779b-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0779b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0779b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0779b-132">CommonParameters</span></span>
<span data-ttu-id="0779b-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0779b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0779b-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0779b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0779b-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0779b-135">INPUTS</span></span>

### <span data-ttu-id="0779b-136">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0779b-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="0779b-137">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0779b-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0779b-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0779b-138">OUTPUTS</span></span>

### <span data-ttu-id="0779b-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0779b-139">System.Boolean</span></span>

## <span data-ttu-id="0779b-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="0779b-140">NOTES</span></span>

## <span data-ttu-id="0779b-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0779b-141">RELATED LINKS</span></span>
