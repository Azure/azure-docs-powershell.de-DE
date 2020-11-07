---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 781b920bf955a84554b9152f54c9847a00a8b160
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828223"
---
# <span data-ttu-id="52a84-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="52a84-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="52a84-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52a84-102">SYNOPSIS</span></span>
<span data-ttu-id="52a84-103">Startet die Rolle der Anforderungs Infrastruktur neu.</span><span class="sxs-lookup"><span data-stu-id="52a84-103">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="52a84-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52a84-104">SYNTAX</span></span>

### <span data-ttu-id="52a84-105">Neustart (Standard)</span><span class="sxs-lookup"><span data-stu-id="52a84-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52a84-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="52a84-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52a84-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52a84-107">DESCRIPTION</span></span>
<span data-ttu-id="52a84-108">Startet die Rolle der Anforderungs Infrastruktur neu.</span><span class="sxs-lookup"><span data-stu-id="52a84-108">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="52a84-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52a84-109">EXAMPLES</span></span>

### <span data-ttu-id="52a84-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="52a84-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="52a84-111">Starten Sie eine abgestürzte Infrastruktur Rolle erneut.</span><span class="sxs-lookup"><span data-stu-id="52a84-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="52a84-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="52a84-112">PARAMETERS</span></span>

### <span data-ttu-id="52a84-113">-Name</span><span class="sxs-lookup"><span data-stu-id="52a84-113">-Name</span></span>
<span data-ttu-id="52a84-114">Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="52a84-114">Infrastructure role name.</span></span>

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

### <span data-ttu-id="52a84-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="52a84-115">-Location</span></span>
<span data-ttu-id="52a84-116">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="52a84-116">Location of the resource.</span></span>

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

### <span data-ttu-id="52a84-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52a84-117">-ResourceGroupName</span></span>
<span data-ttu-id="52a84-118">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="52a84-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="52a84-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="52a84-119">-ResourceId</span></span>
<span data-ttu-id="52a84-120">Ressourcen-ID der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="52a84-120">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="52a84-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52a84-121">-AsJob</span></span>
<span data-ttu-id="52a84-122">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="52a84-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="52a84-123">-Force</span><span class="sxs-lookup"><span data-stu-id="52a84-123">-Force</span></span>
<span data-ttu-id="52a84-124">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="52a84-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="52a84-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52a84-125">-WhatIf</span></span>
<span data-ttu-id="52a84-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="52a84-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52a84-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="52a84-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52a84-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="52a84-128">-Confirm</span></span>
<span data-ttu-id="52a84-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="52a84-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52a84-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a84-130">CommonParameters</span></span>
<span data-ttu-id="52a84-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52a84-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a84-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52a84-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a84-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52a84-133">INPUTS</span></span>

## <span data-ttu-id="52a84-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52a84-134">OUTPUTS</span></span>

## <span data-ttu-id="52a84-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="52a84-135">NOTES</span></span>

## <span data-ttu-id="52a84-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52a84-136">RELATED LINKS</span></span>
