---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b62b8ffbdcdcefff5bbb5c984a19ef0b7cb644
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827703"
---
# <span data-ttu-id="61ec0-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="61ec0-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="61ec0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="61ec0-103">Löschen eines vorhandenen Kontingents</span><span class="sxs-lookup"><span data-stu-id="61ec0-103">Delete an existing quota</span></span>

## <span data-ttu-id="61ec0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61ec0-104">SYNTAX</span></span>

### <span data-ttu-id="61ec0-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="61ec0-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61ec0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="61ec0-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61ec0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61ec0-107">DESCRIPTION</span></span>
<span data-ttu-id="61ec0-108">Löschen eines vorhandenen Kontingents</span><span class="sxs-lookup"><span data-stu-id="61ec0-108">Delete an existing quota</span></span>

## <span data-ttu-id="61ec0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61ec0-109">EXAMPLES</span></span>

### <span data-ttu-id="61ec0-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="61ec0-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="61ec0-111">Entfernen eines Speicherkontingents nach Namen</span><span class="sxs-lookup"><span data-stu-id="61ec0-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="61ec0-112">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="61ec0-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="61ec0-113">Entfernen eines Speicherkontingents durch Piping</span><span class="sxs-lookup"><span data-stu-id="61ec0-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="61ec0-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="61ec0-114">PARAMETERS</span></span>

### <span data-ttu-id="61ec0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="61ec0-115">-Force</span></span>
<span data-ttu-id="61ec0-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="61ec0-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="61ec0-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="61ec0-117">-Location</span></span>
<span data-ttu-id="61ec0-118">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="61ec0-118">Resource location.</span></span>

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

### <span data-ttu-id="61ec0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="61ec0-119">-Name</span></span>
<span data-ttu-id="61ec0-120">Der Name des Speicherkontingents.</span><span class="sxs-lookup"><span data-stu-id="61ec0-120">The name of the storage quota.</span></span>

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

### <span data-ttu-id="61ec0-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="61ec0-121">-ResourceId</span></span>
<span data-ttu-id="61ec0-122">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="61ec0-122">The resource id.</span></span>

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

### <span data-ttu-id="61ec0-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="61ec0-123">-Confirm</span></span>
<span data-ttu-id="61ec0-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="61ec0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61ec0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61ec0-125">-WhatIf</span></span>
<span data-ttu-id="61ec0-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61ec0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61ec0-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61ec0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61ec0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ec0-128">CommonParameters</span></span>
<span data-ttu-id="61ec0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61ec0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ec0-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61ec0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ec0-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61ec0-131">INPUTS</span></span>

## <span data-ttu-id="61ec0-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61ec0-132">OUTPUTS</span></span>

## <span data-ttu-id="61ec0-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="61ec0-133">NOTES</span></span>

## <span data-ttu-id="61ec0-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61ec0-134">RELATED LINKS</span></span>

