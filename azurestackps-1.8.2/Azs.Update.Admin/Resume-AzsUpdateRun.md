---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb3b784d079d1de3cec1d4fe3ec50a2853a4b054
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007270"
---
# <span data-ttu-id="f5d9d-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="f5d9d-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="f5d9d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="f5d9d-103">Setzt eine zuvor gestartete Update Ausführung fort, die fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="f5d9d-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="f5d9d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5d9d-104">SYNTAX</span></span>

### <span data-ttu-id="f5d9d-105">UpdateRuns_Rerun (Standard)</span><span class="sxs-lookup"><span data-stu-id="f5d9d-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5d9d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5d9d-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5d9d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5d9d-107">DESCRIPTION</span></span>
<span data-ttu-id="f5d9d-108">Setzt eine zuvor gestartete Update Ausführung fort, die fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="f5d9d-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="f5d9d-109">Fortgeführte Update Läufe werden an der Stelle fortgesetzt, an der Sie zuletzt fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="f5d9d-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="f5d9d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5d9d-110">EXAMPLES</span></span>

### <span data-ttu-id="f5d9d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f5d9d-111">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="f5d9d-112">Setzt eine zuvor gestartete Update Ausführung fort, die fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="f5d9d-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="f5d9d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5d9d-113">PARAMETERS</span></span>

### <span data-ttu-id="f5d9d-114">-Name</span><span class="sxs-lookup"><span data-stu-id="f5d9d-114">-Name</span></span>
<span data-ttu-id="f5d9d-115">Update Lauf-ID.</span><span class="sxs-lookup"><span data-stu-id="f5d9d-115">Update run identifier.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5d9d-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="f5d9d-116">-Location</span></span>
<span data-ttu-id="f5d9d-117">Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="f5d9d-117">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5d9d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5d9d-118">-ResourceGroupName</span></span>
<span data-ttu-id="f5d9d-119">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="f5d9d-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5d9d-120">-Updatename</span><span class="sxs-lookup"><span data-stu-id="f5d9d-120">-UpdateName</span></span>
<span data-ttu-id="f5d9d-121">Der Anzeigename des Updates.</span><span class="sxs-lookup"><span data-stu-id="f5d9d-121">Display name of the update.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5d9d-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5d9d-122">-AsJob</span></span>
<span data-ttu-id="f5d9d-123">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f5d9d-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f5d9d-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f5d9d-124">-ResourceId</span></span>
<span data-ttu-id="f5d9d-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f5d9d-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5d9d-126">-Force</span><span class="sxs-lookup"><span data-stu-id="f5d9d-126">-Force</span></span>
<span data-ttu-id="f5d9d-127">Kennzeichnen, um das Element ohne Bestätigung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f5d9d-127">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="f5d9d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5d9d-128">-WhatIf</span></span>
<span data-ttu-id="f5d9d-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5d9d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5d9d-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5d9d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5d9d-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f5d9d-131">-Confirm</span></span>
<span data-ttu-id="f5d9d-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5d9d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5d9d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5d9d-133">CommonParameters</span></span>
<span data-ttu-id="f5d9d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5d9d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5d9d-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5d9d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5d9d-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5d9d-136">INPUTS</span></span>

## <span data-ttu-id="f5d9d-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5d9d-137">OUTPUTS</span></span>

## <span data-ttu-id="f5d9d-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5d9d-138">NOTES</span></span>

## <span data-ttu-id="f5d9d-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5d9d-139">RELATED LINKS</span></span>
