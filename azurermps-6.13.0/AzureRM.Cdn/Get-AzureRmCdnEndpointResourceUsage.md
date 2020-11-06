---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: 3fe740fc8643ab6ef4f010feeee57b3339426c21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497526"
---
# <span data-ttu-id="c4304-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="c4304-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="c4304-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4304-102">SYNOPSIS</span></span>
<span data-ttu-id="c4304-103">Ruft die Ressourcenverwendung eines CDN-Endpunkts ab.</span><span class="sxs-lookup"><span data-stu-id="c4304-103">Gets the resource usage of a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4304-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4304-104">SYNTAX</span></span>

### <span data-ttu-id="c4304-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4304-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4304-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4304-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4304-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4304-107">DESCRIPTION</span></span>
<span data-ttu-id="c4304-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="c4304-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="c4304-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4304-109">EXAMPLES</span></span>

### <span data-ttu-id="c4304-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c4304-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c4304-111">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="c4304-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="c4304-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4304-112">PARAMETERS</span></span>

### <span data-ttu-id="c4304-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c4304-113">-CdnEndpoint</span></span>
<span data-ttu-id="c4304-114">Das CDN-Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="c4304-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="c4304-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4304-115">-DefaultProfile</span></span>
<span data-ttu-id="c4304-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c4304-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4304-117">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="c4304-117">-EndpointName</span></span>
<span data-ttu-id="c4304-118">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="c4304-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="c4304-119">-Profilname</span><span class="sxs-lookup"><span data-stu-id="c4304-119">-ProfileName</span></span>
<span data-ttu-id="c4304-120">Azure CDN-Profilname</span><span class="sxs-lookup"><span data-stu-id="c4304-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="c4304-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4304-121">-ResourceGroupName</span></span>
<span data-ttu-id="c4304-122">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="c4304-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="c4304-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4304-123">CommonParameters</span></span>
<span data-ttu-id="c4304-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4304-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4304-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4304-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4304-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4304-126">INPUTS</span></span>

### <span data-ttu-id="c4304-127">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c4304-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="c4304-128">Parameter: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c4304-128">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="c4304-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4304-129">OUTPUTS</span></span>

### <span data-ttu-id="c4304-130">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="c4304-130">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="c4304-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4304-131">NOTES</span></span>

## <span data-ttu-id="c4304-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4304-132">RELATED LINKS</span></span>
