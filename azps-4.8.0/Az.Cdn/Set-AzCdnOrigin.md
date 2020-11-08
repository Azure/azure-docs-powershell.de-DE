---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 9635031d6eaea5a7920a6862fb8cf20ce536c1db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008674"
---
# <span data-ttu-id="0640b-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="0640b-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="0640b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0640b-102">SYNOPSIS</span></span>
<span data-ttu-id="0640b-103">Aktualisiert einen CDN-Ursprungsserver.</span><span class="sxs-lookup"><span data-stu-id="0640b-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="0640b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0640b-104">SYNTAX</span></span>

```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0640b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0640b-105">DESCRIPTION</span></span>
<span data-ttu-id="0640b-106">Das Cmdlet " **Satz-AzCdnOrigin** " aktualisiert einen Server mit Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="0640b-106">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="0640b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0640b-107">EXAMPLES</span></span>

## <span data-ttu-id="0640b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0640b-108">PARAMETERS</span></span>

### <span data-ttu-id="0640b-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="0640b-109">-CdnOrigin</span></span>
<span data-ttu-id="0640b-110">Gibt den Ursprungsserver an, der vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="0640b-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0640b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0640b-111">-DefaultProfile</span></span>
<span data-ttu-id="0640b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0640b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0640b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0640b-113">CommonParameters</span></span>
<span data-ttu-id="0640b-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0640b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0640b-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0640b-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0640b-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0640b-116">INPUTS</span></span>

### <span data-ttu-id="0640b-117">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="0640b-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="0640b-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0640b-118">OUTPUTS</span></span>

### <span data-ttu-id="0640b-119">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="0640b-119">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="0640b-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="0640b-120">NOTES</span></span>

## <span data-ttu-id="0640b-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0640b-121">RELATED LINKS</span></span>

[<span data-ttu-id="0640b-122">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="0640b-122">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


