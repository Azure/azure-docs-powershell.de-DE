---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dbd8de47397e86f2aed9f774b555a587cf69976a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93828007"
---
# <span data-ttu-id="9643c-101">Get-AzsReclaimStorageCapacityStatus</span><span class="sxs-lookup"><span data-stu-id="9643c-101">Get-AzsReclaimStorageCapacityStatus</span></span>

## <span data-ttu-id="9643c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9643c-102">SYNOPSIS</span></span>
<span data-ttu-id="9643c-103">Gibt den Zustand des Garbage Collection-Auftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="9643c-103">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="9643c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9643c-104">SYNTAX</span></span>

```
Get-AzsReclaimStorageCapacityStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="9643c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9643c-105">DESCRIPTION</span></span>
<span data-ttu-id="9643c-106">Gibt den Zustand des Garbage Collection-Auftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="9643c-106">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="9643c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9643c-107">EXAMPLES</span></span>

### <span data-ttu-id="9643c-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9643c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsReclaimStorageCapacityStatus -FarmName "6ddbfe6e-8781-4a3d-b370-4a8b20a494d8" -JobId "92360f29-cd21-429d-a20b-9b11ab5902a0"
```

<span data-ttu-id="9643c-109">Gibt Informationen zum Status der Garbage Collection zurück.</span><span class="sxs-lookup"><span data-stu-id="9643c-109">Return information about the status of garbage collection.</span></span>

## <span data-ttu-id="9643c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9643c-110">PARAMETERS</span></span>

### <span data-ttu-id="9643c-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="9643c-111">-FarmName</span></span>
<span data-ttu-id="9643c-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="9643c-112">Farm Id.</span></span>

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

### <span data-ttu-id="9643c-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="9643c-113">-JobId</span></span>
<span data-ttu-id="9643c-114">Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="9643c-114">Operation Id.</span></span>

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

### <span data-ttu-id="9643c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9643c-115">-ResourceGroupName</span></span>
<span data-ttu-id="9643c-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9643c-116">Resource group name.</span></span>

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

### <span data-ttu-id="9643c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9643c-117">CommonParameters</span></span>
<span data-ttu-id="9643c-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9643c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9643c-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9643c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9643c-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9643c-120">INPUTS</span></span>

## <span data-ttu-id="9643c-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9643c-121">OUTPUTS</span></span>

## <span data-ttu-id="9643c-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="9643c-122">NOTES</span></span>

## <span data-ttu-id="9643c-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9643c-123">RELATED LINKS</span></span>

