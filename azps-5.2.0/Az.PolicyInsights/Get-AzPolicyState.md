---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372516"
---
# <span data-ttu-id="0d63d-101">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="0d63d-101">Get-AzPolicyState</span></span>

## <span data-ttu-id="0d63d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d63d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d63d-103">Ruft Richtlinienkonformitätszustände für Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="0d63d-103">Gets policy compliance states for resources.</span></span>

## <span data-ttu-id="0d63d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d63d-104">SYNTAX</span></span>

### <span data-ttu-id="0d63d-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="0d63d-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d63d-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="0d63d-106">ManagementGroupScope</span></span>
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d63d-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="0d63d-107">ResourceGroupScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d63d-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="0d63d-108">ResourceScope</span></span>
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d63d-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="0d63d-109">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d63d-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="0d63d-110">PolicyDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d63d-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="0d63d-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d63d-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="0d63d-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d63d-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d63d-113">DESCRIPTION</span></span>
<span data-ttu-id="0d63d-114">Ruft Richtlinienkonformitätszustände für Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="0d63d-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="0d63d-115">Datensätze des Richtlinienstatus können in verschiedenen Bereichen abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="0d63d-116">Basierend auf dem angegebenen Zeitintervall (standardmäßig auf "Letzter Tag" festgelegt) können entweder die neuesten Richtlinienzustände oder alle Übergänge des Richtlinienstatus abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="0d63d-117">Ergebnisse können gefiltert, grouped und Gruppenaggregationen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="0d63d-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0d63d-118">EXAMPLES</span></span>

### <span data-ttu-id="0d63d-119">Beispiel 1: Erhalten der neuesten Richtlinienzustände im aktuellen Abonnementbereich</span><span class="sxs-lookup"><span data-stu-id="0d63d-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState
```

<span data-ttu-id="0d63d-120">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="0d63d-121">Beispiel 2: Erhalten der neuesten Richtlinienzustände im angegebenen Abonnementbereich</span><span class="sxs-lookup"><span data-stu-id="0d63d-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="0d63d-122">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen innerhalb des angegebenen Abonnements generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="0d63d-123">Beispiel 3: Alle Richtlinienzustände im aktuellen Abonnementbereich erhalten</span><span class="sxs-lookup"><span data-stu-id="0d63d-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -All
```

<span data-ttu-id="0d63d-124">Ruft alle Datensätze des vergangenen Richtlinienstatus (einschließlich der letzten) ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="0d63d-125">Beispiel 4: Erhalten der neuesten Richtlinienzustände im Bereich der Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0d63d-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="0d63d-126">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen in der angegebenen Verwaltungsgruppe generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="0d63d-127">Beispiel 5: Erhalten der neuesten Richtlinienzustände im Ressourcengruppenbereich im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="0d63d-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="0d63d-128">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im Abonnement im aktuellen Sitzungskontext) generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="0d63d-129">Beispiel 6: Erhalten der neuesten Richtlinienzustände im Ressourcengruppenbereich im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="0d63d-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="0d63d-130">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im angegebenen Abonnement) generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="0d63d-131">Beispiel 7: Erhalten der neuesten Richtlinienzustände für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="0d63d-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="0d63d-132">Ruft die letzten Datensätze zum Richtlinienstatus ab, die am letzten Tag für die angegebene Ressource generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="0d63d-133">Beispiel 8: Erhalten der neuesten Richtlinienzustände für eine Richtliniensatzdefinition im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="0d63d-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="0d63d-134">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniensatzdefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="0d63d-135">Beispiel 9: Erhalten der neuesten Richtlinienzustände für eine Richtliniensatzdefinition im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="0d63d-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="0d63d-136">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniensatzdefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="0d63d-137">Beispiel 10: Erhalten der neuesten Richtlinienzustände für eine Richtliniendefinition im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="0d63d-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="0d63d-138">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="0d63d-139">Beispiel 11: Erhalten der neuesten Richtlinienzustände für eine Richtliniendefinition im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="0d63d-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="0d63d-140">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="0d63d-141">Beispiel 12: Erhalten der neuesten Richtlinienzustände für eine Richtlinienzuweisung im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="0d63d-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="0d63d-142">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="0d63d-143">Beispiel 13: Erhalten der neuesten Richtlinienzustände für eine Richtlinienzuweisung im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="0d63d-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="0d63d-144">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuweisung (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="0d63d-145">Beispiel 14: Erhalten der neuesten Richtlinienzustände für eine Richtlinienzuweisung in der angegebenen Ressourcengruppe im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="0d63d-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="0d63d-146">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuweisung (die in der Ressourcengruppe im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="0d63d-147">Beispiel 15: Erhalten der neuesten Richtlinienzustände im aktuellen Abonnementbereich mit den Abfrageoptionen "OrderBy", "Top" und "Select"</span><span class="sxs-lookup"><span data-stu-id="0d63d-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="0d63d-148">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="0d63d-149">Der Befehl ordnet die Ergebnisse nach Zeitstempel und Eigenschaften von Richtlinienzuordnungsnamen an und nimmt nur die obersten 5 der in dieser Reihenfolge aufgelisteten Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="0d63d-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="0d63d-150">Außerdem wird ausgewählt, dass nur eine Teilmenge der Spalten für jeden Datensatz aufgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d63d-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="0d63d-151">Beispiel 16: Erhalten der neuesten Richtlinienzustände im aktuellen Abonnementbereich mit den Abfrageoptionen "Von" und "An"</span><span class="sxs-lookup"><span data-stu-id="0d63d-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="0d63d-152">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die innerhalb des datumsbezogenen Bereichs generiert werden, der für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0d63d-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="0d63d-153">Beispiel 17: Erhalten der neuesten Richtlinienzustände im aktuellen Abonnementbereich mit Filterabfrageoption</span><span class="sxs-lookup"><span data-stu-id="0d63d-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="0d63d-154">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="0d63d-155">Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse auf Grundlage einer Richtliniendefinitionsaktion (einschließlich Verweigern- oder Überwachungsaktionen), dem Compliancestatus (einschließlich nicht kompatiblem Status) und dem Ressourcenspeicherort ein (schließt den Oststandort aus).</span><span class="sxs-lookup"><span data-stu-id="0d63d-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="0d63d-156">Beispiel 18: Erhalten der neuesten Richtlinienzustände im aktuellen Abonnementbereich mit "Anwenden" als Aggregation der Zeilenanzahl</span><span class="sxs-lookup"><span data-stu-id="0d63d-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="0d63d-157">Ruft die Anzahl der neuesten Richtlinienstatusdatensätze ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="0d63d-158">Der Befehl gibt nur die Anzahl der Richtlinienstatusdatensätze zurück, die innerhalb der Eigenschaft "AdditionalProperties" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d63d-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="0d63d-159">Beispiel 19: Erhalten der neuesten Richtlinienzustände im aktuellen Abonnementbereich mit Angeben der Gruppierung "Anwenden" mit Aggregation</span><span class="sxs-lookup"><span data-stu-id="0d63d-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="0d63d-160">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="0d63d-161">Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf dem Compliancestatus ein (umfasst nur den nicht kompatiblen Status).</span><span class="sxs-lookup"><span data-stu-id="0d63d-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="0d63d-162">Sie gruppieren die Ergebnisse basierend auf Richtlinienzuweisung, Richtliniensatzdefinition und Richtliniendefinition und berechnen die Anzahl von Datensätzen in jeder Gruppe, die in der Eigenschaft "AdditionalProperties" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d63d-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="0d63d-163">Er ordnet die Ergebnisse nach der Anzahlaggregation in absteigender Reihenfolge an und nimmt nur die obersten 5 der in dieser Reihenfolge aufgeführten Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="0d63d-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="0d63d-164">Beispiel 20: Erhalten der neuesten Richtlinienzustände im aktuellen Abonnementbereich mit "Anwenden" als Angabe der Gruppierung ohne Aggregation</span><span class="sxs-lookup"><span data-stu-id="0d63d-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="0d63d-165">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="0d63d-166">Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf dem Compliancestatus ein (umfasst nur den nicht kompatiblen Status).</span><span class="sxs-lookup"><span data-stu-id="0d63d-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="0d63d-167">Die Ergebnisse werden basierend auf der Ressourcen-ID gruppenweise. Dadurch wird die Liste aller Ressourcen im Abonnement generiert, die für mindestens eine Richtlinie nicht kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="0d63d-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="0d63d-168">Beispiel 21: Erhalten der neuesten Richtlinienzustände im aktuellen Abonnementbereich mit "Anwenden" für mehrere Gruppierungen</span><span class="sxs-lookup"><span data-stu-id="0d63d-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### <span data-ttu-id="0d63d-169">Beispiel 22: Erhalten der neuesten Richtlinienzustände, einschließlich Richtlinienauswertungsdetails für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="0d63d-169">Example 22: Get latest policy states including policy evaluation details for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

<span data-ttu-id="0d63d-170">Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-170">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="0d63d-171">Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf dem Compliancestatus ein (umfasst nur den nicht kompatiblen Status).</span><span class="sxs-lookup"><span data-stu-id="0d63d-171">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="0d63d-172">Die Ergebnisse werden zuerst basierend auf Richtlinienzuweisung, Richtliniensatzdefinition, Richtliniendefinition und Ressourcen-ID gruppen. Anschließend werden die Ergebnisse dieser Gruppierung mit denselben Eigenschaften mit Ausnahme der Ressourcen-ID weiter gruppieren und die Anzahl von Datensätzen in jeder dieser Gruppen berechnet, die in der Eigenschaft "AdditionalProperties" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d63d-172">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="0d63d-173">Er ordnet die Ergebnisse nach der Anzahlaggregation in absteigender Reihenfolge an und nimmt nur die obersten 5 der in dieser Reihenfolge aufgeführten Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="0d63d-173">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="0d63d-174">Dadurch werden die 5 wichtigsten Richtlinien mit der meisten nicht kompatiblen Ressourcen generiert.</span><span class="sxs-lookup"><span data-stu-id="0d63d-174">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="0d63d-175">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d63d-175">PARAMETERS</span></span>

### <span data-ttu-id="0d63d-176">-Alle</span><span class="sxs-lookup"><span data-stu-id="0d63d-176">-All</span></span>
<span data-ttu-id="0d63d-177">Innerhalb des angegebenen Zeitintervalls alle Richtlinienzustände anstelle der neuesten erhalten.</span><span class="sxs-lookup"><span data-stu-id="0d63d-177">Within the specified time interval, get all policy states instead of the latest only.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d63d-178">-Apply</span><span class="sxs-lookup"><span data-stu-id="0d63d-178">-Apply</span></span>
<span data-ttu-id="0d63d-179">Anwenden von Ausdrücken auf Aggregationen mithilfe der OData-Notation.</span><span class="sxs-lookup"><span data-stu-id="0d63d-179">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="0d63d-180">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d63d-180">-DefaultProfile</span></span>
<span data-ttu-id="0d63d-181">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d63d-181">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d63d-182">-Expand</span><span class="sxs-lookup"><span data-stu-id="0d63d-182">-Expand</span></span>
<span data-ttu-id="0d63d-183">Erweitern sie den Ausdruck mithilfe der OData-Notation.</span><span class="sxs-lookup"><span data-stu-id="0d63d-183">Expand expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d63d-184">-Filter</span><span class="sxs-lookup"><span data-stu-id="0d63d-184">-Filter</span></span>
<span data-ttu-id="0d63d-185">Filtern von Ausdrücken mithilfe der OData-Notation.</span><span class="sxs-lookup"><span data-stu-id="0d63d-185">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="0d63d-186">-Von</span><span class="sxs-lookup"><span data-stu-id="0d63d-186">-From</span></span>
<span data-ttu-id="0d63d-187">IN ISO 8601 formatierter Zeitstempel, der die Startzeit des zu abfragenden Intervalls an gibt.</span><span class="sxs-lookup"><span data-stu-id="0d63d-187">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="0d63d-188">Ist diese Einstellung nicht angegeben, wird standardmäßig der Parameterwert "An" minus 1 Tag verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d63d-188">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="0d63d-189">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="0d63d-189">-ManagementGroupName</span></span>
<span data-ttu-id="0d63d-190">Name der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0d63d-190">Management group name.</span></span>

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

### <span data-ttu-id="0d63d-191">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="0d63d-191">-OrderBy</span></span>
<span data-ttu-id="0d63d-192">Sortierung des Ausdrucks mithilfe der OData-Notation.</span><span class="sxs-lookup"><span data-stu-id="0d63d-192">Ordering expression using OData notation.</span></span>
<span data-ttu-id="0d63d-193">Mindestens ein durch Kommas getrennte Spaltennamen mit einem optionalen "Desc" (Standard) oder "asc".</span><span class="sxs-lookup"><span data-stu-id="0d63d-193">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="0d63d-194">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="0d63d-194">-PolicyAssignmentName</span></span>
<span data-ttu-id="0d63d-195">Name der Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="0d63d-195">Policy assignment name.</span></span>

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

### <span data-ttu-id="0d63d-196">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0d63d-196">-PolicyDefinitionName</span></span>
<span data-ttu-id="0d63d-197">Name der Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="0d63d-197">Policy definition name.</span></span>

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

### <span data-ttu-id="0d63d-198">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0d63d-198">-PolicySetDefinitionName</span></span>
<span data-ttu-id="0d63d-199">Name der Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="0d63d-199">Policy set definition name.</span></span>

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

### <span data-ttu-id="0d63d-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d63d-200">-ResourceGroupName</span></span>
<span data-ttu-id="0d63d-201">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="0d63d-201">Resource group name.</span></span>

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

### <span data-ttu-id="0d63d-202">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d63d-202">-ResourceId</span></span>
<span data-ttu-id="0d63d-203">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="0d63d-203">Resource ID.</span></span>

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

### <span data-ttu-id="0d63d-204">-Select</span><span class="sxs-lookup"><span data-stu-id="0d63d-204">-Select</span></span>
<span data-ttu-id="0d63d-205">Auswählen eines Ausdrucks mithilfe der OData-Notation.</span><span class="sxs-lookup"><span data-stu-id="0d63d-205">Select expression using OData notation.</span></span>
<span data-ttu-id="0d63d-206">Einen oder mehrere durch Kommas getrennte Spaltennamen.</span><span class="sxs-lookup"><span data-stu-id="0d63d-206">One or more comma-separated column names.</span></span>
<span data-ttu-id="0d63d-207">Beschränkt die Spalten in jedem Datensatz auf die angeforderten Spalten.</span><span class="sxs-lookup"><span data-stu-id="0d63d-207">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="0d63d-208">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d63d-208">-SubscriptionId</span></span>
<span data-ttu-id="0d63d-209">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="0d63d-209">Subscription ID.</span></span>

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

### <span data-ttu-id="0d63d-210">-To</span><span class="sxs-lookup"><span data-stu-id="0d63d-210">-To</span></span>
<span data-ttu-id="0d63d-211">IN ISO 8601 formatierter Zeitstempel, der die Endzeit des zu abfragenden Intervalls an gibt.</span><span class="sxs-lookup"><span data-stu-id="0d63d-211">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="0d63d-212">Ist diese Angabe nicht angegeben, wird standardmäßig der Zeitpunkt der Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d63d-212">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="0d63d-213">-Top</span><span class="sxs-lookup"><span data-stu-id="0d63d-213">-Top</span></span>
<span data-ttu-id="0d63d-214">Maximale Anzahl der zurückzukehrende Datensätze.</span><span class="sxs-lookup"><span data-stu-id="0d63d-214">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="0d63d-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d63d-215">CommonParameters</span></span>
<span data-ttu-id="0d63d-216">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d63d-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d63d-217">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d63d-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d63d-218">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0d63d-218">INPUTS</span></span>

### <span data-ttu-id="0d63d-219">System.String</span><span class="sxs-lookup"><span data-stu-id="0d63d-219">System.String</span></span>

## <span data-ttu-id="0d63d-220">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0d63d-220">OUTPUTS</span></span>

### <span data-ttu-id="0d63d-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span><span class="sxs-lookup"><span data-stu-id="0d63d-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="0d63d-222">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0d63d-222">NOTES</span></span>

## <span data-ttu-id="0d63d-223">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0d63d-223">RELATED LINKS</span></span>

[<span data-ttu-id="0d63d-224">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="0d63d-224">Get-AzPolicyStateSummary</span></span>](./Get-AzPolicyStateSummary.md)
