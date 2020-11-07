---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyState.md
ms.openlocfilehash: 6f5f1c341db0c5f57ffb541b9455369c0c6e5ab0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662509"
---
# <span data-ttu-id="161a2-101">Get-AzureRmPolicyState</span><span class="sxs-lookup"><span data-stu-id="161a2-101">Get-AzureRmPolicyState</span></span>

## <span data-ttu-id="161a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="161a2-102">SYNOPSIS</span></span>
<span data-ttu-id="161a2-103">Ruft Richtlinien Kompatibilitätsstatus für Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="161a2-103">Gets policy compliance states for resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="161a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="161a2-104">SYNTAX</span></span>

### <span data-ttu-id="161a2-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="161a2-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="161a2-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="161a2-106">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="161a2-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="161a2-107">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="161a2-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="161a2-108">ResourceScope</span></span>
```
Get-AzureRmPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="161a2-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="161a2-109">PolicySetDefinitionScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="161a2-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="161a2-110">PolicyDefinitionScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="161a2-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="161a2-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="161a2-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="161a2-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String>
 -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="161a2-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="161a2-113">DESCRIPTION</span></span>
<span data-ttu-id="161a2-114">Ruft Richtlinien Kompatibilitätsstatus für Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="161a2-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="161a2-115">Richtlinien Zustandsdaten Sätze können in verschiedenen Bereichen abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="161a2-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="161a2-116">Basierend auf dem angegebenen Zeitintervall (standardmäßig auf den letzten Tag) können entweder die neuesten Richtlinienzustände oder alle Richtlinien Zustandsübergänge abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="161a2-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="161a2-117">Ergebnisse können gefiltert, gruppiert und Gruppen Aggregationen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="161a2-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="161a2-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="161a2-118">EXAMPLES</span></span>

### <span data-ttu-id="161a2-119">Beispiel 1: Abrufen der neuesten Richtlinienzustände im aktuellen Abonnement Bereich</span><span class="sxs-lookup"><span data-stu-id="161a2-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState
```

<span data-ttu-id="161a2-120">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="161a2-121">Beispiel 2: Abrufen der neuesten Richtlinienstatus im angegebenen Abonnement Bereich</span><span class="sxs-lookup"><span data-stu-id="161a2-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="161a2-122">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb des angegebenen Abonnements generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="161a2-123">Beispiel 3: Abrufen aller Richtlinienzustände im aktuellen Abonnement Bereich</span><span class="sxs-lookup"><span data-stu-id="161a2-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -All
```

<span data-ttu-id="161a2-124">Ruft alle Verlaufs Richtlinien Zustandsdaten Sätze (einschließlich der neuesten) ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="161a2-125">Beispiel 4: Abrufen der neuesten Richtlinienstatus im Verwaltungsgruppen Bereich</span><span class="sxs-lookup"><span data-stu-id="161a2-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="161a2-126">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Verwaltungsgruppe generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="161a2-127">Beispiel 5: Abrufen der neuesten Richtlinienstatus im Ressourcengruppen Bereich im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="161a2-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="161a2-128">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im Kontext des Abonnements im aktuellen Sitzungskontext) generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="161a2-129">Beispiel 6: Abrufen der neuesten Richtlinienstatus im Ressourcengruppen Bereich im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="161a2-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="161a2-130">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im angegebenen Abonnement) generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="161a2-131">Beispiel 7: Abrufen der neuesten Richtlinienstatus für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="161a2-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="161a2-132">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für die angegebene Ressource generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="161a2-133">Beispiel 8: Abrufen der neuesten Richtlinienstatus für eine Richtliniensatz Definition im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="161a2-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="161a2-134">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniensatz Definition (die im aktuellen Sitzungskontext im Abonnement vorhanden ist) erzeugt wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="161a2-135">Beispiel 9: Abrufen der neuesten Richtlinienstatus für eine Richtliniensatz Definition im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="161a2-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="161a2-136">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniensatz Definition (die im angegebenen Abonnement vorhanden ist) erzeugt wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="161a2-137">Beispiel 10: Abrufen der neuesten Richtlinienstatus für eine Richtliniendefinition im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="161a2-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="161a2-138">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniendefinition (die in dem Abonnement im aktuellen Sitzungskontext vorhanden ist) bewirkt wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="161a2-139">Beispiel 11: Abrufen der neuesten Richtlinienstatus für eine Richtliniendefinition im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="161a2-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="161a2-140">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniendefinition (die im angegebenen Abonnement vorhanden ist) bewirkt wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="161a2-141">Beispiel 12: Abrufen der neuesten Richtlinienstatus für eine Richtlinien Aufgabe im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="161a2-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="161a2-142">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die in dem Abonnement im aktuellen Sitzungskontext vorhanden ist) bewirkt wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="161a2-143">Beispiel 13: Abrufen der neuesten Richtlinienstatus für eine Richtlinien Aufgabe im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="161a2-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="161a2-144">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die im angegebenen Abonnement vorhanden ist) erzeugt wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="161a2-145">Beispiel 14: Abrufen der neuesten Richtlinienstatus für eine Richtlinienzuweisung in der angegebenen Ressourcengruppe im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="161a2-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="161a2-146">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die in der Ressourcengruppe im Abonnement im aktuellen Sitzungskontext vorhanden ist) bewirkt wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="161a2-147">Beispiel 15: Abrufen der neuesten Richtlinienzustände im aktuellen Abonnement Bereich mit OrderBy, Top und Auswählen von Abfrageoptionen</span><span class="sxs-lookup"><span data-stu-id="161a2-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="161a2-148">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="161a2-149">Der Befehl ordnet die Ergebnisse nach Timestamp-und Richtlinien Zuordnungsnamen-Eigenschaften an und nimmt nur die ersten fünf der in dieser Reihenfolge aufgelisteten Daten an.</span><span class="sxs-lookup"><span data-stu-id="161a2-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="161a2-150">Außerdem wird ausgewählt, um nur eine Teilmenge der Spalten für jeden Datensatz aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="161a2-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="161a2-151">Beispiel 16: Abrufen der neuesten Richtlinienzustände im aktuellen Abonnement Bereich mit den Optionen von und zu Abfrage</span><span class="sxs-lookup"><span data-stu-id="161a2-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="161a2-152">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die innerhalb des für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext angegebenen Datumsbereichs generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="161a2-153">Beispiel 17: Abrufen der neuesten Richtlinienzustände im aktuellen Abonnement Bereich mit der Option "Filter Abfrage"</span><span class="sxs-lookup"><span data-stu-id="161a2-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and IsCompliant eq false and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="161a2-154">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="161a2-155">Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf der Richtlinien Definitions Aktion (einschließlich Deny-oder Überwachungsaktionen), dem Kompatibilitätsstatus (nur nicht kompatiblen Status) und dem Ressourcen Standort ein (schließt eastus-Standort aus).</span><span class="sxs-lookup"><span data-stu-id="161a2-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="161a2-156">Beispiel 18: Abrufen der neuesten Richtlinienzustände im aktuellen Abonnement Bereich, wobei Apply die Aggregation der Zeilenanzahl angibt</span><span class="sxs-lookup"><span data-stu-id="161a2-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="161a2-157">Ruft die Anzahl der neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="161a2-158">Der Befehl gibt nur die Anzahl der Richtlinien Zustandsdaten Sätze zurück, die in der AdditionalProperties-Eigenschaft zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="161a2-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="161a2-159">Beispiel 19: Abrufen der neuesten Richtlinienzustände im aktuellen Abonnement Bereich mit Apply, der die Gruppierung mit Aggregation angibt</span><span class="sxs-lookup"><span data-stu-id="161a2-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="161a2-160">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="161a2-161">Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf dem Kompatibilitätsstatus ein (enthält nur nicht kompatiblen Status).</span><span class="sxs-lookup"><span data-stu-id="161a2-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="161a2-162">Sie gruppiert die Ergebnisse basierend auf Richtlinienzuweisung, Richtliniensatz Definition und Richtliniendefinition und berechnet die Anzahl der Datensätze in jeder Gruppe, die innerhalb der AdditionalProperties-Eigenschaft zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="161a2-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="161a2-163">Sie ordnet die Ergebnisse nach der Anzahl Aggregation in absteigender Reihenfolge an und nimmt nur die ersten fünf der in dieser Reihenfolge aufgelisteten Daten auf.</span><span class="sxs-lookup"><span data-stu-id="161a2-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="161a2-164">Beispiel 20: Abrufen der neuesten Richtlinienzustände im aktuellen Abonnement Bereich mit Apply, der die Gruppierung ohne Aggregation angibt</span><span class="sxs-lookup"><span data-stu-id="161a2-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="161a2-165">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="161a2-166">Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf dem Kompatibilitätsstatus ein (enthält nur nicht kompatiblen Status).</span><span class="sxs-lookup"><span data-stu-id="161a2-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="161a2-167">Sie gruppiert die Ergebnisse auf der Grundlage der Ressourcen-ID. Dadurch wird die Liste aller Ressourcen innerhalb des Abonnements generiert, die für mindestens eine Richtlinie nicht kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="161a2-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="161a2-168">Beispiel 21: Abrufen der neuesten Richtlinienzustände im aktuellen Abonnement Bereich mit Apply, der mehrere Gruppierungen angibt</span><span class="sxs-lookup"><span data-stu-id="161a2-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

<span data-ttu-id="161a2-169">Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="161a2-169">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="161a2-170">Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf dem Kompatibilitätsstatus ein (enthält nur nicht kompatiblen Status).</span><span class="sxs-lookup"><span data-stu-id="161a2-170">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="161a2-171">Sie gruppiert die Ergebnisse zuerst basierend auf Richtlinienzuweisung, Richtliniensatz Definition, Richtliniendefinition und Ressourcen-ID. Anschließend werden die Ergebnisse dieser Gruppierung mit den gleichen Eigenschaften, mit Ausnahme der Ressourcen-ID, gruppiert, und die Anzahl der Datensätze in jeder dieser Gruppen wird berechnet, die innerhalb der AdditionalProperties-Eigenschaft zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="161a2-171">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="161a2-172">Sie ordnet die Ergebnisse nach der Anzahl Aggregation in absteigender Reihenfolge an und nimmt nur die ersten fünf der in dieser Reihenfolge aufgelisteten Daten auf.</span><span class="sxs-lookup"><span data-stu-id="161a2-172">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="161a2-173">Dadurch werden die obersten fünf Richtlinien mit der größten Anzahl nicht kompatibler Ressourcen generiert.</span><span class="sxs-lookup"><span data-stu-id="161a2-173">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="161a2-174">Parameter</span><span class="sxs-lookup"><span data-stu-id="161a2-174">PARAMETERS</span></span>

### <span data-ttu-id="161a2-175">– Alle</span><span class="sxs-lookup"><span data-stu-id="161a2-175">-All</span></span>
<span data-ttu-id="161a2-176">Rufen Sie innerhalb des angegebenen Zeitintervalls alle Richtlinienzustände anstelle der neuesten ab.</span><span class="sxs-lookup"><span data-stu-id="161a2-176">Within the specified time interval, get all policy states instead of the latest only.</span></span>

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

### <span data-ttu-id="161a2-177">-Apply</span><span class="sxs-lookup"><span data-stu-id="161a2-177">-Apply</span></span>
<span data-ttu-id="161a2-178">Anwenden des Ausdrucks für Aggregationen mithilfe der OData-Notation</span><span class="sxs-lookup"><span data-stu-id="161a2-178">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="161a2-179">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="161a2-179">-DefaultProfile</span></span>
<span data-ttu-id="161a2-180">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="161a2-180">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="161a2-181">-Filter</span><span class="sxs-lookup"><span data-stu-id="161a2-181">-Filter</span></span>
<span data-ttu-id="161a2-182">Filter Ausdruck mit OData-Notation</span><span class="sxs-lookup"><span data-stu-id="161a2-182">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="161a2-183">-Ab</span><span class="sxs-lookup"><span data-stu-id="161a2-183">-From</span></span>
<span data-ttu-id="161a2-184">ISO 8601 formatierter Zeitstempel, der die Startzeit des abzufragenden Intervalls angibt.</span><span class="sxs-lookup"><span data-stu-id="161a2-184">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="161a2-185">Wenn Sie nicht angegeben wird, wird standardmäßig "bis"-Parameterwert minus 1 Tag angegeben.</span><span class="sxs-lookup"><span data-stu-id="161a2-185">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="161a2-186">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="161a2-186">-ManagementGroupName</span></span>
<span data-ttu-id="161a2-187">Name der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="161a2-187">Management group name.</span></span>

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

### <span data-ttu-id="161a2-188">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="161a2-188">-OrderBy</span></span>
<span data-ttu-id="161a2-189">Sortierausdruck mit OData-Notation</span><span class="sxs-lookup"><span data-stu-id="161a2-189">Ordering expression using OData notation.</span></span>
<span data-ttu-id="161a2-190">Eine oder mehrere durch trennzeichengetrennte Spaltennamen mit einem optionalen "DESC" (Standardwert) oder "ASC".</span><span class="sxs-lookup"><span data-stu-id="161a2-190">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="161a2-191">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="161a2-191">-PolicyAssignmentName</span></span>
<span data-ttu-id="161a2-192">Name der Richtlinienzuordnung</span><span class="sxs-lookup"><span data-stu-id="161a2-192">Policy assignment name.</span></span>

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

### <span data-ttu-id="161a2-193">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="161a2-193">-PolicyDefinitionName</span></span>
<span data-ttu-id="161a2-194">Name der Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="161a2-194">Policy definition name.</span></span>

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

### <span data-ttu-id="161a2-195">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="161a2-195">-PolicySetDefinitionName</span></span>
<span data-ttu-id="161a2-196">Richtliniensatz-Definitionsname</span><span class="sxs-lookup"><span data-stu-id="161a2-196">Policy set definition name.</span></span>

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

### <span data-ttu-id="161a2-197">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="161a2-197">-ResourceGroupName</span></span>
<span data-ttu-id="161a2-198">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="161a2-198">Resource group name.</span></span>

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

### <span data-ttu-id="161a2-199">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="161a2-199">-ResourceId</span></span>
<span data-ttu-id="161a2-200">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="161a2-200">Resource ID.</span></span>

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

### <span data-ttu-id="161a2-201">-Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="161a2-201">-Select</span></span>
<span data-ttu-id="161a2-202">Wählen Sie Ausdruck mit OData-Notation aus.</span><span class="sxs-lookup"><span data-stu-id="161a2-202">Select expression using OData notation.</span></span>
<span data-ttu-id="161a2-203">Ein oder mehrere durch trennzeichengetrennte Spaltennamen.</span><span class="sxs-lookup"><span data-stu-id="161a2-203">One or more comma-separated column names.</span></span>
<span data-ttu-id="161a2-204">Schränkt die Spalten für jeden Datensatz auf nur die angeforderten ein.</span><span class="sxs-lookup"><span data-stu-id="161a2-204">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="161a2-205">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="161a2-205">-SubscriptionId</span></span>
<span data-ttu-id="161a2-206">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="161a2-206">Subscription ID.</span></span>

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

### <span data-ttu-id="161a2-207">-To</span><span class="sxs-lookup"><span data-stu-id="161a2-207">-To</span></span>
<span data-ttu-id="161a2-208">ISO 8601 formatierter Zeitstempel, der die Endzeit des abzufragenden Intervalls angibt.</span><span class="sxs-lookup"><span data-stu-id="161a2-208">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="161a2-209">Wenn keine Angabe erfolgt, wird standardmäßig der Zeitpunkt der Anforderung angegeben.</span><span class="sxs-lookup"><span data-stu-id="161a2-209">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="161a2-210">-Top</span><span class="sxs-lookup"><span data-stu-id="161a2-210">-Top</span></span>
<span data-ttu-id="161a2-211">Die maximale Anzahl von Datensätzen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="161a2-211">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="161a2-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="161a2-212">CommonParameters</span></span>
<span data-ttu-id="161a2-213">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="161a2-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="161a2-214">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="161a2-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="161a2-215">Eingaben</span><span class="sxs-lookup"><span data-stu-id="161a2-215">INPUTS</span></span>

### <span data-ttu-id="161a2-216">System. String</span><span class="sxs-lookup"><span data-stu-id="161a2-216">System.String</span></span>

## <span data-ttu-id="161a2-217">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="161a2-217">OUTPUTS</span></span>

### <span data-ttu-id="161a2-218">Microsoft. Azure. Commands. PolicyInsights. Models. PolicyState</span><span class="sxs-lookup"><span data-stu-id="161a2-218">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="161a2-219">Notizen</span><span class="sxs-lookup"><span data-stu-id="161a2-219">NOTES</span></span>

## <span data-ttu-id="161a2-220">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="161a2-220">RELATED LINKS</span></span>

[<span data-ttu-id="161a2-221">Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="161a2-221">Get-AzureRmPolicyStateSummary</span></span>](./Get-AzureRmPolicyStateSummary.md)
