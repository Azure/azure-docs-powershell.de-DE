---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47e4c38d3ccd98350721d358cb98eec55341ba97
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827515"
---
# <span data-ttu-id="843af-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="843af-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="843af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="843af-102">SYNOPSIS</span></span>
<span data-ttu-id="843af-103">Schalten Sie eine Infrastrukturrollen Instanz aus.</span><span class="sxs-lookup"><span data-stu-id="843af-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="843af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="843af-104">SYNTAX</span></span>

### <span data-ttu-id="843af-105">PowerOff (Standard)</span><span class="sxs-lookup"><span data-stu-id="843af-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="843af-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="843af-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="843af-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="843af-107">DESCRIPTION</span></span>
<span data-ttu-id="843af-108">Schalten Sie eine Infrastrukturrollen Instanz aus.</span><span class="sxs-lookup"><span data-stu-id="843af-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="843af-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="843af-109">EXAMPLES</span></span>

### <span data-ttu-id="843af-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="843af-110">EXAMPLE 1</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="843af-111">Schalten Sie eine Infrastrukturrollen Instanz aus.</span><span class="sxs-lookup"><span data-stu-id="843af-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="843af-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="843af-112">PARAMETERS</span></span>

### <span data-ttu-id="843af-113">-Name</span><span class="sxs-lookup"><span data-stu-id="843af-113">-Name</span></span>
<span data-ttu-id="843af-114">Der Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="843af-114">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="843af-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="843af-115">-Location</span></span>
<span data-ttu-id="843af-116">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="843af-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="843af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="843af-117">-ResourceGroupName</span></span>
<span data-ttu-id="843af-118">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="843af-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="843af-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="843af-119">-ResourceId</span></span>
<span data-ttu-id="843af-120">Ressourcen-ID der Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="843af-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="843af-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="843af-121">-AsJob</span></span>
<span data-ttu-id="843af-122">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="843af-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="843af-123">-Force</span><span class="sxs-lookup"><span data-stu-id="843af-123">-Force</span></span>
<span data-ttu-id="843af-124">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="843af-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="843af-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="843af-125">-WhatIf</span></span>
<span data-ttu-id="843af-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="843af-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="843af-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="843af-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="843af-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="843af-128">-Confirm</span></span>
<span data-ttu-id="843af-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="843af-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="843af-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="843af-130">CommonParameters</span></span>
<span data-ttu-id="843af-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="843af-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="843af-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="843af-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="843af-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="843af-133">INPUTS</span></span>

## <span data-ttu-id="843af-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="843af-134">OUTPUTS</span></span>

## <span data-ttu-id="843af-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="843af-135">NOTES</span></span>

## <span data-ttu-id="843af-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="843af-136">RELATED LINKS</span></span>
