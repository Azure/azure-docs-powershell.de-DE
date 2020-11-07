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
ms.locfileid: "93826952"
---
# <span data-ttu-id="38772-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="38772-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="38772-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38772-102">SYNOPSIS</span></span>
<span data-ttu-id="38772-103">Setzt eine zuvor gestartete Update Ausführung fort, die fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="38772-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="38772-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38772-104">SYNTAX</span></span>

### <span data-ttu-id="38772-105">UpdateRuns_Rerun (Standard)</span><span class="sxs-lookup"><span data-stu-id="38772-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38772-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="38772-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38772-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38772-107">DESCRIPTION</span></span>
<span data-ttu-id="38772-108">Setzt eine zuvor gestartete Update Ausführung fort, die fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="38772-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="38772-109">Fortgeführte Update Läufe werden an der Stelle fortgesetzt, an der Sie zuletzt fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="38772-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="38772-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38772-110">EXAMPLES</span></span>

### <span data-ttu-id="38772-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="38772-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="38772-112">Setzt eine zuvor gestartete Update Ausführung fort, die fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="38772-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="38772-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="38772-113">PARAMETERS</span></span>

### <span data-ttu-id="38772-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38772-114">-AsJob</span></span>
<span data-ttu-id="38772-115">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="38772-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="38772-116">-Force</span><span class="sxs-lookup"><span data-stu-id="38772-116">-Force</span></span>
<span data-ttu-id="38772-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="38772-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="38772-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="38772-118">-Location</span></span>
<span data-ttu-id="38772-119">Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="38772-119">The name of the update location.</span></span>

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

### <span data-ttu-id="38772-120">-Name</span><span class="sxs-lookup"><span data-stu-id="38772-120">-Name</span></span>
<span data-ttu-id="38772-121">Update Lauf-ID.</span><span class="sxs-lookup"><span data-stu-id="38772-121">Update run identifier.</span></span>

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

### <span data-ttu-id="38772-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38772-122">-ResourceGroupName</span></span>
<span data-ttu-id="38772-123">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="38772-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="38772-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="38772-124">-ResourceId</span></span>
<span data-ttu-id="38772-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="38772-125">The resource id.</span></span>

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

### <span data-ttu-id="38772-126">-Updatename</span><span class="sxs-lookup"><span data-stu-id="38772-126">-UpdateName</span></span>
<span data-ttu-id="38772-127">Der Anzeigename des Updates.</span><span class="sxs-lookup"><span data-stu-id="38772-127">Display name of the update.</span></span>

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

### <span data-ttu-id="38772-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="38772-128">-Confirm</span></span>
<span data-ttu-id="38772-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="38772-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38772-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38772-130">-WhatIf</span></span>
<span data-ttu-id="38772-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38772-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38772-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38772-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38772-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38772-133">CommonParameters</span></span>
<span data-ttu-id="38772-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38772-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38772-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38772-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38772-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38772-136">INPUTS</span></span>

## <span data-ttu-id="38772-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38772-137">OUTPUTS</span></span>

## <span data-ttu-id="38772-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="38772-138">NOTES</span></span>

## <span data-ttu-id="38772-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38772-139">RELATED LINKS</span></span>

