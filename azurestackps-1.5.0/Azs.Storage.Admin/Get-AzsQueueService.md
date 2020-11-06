---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62c174a3aec5034b230954922f6aab5078fe4bac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475313"
---
# <span data-ttu-id="2028d-101">Get-AzsQueueService</span><span class="sxs-lookup"><span data-stu-id="2028d-101">Get-AzsQueueService</span></span>

## <span data-ttu-id="2028d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2028d-102">SYNOPSIS</span></span>
<span data-ttu-id="2028d-103">Gibt den Warteschlangendienst zurück.</span><span class="sxs-lookup"><span data-stu-id="2028d-103">Returns the queue service.</span></span>

## <span data-ttu-id="2028d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2028d-104">SYNTAX</span></span>

```
Get-AzsQueueService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="2028d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2028d-105">DESCRIPTION</span></span>
<span data-ttu-id="2028d-106">Gibt den Warteschlangendienst zurück.</span><span class="sxs-lookup"><span data-stu-id="2028d-106">Returns the queue service.</span></span>

## <span data-ttu-id="2028d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2028d-107">EXAMPLES</span></span>

### <span data-ttu-id="2028d-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2028d-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="2028d-109">Rufen Sie den Warteschlangendienst ab.</span><span class="sxs-lookup"><span data-stu-id="2028d-109">Get the queue service.</span></span>

## <span data-ttu-id="2028d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2028d-110">PARAMETERS</span></span>

### <span data-ttu-id="2028d-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="2028d-111">-FarmName</span></span>
<span data-ttu-id="2028d-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="2028d-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2028d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2028d-113">-ResourceGroupName</span></span>
<span data-ttu-id="2028d-114">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2028d-114">Resource group name.</span></span>

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

### <span data-ttu-id="2028d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2028d-115">CommonParameters</span></span>
<span data-ttu-id="2028d-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2028d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2028d-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2028d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2028d-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2028d-118">INPUTS</span></span>

## <span data-ttu-id="2028d-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2028d-119">OUTPUTS</span></span>

### <span data-ttu-id="2028d-120">Microsoft. AzureStack. Management. Storage. admin. Models. QueueService</span><span class="sxs-lookup"><span data-stu-id="2028d-120">Microsoft.AzureStack.Management.Storage.Admin.Models.QueueService</span></span>

## <span data-ttu-id="2028d-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="2028d-121">NOTES</span></span>

## <span data-ttu-id="2028d-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2028d-122">RELATED LINKS</span></span>

