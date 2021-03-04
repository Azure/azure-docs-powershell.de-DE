---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 4270f7c9781ef960cdbb20a8a067a3dc22255723
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941939"
---
# <span data-ttu-id="9dd46-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9dd46-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="9dd46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dd46-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd46-103">Aktualisiert einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="9dd46-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="9dd46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9dd46-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9dd46-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9dd46-105">DESCRIPTION</span></span>
<span data-ttu-id="9dd46-106">Das **Set-AzCdnEndpoint-Cmdlet** aktualisiert einen Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="9dd46-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="9dd46-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9dd46-107">EXAMPLES</span></span>

## <span data-ttu-id="9dd46-108">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9dd46-108">PARAMETERS</span></span>

### <span data-ttu-id="9dd46-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9dd46-109">-CdnEndpoint</span></span>
<span data-ttu-id="9dd46-110">Gibt den Endpunkt an, den dieses Cmdlet aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9dd46-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="9dd46-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd46-111">-DefaultProfile</span></span>
<span data-ttu-id="9dd46-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9dd46-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dd46-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9dd46-113">-Confirm</span></span>
<span data-ttu-id="9dd46-114">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9dd46-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dd46-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dd46-115">-WhatIf</span></span>
<span data-ttu-id="9dd46-116">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9dd46-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dd46-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9dd46-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dd46-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd46-118">CommonParameters</span></span>
<span data-ttu-id="9dd46-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dd46-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd46-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dd46-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd46-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9dd46-121">INPUTS</span></span>

### <span data-ttu-id="9dd46-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="9dd46-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="9dd46-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9dd46-123">OUTPUTS</span></span>

### <span data-ttu-id="9dd46-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="9dd46-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="9dd46-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9dd46-125">NOTES</span></span>

## <span data-ttu-id="9dd46-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9dd46-126">RELATED LINKS</span></span>

[<span data-ttu-id="9dd46-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9dd46-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="9dd46-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9dd46-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="9dd46-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9dd46-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="9dd46-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9dd46-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="9dd46-131">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9dd46-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


