---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 744618bb2cc12b4d57bfb1ed42267fcbbe7a86ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459788"
---
# <span data-ttu-id="af0c2-101">Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="af0c2-101">Get-AzPolicyEvent</span></span>

## <span data-ttu-id="af0c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af0c2-102">SYNOPSIS</span></span>
<span data-ttu-id="af0c2-103">Ruft Richtlinienauswertungsereignisse ab, die generiert werden, wenn Ressourcen erstellt oder aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

## <span data-ttu-id="af0c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af0c2-104">SYNTAX</span></span>

### <span data-ttu-id="af0c2-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="af0c2-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af0c2-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="af0c2-106">ManagementGroupScope</span></span>
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af0c2-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="af0c2-107">ResourceGroupScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af0c2-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="af0c2-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af0c2-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="af0c2-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af0c2-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="af0c2-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af0c2-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="af0c2-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af0c2-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="af0c2-112">ResourceScope</span></span>
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af0c2-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af0c2-113">DESCRIPTION</span></span>
<span data-ttu-id="af0c2-114">Ruft Richtlinienauswertungsereignisse ab, die generiert werden, wenn Ressourcen erstellt oder aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="af0c2-115">Richtlinienereignisdatensätze können basierend auf dem angegebenen Zeitintervall (Standardwert auf "Letzter Tag").</span><span class="sxs-lookup"><span data-stu-id="af0c2-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="af0c2-116">Ergebnisse können gefiltert, grouped und Gruppenaggregationen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="af0c2-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="af0c2-117">EXAMPLES</span></span>

### <span data-ttu-id="af0c2-118">Beispiel 1: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich</span><span class="sxs-lookup"><span data-stu-id="af0c2-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent
```

<span data-ttu-id="af0c2-119">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="af0c2-120">Beispiel 2: Erhalten von Richtlinienereignissen im angegebenen Abonnementbereich</span><span class="sxs-lookup"><span data-stu-id="af0c2-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="af0c2-121">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb des angegebenen Abonnements generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="af0c2-122">Beispiel 3: Erhalten von Richtlinienereignissen im Bereich der Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="af0c2-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="af0c2-123">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen in der angegebenen Verwaltungsgruppe generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="af0c2-124">Beispiel 4: Erhalten von Richtlinienereignissen im Ressourcengruppenbereich im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="af0c2-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="af0c2-125">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im Abonnement im aktuellen Sitzungskontext) generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="af0c2-126">Beispiel 5: Erhalten von Richtlinienereignissen im Ressourcengruppenbereich im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="af0c2-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="af0c2-127">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im angegebenen Abonnement) generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="af0c2-128">Beispiel 6: Erhalten von Richtlinienereignissen für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="af0c2-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="af0c2-129">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für die angegebene Ressource generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="af0c2-130">Beispiel 7: Erhalten von Richtlinienereignissen für eine Richtliniensatzdefinition im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="af0c2-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="af0c2-131">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniensatzdefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="af0c2-132">Beispiel 8: Erhalten von Richtlinienereignissen für eine Richtliniensatzdefinition im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="af0c2-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="af0c2-133">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniensatzdefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="af0c2-134">Beispiel 9: Erhalten von Richtlinienereignissen für eine Richtliniendefinition im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="af0c2-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="af0c2-135">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="af0c2-136">Beispiel 10: Erhalten von Richtlinienereignissen für eine Richtliniendefinition im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="af0c2-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="af0c2-137">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="af0c2-138">Beispiel 11: Erhalten von Richtlinienereignissen für eine Richtlinienzuweisung im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="af0c2-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="af0c2-139">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuweisung (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="af0c2-140">Beispiel 12: Erhalten von Richtlinienereignissen für eine Richtlinienzuweisung im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="af0c2-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="af0c2-141">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuweisung (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="af0c2-142">Beispiel 13: Erhalten von Richtlinienereignissen für eine Richtlinienzuordnung in der angegebenen Ressourcengruppe im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="af0c2-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="af0c2-143">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuweisung (die in der Ressourcengruppe im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="af0c2-144">Beispiel 14: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich mit den Abfrageoptionen "OrderBy", "Top" und "Select"</span><span class="sxs-lookup"><span data-stu-id="af0c2-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="af0c2-145">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="af0c2-146">Der Befehl ordnet die Ergebnisse nach Zeitstempel und Eigenschaften des Namens der Richtlinienzuweisung an und nimmt nur die obersten 5 der in dieser Reihenfolge aufgelisteten Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="af0c2-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="af0c2-147">Außerdem wird ausgewählt, dass nur eine Teilmenge der Spalten für jeden Datensatz aufgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af0c2-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="af0c2-148">Beispiel 15: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich mit den Abfrageoptionen "Von" und "An"</span><span class="sxs-lookup"><span data-stu-id="af0c2-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="af0c2-149">Ruft Richtlinienereignisdatensätze ab, die innerhalb des datumsbezogenen Bereichs generiert werden, der für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="af0c2-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="af0c2-150">Beispiel 16: Anzeigen von Richtlinienereignissen im aktuellen Abonnementbereich mit Filterabfrageoption</span><span class="sxs-lookup"><span data-stu-id="af0c2-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="af0c2-151">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="af0c2-152">Der Befehl beschränkt die von der Filterung zurückgegebenen Ergebnisse auf Grundlage einer Richtliniendefinitionsaktion (einschließlich Verweigern- oder Überwachungsaktionen) und dem Ressourcenstandort (schließt den Oststandort aus).</span><span class="sxs-lookup"><span data-stu-id="af0c2-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="af0c2-153">Beispiel 17: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich mit "Anwenden" zur Angabe der Zeilenanzahlaggregation</span><span class="sxs-lookup"><span data-stu-id="af0c2-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="af0c2-154">Ruft die Anzahl der am letzten Tag generierten Richtlinienereignisdatensätze für alle Ressourcen im Abonnement im aktuellen Sitzungskontext ab.</span><span class="sxs-lookup"><span data-stu-id="af0c2-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="af0c2-155">Der Befehl gibt nur die Anzahl der Richtlinienereigniseinträge zurück, die in der Eigenschaft "AdditionalProperties" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="af0c2-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="af0c2-156">Beispiel 18: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich, mit "Anwenden" angegebener Gruppierung mit Aggregation</span><span class="sxs-lookup"><span data-stu-id="af0c2-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="af0c2-157">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="af0c2-158">Der Befehl beschränkt die durch das Filtern auf Basis einer Richtliniendefinitionsaktion zurückgegebenen Ergebnisse (umfasst nur Überwachungs- und Verweigernereignisse).</span><span class="sxs-lookup"><span data-stu-id="af0c2-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="af0c2-159">Sie gruppieren die Ergebnisse basierend auf Richtlinienzuordnung, Richtliniendefinition, Richtliniendefinitionsaktion und Ressourcen-ID und berechnen die Anzahl von Datensätzen in jeder Gruppe, die in der Eigenschaft "AdditionalProperties" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="af0c2-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="af0c2-160">Sie ordnet die Ergebnisse nach der Anzahlaggregation in absteigender Reihenfolge an und nimmt nur die obersten 5 der in dieser Reihenfolge aufgeführten Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="af0c2-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="af0c2-161">Beispiel 19: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich mit "Anwenden" als Gruppierung ohne Aggregation</span><span class="sxs-lookup"><span data-stu-id="af0c2-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="af0c2-162">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="af0c2-163">Der Befehl beschränkt die durch das Filtern auf Basis einer Richtliniendefinitionsaktion zurückgegebenen Ergebnisse (umfasst nur Überwachungs- und Verweigernereignisse).</span><span class="sxs-lookup"><span data-stu-id="af0c2-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="af0c2-164">Die Ergebnisse werden basierend auf der Ressourcen-ID gruppenweise. Dadurch wird die Liste aller Ressourcen innerhalb des Abonnements generiert, von dem ein Richtlinienereignis für mindestens eine Überwachungs- oder Verweigernrichtlinie generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="af0c2-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="af0c2-165">Beispiel 20: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich mit "Anwenden" mit Angabe mehrerer Gruppierungen</span><span class="sxs-lookup"><span data-stu-id="af0c2-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="af0c2-166">Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="af0c2-167">Der Befehl schränkt die von der Filterung auf Grundlage einer Richtliniendefinitionsaktion zurückgegebenen Ergebnisse ein (umfasst nur "Verweigern"-Ereignisse).</span><span class="sxs-lookup"><span data-stu-id="af0c2-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="af0c2-168">Die Ergebnisse werden zuerst basierend auf Richtlinienzuweisung, Richtliniendefinition und Ressourcen-ID gruppenweise. Anschließend werden die Ergebnisse dieser Gruppierung mit denselben Eigenschaften mit Ausnahme der Ressourcen-ID weiter gruppieren und die Anzahl von Datensätzen in jeder dieser Gruppen berechnet, die in der Eigenschaft "AdditionalProperties" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="af0c2-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="af0c2-169">Sie ordnet die Ergebnisse nach der Anzahlaggregation in absteigender Reihenfolge an und nimmt nur die obersten 5 der in dieser Reihenfolge aufgeführten Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="af0c2-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="af0c2-170">Dadurch werden die 5 am häufigsten abgelehnten Richtlinien mit der größten Anzahl verweigerter Ressourcen generiert.</span><span class="sxs-lookup"><span data-stu-id="af0c2-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="af0c2-171">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af0c2-171">PARAMETERS</span></span>

### <span data-ttu-id="af0c2-172">-Apply</span><span class="sxs-lookup"><span data-stu-id="af0c2-172">-Apply</span></span>
<span data-ttu-id="af0c2-173">Anwenden von Ausdrücken auf Aggregationen mithilfe der OData-Notation.</span><span class="sxs-lookup"><span data-stu-id="af0c2-173">Apply expression for aggregations using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af0c2-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af0c2-174">-DefaultProfile</span></span>
<span data-ttu-id="af0c2-175">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af0c2-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af0c2-176">-Filter</span><span class="sxs-lookup"><span data-stu-id="af0c2-176">-Filter</span></span>
<span data-ttu-id="af0c2-177">Filtern von Ausdrücken mithilfe der OData-Notation.</span><span class="sxs-lookup"><span data-stu-id="af0c2-177">Filter expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af0c2-178">-Von</span><span class="sxs-lookup"><span data-stu-id="af0c2-178">-From</span></span>
<span data-ttu-id="af0c2-179">IN ISO 8601 formatierter Zeitstempel, der die Startzeit des zu abfragenden Intervalls an gibt.</span><span class="sxs-lookup"><span data-stu-id="af0c2-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="af0c2-180">Ist diese Einstellung nicht angegeben, wird standardmäßig der Parameterwert "An" minus 1 Tag verwendet.</span><span class="sxs-lookup"><span data-stu-id="af0c2-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af0c2-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="af0c2-181">-ManagementGroupName</span></span>
<span data-ttu-id="af0c2-182">Name der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="af0c2-182">Management group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af0c2-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="af0c2-183">-OrderBy</span></span>
<span data-ttu-id="af0c2-184">Sortierung des Ausdrucks mithilfe der OData-Notation.</span><span class="sxs-lookup"><span data-stu-id="af0c2-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="af0c2-185">Ein oder mehrere durch Kommas getrennte Spaltennamen mit einem optionalen "Desc" (Standard) oder "asc".</span><span class="sxs-lookup"><span data-stu-id="af0c2-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af0c2-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="af0c2-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="af0c2-187">Name der Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="af0c2-187">Policy assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af0c2-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="af0c2-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="af0c2-189">Name der Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="af0c2-189">Policy definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af0c2-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="af0c2-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="af0c2-191">Name der Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="af0c2-191">Policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af0c2-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af0c2-192">-ResourceGroupName</span></span>
<span data-ttu-id="af0c2-193">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="af0c2-193">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af0c2-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af0c2-194">-ResourceId</span></span>
<span data-ttu-id="af0c2-195">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="af0c2-195">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af0c2-196">-Select</span><span class="sxs-lookup"><span data-stu-id="af0c2-196">-Select</span></span>
<span data-ttu-id="af0c2-197">Auswählen von Ausdrücken mithilfe der OData-Notation.</span><span class="sxs-lookup"><span data-stu-id="af0c2-197">Select expression using OData notation.</span></span>
<span data-ttu-id="af0c2-198">Mindestens ein durch Kommas getrennte Spaltennamen.</span><span class="sxs-lookup"><span data-stu-id="af0c2-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="af0c2-199">Beschränkt die Spalten in jedem Datensatz auf die angeforderten Spalten.</span><span class="sxs-lookup"><span data-stu-id="af0c2-199">Limits the columns on each record to just those requested.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af0c2-200">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af0c2-200">-SubscriptionId</span></span>
<span data-ttu-id="af0c2-201">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="af0c2-201">Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af0c2-202">-To</span><span class="sxs-lookup"><span data-stu-id="af0c2-202">-To</span></span>
<span data-ttu-id="af0c2-203">IN ISO 8601 formatierter Zeitstempel, der die Endzeit des zu abfragenden Intervalls an gibt.</span><span class="sxs-lookup"><span data-stu-id="af0c2-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="af0c2-204">Ist diese Angabe nicht angegeben, wird standardmäßig der Zeitpunkt der Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="af0c2-204">When not specified, defaults to time of request.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af0c2-205">-Top</span><span class="sxs-lookup"><span data-stu-id="af0c2-205">-Top</span></span>
<span data-ttu-id="af0c2-206">Maximale Anzahl der zurückzukehrende Datensätze.</span><span class="sxs-lookup"><span data-stu-id="af0c2-206">Maximum number of records to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af0c2-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af0c2-207">CommonParameters</span></span>
<span data-ttu-id="af0c2-208">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af0c2-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af0c2-209">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af0c2-209">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af0c2-210">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="af0c2-210">INPUTS</span></span>

### <span data-ttu-id="af0c2-211">System.String</span><span class="sxs-lookup"><span data-stu-id="af0c2-211">System.String</span></span>

## <span data-ttu-id="af0c2-212">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="af0c2-212">OUTPUTS</span></span>

### <span data-ttu-id="af0c2-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="af0c2-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="af0c2-214">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="af0c2-214">NOTES</span></span>

## <span data-ttu-id="af0c2-215">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="af0c2-215">RELATED LINKS</span></span>
