---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: d3e33e8bf6dea2e06e8ee72199e040a563d0d974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478685"
---
# <span data-ttu-id="419a0-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="419a0-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="419a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="419a0-102">SYNOPSIS</span></span>
<span data-ttu-id="419a0-103">Ruft einen CDN-Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="419a0-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="419a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="419a0-104">SYNTAX</span></span>

### <span data-ttu-id="419a0-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="419a0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="419a0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="419a0-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="419a0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="419a0-107">DESCRIPTION</span></span>
<span data-ttu-id="419a0-108">Das Cmdlet " **Get-AzureRMCdnEndpoint** " Ruft einen Azure Content Delivery Network (CDN)-Endpunkt und die zugehörigen Konfigurationsdaten ab.</span><span class="sxs-lookup"><span data-stu-id="419a0-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="419a0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="419a0-109">EXAMPLES</span></span>

## <span data-ttu-id="419a0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="419a0-110">PARAMETERS</span></span>

### <span data-ttu-id="419a0-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="419a0-111">-CdnProfile</span></span>
<span data-ttu-id="419a0-112">Gibt das CDN-Profilobjekt an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="419a0-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="419a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="419a0-113">-DefaultProfile</span></span>
<span data-ttu-id="419a0-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="419a0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="419a0-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="419a0-115">-EndpointName</span></span>
<span data-ttu-id="419a0-116">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="419a0-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="419a0-117">Der Name des Endpunkts ist nicht der Hostname des Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="419a0-117">The name of the endpoint is not the host name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="419a0-118">-Profilname</span><span class="sxs-lookup"><span data-stu-id="419a0-118">-ProfileName</span></span>
<span data-ttu-id="419a0-119">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="419a0-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="419a0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="419a0-120">-ResourceGroupName</span></span>
<span data-ttu-id="419a0-121">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="419a0-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="419a0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="419a0-122">CommonParameters</span></span>
<span data-ttu-id="419a0-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="419a0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="419a0-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="419a0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="419a0-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="419a0-125">INPUTS</span></span>

### <span data-ttu-id="419a0-126">PSProfile</span><span class="sxs-lookup"><span data-stu-id="419a0-126">PSProfile</span></span>
<span data-ttu-id="419a0-127">Der Parameter "CdnProfile" akzeptiert den Wert vom Typ "PSProfile" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="419a0-127">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="419a0-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="419a0-128">OUTPUTS</span></span>

###  
<span data-ttu-id="419a0-129">Dieses Cmdlet gibt ein Endpunkt Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="419a0-129">This cmdlet returns an endpoint object.</span></span>

## <span data-ttu-id="419a0-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="419a0-130">NOTES</span></span>

## <span data-ttu-id="419a0-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="419a0-131">RELATED LINKS</span></span>

[<span data-ttu-id="419a0-132">Neu – AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="419a0-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="419a0-133">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="419a0-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="419a0-134">Satz-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="419a0-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="419a0-135">Anfang-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="419a0-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="419a0-136">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="419a0-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


