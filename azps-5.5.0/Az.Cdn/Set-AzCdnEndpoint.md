---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 7222b33470dc1fff22039c5e88bf3c6560b80c31
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171389"
---
# <span data-ttu-id="735c9-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="735c9-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="735c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="735c9-102">SYNOPSIS</span></span>
<span data-ttu-id="735c9-103">Aktualisiert einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="735c9-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="735c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="735c9-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="735c9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="735c9-105">DESCRIPTION</span></span>
<span data-ttu-id="735c9-106">Das **Set-AzCdnEndpoint-Cmdlet** aktualisiert einen Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="735c9-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="735c9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="735c9-107">EXAMPLES</span></span>

## <span data-ttu-id="735c9-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="735c9-108">PARAMETERS</span></span>

### <span data-ttu-id="735c9-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="735c9-109">-CdnEndpoint</span></span>
<span data-ttu-id="735c9-110">Gibt den Endpunkt an, den dieses Cmdlet aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="735c9-110">Specifies the endpoint that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="735c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="735c9-111">-DefaultProfile</span></span>
<span data-ttu-id="735c9-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="735c9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="735c9-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="735c9-113">-Confirm</span></span>
<span data-ttu-id="735c9-114">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="735c9-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735c9-115">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="735c9-115">-WhatIf</span></span>
<span data-ttu-id="735c9-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="735c9-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="735c9-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="735c9-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735c9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="735c9-118">CommonParameters</span></span>
<span data-ttu-id="735c9-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="735c9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="735c9-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="735c9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="735c9-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="735c9-121">INPUTS</span></span>

### <span data-ttu-id="735c9-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="735c9-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="735c9-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="735c9-123">OUTPUTS</span></span>

### <span data-ttu-id="735c9-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="735c9-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="735c9-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="735c9-125">NOTES</span></span>

## <span data-ttu-id="735c9-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="735c9-126">RELATED LINKS</span></span>

[<span data-ttu-id="735c9-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="735c9-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="735c9-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="735c9-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="735c9-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="735c9-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="735c9-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="735c9-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="735c9-131">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="735c9-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


