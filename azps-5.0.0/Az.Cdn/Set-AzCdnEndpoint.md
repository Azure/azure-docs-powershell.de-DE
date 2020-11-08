---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 7222b33470dc1fff22039c5e88bf3c6560b80c31
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177853"
---
# <span data-ttu-id="a7920-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7920-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="a7920-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7920-102">SYNOPSIS</span></span>
<span data-ttu-id="a7920-103">Aktualisiert einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="a7920-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="a7920-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7920-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7920-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7920-105">DESCRIPTION</span></span>
<span data-ttu-id="a7920-106">Das Cmdlet " **Satz-AzCdnEndpoint** " aktualisiert einen Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="a7920-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="a7920-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7920-107">EXAMPLES</span></span>

## <span data-ttu-id="a7920-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7920-108">PARAMETERS</span></span>

### <span data-ttu-id="a7920-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7920-109">-CdnEndpoint</span></span>
<span data-ttu-id="a7920-110">Gibt den Endpunkt an, der vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a7920-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="a7920-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7920-111">-DefaultProfile</span></span>
<span data-ttu-id="a7920-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a7920-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7920-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a7920-113">-Confirm</span></span>
<span data-ttu-id="a7920-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7920-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7920-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7920-115">-WhatIf</span></span>
<span data-ttu-id="a7920-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7920-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7920-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7920-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7920-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7920-118">CommonParameters</span></span>
<span data-ttu-id="a7920-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7920-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7920-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7920-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7920-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7920-121">INPUTS</span></span>

### <span data-ttu-id="a7920-122">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7920-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="a7920-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7920-123">OUTPUTS</span></span>

### <span data-ttu-id="a7920-124">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7920-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="a7920-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7920-125">NOTES</span></span>

## <span data-ttu-id="a7920-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7920-126">RELATED LINKS</span></span>

[<span data-ttu-id="a7920-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7920-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="a7920-128">Neu – AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7920-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="a7920-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7920-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="a7920-130">Anfang-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7920-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="a7920-131">Stopp-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7920-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


