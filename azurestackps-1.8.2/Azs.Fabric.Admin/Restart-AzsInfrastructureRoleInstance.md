---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03dfddb3ec666df5096184c5e00692862e091626
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006886"
---
# <span data-ttu-id="b09bb-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="b09bb-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="b09bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b09bb-102">SYNOPSIS</span></span>
<span data-ttu-id="b09bb-103">Starten Sie eine Infrastrukturrollen Instanz neu.</span><span class="sxs-lookup"><span data-stu-id="b09bb-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="b09bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b09bb-104">SYNTAX</span></span>

### <span data-ttu-id="b09bb-105">Neustart (Standard)</span><span class="sxs-lookup"><span data-stu-id="b09bb-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b09bb-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b09bb-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b09bb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b09bb-107">DESCRIPTION</span></span>
<span data-ttu-id="b09bb-108">Starten Sie eine Infrastrukturrollen Instanz neu.</span><span class="sxs-lookup"><span data-stu-id="b09bb-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="b09bb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b09bb-109">EXAMPLES</span></span>

### <span data-ttu-id="b09bb-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b09bb-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="b09bb-111">Starten Sie eine Infrastrukturrollen Instanz neu.</span><span class="sxs-lookup"><span data-stu-id="b09bb-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="b09bb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b09bb-112">PARAMETERS</span></span>

### <span data-ttu-id="b09bb-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b09bb-113">-Name</span></span>
<span data-ttu-id="b09bb-114">Der Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="b09bb-114">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="b09bb-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="b09bb-115">-Location</span></span>
<span data-ttu-id="b09bb-116">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b09bb-116">Location of the resource.</span></span>

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

### <span data-ttu-id="b09bb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b09bb-117">-ResourceGroupName</span></span>
<span data-ttu-id="b09bb-118">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="b09bb-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b09bb-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b09bb-119">-ResourceId</span></span>
<span data-ttu-id="b09bb-120">Ressourcen-ID der Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="b09bb-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="b09bb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b09bb-121">-AsJob</span></span>
<span data-ttu-id="b09bb-122">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="b09bb-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="b09bb-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b09bb-123">-Force</span></span>
<span data-ttu-id="b09bb-124">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="b09bb-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b09bb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b09bb-125">-WhatIf</span></span>
<span data-ttu-id="b09bb-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b09bb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b09bb-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b09bb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b09bb-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b09bb-128">-Confirm</span></span>
<span data-ttu-id="b09bb-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b09bb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b09bb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b09bb-130">CommonParameters</span></span>
<span data-ttu-id="b09bb-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b09bb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b09bb-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b09bb-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b09bb-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b09bb-133">INPUTS</span></span>

## <span data-ttu-id="b09bb-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b09bb-134">OUTPUTS</span></span>

## <span data-ttu-id="b09bb-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b09bb-135">NOTES</span></span>

## <span data-ttu-id="b09bb-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b09bb-136">RELATED LINKS</span></span>
