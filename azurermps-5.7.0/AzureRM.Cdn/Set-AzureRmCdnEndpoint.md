---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
ms.openlocfilehash: 13b5b219ec789ac54332caa366cfb0277f0bfacb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483153"
---
# <span data-ttu-id="e44bf-101">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e44bf-101">Set-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="e44bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e44bf-102">SYNOPSIS</span></span>
<span data-ttu-id="e44bf-103">Aktualisiert einen CDN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="e44bf-103">Updates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e44bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e44bf-104">SYNTAX</span></span>

```
Set-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e44bf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e44bf-105">DESCRIPTION</span></span>
<span data-ttu-id="e44bf-106">Das Cmdlet " **Satz-AzureRmCdnEndpoint** " aktualisiert einen Azure Content Delivery Network (CDN)-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="e44bf-106">The **Set-AzureRmCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e44bf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e44bf-107">EXAMPLES</span></span>

## <span data-ttu-id="e44bf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e44bf-108">PARAMETERS</span></span>

### <span data-ttu-id="e44bf-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e44bf-109">-CdnEndpoint</span></span>
<span data-ttu-id="e44bf-110">Gibt den Endpunkt an, der vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e44bf-110">Specifies the endpoint that this cmdlet updates.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e44bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e44bf-111">-DefaultProfile</span></span>
<span data-ttu-id="e44bf-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e44bf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44bf-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e44bf-113">-Confirm</span></span>
<span data-ttu-id="e44bf-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e44bf-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44bf-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e44bf-115">-WhatIf</span></span>
<span data-ttu-id="e44bf-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e44bf-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e44bf-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e44bf-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44bf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44bf-118">CommonParameters</span></span>
<span data-ttu-id="e44bf-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e44bf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44bf-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e44bf-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44bf-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e44bf-121">INPUTS</span></span>

### <span data-ttu-id="e44bf-122">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e44bf-122">PSEndpoint</span></span>
<span data-ttu-id="e44bf-123">Der Parameter "CdnEndpoint" akzeptiert den Wert vom Typ "PSEndpoint" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e44bf-123">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="e44bf-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e44bf-124">OUTPUTS</span></span>

### <span data-ttu-id="e44bf-125">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e44bf-125">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="e44bf-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="e44bf-126">NOTES</span></span>

## <span data-ttu-id="e44bf-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e44bf-127">RELATED LINKS</span></span>

[<span data-ttu-id="e44bf-128">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e44bf-128">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e44bf-129">Neu – AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e44bf-129">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e44bf-130">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e44bf-130">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e44bf-131">Anfang-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e44bf-131">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e44bf-132">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e44bf-132">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


