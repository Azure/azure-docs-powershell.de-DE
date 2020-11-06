---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: f9d9d307959d53748afe7219ccb4cbce631c5b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505637"
---
# <span data-ttu-id="86ad0-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="86ad0-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="86ad0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86ad0-102">SYNOPSIS</span></span>
<span data-ttu-id="86ad0-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="86ad0-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86ad0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86ad0-104">SYNTAX</span></span>

### <span data-ttu-id="86ad0-105">Parametersatz für fields-Parameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="86ad0-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86ad0-106">Parametersatz für Objektparameter</span><span class="sxs-lookup"><span data-stu-id="86ad0-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86ad0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86ad0-107">DESCRIPTION</span></span>
<span data-ttu-id="86ad0-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="86ad0-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="86ad0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86ad0-109">EXAMPLES</span></span>

### <span data-ttu-id="86ad0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="86ad0-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="86ad0-111">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="86ad0-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="86ad0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="86ad0-112">PARAMETERS</span></span>

### <span data-ttu-id="86ad0-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="86ad0-113">-CdnEndpoint</span></span>
<span data-ttu-id="86ad0-114">Das CDN-Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="86ad0-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="86ad0-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="86ad0-115">-EndpointName</span></span>
<span data-ttu-id="86ad0-116">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="86ad0-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="86ad0-117">-Profilname</span><span class="sxs-lookup"><span data-stu-id="86ad0-117">-ProfileName</span></span>
<span data-ttu-id="86ad0-118">Azure CDN-Profilname</span><span class="sxs-lookup"><span data-stu-id="86ad0-118">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="86ad0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86ad0-119">-ResourceGroupName</span></span>
<span data-ttu-id="86ad0-120">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="86ad0-120">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="86ad0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ad0-121">-DefaultProfile</span></span>
<span data-ttu-id="86ad0-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="86ad0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86ad0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ad0-123">CommonParameters</span></span>
<span data-ttu-id="86ad0-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86ad0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ad0-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86ad0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ad0-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86ad0-126">INPUTS</span></span>

### <span data-ttu-id="86ad0-127">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="86ad0-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="86ad0-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86ad0-128">OUTPUTS</span></span>

### <span data-ttu-id="86ad0-129">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="86ad0-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="86ad0-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="86ad0-130">NOTES</span></span>

## <span data-ttu-id="86ad0-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86ad0-131">RELATED LINKS</span></span>

