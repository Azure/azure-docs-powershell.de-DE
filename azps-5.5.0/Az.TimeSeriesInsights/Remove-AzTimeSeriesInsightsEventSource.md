---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7f647da2543a4675dad53f88e2494aa7f6c39419
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149828"
---
# <span data-ttu-id="2a37a-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="2a37a-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="2a37a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a37a-102">SYNOPSIS</span></span>
<span data-ttu-id="2a37a-103">Löscht die Ereignisquelle mit dem angegebenen Namen in dem angegebenen Abonnement, der Ressourcengruppe und der angegebenen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="2a37a-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="2a37a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a37a-104">SYNTAX</span></span>

### <span data-ttu-id="2a37a-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="2a37a-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2a37a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2a37a-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2a37a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a37a-107">DESCRIPTION</span></span>
<span data-ttu-id="2a37a-108">Löscht die Ereignisquelle mit dem angegebenen Namen in dem angegebenen Abonnement, der Ressourcengruppe und der angegebenen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="2a37a-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="2a37a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2a37a-109">EXAMPLES</span></span>

### <span data-ttu-id="2a37a-110">Beispiel 1: Entfernen einer angegebenen Ereignisquelle nach Name</span><span class="sxs-lookup"><span data-stu-id="2a37a-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="2a37a-111">Dadurch wird eine bestimmte Ereignisquelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="2a37a-111">This removes a specific event source.</span></span>

### <span data-ttu-id="2a37a-112">Beispiel 2: Entfernen einer angegebenen Ereignisquelle nach Objekt</span><span class="sxs-lookup"><span data-stu-id="2a37a-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="2a37a-113">Dadurch wird eine bestimmte Ereignisquelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="2a37a-113">This removes a specific event source.</span></span>

## <span data-ttu-id="2a37a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a37a-114">PARAMETERS</span></span>

### <span data-ttu-id="2a37a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a37a-115">-DefaultProfile</span></span>
<span data-ttu-id="2a37a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a37a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a37a-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="2a37a-117">-EnvironmentName</span></span>
<span data-ttu-id="2a37a-118">Der Name der Zeitreiheneinblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2a37a-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a37a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a37a-119">-InputObject</span></span>
<span data-ttu-id="2a37a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2a37a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a37a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2a37a-121">-Name</span></span>
<span data-ttu-id="2a37a-122">Der Name der Time Series Insights-Ereignisquelle, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2a37a-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a37a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a37a-123">-PassThru</span></span>
<span data-ttu-id="2a37a-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="2a37a-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2a37a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a37a-125">-ResourceGroupName</span></span>
<span data-ttu-id="2a37a-126">Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2a37a-126">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a37a-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a37a-127">-SubscriptionId</span></span>
<span data-ttu-id="2a37a-128">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="2a37a-128">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a37a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a37a-129">-Confirm</span></span>
<span data-ttu-id="2a37a-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a37a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a37a-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2a37a-131">-WhatIf</span></span>
<span data-ttu-id="2a37a-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a37a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a37a-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a37a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a37a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a37a-134">CommonParameters</span></span>
<span data-ttu-id="2a37a-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a37a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a37a-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a37a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a37a-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2a37a-137">INPUTS</span></span>

### <span data-ttu-id="2a37a-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="2a37a-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="2a37a-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2a37a-139">OUTPUTS</span></span>

### <span data-ttu-id="2a37a-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a37a-140">System.Boolean</span></span>

## <span data-ttu-id="2a37a-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2a37a-141">NOTES</span></span>

<span data-ttu-id="2a37a-142">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2a37a-142">ALIASES</span></span>

<span data-ttu-id="2a37a-143">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="2a37a-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2a37a-144">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2a37a-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2a37a-145">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2a37a-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2a37a-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="2a37a-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2a37a-147">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2a37a-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="2a37a-148">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="2a37a-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="2a37a-149">`[EventSourceName <String>]`: Der Name der Time Series Insights-Ereignisquelle, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2a37a-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="2a37a-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="2a37a-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2a37a-151">`[ReferenceDataSetName <String>]`: Name des Referenzdatensets.</span><span class="sxs-lookup"><span data-stu-id="2a37a-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="2a37a-152">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2a37a-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="2a37a-153">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="2a37a-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="2a37a-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2a37a-154">RELATED LINKS</span></span>

