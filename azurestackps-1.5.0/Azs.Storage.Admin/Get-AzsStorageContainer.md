---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4847310f65a0b652d15321cd49583212ef5844d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474806"
---
# <span data-ttu-id="f02f0-101">Get-AzsStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f02f0-101">Get-AzsStorageContainer</span></span>

## <span data-ttu-id="f02f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f02f0-102">SYNOPSIS</span></span>
<span data-ttu-id="f02f0-103">Gibt die Liste der Container zurück, die in der angegebenen Freigabe migriert werden können.</span><span class="sxs-lookup"><span data-stu-id="f02f0-103">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="f02f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f02f0-104">SYNTAX</span></span>

```
Get-AzsStorageContainer [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-MaxCount] <Int32>] [[-StartIndex] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="f02f0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f02f0-105">DESCRIPTION</span></span>
<span data-ttu-id="f02f0-106">Gibt die Liste der Container zurück, die in der angegebenen Freigabe migriert werden können.</span><span class="sxs-lookup"><span data-stu-id="f02f0-106">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="f02f0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f02f0-107">EXAMPLES</span></span>

### <span data-ttu-id="f02f0-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f02f0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageContainer -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="f02f0-109">Rufen Sie eine Liste der Container ab, die in der angegebenen Freigabe migriert werden können.</span><span class="sxs-lookup"><span data-stu-id="f02f0-109">Get a list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="f02f0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f02f0-110">PARAMETERS</span></span>

### <span data-ttu-id="f02f0-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="f02f0-111">-FarmName</span></span>
<span data-ttu-id="f02f0-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="f02f0-112">Farm Id.</span></span>

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

### <span data-ttu-id="f02f0-113">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="f02f0-113">-MaxCount</span></span>
<span data-ttu-id="f02f0-114">Die maximale Anzahl von Containern.</span><span class="sxs-lookup"><span data-stu-id="f02f0-114">The max count of containers.</span></span>

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

### <span data-ttu-id="f02f0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f02f0-115">-ResourceGroupName</span></span>
<span data-ttu-id="f02f0-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f02f0-116">Resource group name.</span></span>

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

### <span data-ttu-id="f02f0-117">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="f02f0-117">-ShareName</span></span>
<span data-ttu-id="f02f0-118">Freigabename, in dem die Speichercontainer gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f02f0-118">Share name which holds the storage containers.</span></span>

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

### <span data-ttu-id="f02f0-119">-StartIndex</span><span class="sxs-lookup"><span data-stu-id="f02f0-119">-StartIndex</span></span>
<span data-ttu-id="f02f0-120">Der startIndex von Get Containers.</span><span class="sxs-lookup"><span data-stu-id="f02f0-120">The start index of get containers.</span></span>

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

### <span data-ttu-id="f02f0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f02f0-121">CommonParameters</span></span>
<span data-ttu-id="f02f0-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f02f0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f02f0-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f02f0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f02f0-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f02f0-124">INPUTS</span></span>

## <span data-ttu-id="f02f0-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f02f0-125">OUTPUTS</span></span>

## <span data-ttu-id="f02f0-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="f02f0-126">NOTES</span></span>

## <span data-ttu-id="f02f0-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f02f0-127">RELATED LINKS</span></span>

