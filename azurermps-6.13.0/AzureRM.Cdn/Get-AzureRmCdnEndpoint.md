---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: eb4215a281b83bd533a7502e3ec538ec4e3a570c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500265"
---
# <span data-ttu-id="9712c-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9712c-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="9712c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9712c-102">SYNOPSIS</span></span>
<span data-ttu-id="9712c-103">Ruft einen CDN-Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="9712c-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9712c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9712c-104">SYNTAX</span></span>

### <span data-ttu-id="9712c-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9712c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9712c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9712c-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9712c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9712c-107">DESCRIPTION</span></span>
<span data-ttu-id="9712c-108">Das Cmdlet " **Get-AzureRMCdnEndpoint** " Ruft einen Azure Content Delivery Network (CDN)-Endpunkt und die zugehörigen Konfigurationsdaten ab.</span><span class="sxs-lookup"><span data-stu-id="9712c-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="9712c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9712c-109">EXAMPLES</span></span>

## <span data-ttu-id="9712c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9712c-110">PARAMETERS</span></span>

### <span data-ttu-id="9712c-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="9712c-111">-CdnProfile</span></span>
<span data-ttu-id="9712c-112">Gibt das CDN-Profilobjekt an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="9712c-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9712c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9712c-113">-DefaultProfile</span></span>
<span data-ttu-id="9712c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9712c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9712c-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="9712c-115">-EndpointName</span></span>
<span data-ttu-id="9712c-116">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="9712c-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="9712c-117">Der Name des Endpunkts ist nicht der Hostname des Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="9712c-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="9712c-118">-Profilname</span><span class="sxs-lookup"><span data-stu-id="9712c-118">-ProfileName</span></span>
<span data-ttu-id="9712c-119">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="9712c-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="9712c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9712c-120">-ResourceGroupName</span></span>
<span data-ttu-id="9712c-121">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="9712c-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="9712c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9712c-122">CommonParameters</span></span>
<span data-ttu-id="9712c-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9712c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9712c-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9712c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9712c-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9712c-125">INPUTS</span></span>

### <span data-ttu-id="9712c-126">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="9712c-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="9712c-127">Parameter: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9712c-127">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="9712c-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9712c-128">OUTPUTS</span></span>

### <span data-ttu-id="9712c-129">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="9712c-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="9712c-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="9712c-130">NOTES</span></span>

## <span data-ttu-id="9712c-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9712c-131">RELATED LINKS</span></span>

[<span data-ttu-id="9712c-132">Neu – AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9712c-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9712c-133">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9712c-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9712c-134">Satz-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9712c-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9712c-135">Anfang-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9712c-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9712c-136">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9712c-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


