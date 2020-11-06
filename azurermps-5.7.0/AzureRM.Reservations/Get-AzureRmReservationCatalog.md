---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
ms.openlocfilehash: 4714b97773583197807d6ca54152ee25ab520909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482773"
---
# <span data-ttu-id="44e08-101">Get-AzureRmReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="44e08-101">Get-AzureRmReservationCatalog</span></span>

## <span data-ttu-id="44e08-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="44e08-102">SYNOPSIS</span></span>
<span data-ttu-id="44e08-103">Katalog der verfügbaren Reservierungen abrufen</span><span class="sxs-lookup"><span data-stu-id="44e08-103">Get the catalog of available reservation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44e08-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="44e08-104">SYNTAX</span></span>

```
Get-AzureRmReservationCatalog [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="44e08-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44e08-105">DESCRIPTION</span></span>
<span data-ttu-id="44e08-106">Rufen Sie die Regionen und SKUs ab, die für das angegebene Azure-Abonnement für den Kauf reservierter Instanzen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="44e08-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="44e08-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44e08-107">EXAMPLES</span></span>

### <span data-ttu-id="44e08-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="44e08-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationCatalog
```

<span data-ttu-id="44e08-109">Abrufen des Katalogs für das Standardabonnement</span><span class="sxs-lookup"><span data-stu-id="44e08-109">Get the catalog for the default subscription</span></span>

### <span data-ttu-id="44e08-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="44e08-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="44e08-111">Abrufen des Katalogs für das angegebene Abonnement</span><span class="sxs-lookup"><span data-stu-id="44e08-111">Get the catalog for the specified subscription</span></span>

## <span data-ttu-id="44e08-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="44e08-112">PARAMETERS</span></span>

### <span data-ttu-id="44e08-113">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="44e08-113">-SubscriptionId</span></span>
<span data-ttu-id="44e08-114">ID des Abonnements</span><span class="sxs-lookup"><span data-stu-id="44e08-114">Id of the subscription</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e08-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44e08-115">CommonParameters</span></span>
<span data-ttu-id="44e08-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44e08-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44e08-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44e08-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44e08-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="44e08-118">INPUTS</span></span>

### <span data-ttu-id="44e08-119">Keine</span><span class="sxs-lookup"><span data-stu-id="44e08-119">None</span></span>

## <span data-ttu-id="44e08-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="44e08-120">OUTPUTS</span></span>

### <span data-ttu-id="44e08-121">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. reservations. Models. PSCatalog, Microsoft. Azure. Commands. Reservations, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="44e08-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSCatalog, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="44e08-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="44e08-122">NOTES</span></span>

## <span data-ttu-id="44e08-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="44e08-123">RELATED LINKS</span></span>

