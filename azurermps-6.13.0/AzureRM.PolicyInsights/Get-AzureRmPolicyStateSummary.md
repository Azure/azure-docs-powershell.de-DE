---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
ms.openlocfilehash: 4b4d45414a9a27561c3be4be195a1e5f77076e6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480213"
---
# <span data-ttu-id="65fca-101">Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="65fca-101">Get-AzureRmPolicyStateSummary</span></span>

## <span data-ttu-id="65fca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65fca-102">SYNOPSIS</span></span>
<span data-ttu-id="65fca-103">Ruft die aktuelle Zusammenfassung der Richtlinien Konformitätsstatus für Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="65fca-103">Gets latest policy compliance states summary for resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65fca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65fca-104">SYNTAX</span></span>

### <span data-ttu-id="65fca-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="65fca-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65fca-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="65fca-106">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65fca-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="65fca-107">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65fca-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="65fca-108">PolicySetDefinitionScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65fca-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="65fca-109">PolicyDefinitionScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65fca-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="65fca-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65fca-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="65fca-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String>
 -PolicyAssignmentName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65fca-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="65fca-112">ResourceScope</span></span>
```
Get-AzureRmPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65fca-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65fca-113">DESCRIPTION</span></span>
<span data-ttu-id="65fca-114">Ruft eine Zusammenfassungsansicht der neuesten Richtlinien Kompatibilitätszustands Nummern in verschiedenen Bereichen ab, aufgeschlüsselt nach Richtlinienzuweisungen und Richtlinien Definitionen.</span><span class="sxs-lookup"><span data-stu-id="65fca-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="65fca-115">Es enthält nur nicht richtlinienkonforme Richtlinienzustände.</span><span class="sxs-lookup"><span data-stu-id="65fca-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="65fca-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65fca-116">EXAMPLES</span></span>

### <span data-ttu-id="65fca-117">Beispiel 1: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung im aktuellen Abonnement Bereich</span><span class="sxs-lookup"><span data-stu-id="65fca-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary
```

<span data-ttu-id="65fca-118">Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="65fca-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="65fca-119">Beispiel 2: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung im angegebenen Abonnement Bereich</span><span class="sxs-lookup"><span data-stu-id="65fca-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="65fca-120">Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen innerhalb des angegebenen Abonnements generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="65fca-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="65fca-121">Beispiel 3: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung im Verwaltungsgruppen Bereich</span><span class="sxs-lookup"><span data-stu-id="65fca-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="65fca-122">Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Verwaltungsgruppe generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="65fca-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="65fca-123">Beispiel 4: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung im Ressourcengruppen Bereich im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="65fca-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="65fca-124">Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im Kontext des Abonnements im aktuellen Sitzungskontext) generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="65fca-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="65fca-125">Beispiel 5: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung im Ressourcengruppen Bereich im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="65fca-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="65fca-126">Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im angegebenen Abonnement) generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="65fca-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="65fca-127">Beispiel 6: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="65fca-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="65fca-128">Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für die angegebene Ressource generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="65fca-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="65fca-129">Beispiel 7: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung für eine Richtliniensatz Definition im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="65fca-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="65fca-130">Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniensatz Definition (die in dem Abonnement im aktuellen Sitzungskontext vorhanden ist) bewirkt wurden.</span><span class="sxs-lookup"><span data-stu-id="65fca-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="65fca-131">Beispiel 8: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung für eine Richtliniensatz Definition im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="65fca-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="65fca-132">Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniensatz Definition (die im angegebenen Abonnement vorhanden ist) erzeugt wurden.</span><span class="sxs-lookup"><span data-stu-id="65fca-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="65fca-133">Beispiel 9: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung für eine Richtliniendefinition im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="65fca-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="65fca-134">Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniendefinition (die in dem Abonnement im aktuellen Sitzungskontext vorhanden ist) bewirkt wurden.</span><span class="sxs-lookup"><span data-stu-id="65fca-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="65fca-135">Beispiel 10: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung für eine Richtliniendefinition im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="65fca-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="65fca-136">Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im angegebenen Abonnement vorhanden ist) bewirkt wurden.</span><span class="sxs-lookup"><span data-stu-id="65fca-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="65fca-137">Beispiel 11: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung für eine Richtlinien Aufgabe im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="65fca-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="65fca-138">Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die in den letzten Tagen für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuweisung (die in dem Abonnement im aktuellen Sitzungskontext vorhanden ist) bewirkt wurden.</span><span class="sxs-lookup"><span data-stu-id="65fca-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="65fca-139">Beispiel 12: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung für eine Richtlinien Aufgabe im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="65fca-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="65fca-140">Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die in den letzten Tagen für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuweisung (die im angegebenen Abonnement vorhanden ist) bewirkt wurden.</span><span class="sxs-lookup"><span data-stu-id="65fca-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="65fca-141">Beispiel 13: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung für eine Richtlinien Aufgabe in der angegebenen Ressourcengruppe im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="65fca-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="65fca-142">Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die in den letzten Tagen für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuweisung (die in der Ressourcengruppe im Abonnement im aktuellen Sitzungskontext vorhanden ist) erfolgen.</span><span class="sxs-lookup"><span data-stu-id="65fca-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="65fca-143">Beispiel 14: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung im aktuellen Abonnement Bereich mit der Option "obere Abfrage"</span><span class="sxs-lookup"><span data-stu-id="65fca-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Top 5
```

<span data-ttu-id="65fca-144">Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="65fca-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="65fca-145">Der Befehl ordnet die Richtlinien Zuordnungs Zusammenfassungen in den Ergebnissen nach nicht kompatiblen Ressourcen Zählern in absteigender Reihenfolge an und nimmt nur die ersten fünf dieser Richtlinien Zuordnungs Zusammenfassungen auf.</span><span class="sxs-lookup"><span data-stu-id="65fca-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="65fca-146">Beispiel 15: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung im aktuellen Abonnement Bereich mit den Optionen von und zu Abfrage</span><span class="sxs-lookup"><span data-stu-id="65fca-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="65fca-147">Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die innerhalb des für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext angegebenen Datumsbereichs generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="65fca-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="65fca-148">Beispiel 16: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung im aktuellen Abonnement Bereich mit der Option "Filter Abfrage"</span><span class="sxs-lookup"><span data-stu-id="65fca-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="65fca-149">Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="65fca-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="65fca-150">Der Befehl schränkt die von Filtern zurückgegebenen Ergebnisse auf der Grundlage der Richtlinien Definitions Aktion (einschließlich Deny-oder Überwachungsaktionen) und des Ressourcen Speicherorts ein (schließt eastus-Standort aus).</span><span class="sxs-lookup"><span data-stu-id="65fca-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="65fca-151">Parameter</span><span class="sxs-lookup"><span data-stu-id="65fca-151">PARAMETERS</span></span>

### <span data-ttu-id="65fca-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65fca-152">-DefaultProfile</span></span>
<span data-ttu-id="65fca-153">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65fca-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65fca-154">-Filter</span><span class="sxs-lookup"><span data-stu-id="65fca-154">-Filter</span></span>
<span data-ttu-id="65fca-155">Filter Ausdruck mit OData-Notation</span><span class="sxs-lookup"><span data-stu-id="65fca-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="65fca-156">-Ab</span><span class="sxs-lookup"><span data-stu-id="65fca-156">-From</span></span>
<span data-ttu-id="65fca-157">ISO 8601 formatierter Zeitstempel, der die Startzeit des abzufragenden Intervalls angibt.</span><span class="sxs-lookup"><span data-stu-id="65fca-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="65fca-158">Wenn Sie nicht angegeben wird, wird standardmäßig "bis"-Parameterwert minus 1 Tag angegeben.</span><span class="sxs-lookup"><span data-stu-id="65fca-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="65fca-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="65fca-159">-ManagementGroupName</span></span>
<span data-ttu-id="65fca-160">Name der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="65fca-160">Management group name.</span></span>

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

### <span data-ttu-id="65fca-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="65fca-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="65fca-162">Name der Richtlinienzuordnung</span><span class="sxs-lookup"><span data-stu-id="65fca-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="65fca-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="65fca-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="65fca-164">Name der Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="65fca-164">Policy definition name.</span></span>

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

### <span data-ttu-id="65fca-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="65fca-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="65fca-166">Richtliniensatz-Definitionsname</span><span class="sxs-lookup"><span data-stu-id="65fca-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="65fca-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65fca-167">-ResourceGroupName</span></span>
<span data-ttu-id="65fca-168">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="65fca-168">Resource group name.</span></span>

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

### <span data-ttu-id="65fca-169">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="65fca-169">-ResourceId</span></span>
<span data-ttu-id="65fca-170">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="65fca-170">Resource ID.</span></span>

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

### <span data-ttu-id="65fca-171">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="65fca-171">-SubscriptionId</span></span>
<span data-ttu-id="65fca-172">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="65fca-172">Subscription ID.</span></span>

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

### <span data-ttu-id="65fca-173">-To</span><span class="sxs-lookup"><span data-stu-id="65fca-173">-To</span></span>
<span data-ttu-id="65fca-174">ISO 8601 formatierter Zeitstempel, der die Endzeit des abzufragenden Intervalls angibt.</span><span class="sxs-lookup"><span data-stu-id="65fca-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="65fca-175">Wenn keine Angabe erfolgt, wird standardmäßig der Zeitpunkt der Anforderung angegeben.</span><span class="sxs-lookup"><span data-stu-id="65fca-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="65fca-176">-Top</span><span class="sxs-lookup"><span data-stu-id="65fca-176">-Top</span></span>
<span data-ttu-id="65fca-177">Die maximale Anzahl von Datensätzen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="65fca-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="65fca-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65fca-178">CommonParameters</span></span>
<span data-ttu-id="65fca-179">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65fca-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65fca-180">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65fca-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65fca-181">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65fca-181">INPUTS</span></span>

### <span data-ttu-id="65fca-182">System. String</span><span class="sxs-lookup"><span data-stu-id="65fca-182">System.String</span></span>

## <span data-ttu-id="65fca-183">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65fca-183">OUTPUTS</span></span>

### <span data-ttu-id="65fca-184">Microsoft. Azure. Commands. PolicyInsights. Models. PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="65fca-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="65fca-185">Notizen</span><span class="sxs-lookup"><span data-stu-id="65fca-185">NOTES</span></span>

## <span data-ttu-id="65fca-186">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65fca-186">RELATED LINKS</span></span>

[<span data-ttu-id="65fca-187">Get-AzureRmPolicyState</span><span class="sxs-lookup"><span data-stu-id="65fca-187">Get-AzureRmPolicyState</span></span>](./Get-AzureRmPolicyState.md)
