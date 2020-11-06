---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: 0912ba8913bae430c3878dc0bde578420a5ea429
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477929"
---
# <span data-ttu-id="0a6f5-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="0a6f5-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="0a6f5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a6f5-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6f5-103">Ruft einen CDN-Ursprungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="0a6f5-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a6f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a6f5-104">SYNTAX</span></span>

### <span data-ttu-id="0a6f5-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0a6f5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a6f5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a6f5-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a6f5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a6f5-107">DESCRIPTION</span></span>
<span data-ttu-id="0a6f5-108">Das Cmdlet " **Get-AzureRmCdnOrigin** " Ruft einen Azure Content Delivery Network (CDN)-Ursprungsserver und dessen Konfigurationsdaten ab.</span><span class="sxs-lookup"><span data-stu-id="0a6f5-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="0a6f5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a6f5-109">EXAMPLES</span></span>

## <span data-ttu-id="0a6f5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a6f5-110">PARAMETERS</span></span>

### <span data-ttu-id="0a6f5-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a6f5-111">-CdnEndpoint</span></span>
<span data-ttu-id="0a6f5-112">Gibt das CDN-Endpunkt Objekt an, zu dem der Ursprung gehört.</span><span class="sxs-lookup"><span data-stu-id="0a6f5-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="0a6f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6f5-113">-DefaultProfile</span></span>
<span data-ttu-id="0a6f5-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0a6f5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a6f5-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="0a6f5-115">-EndpointName</span></span>
<span data-ttu-id="0a6f5-116">Gibt den Namen des Endpunkts an, zu dem der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="0a6f5-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="0a6f5-117">-OriginName</span><span class="sxs-lookup"><span data-stu-id="0a6f5-117">-OriginName</span></span>
<span data-ttu-id="0a6f5-118">Gibt den Namen des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="0a6f5-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="0a6f5-119">-Profilname</span><span class="sxs-lookup"><span data-stu-id="0a6f5-119">-ProfileName</span></span>
<span data-ttu-id="0a6f5-120">Gibt den Namen des Profils an, zu dem der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="0a6f5-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="0a6f5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a6f5-121">-ResourceGroupName</span></span>
<span data-ttu-id="0a6f5-122">Gibt den Namen der Ressourcengruppe an, zu der der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="0a6f5-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="0a6f5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6f5-123">CommonParameters</span></span>
<span data-ttu-id="0a6f5-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a6f5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6f5-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a6f5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6f5-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a6f5-126">INPUTS</span></span>

### <span data-ttu-id="0a6f5-127">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a6f5-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="0a6f5-128">Parameter: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0a6f5-128">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="0a6f5-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a6f5-129">OUTPUTS</span></span>

### <span data-ttu-id="0a6f5-130">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="0a6f5-130">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="0a6f5-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a6f5-131">NOTES</span></span>

## <span data-ttu-id="0a6f5-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a6f5-132">RELATED LINKS</span></span>

[<span data-ttu-id="0a6f5-133">Satz-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="0a6f5-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


