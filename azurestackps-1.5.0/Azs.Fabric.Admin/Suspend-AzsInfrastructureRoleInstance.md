---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348582b008d50371bc937961cd76edbf1ba13762
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475753"
---
# <span data-ttu-id="248d3-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="248d3-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="248d3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="248d3-102">SYNOPSIS</span></span>
<span data-ttu-id="248d3-103">Beenden Sie eine Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="248d3-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="248d3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="248d3-104">SYNTAX</span></span>

### <span data-ttu-id="248d3-105">Shutdown (Standard)</span><span class="sxs-lookup"><span data-stu-id="248d3-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="248d3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="248d3-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="248d3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="248d3-107">DESCRIPTION</span></span>
<span data-ttu-id="248d3-108">Beenden Sie eine Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="248d3-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="248d3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="248d3-109">EXAMPLES</span></span>

### <span data-ttu-id="248d3-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="248d3-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="248d3-111">Beenden Sie eine Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="248d3-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="248d3-112">Bei einem Fehler wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="248d3-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="248d3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="248d3-113">PARAMETERS</span></span>

### <span data-ttu-id="248d3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="248d3-114">-AsJob</span></span>
<span data-ttu-id="248d3-115">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="248d3-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="248d3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="248d3-116">-Force</span></span>
<span data-ttu-id="248d3-117">Keine Bestätigung anfordern</span><span class="sxs-lookup"><span data-stu-id="248d3-117">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="248d3-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="248d3-118">-Location</span></span>
<span data-ttu-id="248d3-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="248d3-119">Location of the resource.</span></span>

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

### <span data-ttu-id="248d3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="248d3-120">-Name</span></span>
<span data-ttu-id="248d3-121">Der Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="248d3-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="248d3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="248d3-122">-ResourceGroupName</span></span>
<span data-ttu-id="248d3-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="248d3-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="248d3-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="248d3-124">-ResourceId</span></span>
<span data-ttu-id="248d3-125">Ressourcen-ID der Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="248d3-125">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="248d3-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="248d3-126">-Confirm</span></span>
<span data-ttu-id="248d3-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="248d3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="248d3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="248d3-128">-WhatIf</span></span>
<span data-ttu-id="248d3-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="248d3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="248d3-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="248d3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="248d3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="248d3-131">CommonParameters</span></span>
<span data-ttu-id="248d3-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="248d3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="248d3-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="248d3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="248d3-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="248d3-134">INPUTS</span></span>

## <span data-ttu-id="248d3-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="248d3-135">OUTPUTS</span></span>

## <span data-ttu-id="248d3-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="248d3-136">NOTES</span></span>

## <span data-ttu-id="248d3-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="248d3-137">RELATED LINKS</span></span>

