---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 1c9e83e8181d716024ae993ba0c3f5a9f75c6ef1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661626"
---
# <span data-ttu-id="1c356-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="1c356-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="1c356-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c356-102">SYNOPSIS</span></span>
<span data-ttu-id="1c356-103">Ruft die Ressourcenverwendung eines CDN-Endpunkts ab.</span><span class="sxs-lookup"><span data-stu-id="1c356-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="1c356-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c356-104">SYNTAX</span></span>

### <span data-ttu-id="1c356-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1c356-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c356-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c356-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c356-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c356-107">DESCRIPTION</span></span>
<span data-ttu-id="1c356-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="1c356-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="1c356-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c356-109">EXAMPLES</span></span>

### <span data-ttu-id="1c356-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1c356-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1c356-111">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="1c356-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="1c356-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c356-112">PARAMETERS</span></span>

### <span data-ttu-id="1c356-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c356-113">-CdnEndpoint</span></span>
<span data-ttu-id="1c356-114">Das CDN-Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="1c356-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="1c356-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c356-115">-DefaultProfile</span></span>
<span data-ttu-id="1c356-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1c356-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c356-117">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="1c356-117">-EndpointName</span></span>
<span data-ttu-id="1c356-118">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="1c356-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="1c356-119">-Profilname</span><span class="sxs-lookup"><span data-stu-id="1c356-119">-ProfileName</span></span>
<span data-ttu-id="1c356-120">Azure CDN-Profilname</span><span class="sxs-lookup"><span data-stu-id="1c356-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="1c356-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c356-121">-ResourceGroupName</span></span>
<span data-ttu-id="1c356-122">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="1c356-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="1c356-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c356-123">CommonParameters</span></span>
<span data-ttu-id="1c356-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c356-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c356-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c356-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c356-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c356-126">INPUTS</span></span>

### <span data-ttu-id="1c356-127">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c356-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="1c356-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c356-128">OUTPUTS</span></span>

### <span data-ttu-id="1c356-129">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="1c356-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="1c356-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c356-130">NOTES</span></span>

## <span data-ttu-id="1c356-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c356-131">RELATED LINKS</span></span>
