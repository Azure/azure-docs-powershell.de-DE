---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a63ccb6706f4d43e890b8805af0d00aff350bc4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827240"
---
# <span data-ttu-id="7b776-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="7b776-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="7b776-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b776-102">SYNOPSIS</span></span>
<span data-ttu-id="7b776-103">Schalten Sie eine Infrastrukturrollen Instanz aus.</span><span class="sxs-lookup"><span data-stu-id="7b776-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="7b776-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b776-104">SYNTAX</span></span>

### <span data-ttu-id="7b776-105">PowerOff (Standard)</span><span class="sxs-lookup"><span data-stu-id="7b776-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b776-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b776-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b776-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b776-107">DESCRIPTION</span></span>
<span data-ttu-id="7b776-108">Schalten Sie eine Infrastrukturrollen Instanz aus.</span><span class="sxs-lookup"><span data-stu-id="7b776-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="7b776-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b776-109">EXAMPLES</span></span>

### <span data-ttu-id="7b776-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7b776-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="7b776-111">Schalten Sie eine Infrastrukturrollen Instanz aus.</span><span class="sxs-lookup"><span data-stu-id="7b776-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="7b776-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b776-112">PARAMETERS</span></span>

### <span data-ttu-id="7b776-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b776-113">-AsJob</span></span>
<span data-ttu-id="7b776-114">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="7b776-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="7b776-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7b776-115">-Force</span></span>
<span data-ttu-id="7b776-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="7b776-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="7b776-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="7b776-117">-Location</span></span>
<span data-ttu-id="7b776-118">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="7b776-118">Location of the resource.</span></span>

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

### <span data-ttu-id="7b776-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7b776-119">-Name</span></span>
<span data-ttu-id="7b776-120">Der Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="7b776-120">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="7b776-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b776-121">-ResourceGroupName</span></span>
<span data-ttu-id="7b776-122">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="7b776-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="7b776-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7b776-123">-ResourceId</span></span>
<span data-ttu-id="7b776-124">Ressourcen-ID der Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="7b776-124">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="7b776-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7b776-125">-Confirm</span></span>
<span data-ttu-id="7b776-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7b776-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b776-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b776-127">-WhatIf</span></span>
<span data-ttu-id="7b776-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b776-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b776-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b776-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b776-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b776-130">CommonParameters</span></span>
<span data-ttu-id="7b776-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b776-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b776-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b776-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b776-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b776-133">INPUTS</span></span>

## <span data-ttu-id="7b776-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b776-134">OUTPUTS</span></span>

## <span data-ttu-id="7b776-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b776-135">NOTES</span></span>

## <span data-ttu-id="7b776-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b776-136">RELATED LINKS</span></span>

