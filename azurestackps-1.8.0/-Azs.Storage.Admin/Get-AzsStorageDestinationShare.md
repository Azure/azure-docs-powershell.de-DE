---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47ac85406955592cba566df505900e6c42befb7a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827992"
---
# <span data-ttu-id="341a0-101">Get-AzsStorageDestinationShare</span><span class="sxs-lookup"><span data-stu-id="341a0-101">Get-AzsStorageDestinationShare</span></span>

## <span data-ttu-id="341a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="341a0-102">SYNOPSIS</span></span>
<span data-ttu-id="341a0-103">Gibt eine Liste der Ziel Freigaben zurück, die das System als beste Kandidaten für die Migration betrachtet.</span><span class="sxs-lookup"><span data-stu-id="341a0-103">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="341a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="341a0-104">SYNTAX</span></span>

```
Get-AzsStorageDestinationShare [-SourceShareName] <String> [-FarmName] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="341a0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="341a0-105">DESCRIPTION</span></span>
<span data-ttu-id="341a0-106">Gibt eine Liste der Ziel Freigaben zurück, die das System als beste Kandidaten für die Migration betrachtet.</span><span class="sxs-lookup"><span data-stu-id="341a0-106">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="341a0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="341a0-107">EXAMPLES</span></span>

### <span data-ttu-id="341a0-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="341a0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageDestinationShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -SourceShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="341a0-109">Rufen Sie eine Liste der Ziel Freigaben ab, die das System als beste Kandidaten für die Migration betrachtet.</span><span class="sxs-lookup"><span data-stu-id="341a0-109">Get a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="341a0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="341a0-110">PARAMETERS</span></span>

### <span data-ttu-id="341a0-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="341a0-111">-FarmName</span></span>
<span data-ttu-id="341a0-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="341a0-112">Farm Id.</span></span>

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

### <span data-ttu-id="341a0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="341a0-113">-ResourceGroupName</span></span>
<span data-ttu-id="341a0-114">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="341a0-114">Resource group name.</span></span>

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

### <span data-ttu-id="341a0-115">-SourceShareName</span><span class="sxs-lookup"><span data-stu-id="341a0-115">-SourceShareName</span></span>
<span data-ttu-id="341a0-116">Der Name der Freigabe, die Container enthält, die migriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="341a0-116">Name of the share which holds containers to be migrated.</span></span>

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

### <span data-ttu-id="341a0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="341a0-117">CommonParameters</span></span>
<span data-ttu-id="341a0-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="341a0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="341a0-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="341a0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="341a0-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="341a0-120">INPUTS</span></span>

## <span data-ttu-id="341a0-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="341a0-121">OUTPUTS</span></span>

## <span data-ttu-id="341a0-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="341a0-122">NOTES</span></span>

## <span data-ttu-id="341a0-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="341a0-123">RELATED LINKS</span></span>

