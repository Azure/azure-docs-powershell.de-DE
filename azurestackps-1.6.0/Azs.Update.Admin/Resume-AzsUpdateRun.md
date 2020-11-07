---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19c8f8fce7c3711c5002f9588900e6bdf8efcbb0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661974"
---
# <span data-ttu-id="8c8f6-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="8c8f6-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="8c8f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c8f6-102">SYNOPSIS</span></span>
<span data-ttu-id="8c8f6-103">Setzt eine zuvor gestartete Update Ausführung fort, die fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="8c8f6-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="8c8f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c8f6-104">SYNTAX</span></span>

### <span data-ttu-id="8c8f6-105">UpdateRuns_Rerun (Standard)</span><span class="sxs-lookup"><span data-stu-id="8c8f6-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c8f6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c8f6-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c8f6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c8f6-107">DESCRIPTION</span></span>
<span data-ttu-id="8c8f6-108">Setzt eine zuvor gestartete Update Ausführung fort, die fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="8c8f6-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="8c8f6-109">Fortgeführte Update Läufe werden an der Stelle fortgesetzt, an der Sie zuletzt fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="8c8f6-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="8c8f6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c8f6-110">EXAMPLES</span></span>

### <span data-ttu-id="8c8f6-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8c8f6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="8c8f6-112">Setzt eine zuvor gestartete Update Ausführung fort, die fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="8c8f6-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="8c8f6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c8f6-113">PARAMETERS</span></span>

### <span data-ttu-id="8c8f6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c8f6-114">-AsJob</span></span>
<span data-ttu-id="8c8f6-115">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="8c8f6-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="8c8f6-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8c8f6-116">-Force</span></span>
<span data-ttu-id="8c8f6-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="8c8f6-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8c8f6-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="8c8f6-118">-Location</span></span>
<span data-ttu-id="8c8f6-119">Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="8c8f6-119">The name of the update location.</span></span>

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

### <span data-ttu-id="8c8f6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8c8f6-120">-Name</span></span>
<span data-ttu-id="8c8f6-121">Update Lauf-ID.</span><span class="sxs-lookup"><span data-stu-id="8c8f6-121">Update run identifier.</span></span>

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

### <span data-ttu-id="8c8f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c8f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="8c8f6-123">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="8c8f6-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="8c8f6-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8c8f6-124">-ResourceId</span></span>
<span data-ttu-id="8c8f6-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8c8f6-125">The resource id.</span></span>

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

### <span data-ttu-id="8c8f6-126">-Updatename</span><span class="sxs-lookup"><span data-stu-id="8c8f6-126">-UpdateName</span></span>
<span data-ttu-id="8c8f6-127">Der Anzeigename des Updates.</span><span class="sxs-lookup"><span data-stu-id="8c8f6-127">Display name of the update.</span></span>

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

### <span data-ttu-id="8c8f6-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8c8f6-128">-Confirm</span></span>
<span data-ttu-id="8c8f6-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c8f6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c8f6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c8f6-130">-WhatIf</span></span>
<span data-ttu-id="8c8f6-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c8f6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c8f6-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c8f6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c8f6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c8f6-133">CommonParameters</span></span>
<span data-ttu-id="8c8f6-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c8f6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c8f6-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c8f6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c8f6-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c8f6-136">INPUTS</span></span>

## <span data-ttu-id="8c8f6-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c8f6-137">OUTPUTS</span></span>

## <span data-ttu-id="8c8f6-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c8f6-138">NOTES</span></span>

## <span data-ttu-id="8c8f6-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c8f6-139">RELATED LINKS</span></span>

