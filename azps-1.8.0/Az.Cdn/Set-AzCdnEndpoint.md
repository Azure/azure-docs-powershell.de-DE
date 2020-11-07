---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: cce3e2f9deb1f5df5c85d4f0b289b97e9cd36820
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661605"
---
# <span data-ttu-id="d9bbf-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9bbf-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="d9bbf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="d9bbf-103">Aktualisiert einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="d9bbf-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="d9bbf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9bbf-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9bbf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9bbf-105">DESCRIPTION</span></span>
<span data-ttu-id="d9bbf-106">Das Cmdlet " **Satz-AzCdnEndpoint** " aktualisiert einen Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="d9bbf-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="d9bbf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9bbf-107">EXAMPLES</span></span>

## <span data-ttu-id="d9bbf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9bbf-108">PARAMETERS</span></span>

### <span data-ttu-id="d9bbf-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9bbf-109">-CdnEndpoint</span></span>
<span data-ttu-id="d9bbf-110">Gibt den Endpunkt an, der vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d9bbf-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="d9bbf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9bbf-111">-DefaultProfile</span></span>
<span data-ttu-id="d9bbf-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d9bbf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9bbf-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d9bbf-113">-Confirm</span></span>
<span data-ttu-id="d9bbf-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9bbf-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9bbf-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9bbf-115">-WhatIf</span></span>
<span data-ttu-id="d9bbf-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9bbf-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9bbf-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9bbf-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9bbf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9bbf-118">CommonParameters</span></span>
<span data-ttu-id="d9bbf-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9bbf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9bbf-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9bbf-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9bbf-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9bbf-121">INPUTS</span></span>

### <span data-ttu-id="d9bbf-122">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9bbf-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="d9bbf-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9bbf-123">OUTPUTS</span></span>

### <span data-ttu-id="d9bbf-124">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9bbf-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="d9bbf-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9bbf-125">NOTES</span></span>

## <span data-ttu-id="d9bbf-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9bbf-126">RELATED LINKS</span></span>

[<span data-ttu-id="d9bbf-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9bbf-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="d9bbf-128">Neu – AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9bbf-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="d9bbf-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9bbf-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="d9bbf-130">Anfang-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9bbf-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="d9bbf-131">Stopp-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9bbf-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


