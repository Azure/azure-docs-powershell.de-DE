---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48f7fd6280596e70810d330f3fe69b37059e15cd
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827535"
---
# <span data-ttu-id="13356-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="13356-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="13356-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13356-102">SYNOPSIS</span></span>
<span data-ttu-id="13356-103">Schalten Sie eine Infrastrukturrollen Instanz ein.</span><span class="sxs-lookup"><span data-stu-id="13356-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="13356-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13356-104">SYNTAX</span></span>

### <span data-ttu-id="13356-105">PowerOn (Standard)</span><span class="sxs-lookup"><span data-stu-id="13356-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13356-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="13356-106">ResourceId</span></span>
```
Start-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13356-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13356-107">DESCRIPTION</span></span>
<span data-ttu-id="13356-108">Schalten Sie eine Infrastrukturrollen Instanz ein.</span><span class="sxs-lookup"><span data-stu-id="13356-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="13356-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13356-109">EXAMPLES</span></span>

### <span data-ttu-id="13356-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="13356-110">EXAMPLE 1</span></span>
```
Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="13356-111">Schalten Sie eine Infrastrukturrollen Instanz ein.</span><span class="sxs-lookup"><span data-stu-id="13356-111">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="13356-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="13356-112">PARAMETERS</span></span>

### <span data-ttu-id="13356-113">-Name</span><span class="sxs-lookup"><span data-stu-id="13356-113">-Name</span></span>
<span data-ttu-id="13356-114">Der Name der Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="13356-114">Name of the infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13356-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="13356-115">-Location</span></span>
<span data-ttu-id="13356-116">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="13356-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13356-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13356-117">-ResourceGroupName</span></span>
<span data-ttu-id="13356-118">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="13356-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13356-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="13356-119">-ResourceId</span></span>
<span data-ttu-id="13356-120">Ressourcen-ID der Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="13356-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="13356-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13356-121">-AsJob</span></span>
<span data-ttu-id="13356-122">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="13356-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="13356-123">-Force</span><span class="sxs-lookup"><span data-stu-id="13356-123">-Force</span></span>
<span data-ttu-id="13356-124">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="13356-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="13356-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13356-125">-WhatIf</span></span>
<span data-ttu-id="13356-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13356-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13356-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="13356-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13356-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="13356-128">-Confirm</span></span>
<span data-ttu-id="13356-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="13356-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13356-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13356-130">CommonParameters</span></span>
<span data-ttu-id="13356-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13356-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13356-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13356-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13356-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13356-133">INPUTS</span></span>

## <span data-ttu-id="13356-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13356-134">OUTPUTS</span></span>

## <span data-ttu-id="13356-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="13356-135">NOTES</span></span>

## <span data-ttu-id="13356-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13356-136">RELATED LINKS</span></span>
