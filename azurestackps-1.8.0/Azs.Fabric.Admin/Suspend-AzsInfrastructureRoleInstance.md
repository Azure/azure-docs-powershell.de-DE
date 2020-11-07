---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04b011279d88f294e1caf95519e29a8368b08546
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827755"
---
# <span data-ttu-id="a1e1b-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="a1e1b-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="a1e1b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a1e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e1b-103">Beenden Sie eine Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="a1e1b-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="a1e1b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1e1b-104">SYNTAX</span></span>

### <span data-ttu-id="a1e1b-105">Shutdown (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1e1b-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1e1b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1e1b-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1e1b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1e1b-107">DESCRIPTION</span></span>
<span data-ttu-id="a1e1b-108">Beenden Sie eine Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="a1e1b-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="a1e1b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1e1b-109">EXAMPLES</span></span>

### <span data-ttu-id="a1e1b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a1e1b-110">EXAMPLE 1</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="a1e1b-111">Beenden Sie eine Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="a1e1b-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="a1e1b-112">Bei einem Fehler wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="a1e1b-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="a1e1b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1e1b-113">PARAMETERS</span></span>

### <span data-ttu-id="a1e1b-114">-Name</span><span class="sxs-lookup"><span data-stu-id="a1e1b-114">-Name</span></span>
<span data-ttu-id="a1e1b-115">Der Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="a1e1b-115">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1e1b-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="a1e1b-116">-Location</span></span>
<span data-ttu-id="a1e1b-117">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a1e1b-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1e1b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e1b-118">-ResourceGroupName</span></span>
<span data-ttu-id="a1e1b-119">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="a1e1b-119">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1e1b-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a1e1b-120">-ResourceId</span></span>
<span data-ttu-id="a1e1b-121">Ressourcen-ID der Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="a1e1b-121">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="a1e1b-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1e1b-122">-AsJob</span></span>
<span data-ttu-id="a1e1b-123">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="a1e1b-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="a1e1b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a1e1b-124">-Force</span></span>
<span data-ttu-id="a1e1b-125">Keine Bestätigung anfordern</span><span class="sxs-lookup"><span data-stu-id="a1e1b-125">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="a1e1b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1e1b-126">-WhatIf</span></span>
<span data-ttu-id="a1e1b-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1e1b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1e1b-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1e1b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1e1b-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a1e1b-129">-Confirm</span></span>
<span data-ttu-id="a1e1b-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1e1b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1e1b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e1b-131">CommonParameters</span></span>
<span data-ttu-id="a1e1b-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1e1b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e1b-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1e1b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e1b-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a1e1b-134">INPUTS</span></span>

## <span data-ttu-id="a1e1b-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a1e1b-135">OUTPUTS</span></span>

## <span data-ttu-id="a1e1b-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a1e1b-136">NOTES</span></span>

## <span data-ttu-id="a1e1b-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a1e1b-137">RELATED LINKS</span></span>
