---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: f648d347e45b6394776a25735efbb06157cc5611
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996826"
---
# <span data-ttu-id="79d11-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="79d11-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="79d11-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79d11-102">SYNOPSIS</span></span>
<span data-ttu-id="79d11-103">Ruft einen CDN-Ursprungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="79d11-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="79d11-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79d11-104">SYNTAX</span></span>

### <span data-ttu-id="79d11-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="79d11-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79d11-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79d11-106">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79d11-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79d11-107">DESCRIPTION</span></span>
<span data-ttu-id="79d11-108">Das Cmdlet " **Get-AzCdnOrigin** " Ruft einen Azure Content Delivery Network (CDN)-Ursprungsserver und dessen Konfigurationsdaten ab.</span><span class="sxs-lookup"><span data-stu-id="79d11-108">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="79d11-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79d11-109">EXAMPLES</span></span>

## <span data-ttu-id="79d11-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="79d11-110">PARAMETERS</span></span>

### <span data-ttu-id="79d11-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="79d11-111">-CdnEndpoint</span></span>
<span data-ttu-id="79d11-112">Gibt das CDN-Endpunkt Objekt an, zu dem der Ursprung gehört.</span><span class="sxs-lookup"><span data-stu-id="79d11-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="79d11-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79d11-113">-DefaultProfile</span></span>
<span data-ttu-id="79d11-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="79d11-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79d11-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="79d11-115">-EndpointName</span></span>
<span data-ttu-id="79d11-116">Gibt den Namen des Endpunkts an, zu dem der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="79d11-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="79d11-117">-OriginName</span><span class="sxs-lookup"><span data-stu-id="79d11-117">-OriginName</span></span>
<span data-ttu-id="79d11-118">Gibt den Namen des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="79d11-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="79d11-119">-Profilname</span><span class="sxs-lookup"><span data-stu-id="79d11-119">-ProfileName</span></span>
<span data-ttu-id="79d11-120">Gibt den Namen des Profils an, zu dem der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="79d11-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="79d11-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79d11-121">-ResourceGroupName</span></span>
<span data-ttu-id="79d11-122">Gibt den Namen der Ressourcengruppe an, zu der der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="79d11-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="79d11-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79d11-123">CommonParameters</span></span>
<span data-ttu-id="79d11-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79d11-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79d11-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79d11-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79d11-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79d11-126">INPUTS</span></span>

### <span data-ttu-id="79d11-127">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="79d11-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="79d11-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79d11-128">OUTPUTS</span></span>

### <span data-ttu-id="79d11-129">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="79d11-129">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="79d11-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="79d11-130">NOTES</span></span>

## <span data-ttu-id="79d11-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79d11-131">RELATED LINKS</span></span>

[<span data-ttu-id="79d11-132">Satz-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="79d11-132">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


