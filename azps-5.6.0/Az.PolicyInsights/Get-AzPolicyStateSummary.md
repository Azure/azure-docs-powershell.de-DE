---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: 09fce075ae0f6d8c55f5ef18d070a72daafa2cac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937496"
---
# <span data-ttu-id="6c405-101">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="6c405-101">Get-AzPolicyStateSummary</span></span>

## <span data-ttu-id="6c405-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c405-102">SYNOPSIS</span></span>
<span data-ttu-id="6c405-103">Ruft die neueste Zusammenfassung der Richtlinienkonformitätszustände für Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="6c405-103">Gets latest policy compliance states summary for resources.</span></span>

## <span data-ttu-id="6c405-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c405-104">SYNTAX</span></span>

### <span data-ttu-id="6c405-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="6c405-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c405-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="6c405-106">ManagementGroupScope</span></span>
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c405-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="6c405-107">ResourceGroupScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c405-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="6c405-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c405-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="6c405-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c405-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="6c405-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c405-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="6c405-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c405-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="6c405-112">ResourceScope</span></span>
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c405-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c405-113">DESCRIPTION</span></span>
<span data-ttu-id="6c405-114">Ruft eine Zusammenfassungsansicht der neuesten Richtlinienkonformitätsstatusnummern in verschiedenen Bereichen ab, die in Richtlinienzuordnungen und Richtliniendefinitionen aufgeschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="6c405-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="6c405-115">Sie umfasst nur nicht kompatible Richtlinienzustände.</span><span class="sxs-lookup"><span data-stu-id="6c405-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="6c405-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6c405-116">EXAMPLES</span></span>

### <span data-ttu-id="6c405-117">Beispiel 1: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände im aktuellen Abonnementbereich</span><span class="sxs-lookup"><span data-stu-id="6c405-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary
```

<span data-ttu-id="6c405-118">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6c405-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="6c405-119">Beispiel 2: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände im angegebenen Abonnementbereich</span><span class="sxs-lookup"><span data-stu-id="6c405-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="6c405-120">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb des angegebenen Abonnements generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6c405-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="6c405-121">Beispiel 3: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände im Bereich der Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="6c405-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="6c405-122">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Verwaltungsgruppe generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6c405-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="6c405-123">Beispiel 4: Zusammenfassung der aktuellen nicht kompatiblen Richtlinienzustände im Ressourcengruppenbereich im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="6c405-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="6c405-124">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im Abonnement im aktuellen Sitzungskontext) generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6c405-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="6c405-125">Beispiel 5: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände im Ressourcengruppenbereich im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="6c405-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="6c405-126">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im angegebenen Abonnement) generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6c405-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="6c405-127">Beispiel 6: Zusammenfassung der neuesten nicht kompatiblen Richtlinienzustände für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="6c405-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="6c405-128">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für die angegebene Ressource generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6c405-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="6c405-129">Beispiel 7: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtliniensatzdefinition im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="6c405-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="6c405-130">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniensatzdefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6c405-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="6c405-131">Beispiel 8: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtliniensatzdefinition im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="6c405-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="6c405-132">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniensatzdefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6c405-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="6c405-133">Beispiel 9: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtliniendefinition im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="6c405-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="6c405-134">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6c405-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="6c405-135">Beispiel 10: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtliniendefinition im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="6c405-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="6c405-136">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6c405-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="6c405-137">Beispiel 11: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtlinienzuordnung im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="6c405-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="6c405-138">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuordnung (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6c405-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="6c405-139">Beispiel 12: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtlinienzuordnung im angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="6c405-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="6c405-140">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuordnung (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6c405-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="6c405-141">Beispiel 13: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtlinienzuordnung in der angegebenen Ressourcengruppe im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="6c405-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="6c405-142">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuordnung (die in der Ressourcengruppe im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6c405-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="6c405-143">Beispiel 14: Holen Sie sich die neueste Zusammenfassung nicht kompatibler Richtlinienzustände im aktuellen Abonnementbereich mit der Option "Top query"</span><span class="sxs-lookup"><span data-stu-id="6c405-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

<span data-ttu-id="6c405-144">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6c405-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="6c405-145">Der Befehl ordnet die Richtlinienzuordnungszusammenfassungen in den Ergebnissen nach nicht kompatiblen Ressourcenanzahlen in absteigender Reihenfolge an und nimmt nur die obersten 5 dieser Richtlinienzuordnungszusammenfassungen an.</span><span class="sxs-lookup"><span data-stu-id="6c405-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="6c405-146">Beispiel 15: Holen Sie sich die neueste Zusammenfassung nicht kompatibler Richtlinienzustände im aktuellen Abonnementbereich mit den Abfrageoptionen Von und An.</span><span class="sxs-lookup"><span data-stu-id="6c405-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="6c405-147">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die innerhalb des Datumsbereichs generiert werden, der für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6c405-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="6c405-148">Beispiel 16: Anzeigen der neuesten, nicht kompatiblen Richtlinienzustände im aktuellen Abonnementbereich mit Filterabfrageoption</span><span class="sxs-lookup"><span data-stu-id="6c405-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="6c405-149">Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6c405-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="6c405-150">Der Befehl schränkt die Ergebnisse ein, die durch Filtern basierend auf richtliniendefinitionsbezogenen Aktionen (einschließlich Deny- oder Überwachungsaktionen) und Ressourcenspeicherort (ohne Ostspeicherort) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6c405-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="6c405-151">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6c405-151">PARAMETERS</span></span>

### <span data-ttu-id="6c405-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c405-152">-DefaultProfile</span></span>
<span data-ttu-id="6c405-153">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c405-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c405-154">-Filter</span><span class="sxs-lookup"><span data-stu-id="6c405-154">-Filter</span></span>
<span data-ttu-id="6c405-155">Filtern sie Ausdruck mithilfe der OData-Notation.</span><span class="sxs-lookup"><span data-stu-id="6c405-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="6c405-156">-Von</span><span class="sxs-lookup"><span data-stu-id="6c405-156">-From</span></span>
<span data-ttu-id="6c405-157">Nach ISO 8601 formatierter Zeitstempel, der die Startzeit des Abfrageintervalls an gibt.</span><span class="sxs-lookup"><span data-stu-id="6c405-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="6c405-158">Wenn nicht angegeben, wird standardmäßig der Parameterwert "An" minus 1 Tag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6c405-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="6c405-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="6c405-159">-ManagementGroupName</span></span>
<span data-ttu-id="6c405-160">Name der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="6c405-160">Management group name.</span></span>

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

### <span data-ttu-id="6c405-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="6c405-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="6c405-162">Name der Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="6c405-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="6c405-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6c405-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="6c405-164">Richtliniendefinitionsname.</span><span class="sxs-lookup"><span data-stu-id="6c405-164">Policy definition name.</span></span>

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

### <span data-ttu-id="6c405-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6c405-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="6c405-166">Name der Richtliniensatzdefinition.</span><span class="sxs-lookup"><span data-stu-id="6c405-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="6c405-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c405-167">-ResourceGroupName</span></span>
<span data-ttu-id="6c405-168">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6c405-168">Resource group name.</span></span>

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

### <span data-ttu-id="6c405-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c405-169">-ResourceId</span></span>
<span data-ttu-id="6c405-170">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6c405-170">Resource ID.</span></span>

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

### <span data-ttu-id="6c405-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6c405-171">-SubscriptionId</span></span>
<span data-ttu-id="6c405-172">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="6c405-172">Subscription ID.</span></span>

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

### <span data-ttu-id="6c405-173">-To</span><span class="sxs-lookup"><span data-stu-id="6c405-173">-To</span></span>
<span data-ttu-id="6c405-174">Nach ISO 8601 formatierter Zeitstempel, der die Endzeit des Abfrageintervalls an gibt.</span><span class="sxs-lookup"><span data-stu-id="6c405-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="6c405-175">Wenn nicht angegeben, wird standardmäßig die Uhrzeit der Anforderung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6c405-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="6c405-176">-Top</span><span class="sxs-lookup"><span data-stu-id="6c405-176">-Top</span></span>
<span data-ttu-id="6c405-177">Maximale Anzahl von Datensätzen, die zurückzukehren sind.</span><span class="sxs-lookup"><span data-stu-id="6c405-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="6c405-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c405-178">CommonParameters</span></span>
<span data-ttu-id="6c405-179">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c405-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c405-180">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c405-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c405-181">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6c405-181">INPUTS</span></span>

### <span data-ttu-id="6c405-182">System.String</span><span class="sxs-lookup"><span data-stu-id="6c405-182">System.String</span></span>

## <span data-ttu-id="6c405-183">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6c405-183">OUTPUTS</span></span>

### <span data-ttu-id="6c405-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="6c405-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="6c405-185">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6c405-185">NOTES</span></span>

## <span data-ttu-id="6c405-186">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6c405-186">RELATED LINKS</span></span>

[<span data-ttu-id="6c405-187">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="6c405-187">Get-AzPolicyState</span></span>](./Get-AzPolicyState.md)
