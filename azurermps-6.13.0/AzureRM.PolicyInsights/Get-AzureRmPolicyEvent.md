---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyEvent.md
ms.openlocfilehash: 0c4e4f531dac3f75f0eff69ba1dcfc644473ea06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498205"
---
# <span data-ttu-id="9f4e3-101">Get-AzureRmPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="9f4e3-101">Get-AzureRmPolicyEvent</span></span>

## <span data-ttu-id="9f4e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9f4e3-102">SYNOPSIS</span></span>
<span data-ttu-id="9f4e3-103">Ruft Richtlinien Auswertungs Ereignisse ab, die beim Erstellen oder Aktualisieren von Ressourcen generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f4e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f4e3-104">SYNTAX</span></span>

### <span data-ttu-id="9f4e3-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="9f4e3-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f4e3-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="9f4e3-106">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f4e3-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="9f4e3-107">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f4e3-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="9f4e3-108">PolicySetDefinitionScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f4e3-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="9f4e3-109">PolicyDefinitionScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f4e3-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="9f4e3-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f4e3-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="9f4e3-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f4e3-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="9f4e3-112">ResourceScope</span></span>
```
Get-AzureRmPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f4e3-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f4e3-113">DESCRIPTION</span></span>
<span data-ttu-id="9f4e3-114">Ruft Richtlinien Auswertungs Ereignisse ab, die beim Erstellen oder Aktualisieren von Ressourcen generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="9f4e3-115">Richtlinien Ereigniseinträge können anhand des angegebenen Zeitintervalls in unterschiedlichen Bereichen abgefragt werden (Standardmäßig ist der letzte Tag).</span><span class="sxs-lookup"><span data-stu-id="9f4e3-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="9f4e3-116">Ergebnisse können gefiltert, gruppiert und Gruppen Aggregationen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="9f4e3-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f4e3-117">EXAMPLES</span></span>

### <span data-ttu-id="9f4e3-118">Beispiel 1: Abrufen von Richtlinien Ereignissen im aktuellen Abonnement Bereich</span><span class="sxs-lookup"><span data-stu-id="9f4e3-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent
```

<span data-ttu-id="9f4e3-119">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="9f4e3-120">Beispiel 2: Abrufen von Richtlinien Ereignissen im angegebenen Abonnement Bereich</span><span class="sxs-lookup"><span data-stu-id="9f4e3-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="9f4e3-121">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb des angegebenen Abonnements generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="9f4e3-122">Beispiel 3: Abrufen von Richtlinien Ereignissen im Verwaltungsgruppen Bereich</span><span class="sxs-lookup"><span data-stu-id="9f4e3-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="9f4e3-123">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Verwaltungsgruppe generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="9f4e3-124">Beispiel 4: Abrufen von Richtlinien Ereignissen im Ressourcengruppen Bereich im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="9f4e3-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="9f4e3-125">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im Kontext des Abonnements im aktuellen Sitzungskontext) generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="9f4e3-126">Beispiel 5: Abrufen von Richtlinien Ereignissen im Ressourcengruppen Bereich des angegebenen Abonnements</span><span class="sxs-lookup"><span data-stu-id="9f4e3-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="9f4e3-127">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im angegebenen Abonnement) generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="9f4e3-128">Beispiel 6: Abrufen von Richtlinien Ereignissen für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="9f4e3-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="9f4e3-129">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für die angegebene Ressource generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="9f4e3-130">Beispiel 7: Abrufen von Richtlinien Ereignissen für eine Richtliniensatz Definition im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="9f4e3-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="9f4e3-131">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniensatz Definition (die im aktuellen Sitzungskontext im Abonnement vorhanden ist) generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="9f4e3-132">Beispiel 8: Abrufen von Richtlinien Ereignissen für eine Richtliniensatz Definition im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="9f4e3-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="9f4e3-133">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniensatz Definition (die im angegebenen Abonnement vorhanden ist) erzeugt wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="9f4e3-134">Beispiel 9: Abrufen von Richtlinien Ereignissen für eine Richtliniendefinition im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="9f4e3-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="9f4e3-135">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniendefinition (die im aktuellen Sitzungskontext im Abonnement vorhanden ist) erzeugt wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="9f4e3-136">Beispiel 10: Abrufen von Richtlinien Ereignissen für eine Richtliniendefinition im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="9f4e3-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="9f4e3-137">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniendefinition (die im angegebenen Abonnement vorhanden ist) erzeugt wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="9f4e3-138">Beispiel 11: Abrufen von Richtlinien Ereignissen für eine Richtlinien Aufgabe im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="9f4e3-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="9f4e3-139">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die im aktuellen Sitzungskontext im Abonnement vorhanden ist) erzeugt wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="9f4e3-140">Beispiel 12: Abrufen von Richtlinien Ereignissen für eine Richtlinien Aufgabe im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="9f4e3-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="9f4e3-141">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die im angegebenen Abonnement vorhanden ist) erzeugt wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="9f4e3-142">Beispiel 13: Abrufen von Richtlinien Ereignissen für eine Richtlinienzuweisung in der angegebenen Ressourcengruppe im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="9f4e3-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="9f4e3-143">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die in der Ressourcengruppe im Abonnement im aktuellen Sitzungskontext vorhanden ist) bewirkt wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="9f4e3-144">Beispiel 14: Abrufen von Richtlinien Ereignissen im aktuellen Abonnement Bereich mit OrderBy, Top und Auswählen von Abfrageoptionen</span><span class="sxs-lookup"><span data-stu-id="9f4e3-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="9f4e3-145">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="9f4e3-146">Der Befehl ordnet die Ergebnisse nach Timestamp-und Richtlinien Zuordnungsnamen-Eigenschaften an und nimmt nur die ersten fünf der in dieser Reihenfolge aufgelisteten Daten an.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="9f4e3-147">Außerdem wird ausgewählt, um nur eine Teilmenge der Spalten für jeden Datensatz aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="9f4e3-148">Beispiel 15: Abrufen von Richtlinien Ereignissen im aktuellen Abonnement Bereich mit den Abfrageoptionen "von" und "zu"</span><span class="sxs-lookup"><span data-stu-id="9f4e3-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="9f4e3-149">Ruft Richtlinien Ereignisdatensätze ab, die innerhalb des für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext angegebenen Datumsbereichs generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="9f4e3-150">Beispiel 16: Abrufen von Richtlinien Ereignissen im aktuellen Abonnement Bereich mit der Option "Filter Abfrage"</span><span class="sxs-lookup"><span data-stu-id="9f4e3-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="9f4e3-151">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="9f4e3-152">Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf der Richtlinien Definitions Aktion (einschließlich Deny-oder Überwachungsaktionen) und dem Ressourcen Standort ein (schließt eastus-Standort aus).</span><span class="sxs-lookup"><span data-stu-id="9f4e3-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="9f4e3-153">Beispiel 17: Abrufen von Richtlinien Ereignissen im aktuellen Abonnement Bereich, wobei Apply die Aggregation der Zeilenanzahl angibt</span><span class="sxs-lookup"><span data-stu-id="9f4e3-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="9f4e3-154">Ruft die Anzahl von Richtlinien Ereignisdatensätzen ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="9f4e3-155">Der Befehl gibt nur die Anzahl der Richtlinien Ereignisdatensätze zurück, die in der AdditionalProperties-Eigenschaft zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="9f4e3-156">Beispiel 18: Abrufen von Richtlinien Ereignissen im aktuellen Abonnement Bereich mit Apply, der die Gruppierung mit Aggregation angibt</span><span class="sxs-lookup"><span data-stu-id="9f4e3-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="9f4e3-157">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="9f4e3-158">Der Befehl schränkt die von Filtern zurückgegebenen Ergebnisse basierend auf der Richtlinien Definitions Aktion ein (umfasst nur Überwachungs-und ablehnungsereignisse).</span><span class="sxs-lookup"><span data-stu-id="9f4e3-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="9f4e3-159">Sie gruppiert die Ergebnisse basierend auf Richtlinienzuweisung, Richtliniendefinition, Richtlinien Definitions Aktion und Ressourcen-ID und berechnet die Anzahl der Datensätze in jeder Gruppe, die innerhalb der AdditionalProperties-Eigenschaft zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="9f4e3-160">Sie ordnet die Ergebnisse nach der Anzahl Aggregation in absteigender Reihenfolge an und nimmt nur die ersten fünf der in dieser Reihenfolge aufgelisteten Daten auf.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="9f4e3-161">Beispiel 19: Abrufen von Richtlinien Ereignissen im aktuellen Abonnement Bereich mit Apply, der die Gruppierung ohne Aggregation angibt</span><span class="sxs-lookup"><span data-stu-id="9f4e3-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="9f4e3-162">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="9f4e3-163">Der Befehl schränkt die von Filtern zurückgegebenen Ergebnisse basierend auf der Richtlinien Definitions Aktion ein (umfasst nur Überwachungs-und ablehnungsereignisse).</span><span class="sxs-lookup"><span data-stu-id="9f4e3-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="9f4e3-164">Sie gruppiert die Ergebnisse auf der Grundlage der Ressourcen-ID. Dadurch wird die Liste aller Ressourcen innerhalb des Abonnements generiert, die ein Richtlinien Ereignis für mindestens eine Überwachungs-oder Ablehnungs Richtlinie generiert haben.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="9f4e3-165">Beispiel 20: Abrufen von Richtlinien Ereignissen im aktuellen Abonnement Bereich mit Apply, der mehrere Gruppierungen angibt</span><span class="sxs-lookup"><span data-stu-id="9f4e3-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="9f4e3-166">Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="9f4e3-167">Der Befehl schränkt die von Filtern zurückgegebenen Ergebnisse auf der Grundlage der Richtlinien Definitions Aktion ein (enthält nur Deny-Ereignisse).</span><span class="sxs-lookup"><span data-stu-id="9f4e3-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="9f4e3-168">Sie gruppiert die Ergebnisse zuerst basierend auf Richtlinienzuweisung, Richtliniendefinition und Ressourcen-ID. Anschließend werden die Ergebnisse dieser Gruppierung mit den gleichen Eigenschaften, mit Ausnahme der Ressourcen-ID, gruppiert, und die Anzahl der Datensätze in jeder dieser Gruppen wird berechnet, die innerhalb der AdditionalProperties-Eigenschaft zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="9f4e3-169">Sie ordnet die Ergebnisse nach der Anzahl Aggregation in absteigender Reihenfolge an und nimmt nur die ersten fünf der in dieser Reihenfolge aufgelisteten Daten auf.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="9f4e3-170">Dadurch werden die obersten 5 Deny-Richtlinien mit der meisten Anzahl verweigerter Ressourcen generiert.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="9f4e3-171">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f4e3-171">PARAMETERS</span></span>

### <span data-ttu-id="9f4e3-172">-Apply</span><span class="sxs-lookup"><span data-stu-id="9f4e3-172">-Apply</span></span>
<span data-ttu-id="9f4e3-173">Anwenden des Ausdrucks für Aggregationen mithilfe der OData-Notation</span><span class="sxs-lookup"><span data-stu-id="9f4e3-173">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="9f4e3-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f4e3-174">-DefaultProfile</span></span>
<span data-ttu-id="9f4e3-175">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f4e3-176">-Filter</span><span class="sxs-lookup"><span data-stu-id="9f4e3-176">-Filter</span></span>
<span data-ttu-id="9f4e3-177">Filter Ausdruck mit OData-Notation</span><span class="sxs-lookup"><span data-stu-id="9f4e3-177">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="9f4e3-178">-Ab</span><span class="sxs-lookup"><span data-stu-id="9f4e3-178">-From</span></span>
<span data-ttu-id="9f4e3-179">ISO 8601 formatierter Zeitstempel, der die Startzeit des abzufragenden Intervalls angibt.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="9f4e3-180">Wenn Sie nicht angegeben wird, wird standardmäßig "bis"-Parameterwert minus 1 Tag angegeben.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="9f4e3-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="9f4e3-181">-ManagementGroupName</span></span>
<span data-ttu-id="9f4e3-182">Name der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-182">Management group name.</span></span>

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

### <span data-ttu-id="9f4e3-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="9f4e3-183">-OrderBy</span></span>
<span data-ttu-id="9f4e3-184">Sortierausdruck mit OData-Notation</span><span class="sxs-lookup"><span data-stu-id="9f4e3-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="9f4e3-185">Eine oder mehrere durch trennzeichengetrennte Spaltennamen mit einem optionalen "DESC" (Standardwert) oder "ASC".</span><span class="sxs-lookup"><span data-stu-id="9f4e3-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="9f4e3-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="9f4e3-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="9f4e3-187">Name der Richtlinienzuordnung</span><span class="sxs-lookup"><span data-stu-id="9f4e3-187">Policy assignment name.</span></span>

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

### <span data-ttu-id="9f4e3-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="9f4e3-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="9f4e3-189">Name der Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="9f4e3-189">Policy definition name.</span></span>

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

### <span data-ttu-id="9f4e3-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="9f4e3-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="9f4e3-191">Richtliniensatz-Definitionsname</span><span class="sxs-lookup"><span data-stu-id="9f4e3-191">Policy set definition name.</span></span>

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

### <span data-ttu-id="9f4e3-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f4e3-192">-ResourceGroupName</span></span>
<span data-ttu-id="9f4e3-193">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-193">Resource group name.</span></span>

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

### <span data-ttu-id="9f4e3-194">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9f4e3-194">-ResourceId</span></span>
<span data-ttu-id="9f4e3-195">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-195">Resource ID.</span></span>

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

### <span data-ttu-id="9f4e3-196">-Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="9f4e3-196">-Select</span></span>
<span data-ttu-id="9f4e3-197">Wählen Sie Ausdruck mit OData-Notation aus.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-197">Select expression using OData notation.</span></span>
<span data-ttu-id="9f4e3-198">Ein oder mehrere durch trennzeichengetrennte Spaltennamen.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="9f4e3-199">Schränkt die Spalten für jeden Datensatz auf nur die angeforderten ein.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-199">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="9f4e3-200">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9f4e3-200">-SubscriptionId</span></span>
<span data-ttu-id="9f4e3-201">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-201">Subscription ID.</span></span>

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

### <span data-ttu-id="9f4e3-202">-To</span><span class="sxs-lookup"><span data-stu-id="9f4e3-202">-To</span></span>
<span data-ttu-id="9f4e3-203">ISO 8601 formatierter Zeitstempel, der die Endzeit des abzufragenden Intervalls angibt.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="9f4e3-204">Wenn keine Angabe erfolgt, wird standardmäßig der Zeitpunkt der Anforderung angegeben.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-204">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="9f4e3-205">-Top</span><span class="sxs-lookup"><span data-stu-id="9f4e3-205">-Top</span></span>
<span data-ttu-id="9f4e3-206">Die maximale Anzahl von Datensätzen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-206">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="9f4e3-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f4e3-207">CommonParameters</span></span>
<span data-ttu-id="9f4e3-208">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f4e3-209">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f4e3-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f4e3-210">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9f4e3-210">INPUTS</span></span>

### <span data-ttu-id="9f4e3-211">System. String</span><span class="sxs-lookup"><span data-stu-id="9f4e3-211">System.String</span></span>

## <span data-ttu-id="9f4e3-212">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9f4e3-212">OUTPUTS</span></span>

### <span data-ttu-id="9f4e3-213">Microsoft. Azure. Commands. PolicyInsights. Models. PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="9f4e3-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="9f4e3-214">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f4e3-214">NOTES</span></span>

## <span data-ttu-id="9f4e3-215">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9f4e3-215">RELATED LINKS</span></span>
