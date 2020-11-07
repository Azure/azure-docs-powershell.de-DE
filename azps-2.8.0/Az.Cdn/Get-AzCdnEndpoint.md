---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 09439fd202d01d6cf5ffc8be614940cdf39ad1ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652314"
---
# <span data-ttu-id="e451e-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e451e-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="e451e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e451e-102">SYNOPSIS</span></span>
<span data-ttu-id="e451e-103">Ruft einen CDN-Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="e451e-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="e451e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e451e-104">SYNTAX</span></span>

### <span data-ttu-id="e451e-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e451e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e451e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e451e-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e451e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e451e-107">DESCRIPTION</span></span>
<span data-ttu-id="e451e-108">Das Cmdlet " **Get-AzCdnEndpoint** " Ruft einen Azure Content Delivery Network (CDN)-Endpunkt und die zugehörigen Konfigurationsdaten ab.</span><span class="sxs-lookup"><span data-stu-id="e451e-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="e451e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e451e-109">EXAMPLES</span></span>

## <span data-ttu-id="e451e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e451e-110">PARAMETERS</span></span>

### <span data-ttu-id="e451e-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="e451e-111">-CdnProfile</span></span>
<span data-ttu-id="e451e-112">Gibt das CDN-Profilobjekt an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="e451e-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e451e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e451e-113">-DefaultProfile</span></span>
<span data-ttu-id="e451e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e451e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e451e-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="e451e-115">-EndpointName</span></span>
<span data-ttu-id="e451e-116">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="e451e-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="e451e-117">Der Name des Endpunkts ist nicht der Hostname des Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="e451e-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="e451e-118">-Profilname</span><span class="sxs-lookup"><span data-stu-id="e451e-118">-ProfileName</span></span>
<span data-ttu-id="e451e-119">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="e451e-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e451e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e451e-120">-ResourceGroupName</span></span>
<span data-ttu-id="e451e-121">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="e451e-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e451e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e451e-122">CommonParameters</span></span>
<span data-ttu-id="e451e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e451e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e451e-124">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e451e-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e451e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e451e-125">INPUTS</span></span>

### <span data-ttu-id="e451e-126">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="e451e-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="e451e-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e451e-127">OUTPUTS</span></span>

### <span data-ttu-id="e451e-128">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e451e-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="e451e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="e451e-129">NOTES</span></span>

## <span data-ttu-id="e451e-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e451e-130">RELATED LINKS</span></span>

[<span data-ttu-id="e451e-131">Neu – AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e451e-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="e451e-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e451e-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="e451e-133">Satz-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e451e-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="e451e-134">Anfang-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e451e-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="e451e-135">Stopp-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e451e-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


