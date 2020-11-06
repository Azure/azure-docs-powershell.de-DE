---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6e7801a2188fe80577bc6cef9315069b0207f91
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475286"
---
# <span data-ttu-id="96c7a-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="96c7a-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="96c7a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96c7a-102">SYNOPSIS</span></span>
<span data-ttu-id="96c7a-103">Starten Sie eine Infrastrukturrollen Instanz neu.</span><span class="sxs-lookup"><span data-stu-id="96c7a-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="96c7a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96c7a-104">SYNTAX</span></span>

### <span data-ttu-id="96c7a-105">Neustart (Standard)</span><span class="sxs-lookup"><span data-stu-id="96c7a-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96c7a-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="96c7a-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96c7a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96c7a-107">DESCRIPTION</span></span>
<span data-ttu-id="96c7a-108">Starten Sie eine Infrastrukturrollen Instanz neu.</span><span class="sxs-lookup"><span data-stu-id="96c7a-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="96c7a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96c7a-109">EXAMPLES</span></span>

### <span data-ttu-id="96c7a-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="96c7a-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="96c7a-111">Starten Sie eine Infrastrukturrollen Instanz neu.</span><span class="sxs-lookup"><span data-stu-id="96c7a-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="96c7a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="96c7a-112">PARAMETERS</span></span>

### <span data-ttu-id="96c7a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96c7a-113">-AsJob</span></span>
<span data-ttu-id="96c7a-114">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="96c7a-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="96c7a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="96c7a-115">-Force</span></span>
<span data-ttu-id="96c7a-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="96c7a-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="96c7a-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="96c7a-117">-Location</span></span>
<span data-ttu-id="96c7a-118">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="96c7a-118">Location of the resource.</span></span>

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

### <span data-ttu-id="96c7a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="96c7a-119">-Name</span></span>
<span data-ttu-id="96c7a-120">Der Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="96c7a-120">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="96c7a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96c7a-121">-ResourceGroupName</span></span>
<span data-ttu-id="96c7a-122">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="96c7a-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="96c7a-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="96c7a-123">-ResourceId</span></span>
<span data-ttu-id="96c7a-124">Ressourcen-ID der Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="96c7a-124">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="96c7a-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="96c7a-125">-Confirm</span></span>
<span data-ttu-id="96c7a-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="96c7a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96c7a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96c7a-127">-WhatIf</span></span>
<span data-ttu-id="96c7a-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96c7a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96c7a-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96c7a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96c7a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c7a-130">CommonParameters</span></span>
<span data-ttu-id="96c7a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96c7a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c7a-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96c7a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c7a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96c7a-133">INPUTS</span></span>

## <span data-ttu-id="96c7a-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96c7a-134">OUTPUTS</span></span>

## <span data-ttu-id="96c7a-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="96c7a-135">NOTES</span></span>

## <span data-ttu-id="96c7a-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96c7a-136">RELATED LINKS</span></span>

