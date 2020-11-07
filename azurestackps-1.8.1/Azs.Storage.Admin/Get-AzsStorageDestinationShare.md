---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a75fafa646839375bf9dc7f1a64b3084fd31ee4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840659"
---
# <span data-ttu-id="7715f-101">Get-AzsStorageDestinationShare</span><span class="sxs-lookup"><span data-stu-id="7715f-101">Get-AzsStorageDestinationShare</span></span>

## <span data-ttu-id="7715f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7715f-102">SYNOPSIS</span></span>
<span data-ttu-id="7715f-103">Gibt eine Liste der Ziel Freigaben zurück, die das System als beste Kandidaten für die Migration betrachtet.</span><span class="sxs-lookup"><span data-stu-id="7715f-103">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="7715f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7715f-104">SYNTAX</span></span>

```
Get-AzsStorageDestinationShare [-SourceShareName] <String> [-FarmName] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="7715f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7715f-105">DESCRIPTION</span></span>
<span data-ttu-id="7715f-106">Gibt eine Liste der Ziel Freigaben zurück, die das System als beste Kandidaten für die Migration betrachtet.</span><span class="sxs-lookup"><span data-stu-id="7715f-106">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="7715f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7715f-107">EXAMPLES</span></span>

### <span data-ttu-id="7715f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7715f-108">EXAMPLE 1</span></span>
```
Get-AzsStorageDestinationShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -SourceShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="7715f-109">Rufen Sie eine Liste der Ziel Freigaben ab, die das System als beste Kandidaten für die Migration betrachtet.</span><span class="sxs-lookup"><span data-stu-id="7715f-109">Get a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="7715f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7715f-110">PARAMETERS</span></span>

### <span data-ttu-id="7715f-111">-SourceShareName</span><span class="sxs-lookup"><span data-stu-id="7715f-111">-SourceShareName</span></span>
<span data-ttu-id="7715f-112">Der Name der Freigabe, die Container enthält, die migriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7715f-112">Name of the share which holds containers to be migrated.</span></span>

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

### <span data-ttu-id="7715f-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="7715f-113">-FarmName</span></span>
<span data-ttu-id="7715f-114">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="7715f-114">Farm Id.</span></span>

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

### <span data-ttu-id="7715f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7715f-115">-ResourceGroupName</span></span>
<span data-ttu-id="7715f-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7715f-116">Resource group name.</span></span>

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

### <span data-ttu-id="7715f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7715f-117">CommonParameters</span></span>
<span data-ttu-id="7715f-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7715f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7715f-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7715f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7715f-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7715f-120">INPUTS</span></span>

## <span data-ttu-id="7715f-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7715f-121">OUTPUTS</span></span>

## <span data-ttu-id="7715f-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="7715f-122">NOTES</span></span>

## <span data-ttu-id="7715f-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7715f-123">RELATED LINKS</span></span>
