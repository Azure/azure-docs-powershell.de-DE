---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: e0c1d2e49cce4798499506352811d1e341bf47e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504498"
---
# <span data-ttu-id="b29af-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b29af-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="b29af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b29af-102">SYNOPSIS</span></span>
<span data-ttu-id="b29af-103">Ruft eine benutzerdefinierte CDN-Domäne ab.</span><span class="sxs-lookup"><span data-stu-id="b29af-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b29af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b29af-104">SYNTAX</span></span>

### <span data-ttu-id="b29af-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b29af-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b29af-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b29af-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b29af-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b29af-107">DESCRIPTION</span></span>
<span data-ttu-id="b29af-108">Das Cmdlet " **Get-AzureRmCdnCustomDomain** " Ruft eine benutzerdefinierte Domäne vom Azure Content Delivery Network (CDN) und die zugehörigen Einstellungen ab.</span><span class="sxs-lookup"><span data-stu-id="b29af-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="b29af-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b29af-109">EXAMPLES</span></span>

## <span data-ttu-id="b29af-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b29af-110">PARAMETERS</span></span>

### <span data-ttu-id="b29af-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b29af-111">-CdnEndpoint</span></span>
<span data-ttu-id="b29af-112">Gibt das CDN-Endpunkt Objekt an, dessen Mitglied die benutzerdefinierte Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="b29af-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="b29af-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="b29af-113">-CustomDomainName</span></span>
<span data-ttu-id="b29af-114">Gibt den Namen der benutzerdefinierten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="b29af-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="b29af-115">Der Name der benutzerdefinierten Domäne weicht vom Hostnamen der benutzerdefinierten Domäne ab.</span><span class="sxs-lookup"><span data-stu-id="b29af-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b29af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b29af-116">-DefaultProfile</span></span>
<span data-ttu-id="b29af-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b29af-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b29af-118">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="b29af-118">-EndpointName</span></span>
<span data-ttu-id="b29af-119">Gibt den Namen des Endpunkts an, zu dem die benutzerdefinierte Domäne gehört.</span><span class="sxs-lookup"><span data-stu-id="b29af-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="b29af-120">-Profilname</span><span class="sxs-lookup"><span data-stu-id="b29af-120">-ProfileName</span></span>
<span data-ttu-id="b29af-121">Gibt den Namen des Profils an, zu dem die benutzerdefinierte Domäne gehört.</span><span class="sxs-lookup"><span data-stu-id="b29af-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="b29af-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b29af-122">-ResourceGroupName</span></span>
<span data-ttu-id="b29af-123">Gibt den Namen der Ressourcengruppe an, zu der die benutzerdefinierte Domäne gehört.</span><span class="sxs-lookup"><span data-stu-id="b29af-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="b29af-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b29af-124">CommonParameters</span></span>
<span data-ttu-id="b29af-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b29af-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b29af-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b29af-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b29af-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b29af-127">INPUTS</span></span>

### <span data-ttu-id="b29af-128">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b29af-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="b29af-129">Parameter: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b29af-129">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="b29af-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b29af-130">OUTPUTS</span></span>

### <span data-ttu-id="b29af-131">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b29af-131">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="b29af-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="b29af-132">NOTES</span></span>

## <span data-ttu-id="b29af-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b29af-133">RELATED LINKS</span></span>

[<span data-ttu-id="b29af-134">Neu – AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b29af-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="b29af-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b29af-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


