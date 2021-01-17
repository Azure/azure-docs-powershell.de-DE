---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 8b56475d2510099b7873fa444a0dc78497aeb729
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471656"
---
# <span data-ttu-id="6de46-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="6de46-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="6de46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6de46-102">SYNOPSIS</span></span>
<span data-ttu-id="6de46-103">Löscht die Umgebung mit dem angegebenen Namen in der angegebenen Abonnement- und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6de46-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="6de46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6de46-104">SYNTAX</span></span>

### <span data-ttu-id="6de46-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="6de46-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6de46-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6de46-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6de46-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6de46-107">DESCRIPTION</span></span>
<span data-ttu-id="6de46-108">Löscht die Umgebung mit dem angegebenen Namen in der angegebenen Abonnement- und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6de46-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="6de46-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6de46-109">EXAMPLES</span></span>

### <span data-ttu-id="6de46-110">Beispiel 1: Entfernen einer Umgebung für Zeitreiheneinblicke nach Name</span><span class="sxs-lookup"><span data-stu-id="6de46-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="6de46-111">Mit diesem Befehl wird eine Umgebung für Zeitreiheneinblicke entfernt.</span><span class="sxs-lookup"><span data-stu-id="6de46-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="6de46-112">Beispiel 2: Entfernen einer Umgebung für Zeitreiheneinblicke nach Objekt</span><span class="sxs-lookup"><span data-stu-id="6de46-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="6de46-113">Mit diesem Befehl wird eine Umgebung für Zeitreiheneinblicke entfernt.</span><span class="sxs-lookup"><span data-stu-id="6de46-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="6de46-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6de46-114">PARAMETERS</span></span>

### <span data-ttu-id="6de46-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de46-115">-DefaultProfile</span></span>
<span data-ttu-id="6de46-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6de46-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6de46-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6de46-117">-InputObject</span></span>
<span data-ttu-id="6de46-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6de46-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6de46-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6de46-119">-Name</span></span>
<span data-ttu-id="6de46-120">Der Name der Zeitreiheneinblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6de46-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de46-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6de46-121">-PassThru</span></span>
<span data-ttu-id="6de46-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="6de46-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6de46-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6de46-123">-ResourceGroupName</span></span>
<span data-ttu-id="6de46-124">Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6de46-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="6de46-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6de46-125">-SubscriptionId</span></span>
<span data-ttu-id="6de46-126">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="6de46-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="6de46-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6de46-127">-Confirm</span></span>
<span data-ttu-id="6de46-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6de46-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6de46-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6de46-129">-WhatIf</span></span>
<span data-ttu-id="6de46-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6de46-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6de46-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6de46-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6de46-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de46-132">CommonParameters</span></span>
<span data-ttu-id="6de46-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de46-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de46-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6de46-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de46-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6de46-135">INPUTS</span></span>

### <span data-ttu-id="6de46-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="6de46-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="6de46-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6de46-137">OUTPUTS</span></span>

### <span data-ttu-id="6de46-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6de46-138">System.Boolean</span></span>

## <span data-ttu-id="6de46-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6de46-139">NOTES</span></span>

<span data-ttu-id="6de46-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="6de46-140">ALIASES</span></span>

<span data-ttu-id="6de46-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="6de46-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6de46-142">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6de46-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6de46-143">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6de46-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6de46-144">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6de46-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6de46-145">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="6de46-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="6de46-146">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="6de46-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="6de46-147">`[EventSourceName <String>]`: Der Name der Ereignisquelle für Zeitreiheneinblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6de46-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="6de46-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="6de46-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6de46-149">`[ReferenceDataSetName <String>]`: Name des Referenzdatensets.</span><span class="sxs-lookup"><span data-stu-id="6de46-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="6de46-150">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6de46-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="6de46-151">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="6de46-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="6de46-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6de46-152">RELATED LINKS</span></span>

