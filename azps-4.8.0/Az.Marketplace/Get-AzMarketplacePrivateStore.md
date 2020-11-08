---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: fcd59eb37a518cc4f6cd0b5d1c580706d2f6e8bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009747"
---
# <span data-ttu-id="f3729-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="f3729-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="f3729-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3729-102">SYNOPSIS</span></span>
<span data-ttu-id="f3729-103">Private Store-Liste abrufen</span><span class="sxs-lookup"><span data-stu-id="f3729-103">Get private store list</span></span>

## <span data-ttu-id="f3729-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3729-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3729-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3729-105">DESCRIPTION</span></span>
<span data-ttu-id="f3729-106">Private Store-Liste abrufen, die unter MANDANTENBEREICH erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="f3729-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="f3729-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3729-107">EXAMPLES</span></span>

### <span data-ttu-id="f3729-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f3729-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="f3729-109">Liste privater Stores, die unter MANDANTENBEREICH erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="f3729-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="f3729-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3729-110">PARAMETERS</span></span>

### <span data-ttu-id="f3729-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3729-111">-DefaultProfile</span></span>
<span data-ttu-id="f3729-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3729-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3729-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3729-113">CommonParameters</span></span>
<span data-ttu-id="f3729-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3729-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3729-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3729-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3729-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3729-116">INPUTS</span></span>

### <span data-ttu-id="f3729-117">Keine</span><span class="sxs-lookup"><span data-stu-id="f3729-117">None</span></span>

## <span data-ttu-id="f3729-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3729-118">OUTPUTS</span></span>

### <span data-ttu-id="f3729-119">Microsoft. Azure. Commands. Marketplace. Models. PrivateStore. PSPrivateStore</span><span class="sxs-lookup"><span data-stu-id="f3729-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="f3729-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3729-120">NOTES</span></span>

## <span data-ttu-id="f3729-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3729-121">RELATED LINKS</span></span>
