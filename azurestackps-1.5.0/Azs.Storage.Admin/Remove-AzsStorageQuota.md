---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b62b8ffbdcdcefff5bbb5c984a19ef0b7cb644
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475813"
---
# <span data-ttu-id="c17f5-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="c17f5-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="c17f5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c17f5-102">SYNOPSIS</span></span>
<span data-ttu-id="c17f5-103">Löschen eines vorhandenen Kontingents</span><span class="sxs-lookup"><span data-stu-id="c17f5-103">Delete an existing quota</span></span>

## <span data-ttu-id="c17f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c17f5-104">SYNTAX</span></span>

### <span data-ttu-id="c17f5-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="c17f5-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c17f5-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c17f5-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c17f5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c17f5-107">DESCRIPTION</span></span>
<span data-ttu-id="c17f5-108">Löschen eines vorhandenen Kontingents</span><span class="sxs-lookup"><span data-stu-id="c17f5-108">Delete an existing quota</span></span>

## <span data-ttu-id="c17f5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c17f5-109">EXAMPLES</span></span>

### <span data-ttu-id="c17f5-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c17f5-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="c17f5-111">Entfernen eines Speicherkontingents nach Namen</span><span class="sxs-lookup"><span data-stu-id="c17f5-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="c17f5-112">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c17f5-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="c17f5-113">Entfernen eines Speicherkontingents durch Piping</span><span class="sxs-lookup"><span data-stu-id="c17f5-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="c17f5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c17f5-114">PARAMETERS</span></span>

### <span data-ttu-id="c17f5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c17f5-115">-Force</span></span>
<span data-ttu-id="c17f5-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="c17f5-116">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17f5-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="c17f5-117">-Location</span></span>
<span data-ttu-id="c17f5-118">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="c17f5-118">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17f5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c17f5-119">-Name</span></span>
<span data-ttu-id="c17f5-120">Der Name des Speicherkontingents.</span><span class="sxs-lookup"><span data-stu-id="c17f5-120">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17f5-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c17f5-121">-ResourceId</span></span>
<span data-ttu-id="c17f5-122">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c17f5-122">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c17f5-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c17f5-123">-Confirm</span></span>
<span data-ttu-id="c17f5-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c17f5-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17f5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c17f5-125">-WhatIf</span></span>
<span data-ttu-id="c17f5-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c17f5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c17f5-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c17f5-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17f5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c17f5-128">CommonParameters</span></span>
<span data-ttu-id="c17f5-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c17f5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c17f5-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c17f5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c17f5-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c17f5-131">INPUTS</span></span>

## <span data-ttu-id="c17f5-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c17f5-132">OUTPUTS</span></span>

## <span data-ttu-id="c17f5-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c17f5-133">NOTES</span></span>

## <span data-ttu-id="c17f5-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c17f5-134">RELATED LINKS</span></span>

