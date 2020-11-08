---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 8ceb1fe02ba4a7d5cf4435ac79d404b331b58ea9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173097"
---
# <span data-ttu-id="1a359-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="1a359-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="1a359-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a359-102">SYNOPSIS</span></span>
<span data-ttu-id="1a359-103">Überprüft, ob einem Endpunkt eine benutzerdefinierte Domäne hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1a359-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="1a359-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a359-104">SYNTAX</span></span>

### <span data-ttu-id="1a359-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1a359-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a359-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a359-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a359-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a359-107">DESCRIPTION</span></span>
<span data-ttu-id="1a359-108">Das Cmdlet **Test-AzCdnCustomDomain** überprüft, ob eine benutzerdefinierte Domäne einem Endpunkt hinzugefügt werden kann, indem die CNAME-Zuordnung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="1a359-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="1a359-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a359-109">EXAMPLES</span></span>

## <span data-ttu-id="1a359-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a359-110">PARAMETERS</span></span>

### <span data-ttu-id="1a359-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a359-111">-CdnEndpoint</span></span>
<span data-ttu-id="1a359-112">Gibt den Endpunkt an, dem Sie die benutzerdefinierte Domäne hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="1a359-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="1a359-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="1a359-113">-CustomDomainHostName</span></span>
<span data-ttu-id="1a359-114">Gibt den Hostnamen der benutzerdefinierten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="1a359-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="1a359-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a359-115">-DefaultProfile</span></span>
<span data-ttu-id="1a359-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1a359-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a359-117">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="1a359-117">-EndpointName</span></span>
<span data-ttu-id="1a359-118">Gibt den Namen des Endpunkts an, dem Sie die benutzerdefinierte Domäne hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="1a359-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="1a359-119">-Profilname</span><span class="sxs-lookup"><span data-stu-id="1a359-119">-ProfileName</span></span>
<span data-ttu-id="1a359-120">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="1a359-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="1a359-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a359-121">-ResourceGroupName</span></span>
<span data-ttu-id="1a359-122">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1a359-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1a359-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a359-123">CommonParameters</span></span>
<span data-ttu-id="1a359-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a359-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a359-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a359-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a359-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a359-126">INPUTS</span></span>

### <span data-ttu-id="1a359-127">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a359-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="1a359-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a359-128">OUTPUTS</span></span>

### <span data-ttu-id="1a359-129">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="1a359-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="1a359-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a359-130">NOTES</span></span>

## <span data-ttu-id="1a359-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a359-131">RELATED LINKS</span></span>

[<span data-ttu-id="1a359-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="1a359-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="1a359-133">Neu – AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="1a359-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="1a359-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="1a359-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


