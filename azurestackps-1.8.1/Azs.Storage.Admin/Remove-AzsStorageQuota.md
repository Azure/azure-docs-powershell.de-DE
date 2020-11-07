---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0983e05a36de72148571ccbbc7f1454343ad393a
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840836"
---
# <span data-ttu-id="89a5c-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="89a5c-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="89a5c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="89a5c-103">Löschen eines vorhandenen Kontingents</span><span class="sxs-lookup"><span data-stu-id="89a5c-103">Delete an existing quota</span></span>

## <span data-ttu-id="89a5c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89a5c-104">SYNTAX</span></span>

### <span data-ttu-id="89a5c-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="89a5c-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89a5c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="89a5c-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89a5c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89a5c-107">DESCRIPTION</span></span>
<span data-ttu-id="89a5c-108">Löschen eines vorhandenen Kontingents</span><span class="sxs-lookup"><span data-stu-id="89a5c-108">Delete an existing quota</span></span>

## <span data-ttu-id="89a5c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89a5c-109">EXAMPLES</span></span>

### <span data-ttu-id="89a5c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="89a5c-110">EXAMPLE 1</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="89a5c-111">Entfernen eines Speicherkontingents nach Namen</span><span class="sxs-lookup"><span data-stu-id="89a5c-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="89a5c-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="89a5c-112">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="89a5c-113">Entfernen eines Speicherkontingents durch Piping</span><span class="sxs-lookup"><span data-stu-id="89a5c-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="89a5c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="89a5c-114">PARAMETERS</span></span>

### <span data-ttu-id="89a5c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="89a5c-115">-Name</span></span>
<span data-ttu-id="89a5c-116">Der Name des Speicherkontingents.</span><span class="sxs-lookup"><span data-stu-id="89a5c-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="89a5c-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="89a5c-117">-Location</span></span>
<span data-ttu-id="89a5c-118">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="89a5c-118">Resource location.</span></span>

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

### <span data-ttu-id="89a5c-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="89a5c-119">-ResourceId</span></span>
<span data-ttu-id="89a5c-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="89a5c-120">The resource id.</span></span>

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

### <span data-ttu-id="89a5c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="89a5c-121">-Force</span></span>
<span data-ttu-id="89a5c-122">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="89a5c-122">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="89a5c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89a5c-123">-WhatIf</span></span>
<span data-ttu-id="89a5c-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89a5c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89a5c-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="89a5c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89a5c-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="89a5c-126">-Confirm</span></span>
<span data-ttu-id="89a5c-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="89a5c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89a5c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89a5c-128">CommonParameters</span></span>
<span data-ttu-id="89a5c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89a5c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89a5c-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89a5c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89a5c-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89a5c-131">INPUTS</span></span>

## <span data-ttu-id="89a5c-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89a5c-132">OUTPUTS</span></span>

## <span data-ttu-id="89a5c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="89a5c-133">NOTES</span></span>

## <span data-ttu-id="89a5c-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89a5c-134">RELATED LINKS</span></span>
