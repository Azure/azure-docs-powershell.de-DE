---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
ms.openlocfilehash: a3d92c095173d9eeb0b5e84812d42656e414b9d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499710"
---
# <span data-ttu-id="c303b-101">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c303b-101">New-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="c303b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c303b-102">SYNOPSIS</span></span>
<span data-ttu-id="c303b-103">Erstellt eine benutzerdefinierte Domäne für einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="c303b-103">Creates a custom domain for a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c303b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c303b-104">SYNTAX</span></span>

### <span data-ttu-id="c303b-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c303b-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c303b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c303b-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c303b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c303b-107">DESCRIPTION</span></span>
<span data-ttu-id="c303b-108">Das Cmdlet **New-AzureRmCdnCustomDomain** erstellt eine benutzerdefinierte Domäne für den Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="c303b-108">The **New-AzureRmCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="c303b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c303b-109">EXAMPLES</span></span>

## <span data-ttu-id="c303b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c303b-110">PARAMETERS</span></span>

### <span data-ttu-id="c303b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c303b-111">-CdnEndpoint</span></span>
<span data-ttu-id="c303b-112">Gibt das CDN-Endpunkt Objekt an, dem die benutzerdefinierte Domäne hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c303b-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c303b-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="c303b-113">-CustomDomainName</span></span>
<span data-ttu-id="c303b-114">Gibt den Ressourcennamen der benutzerdefinierten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="c303b-114">Specifies the resource name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c303b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c303b-115">-DefaultProfile</span></span>
<span data-ttu-id="c303b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c303b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c303b-117">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="c303b-117">-EndpointName</span></span>
<span data-ttu-id="c303b-118">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="c303b-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="c303b-119">-Hostname</span><span class="sxs-lookup"><span data-stu-id="c303b-119">-HostName</span></span>
<span data-ttu-id="c303b-120">Gibt den Hostnamen der benutzerdefinierten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="c303b-120">Specifies the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c303b-121">-Profilname</span><span class="sxs-lookup"><span data-stu-id="c303b-121">-ProfileName</span></span>
<span data-ttu-id="c303b-122">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="c303b-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="c303b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c303b-123">-ResourceGroupName</span></span>
<span data-ttu-id="c303b-124">Gibt den Namen der Ressourcengruppe an, zu der die benutzerdefinierte Domäne gehört.</span><span class="sxs-lookup"><span data-stu-id="c303b-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="c303b-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c303b-125">-Confirm</span></span>
<span data-ttu-id="c303b-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c303b-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c303b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c303b-127">-WhatIf</span></span>
<span data-ttu-id="c303b-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c303b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c303b-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c303b-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c303b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c303b-130">CommonParameters</span></span>
<span data-ttu-id="c303b-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c303b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c303b-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c303b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c303b-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c303b-133">INPUTS</span></span>

### <span data-ttu-id="c303b-134">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c303b-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="c303b-135">Parameter: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c303b-135">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="c303b-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c303b-136">OUTPUTS</span></span>

### <span data-ttu-id="c303b-137">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c303b-137">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="c303b-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="c303b-138">NOTES</span></span>

## <span data-ttu-id="c303b-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c303b-139">RELATED LINKS</span></span>

[<span data-ttu-id="c303b-140">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c303b-140">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="c303b-141">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c303b-141">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="c303b-142">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c303b-142">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


