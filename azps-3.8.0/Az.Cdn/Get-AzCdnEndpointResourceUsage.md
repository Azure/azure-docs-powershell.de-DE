---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 7b8773f4e8e0f63404d81c56703181124f6f8ad0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996827"
---
# <span data-ttu-id="261f0-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="261f0-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="261f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="261f0-102">SYNOPSIS</span></span>
<span data-ttu-id="261f0-103">Ruft die Ressourcenverwendung eines CDN-Endpunkts ab.</span><span class="sxs-lookup"><span data-stu-id="261f0-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="261f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="261f0-104">SYNTAX</span></span>

### <span data-ttu-id="261f0-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="261f0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="261f0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="261f0-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="261f0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="261f0-107">DESCRIPTION</span></span>
<span data-ttu-id="261f0-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="261f0-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="261f0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="261f0-109">EXAMPLES</span></span>

### <span data-ttu-id="261f0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="261f0-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="261f0-111">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="261f0-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="261f0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="261f0-112">PARAMETERS</span></span>

### <span data-ttu-id="261f0-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="261f0-113">-CdnEndpoint</span></span>
<span data-ttu-id="261f0-114">Das CDN-Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="261f0-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="261f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="261f0-115">-DefaultProfile</span></span>
<span data-ttu-id="261f0-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="261f0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="261f0-117">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="261f0-117">-EndpointName</span></span>
<span data-ttu-id="261f0-118">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="261f0-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="261f0-119">-Profilname</span><span class="sxs-lookup"><span data-stu-id="261f0-119">-ProfileName</span></span>
<span data-ttu-id="261f0-120">Azure CDN-Profilname</span><span class="sxs-lookup"><span data-stu-id="261f0-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="261f0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="261f0-121">-ResourceGroupName</span></span>
<span data-ttu-id="261f0-122">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="261f0-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="261f0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="261f0-123">CommonParameters</span></span>
<span data-ttu-id="261f0-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="261f0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="261f0-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="261f0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="261f0-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="261f0-126">INPUTS</span></span>

### <span data-ttu-id="261f0-127">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="261f0-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="261f0-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="261f0-128">OUTPUTS</span></span>

### <span data-ttu-id="261f0-129">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="261f0-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="261f0-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="261f0-130">NOTES</span></span>

## <span data-ttu-id="261f0-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="261f0-131">RELATED LINKS</span></span>
