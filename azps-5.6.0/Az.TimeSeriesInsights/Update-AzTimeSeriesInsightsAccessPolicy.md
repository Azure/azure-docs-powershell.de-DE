---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 3ef56e9c554b7efbd762b4b373806aad649e0449
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936560"
---
# <span data-ttu-id="78f97-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="78f97-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="78f97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78f97-102">SYNOPSIS</span></span>
<span data-ttu-id="78f97-103">Aktualisiert die Zugriffsrichtlinie mit dem angegebenen Namen in dem angegebenen Abonnement, der Ressourcengruppe und der Angegebenen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="78f97-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="78f97-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78f97-104">SYNTAX</span></span>

### <span data-ttu-id="78f97-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="78f97-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="78f97-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="78f97-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="78f97-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78f97-107">DESCRIPTION</span></span>
<span data-ttu-id="78f97-108">Aktualisiert die Zugriffsrichtlinie mit dem angegebenen Namen in dem angegebenen Abonnement, der Ressourcengruppe und der Angegebenen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="78f97-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="78f97-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="78f97-109">EXAMPLES</span></span>

### <span data-ttu-id="78f97-110">Beispiel 1: Aktualisieren einer angegebenen Zugriffsrichtlinie nach Name</span><span class="sxs-lookup"><span data-stu-id="78f97-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="78f97-111">Mit diesem Befehl wird eine angegebene Zugriffsrichtlinie aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="78f97-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="78f97-112">Beispiel 2: Aktualisieren einer angegebenen Zugriffsrichtlinie nach Objekt</span><span class="sxs-lookup"><span data-stu-id="78f97-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="78f97-113">Mit diesem Befehl wird eine angegebene Zugriffsrichtlinie aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="78f97-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="78f97-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="78f97-114">PARAMETERS</span></span>

### <span data-ttu-id="78f97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f97-115">-DefaultProfile</span></span>
<span data-ttu-id="78f97-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78f97-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f97-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78f97-117">-Description</span></span>
<span data-ttu-id="78f97-118">Eine Beschreibung der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="78f97-118">An description of the access policy.</span></span>

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

### <span data-ttu-id="78f97-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="78f97-119">-EnvironmentName</span></span>
<span data-ttu-id="78f97-120">Der Name der Zeitreiheneinblickumgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="78f97-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f97-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78f97-121">-InputObject</span></span>
<span data-ttu-id="78f97-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="78f97-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78f97-123">-Name</span><span class="sxs-lookup"><span data-stu-id="78f97-123">-Name</span></span>
<span data-ttu-id="78f97-124">Der Name der Time Series Insights-Zugriffsrichtlinie, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="78f97-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f97-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78f97-125">-ResourceGroupName</span></span>
<span data-ttu-id="78f97-126">Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="78f97-126">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f97-127">-Rolle</span><span class="sxs-lookup"><span data-stu-id="78f97-127">-Role</span></span>
<span data-ttu-id="78f97-128">Die Liste der Rollen, denen der Prinzipal in der Umgebung zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="78f97-128">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f97-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="78f97-129">-SubscriptionId</span></span>
<span data-ttu-id="78f97-130">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="78f97-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f97-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78f97-131">-Confirm</span></span>
<span data-ttu-id="78f97-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78f97-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f97-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78f97-133">-WhatIf</span></span>
<span data-ttu-id="78f97-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78f97-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78f97-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78f97-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f97-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f97-136">CommonParameters</span></span>
<span data-ttu-id="78f97-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78f97-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f97-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78f97-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f97-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="78f97-139">INPUTS</span></span>

### <span data-ttu-id="78f97-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="78f97-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="78f97-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="78f97-141">OUTPUTS</span></span>

### <span data-ttu-id="78f97-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="78f97-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="78f97-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="78f97-143">NOTES</span></span>

<span data-ttu-id="78f97-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="78f97-144">ALIASES</span></span>

<span data-ttu-id="78f97-145">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="78f97-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="78f97-146">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="78f97-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="78f97-147">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="78f97-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="78f97-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="78f97-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="78f97-149">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="78f97-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="78f97-150">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="78f97-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="78f97-151">`[EventSourceName <String>]`: Der Name der Time Series Insights-Ereignisquelle, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="78f97-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="78f97-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="78f97-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="78f97-153">`[ReferenceDataSetName <String>]`: Name des Bezugsdatensets.</span><span class="sxs-lookup"><span data-stu-id="78f97-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="78f97-154">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="78f97-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="78f97-155">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="78f97-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="78f97-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="78f97-156">RELATED LINKS</span></span>

