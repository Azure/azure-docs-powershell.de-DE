---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0983e05a36de72148571ccbbc7f1454343ad393a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006840"
---
# <span data-ttu-id="825df-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="825df-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="825df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="825df-102">SYNOPSIS</span></span>
<span data-ttu-id="825df-103">Löschen eines vorhandenen Kontingents</span><span class="sxs-lookup"><span data-stu-id="825df-103">Delete an existing quota</span></span>

## <span data-ttu-id="825df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="825df-104">SYNTAX</span></span>

### <span data-ttu-id="825df-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="825df-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="825df-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="825df-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="825df-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="825df-107">DESCRIPTION</span></span>
<span data-ttu-id="825df-108">Löschen eines vorhandenen Kontingents</span><span class="sxs-lookup"><span data-stu-id="825df-108">Delete an existing quota</span></span>

## <span data-ttu-id="825df-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="825df-109">EXAMPLES</span></span>

### <span data-ttu-id="825df-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="825df-110">EXAMPLE 1</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="825df-111">Entfernen eines Speicherkontingents nach Namen</span><span class="sxs-lookup"><span data-stu-id="825df-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="825df-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="825df-112">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="825df-113">Entfernen eines Speicherkontingents durch Piping</span><span class="sxs-lookup"><span data-stu-id="825df-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="825df-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="825df-114">PARAMETERS</span></span>

### <span data-ttu-id="825df-115">-Name</span><span class="sxs-lookup"><span data-stu-id="825df-115">-Name</span></span>
<span data-ttu-id="825df-116">Der Name des Speicherkontingents.</span><span class="sxs-lookup"><span data-stu-id="825df-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="825df-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="825df-117">-Location</span></span>
<span data-ttu-id="825df-118">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="825df-118">Resource location.</span></span>

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

### <span data-ttu-id="825df-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="825df-119">-ResourceId</span></span>
<span data-ttu-id="825df-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="825df-120">The resource id.</span></span>

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

### <span data-ttu-id="825df-121">-Force</span><span class="sxs-lookup"><span data-stu-id="825df-121">-Force</span></span>
<span data-ttu-id="825df-122">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="825df-122">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="825df-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="825df-123">-WhatIf</span></span>
<span data-ttu-id="825df-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="825df-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="825df-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="825df-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="825df-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="825df-126">-Confirm</span></span>
<span data-ttu-id="825df-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="825df-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="825df-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="825df-128">CommonParameters</span></span>
<span data-ttu-id="825df-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="825df-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="825df-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="825df-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="825df-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="825df-131">INPUTS</span></span>

## <span data-ttu-id="825df-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="825df-132">OUTPUTS</span></span>

## <span data-ttu-id="825df-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="825df-133">NOTES</span></span>

## <span data-ttu-id="825df-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="825df-134">RELATED LINKS</span></span>
