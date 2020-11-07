---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3a64a045d988d59c2b1aefa650aa695ba09486f
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827739"
---
# <span data-ttu-id="b332e-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="b332e-101">Get-AzsAlert</span></span>

## <span data-ttu-id="b332e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b332e-102">SYNOPSIS</span></span>
<span data-ttu-id="b332e-103">Gibt die Liste aller Benachrichtigungen an einem bestimmten Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="b332e-103">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="b332e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b332e-104">SYNTAX</span></span>

### <span data-ttu-id="b332e-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="b332e-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b332e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="b332e-106">Get</span></span>
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b332e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b332e-107">ResourceId</span></span>
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b332e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b332e-108">DESCRIPTION</span></span>
<span data-ttu-id="b332e-109">Gibt die Liste aller Benachrichtigungen an einem bestimmten Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="b332e-109">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="b332e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b332e-110">EXAMPLES</span></span>

### <span data-ttu-id="b332e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b332e-111">EXAMPLE 1</span></span>
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="b332e-112">Erhalten Sie eine Benachrichtigung nach Namen.</span><span class="sxs-lookup"><span data-stu-id="b332e-112">Get an alert by Name.</span></span>

### <span data-ttu-id="b332e-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b332e-113">EXAMPLE 2</span></span>
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="b332e-114">Rufen Sie alle aktiven Benachrichtigungen ab, und zeigen Sie deren Fehler und Titel an.</span><span class="sxs-lookup"><span data-stu-id="b332e-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="b332e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b332e-115">PARAMETERS</span></span>

### <span data-ttu-id="b332e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b332e-116">-Name</span></span>
<span data-ttu-id="b332e-117">Der Warnungs Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="b332e-117">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b332e-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="b332e-118">-Location</span></span>
<span data-ttu-id="b332e-119">Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="b332e-119">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b332e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b332e-120">-ResourceGroupName</span></span>
<span data-ttu-id="b332e-121">Der Ressourcengruppenname der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="b332e-121">Resource group name of the alert.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b332e-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b332e-122">-ResourceId</span></span>
<span data-ttu-id="b332e-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b332e-123">The resource id.</span></span>

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

### <span data-ttu-id="b332e-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="b332e-124">-Filter</span></span>
<span data-ttu-id="b332e-125">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="b332e-125">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b332e-126">-Top</span><span class="sxs-lookup"><span data-stu-id="b332e-126">-Top</span></span>
<span data-ttu-id="b332e-127">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="b332e-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b332e-128">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="b332e-128">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b332e-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="b332e-129">-Skip</span></span>
<span data-ttu-id="b332e-130">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="b332e-130">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b332e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b332e-131">CommonParameters</span></span>
<span data-ttu-id="b332e-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b332e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b332e-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b332e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b332e-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b332e-134">INPUTS</span></span>

## <span data-ttu-id="b332e-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b332e-135">OUTPUTS</span></span>

### <span data-ttu-id="b332e-136">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. Alert</span><span class="sxs-lookup"><span data-stu-id="b332e-136">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="b332e-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="b332e-137">NOTES</span></span>

## <span data-ttu-id="b332e-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b332e-138">RELATED LINKS</span></span>
