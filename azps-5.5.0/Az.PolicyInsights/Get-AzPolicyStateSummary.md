---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172260"
---
# <span data-ttu-id="fff42-101">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="fff42-101">Get-AzPolicyStateSummary</span></span>

## <span data-ttu-id="fff42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fff42-102">SYNOPSIS</span></span>
<span data-ttu-id="fff42-103">Ruft die neueste Zusammenfassung der Richtlinienkonformitätszustände für Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="fff42-103">Gets latest policy compliance states summary for resources.</span></span>

## <span data-ttu-id="fff42-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fff42-104">SYNTAX</span></span>

### <span data-ttu-id="fff42-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="fff42-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fff42-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="fff42-106">ManagementGroupScope</span></span>
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fff42-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="fff42-107">ResourceGroupScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fff42-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="fff42-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fff42-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="fff42-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fff42-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="fff42-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fff42-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="fff42-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fff42-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="fff42-112">ResourceScope</span></span>
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fff42-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fff42-113">DESCRIPTION</span></span>
<span data-ttu-id="fff42-114">Ruft eine Zusammenfassungsansicht der neuesten Nummern von Richtlinienkonformitätsstatus in verschiedenen Bereichen ab, aufgeschlüsselt in Richtlinienzuweisungen und Richtliniendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="fff42-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="fff42-115">Sie umfasst nur nicht kompatible Richtlinienzustände.</span><span class="sxs-lookup"><span data-stu-id="fff42-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="fff42-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fff42-116">EXAMPLES</span></span>

### <span data-ttu-id="fff42-117">Beispiel 1: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände im aktuellen Abonnementbereich</span><span class="sxs-lookup"><span data-stu-id="fff42-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary
```

<span data-ttu-id="fff42-118">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="fff42-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="fff42-119">Beispiel 2: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände im angegebenen Abonnementbereich</span><span class="sxs-lookup"><span data-stu-id="fff42-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="fff42-120">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb des angegebenen Abonnements generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="fff42-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="fff42-121">Beispiel 3: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände im Bereich der Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="fff42-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="fff42-122">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen in der angegebenen Verwaltungsgruppe generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="fff42-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="fff42-123">Beispiel 4: Erhalten der aktuellen Zusammenfassung der nicht kompatiblen Richtlinienzustände im Bereich "Ressourcengruppe" im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="fff42-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="fff42-124">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im Abonnement im aktuellen Sitzungskontext) generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="fff42-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="fff42-125">Beispiel 5: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände im Ressourcengruppenbereich im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="fff42-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="fff42-126">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im angegebenen Abonnement) generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="fff42-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="fff42-127">Beispiel 6: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="fff42-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="fff42-128">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für die angegebene Ressource generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="fff42-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="fff42-129">Beispiel 7: Erhalten der neuesten Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtliniensatzdefinition im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="fff42-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="fff42-130">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniensatzdefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fff42-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="fff42-131">Beispiel 8: Erhalten der neuesten Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtliniensatzdefinition im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="fff42-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="fff42-132">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniensatzdefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fff42-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="fff42-133">Beispiel 9: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände für eine Richtliniendefinition im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="fff42-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="fff42-134">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fff42-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="fff42-135">Beispiel 10: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände für eine Richtliniendefinition im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="fff42-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="fff42-136">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fff42-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="fff42-137">Beispiel 11: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände für eine Richtlinienzuweisung im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="fff42-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="fff42-138">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fff42-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="fff42-139">Beispiel 12: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände für eine Richtlinienzuweisung im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="fff42-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="fff42-140">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fff42-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="fff42-141">Beispiel 13: Aktuelle Zusammenfassung der nicht kompatiblen Richtlinienzustände für eine Richtlinienzuweisung in der angegebenen Ressourcengruppe im aktuellen Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="fff42-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="fff42-142">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die in der Ressourcengruppe im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fff42-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="fff42-143">Beispiel 14: Holen Sie sich die neueste Zusammenfassung der nicht kompatiblen Richtlinienzustände im aktuellen Abonnementbereich mit der Option "Spitzenabfrage".</span><span class="sxs-lookup"><span data-stu-id="fff42-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

<span data-ttu-id="fff42-144">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="fff42-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="fff42-145">Der Befehl ordnet die Richtlinienzuweisung in den Ergebnissen nach nicht kompatibler Ressourcenanzahl in absteigender Reihenfolge und nimmt nur die Obersten 5 dieser Zusammenfassungen für Richtlinienzuweisungen an.</span><span class="sxs-lookup"><span data-stu-id="fff42-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="fff42-146">Beispiel 15: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände im aktuellen Abonnementbereich mit den Optionen "Von" und "Bis"</span><span class="sxs-lookup"><span data-stu-id="fff42-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="fff42-147">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die innerhalb des datumsbezogenen Bereichs generiert werden, der für alle Ressourcen im Abonnement im aktuellen Sitzungskontext angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="fff42-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="fff42-148">Beispiel 16: Holen Sie sich die neueste Zusammenfassung der nicht kompatiblen Richtlinienzustände im aktuellen Abonnementbereich mit der Option "Filterabfrage".</span><span class="sxs-lookup"><span data-stu-id="fff42-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="fff42-149">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="fff42-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="fff42-150">Der Befehl beschränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf einer Richtliniendefinitionsaktion (einschließlich Verweigern- oder Überwachungsaktionen) und dem Ressourcenspeicherort (schließt den Oststandort aus).</span><span class="sxs-lookup"><span data-stu-id="fff42-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="fff42-151">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fff42-151">PARAMETERS</span></span>

### <span data-ttu-id="fff42-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fff42-152">-DefaultProfile</span></span>
<span data-ttu-id="fff42-153">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fff42-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fff42-154">-Filter</span><span class="sxs-lookup"><span data-stu-id="fff42-154">-Filter</span></span>
<span data-ttu-id="fff42-155">Filtern von Ausdrücken mithilfe der OData-Notation.</span><span class="sxs-lookup"><span data-stu-id="fff42-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="fff42-156">-Von</span><span class="sxs-lookup"><span data-stu-id="fff42-156">-From</span></span>
<span data-ttu-id="fff42-157">IN ISO 8601 formatierter Zeitstempel, der die Startzeit des zu abfragenden Intervalls an gibt.</span><span class="sxs-lookup"><span data-stu-id="fff42-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="fff42-158">Ist diese Einstellung nicht angegeben, wird standardmäßig der Parameterwert "An" minus 1 Tag verwendet.</span><span class="sxs-lookup"><span data-stu-id="fff42-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="fff42-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="fff42-159">-ManagementGroupName</span></span>
<span data-ttu-id="fff42-160">Name der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="fff42-160">Management group name.</span></span>

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

### <span data-ttu-id="fff42-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="fff42-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="fff42-162">Name der Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="fff42-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="fff42-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="fff42-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="fff42-164">Name der Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="fff42-164">Policy definition name.</span></span>

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

### <span data-ttu-id="fff42-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="fff42-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="fff42-166">Name der Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="fff42-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="fff42-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fff42-167">-ResourceGroupName</span></span>
<span data-ttu-id="fff42-168">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="fff42-168">Resource group name.</span></span>

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

### <span data-ttu-id="fff42-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fff42-169">-ResourceId</span></span>
<span data-ttu-id="fff42-170">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="fff42-170">Resource ID.</span></span>

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

### <span data-ttu-id="fff42-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fff42-171">-SubscriptionId</span></span>
<span data-ttu-id="fff42-172">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="fff42-172">Subscription ID.</span></span>

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

### <span data-ttu-id="fff42-173">-To</span><span class="sxs-lookup"><span data-stu-id="fff42-173">-To</span></span>
<span data-ttu-id="fff42-174">IN ISO 8601 formatierter Zeitstempel, der die Endzeit des zu abfragenden Intervalls an gibt.</span><span class="sxs-lookup"><span data-stu-id="fff42-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="fff42-175">Ist diese Angabe nicht angegeben, wird standardmäßig der Zeitpunkt der Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="fff42-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="fff42-176">-Top</span><span class="sxs-lookup"><span data-stu-id="fff42-176">-Top</span></span>
<span data-ttu-id="fff42-177">Maximale Anzahl der zurückzukehrende Datensätze.</span><span class="sxs-lookup"><span data-stu-id="fff42-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="fff42-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fff42-178">CommonParameters</span></span>
<span data-ttu-id="fff42-179">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fff42-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fff42-180">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fff42-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fff42-181">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fff42-181">INPUTS</span></span>

### <span data-ttu-id="fff42-182">System.String</span><span class="sxs-lookup"><span data-stu-id="fff42-182">System.String</span></span>

## <span data-ttu-id="fff42-183">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fff42-183">OUTPUTS</span></span>

### <span data-ttu-id="fff42-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="fff42-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="fff42-185">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fff42-185">NOTES</span></span>

## <span data-ttu-id="fff42-186">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fff42-186">RELATED LINKS</span></span>

[<span data-ttu-id="fff42-187">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="fff42-187">Get-AzPolicyState</span></span>](./Get-AzPolicyState.md)
