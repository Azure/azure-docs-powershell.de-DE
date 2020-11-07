---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 74af4f7c4bc4f211f22be111bff4ecf0a8b9831a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820859"
---
# <span data-ttu-id="b4267-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b4267-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="b4267-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4267-102">SYNOPSIS</span></span>
<span data-ttu-id="b4267-103">Aktualisiert einen CDN-Ursprungsserver.</span><span class="sxs-lookup"><span data-stu-id="b4267-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="b4267-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4267-104">SYNTAX</span></span>

```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4267-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4267-105">DESCRIPTION</span></span>
<span data-ttu-id="b4267-106">Das Cmdlet " **Satz-AzCdnOrigin** " aktualisiert einen Server mit Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="b4267-106">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="b4267-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4267-107">EXAMPLES</span></span>

## <span data-ttu-id="b4267-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4267-108">PARAMETERS</span></span>

### <span data-ttu-id="b4267-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b4267-109">-CdnOrigin</span></span>
<span data-ttu-id="b4267-110">Gibt den Ursprungsserver an, der vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b4267-110">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="b4267-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4267-111">-DefaultProfile</span></span>
<span data-ttu-id="b4267-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b4267-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4267-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4267-113">CommonParameters</span></span>
<span data-ttu-id="b4267-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4267-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4267-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4267-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4267-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4267-116">INPUTS</span></span>

### <span data-ttu-id="b4267-117">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="b4267-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="b4267-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4267-118">OUTPUTS</span></span>

### <span data-ttu-id="b4267-119">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="b4267-119">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="b4267-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4267-120">NOTES</span></span>

## <span data-ttu-id="b4267-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4267-121">RELATED LINKS</span></span>

[<span data-ttu-id="b4267-122">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b4267-122">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


