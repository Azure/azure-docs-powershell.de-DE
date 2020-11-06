---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: 088f9ff5ee1c41b4529353b2740bf9ef1fa8e33c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500926"
---
# <span data-ttu-id="353fb-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="353fb-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="353fb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="353fb-102">SYNOPSIS</span></span>
<span data-ttu-id="353fb-103">Ruft einen CDN-Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="353fb-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="353fb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="353fb-104">SYNTAX</span></span>

### <span data-ttu-id="353fb-105">Parametersatz für fields-Parameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="353fb-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="353fb-106">Parametersatz für Objektparameter</span><span class="sxs-lookup"><span data-stu-id="353fb-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="353fb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="353fb-107">DESCRIPTION</span></span>
<span data-ttu-id="353fb-108">Das Cmdlet " **Get-AzureRMCdnEndpoint** " Ruft einen Azure Content Delivery Network (CDN)-Endpunkt und die zugehörigen Konfigurationsdaten ab.</span><span class="sxs-lookup"><span data-stu-id="353fb-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="353fb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="353fb-109">EXAMPLES</span></span>

## <span data-ttu-id="353fb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="353fb-110">PARAMETERS</span></span>

### <span data-ttu-id="353fb-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="353fb-111">-CdnProfile</span></span>
<span data-ttu-id="353fb-112">Gibt das CDN-Profilobjekt an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="353fb-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="353fb-113">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="353fb-113">-EndpointName</span></span>
<span data-ttu-id="353fb-114">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="353fb-114">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="353fb-115">Der Name des Endpunkts ist nicht der Hostname des Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="353fb-115">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="353fb-116">-Profilname</span><span class="sxs-lookup"><span data-stu-id="353fb-116">-ProfileName</span></span>
<span data-ttu-id="353fb-117">Gibt den Namen des Profils an, zu dem der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="353fb-117">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353fb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="353fb-118">-ResourceGroupName</span></span>
<span data-ttu-id="353fb-119">Gibt den Namen der Ressourcengruppe an, zu der der Endpunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="353fb-119">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353fb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="353fb-120">-DefaultProfile</span></span>
<span data-ttu-id="353fb-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="353fb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="353fb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="353fb-122">CommonParameters</span></span>
<span data-ttu-id="353fb-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="353fb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="353fb-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="353fb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="353fb-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="353fb-125">INPUTS</span></span>

### <span data-ttu-id="353fb-126">PSProfile</span><span class="sxs-lookup"><span data-stu-id="353fb-126">PSProfile</span></span>
<span data-ttu-id="353fb-127">Der Parameter "CdnProfile" akzeptiert den Wert vom Typ "PSProfile" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="353fb-127">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="353fb-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="353fb-128">OUTPUTS</span></span>

###  
<span data-ttu-id="353fb-129">Dieses Cmdlet gibt ein Endpunkt Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="353fb-129">This cmdlet returns an endpoint object.</span></span>

## <span data-ttu-id="353fb-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="353fb-130">NOTES</span></span>

## <span data-ttu-id="353fb-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="353fb-131">RELATED LINKS</span></span>

[<span data-ttu-id="353fb-132">Neu – AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="353fb-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="353fb-133">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="353fb-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="353fb-134">Satz-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="353fb-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="353fb-135">Anfang-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="353fb-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="353fb-136">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="353fb-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


