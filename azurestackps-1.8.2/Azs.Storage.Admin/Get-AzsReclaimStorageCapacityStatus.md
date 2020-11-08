---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd62756b3a41af82a245a39d4f80478d47d90e1c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007102"
---
# <span data-ttu-id="a89f9-101">Get-AzsReclaimStorageCapacityStatus</span><span class="sxs-lookup"><span data-stu-id="a89f9-101">Get-AzsReclaimStorageCapacityStatus</span></span>

## <span data-ttu-id="a89f9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a89f9-102">SYNOPSIS</span></span>
<span data-ttu-id="a89f9-103">Gibt den Zustand des Garbage Collection-Auftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="a89f9-103">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="a89f9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a89f9-104">SYNTAX</span></span>

```
Get-AzsReclaimStorageCapacityStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a89f9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a89f9-105">DESCRIPTION</span></span>
<span data-ttu-id="a89f9-106">Gibt den Zustand des Garbage Collection-Auftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="a89f9-106">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="a89f9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a89f9-107">EXAMPLES</span></span>

### <span data-ttu-id="a89f9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a89f9-108">EXAMPLE 1</span></span>
```
Get-AzsReclaimStorageCapacityStatus -FarmName "6ddbfe6e-8781-4a3d-b370-4a8b20a494d8" -JobId "92360f29-cd21-429d-a20b-9b11ab5902a0"
```

<span data-ttu-id="a89f9-109">Gibt Informationen zum Status der Garbage Collection zurück.</span><span class="sxs-lookup"><span data-stu-id="a89f9-109">Return information about the status of garbage collection.</span></span>

## <span data-ttu-id="a89f9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a89f9-110">PARAMETERS</span></span>

### <span data-ttu-id="a89f9-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="a89f9-111">-FarmName</span></span>
<span data-ttu-id="a89f9-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="a89f9-112">Farm Id.</span></span>

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

### <span data-ttu-id="a89f9-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="a89f9-113">-JobId</span></span>
<span data-ttu-id="a89f9-114">Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="a89f9-114">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89f9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a89f9-115">-ResourceGroupName</span></span>
<span data-ttu-id="a89f9-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a89f9-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89f9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a89f9-117">CommonParameters</span></span>
<span data-ttu-id="a89f9-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a89f9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a89f9-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a89f9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a89f9-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a89f9-120">INPUTS</span></span>

## <span data-ttu-id="a89f9-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a89f9-121">OUTPUTS</span></span>

## <span data-ttu-id="a89f9-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="a89f9-122">NOTES</span></span>

## <span data-ttu-id="a89f9-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a89f9-123">RELATED LINKS</span></span>
