---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/disable-azurermcdncustomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Disable-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Disable-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 1f0694d93f95f9fed6f23d7912003a179598ac91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498389"
---
# <span data-ttu-id="3197e-101">Disable-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3197e-101">Disable-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="3197e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3197e-102">SYNOPSIS</span></span>
<span data-ttu-id="3197e-103">Deaktiviert benutzerdefiniertes HTTPS.</span><span class="sxs-lookup"><span data-stu-id="3197e-103">Disables custom HTTPS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3197e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3197e-104">SYNTAX</span></span>

### <span data-ttu-id="3197e-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3197e-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3197e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3197e-106">ByObjectParameterSet</span></span>
```
Disable-AzureRmCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3197e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3197e-107">DESCRIPTION</span></span>
<span data-ttu-id="3197e-108">Das Cmdlet **Disable-AzureRmCdnCustomDomain** deaktiviert die gesicherte HTTPS-Zustellung einer benutzerdefinierten CDN-Domäne.</span><span class="sxs-lookup"><span data-stu-id="3197e-108">The **Disable-AzureRmCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="3197e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3197e-109">EXAMPLES</span></span>

### <span data-ttu-id="3197e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3197e-110">Example 1</span></span>
```powershell
Disable-AzureRmCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="3197e-111">Deaktivieren Sie die HTTPS-Zustellung der benutzerdefinierten Domäne.</span><span class="sxs-lookup"><span data-stu-id="3197e-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="3197e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3197e-112">PARAMETERS</span></span>

### <span data-ttu-id="3197e-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="3197e-113">-CustomDomainName</span></span>
<span data-ttu-id="3197e-114">Benutzerdefinierter Azure CDN-Domänen Anzeigename</span><span class="sxs-lookup"><span data-stu-id="3197e-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="3197e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3197e-115">-DefaultProfile</span></span>
<span data-ttu-id="3197e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3197e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3197e-117">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="3197e-117">-EndpointName</span></span>
<span data-ttu-id="3197e-118">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="3197e-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="3197e-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3197e-119">-InputObject</span></span>
<span data-ttu-id="3197e-120">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="3197e-120">The custom domain object.</span></span>

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

### <span data-ttu-id="3197e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3197e-121">-PassThru</span></span>
<span data-ttu-id="3197e-122">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="3197e-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="3197e-123">-Profilname</span><span class="sxs-lookup"><span data-stu-id="3197e-123">-ProfileName</span></span>
<span data-ttu-id="3197e-124">Azure CDN-Profilname</span><span class="sxs-lookup"><span data-stu-id="3197e-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="3197e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3197e-125">-ResourceGroupName</span></span>
<span data-ttu-id="3197e-126">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="3197e-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="3197e-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3197e-127">-Confirm</span></span>
<span data-ttu-id="3197e-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3197e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3197e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3197e-129">-WhatIf</span></span>
<span data-ttu-id="3197e-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3197e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3197e-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3197e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3197e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3197e-132">CommonParameters</span></span>
<span data-ttu-id="3197e-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3197e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3197e-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3197e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3197e-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3197e-135">INPUTS</span></span>

### <span data-ttu-id="3197e-136">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3197e-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="3197e-137">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3197e-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="3197e-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3197e-138">OUTPUTS</span></span>

### <span data-ttu-id="3197e-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3197e-139">System.Boolean</span></span>

## <span data-ttu-id="3197e-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="3197e-140">NOTES</span></span>

## <span data-ttu-id="3197e-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3197e-141">RELATED LINKS</span></span>
