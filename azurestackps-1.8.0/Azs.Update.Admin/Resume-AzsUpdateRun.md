---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb3b784d079d1de3cec1d4fe3ec50a2853a4b054
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827427"
---
# <span data-ttu-id="f8b14-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="f8b14-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="f8b14-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8b14-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b14-103">Setzt eine zuvor gestartete Update Ausführung fort, die fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="f8b14-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="f8b14-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8b14-104">SYNTAX</span></span>

### <span data-ttu-id="f8b14-105">UpdateRuns_Rerun (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8b14-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8b14-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8b14-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8b14-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8b14-107">DESCRIPTION</span></span>
<span data-ttu-id="f8b14-108">Setzt eine zuvor gestartete Update Ausführung fort, die fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="f8b14-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="f8b14-109">Fortgeführte Update Läufe werden an der Stelle fortgesetzt, an der Sie zuletzt fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="f8b14-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="f8b14-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8b14-110">EXAMPLES</span></span>

### <span data-ttu-id="f8b14-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8b14-111">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="f8b14-112">Setzt eine zuvor gestartete Update Ausführung fort, die fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="f8b14-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="f8b14-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8b14-113">PARAMETERS</span></span>

### <span data-ttu-id="f8b14-114">-Name</span><span class="sxs-lookup"><span data-stu-id="f8b14-114">-Name</span></span>
<span data-ttu-id="f8b14-115">Update Lauf-ID.</span><span class="sxs-lookup"><span data-stu-id="f8b14-115">Update run identifier.</span></span>

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

### <span data-ttu-id="f8b14-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="f8b14-116">-Location</span></span>
<span data-ttu-id="f8b14-117">Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="f8b14-117">The name of the update location.</span></span>

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

### <span data-ttu-id="f8b14-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8b14-118">-ResourceGroupName</span></span>
<span data-ttu-id="f8b14-119">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="f8b14-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="f8b14-120">-Updatename</span><span class="sxs-lookup"><span data-stu-id="f8b14-120">-UpdateName</span></span>
<span data-ttu-id="f8b14-121">Der Anzeigename des Updates.</span><span class="sxs-lookup"><span data-stu-id="f8b14-121">Display name of the update.</span></span>

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

### <span data-ttu-id="f8b14-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8b14-122">-AsJob</span></span>
<span data-ttu-id="f8b14-123">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f8b14-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f8b14-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f8b14-124">-ResourceId</span></span>
<span data-ttu-id="f8b14-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f8b14-125">The resource id.</span></span>

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

### <span data-ttu-id="f8b14-126">-Force</span><span class="sxs-lookup"><span data-stu-id="f8b14-126">-Force</span></span>
<span data-ttu-id="f8b14-127">Kennzeichnen, um das Element ohne Bestätigung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f8b14-127">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="f8b14-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8b14-128">-WhatIf</span></span>
<span data-ttu-id="f8b14-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8b14-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8b14-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8b14-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8b14-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8b14-131">-Confirm</span></span>
<span data-ttu-id="f8b14-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8b14-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8b14-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b14-133">CommonParameters</span></span>
<span data-ttu-id="f8b14-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b14-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b14-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8b14-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b14-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8b14-136">INPUTS</span></span>

## <span data-ttu-id="f8b14-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8b14-137">OUTPUTS</span></span>

## <span data-ttu-id="f8b14-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8b14-138">NOTES</span></span>

## <span data-ttu-id="f8b14-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8b14-139">RELATED LINKS</span></span>
