---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: aba554d2c81e4fce438e9bd6e10a8dfec63da465
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505642"
---
# <span data-ttu-id="2fe96-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="2fe96-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="2fe96-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2fe96-102">SYNOPSIS</span></span>
<span data-ttu-id="2fe96-103">Ruft einen CDN-Ursprungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="2fe96-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fe96-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fe96-104">SYNTAX</span></span>

### <span data-ttu-id="2fe96-105">Parametersatz für fields-Parameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="2fe96-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fe96-106">Parametersatz für Objektparameter</span><span class="sxs-lookup"><span data-stu-id="2fe96-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fe96-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2fe96-107">DESCRIPTION</span></span>
<span data-ttu-id="2fe96-108">Das Cmdlet " **Get-AzureRmCdnOrigin** " Ruft einen Azure Content Delivery Network (CDN)-Ursprungsserver und dessen Konfigurationsdaten ab.</span><span class="sxs-lookup"><span data-stu-id="2fe96-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="2fe96-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fe96-109">EXAMPLES</span></span>

## <span data-ttu-id="2fe96-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fe96-110">PARAMETERS</span></span>

### <span data-ttu-id="2fe96-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2fe96-111">-CdnEndpoint</span></span>
<span data-ttu-id="2fe96-112">Gibt das CDN-Endpunkt Objekt an, zu dem der Ursprung gehört.</span><span class="sxs-lookup"><span data-stu-id="2fe96-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fe96-113">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="2fe96-113">-EndpointName</span></span>
<span data-ttu-id="2fe96-114">Gibt den Namen des Endpunkts an, zu dem der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="2fe96-114">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2fe96-115">-OriginName</span><span class="sxs-lookup"><span data-stu-id="2fe96-115">-OriginName</span></span>
<span data-ttu-id="2fe96-116">Gibt den Namen des Ursprungsservers an.</span><span class="sxs-lookup"><span data-stu-id="2fe96-116">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="2fe96-117">-Profilname</span><span class="sxs-lookup"><span data-stu-id="2fe96-117">-ProfileName</span></span>
<span data-ttu-id="2fe96-118">Gibt den Namen des Profils an, zu dem der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="2fe96-118">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2fe96-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fe96-119">-ResourceGroupName</span></span>
<span data-ttu-id="2fe96-120">Gibt den Namen der Ressourcengruppe an, zu der der Ursprungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="2fe96-120">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2fe96-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fe96-121">-DefaultProfile</span></span>
<span data-ttu-id="2fe96-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2fe96-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fe96-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fe96-123">CommonParameters</span></span>
<span data-ttu-id="2fe96-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fe96-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fe96-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fe96-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fe96-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2fe96-126">INPUTS</span></span>

### <span data-ttu-id="2fe96-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2fe96-127">PSEndpoint</span></span>
<span data-ttu-id="2fe96-128">Der Parameter "CdnEndpoint" akzeptiert den Wert vom Typ "PSEndpoint" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2fe96-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="2fe96-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2fe96-129">OUTPUTS</span></span>

###  
<span data-ttu-id="2fe96-130">Dieses Cmdlet gibt ein Origin-Serverobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="2fe96-130">This cmdlet returns an origin server object.</span></span>

## <span data-ttu-id="2fe96-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="2fe96-131">NOTES</span></span>

## <span data-ttu-id="2fe96-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2fe96-132">RELATED LINKS</span></span>

[<span data-ttu-id="2fe96-133">Satz-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="2fe96-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


