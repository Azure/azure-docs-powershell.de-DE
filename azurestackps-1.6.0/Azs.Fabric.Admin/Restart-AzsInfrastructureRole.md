---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: da781ee77cb94e7bc442b72ad0655041cf23b546
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474805"
---
# <span data-ttu-id="5935f-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="5935f-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="5935f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5935f-102">SYNOPSIS</span></span>
<span data-ttu-id="5935f-103">Startet die angeforderte Infrastruktur Rolle neu.</span><span class="sxs-lookup"><span data-stu-id="5935f-103">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="5935f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5935f-104">SYNTAX</span></span>

### <span data-ttu-id="5935f-105">Neustart (Standard)</span><span class="sxs-lookup"><span data-stu-id="5935f-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5935f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5935f-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5935f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5935f-107">DESCRIPTION</span></span>
<span data-ttu-id="5935f-108">Startet die angeforderte Infrastruktur Rolle neu.</span><span class="sxs-lookup"><span data-stu-id="5935f-108">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="5935f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5935f-109">EXAMPLES</span></span>

### <span data-ttu-id="5935f-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5935f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restart-AzsInfrastructureRole -Name "Compute Controller"
```

<span data-ttu-id="5935f-111">Starten Sie eine abgestürzte Infrastruktur Rolle erneut.</span><span class="sxs-lookup"><span data-stu-id="5935f-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="5935f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5935f-112">PARAMETERS</span></span>

### <span data-ttu-id="5935f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5935f-113">-AsJob</span></span>
<span data-ttu-id="5935f-114">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="5935f-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="5935f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5935f-115">-Force</span></span>
<span data-ttu-id="5935f-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="5935f-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5935f-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="5935f-117">-Location</span></span>
<span data-ttu-id="5935f-118">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5935f-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5935f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5935f-119">-Name</span></span>
<span data-ttu-id="5935f-120">Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="5935f-120">Infrastructure role name.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5935f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5935f-121">-ResourceGroupName</span></span>
<span data-ttu-id="5935f-122">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="5935f-122">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5935f-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5935f-123">-ResourceId</span></span>
<span data-ttu-id="5935f-124">Ressourcen-ID der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="5935f-124">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="5935f-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5935f-125">-Confirm</span></span>
<span data-ttu-id="5935f-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5935f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5935f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5935f-127">-WhatIf</span></span>
<span data-ttu-id="5935f-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5935f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5935f-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5935f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5935f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5935f-130">CommonParameters</span></span>
<span data-ttu-id="5935f-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5935f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5935f-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5935f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5935f-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5935f-133">INPUTS</span></span>

## <span data-ttu-id="5935f-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5935f-134">OUTPUTS</span></span>

## <span data-ttu-id="5935f-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="5935f-135">NOTES</span></span>

## <span data-ttu-id="5935f-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5935f-136">RELATED LINKS</span></span>

