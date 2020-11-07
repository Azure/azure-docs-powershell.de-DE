---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34d5c967154f08526a0002f187b8cb869d933d39
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840875"
---
# <span data-ttu-id="d009c-101">Get-AzsStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d009c-101">Get-AzsStorageContainer</span></span>

## <span data-ttu-id="d009c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d009c-102">SYNOPSIS</span></span>
<span data-ttu-id="d009c-103">Gibt die Liste der Container zurück, die in der angegebenen Freigabe migriert werden können.</span><span class="sxs-lookup"><span data-stu-id="d009c-103">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="d009c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d009c-104">SYNTAX</span></span>

```
Get-AzsStorageContainer [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-MaxCount] <Int32>] [[-StartIndex] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d009c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d009c-105">DESCRIPTION</span></span>
<span data-ttu-id="d009c-106">Gibt die Liste der Container zurück, die in der angegebenen Freigabe migriert werden können.</span><span class="sxs-lookup"><span data-stu-id="d009c-106">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="d009c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d009c-107">EXAMPLES</span></span>

### <span data-ttu-id="d009c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d009c-108">EXAMPLE 1</span></span>
```
Get-AzsStorageContainer -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="d009c-109">Rufen Sie eine Liste der Container ab, die in der angegebenen Freigabe migriert werden können.</span><span class="sxs-lookup"><span data-stu-id="d009c-109">Get a list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="d009c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d009c-110">PARAMETERS</span></span>

### <span data-ttu-id="d009c-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="d009c-111">-FarmName</span></span>
<span data-ttu-id="d009c-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="d009c-112">Farm Id.</span></span>

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

### <span data-ttu-id="d009c-113">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="d009c-113">-ShareName</span></span>
<span data-ttu-id="d009c-114">Freigabename, in dem die Speichercontainer gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="d009c-114">Share name which holds the storage containers.</span></span>

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

### <span data-ttu-id="d009c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d009c-115">-ResourceGroupName</span></span>
<span data-ttu-id="d009c-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d009c-116">Resource group name.</span></span>

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

### <span data-ttu-id="d009c-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d009c-117">-MaxCount</span></span>
<span data-ttu-id="d009c-118">Die maximale Anzahl von Containern.</span><span class="sxs-lookup"><span data-stu-id="d009c-118">The max count of containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 100000000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d009c-119">-StartIndex</span><span class="sxs-lookup"><span data-stu-id="d009c-119">-StartIndex</span></span>
<span data-ttu-id="d009c-120">Der startIndex von Get Containers.</span><span class="sxs-lookup"><span data-stu-id="d009c-120">The start index of get containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d009c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d009c-121">CommonParameters</span></span>
<span data-ttu-id="d009c-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d009c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d009c-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d009c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d009c-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d009c-124">INPUTS</span></span>

## <span data-ttu-id="d009c-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d009c-125">OUTPUTS</span></span>

## <span data-ttu-id="d009c-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="d009c-126">NOTES</span></span>

## <span data-ttu-id="d009c-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d009c-127">RELATED LINKS</span></span>
