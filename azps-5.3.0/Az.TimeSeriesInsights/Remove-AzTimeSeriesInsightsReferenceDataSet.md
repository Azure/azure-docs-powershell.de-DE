---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 56173c8ca384c817912395a536583fb26e9dfa76
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460523"
---
# <span data-ttu-id="125a0-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="125a0-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="125a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="125a0-102">SYNOPSIS</span></span>
<span data-ttu-id="125a0-103">Löscht das Referenzdatenset mit dem angegebenen Namen in dem angegebenen Abonnement, der Ressourcengruppe und der angegebenen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="125a0-103">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="125a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="125a0-104">SYNTAX</span></span>

### <span data-ttu-id="125a0-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="125a0-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="125a0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="125a0-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="125a0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="125a0-107">DESCRIPTION</span></span>
<span data-ttu-id="125a0-108">Löscht das Referenzdatenset mit dem angegebenen Namen in dem angegebenen Abonnement, der Ressourcengruppe und der angegebenen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="125a0-108">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="125a0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="125a0-109">EXAMPLES</span></span>

### <span data-ttu-id="125a0-110">Beispiel 1: Entfernen eines angegebenen Bezugsdatensets nach Name</span><span class="sxs-lookup"><span data-stu-id="125a0-110">Example 1: Remove a specified reference data set by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup

```

<span data-ttu-id="125a0-111">Mit diesem Befehl wird ein angegebenes Referenzdatenset entfernt.</span><span class="sxs-lookup"><span data-stu-id="125a0-111">This command removes a specified reference data set.</span></span>

### <span data-ttu-id="125a0-112">Beispiel 2: Entfernen eines angegebenen Verweisdatensets nach Objekt</span><span class="sxs-lookup"><span data-stu-id="125a0-112">Example 2: Remove a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

```

<span data-ttu-id="125a0-113">Mit diesem Befehl wird ein angegebenes Referenzdatenset entfernt.</span><span class="sxs-lookup"><span data-stu-id="125a0-113">This command removes a specified reference data set.</span></span>

## <span data-ttu-id="125a0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="125a0-114">PARAMETERS</span></span>

### <span data-ttu-id="125a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="125a0-115">-DefaultProfile</span></span>
<span data-ttu-id="125a0-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="125a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="125a0-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="125a0-117">-EnvironmentName</span></span>
<span data-ttu-id="125a0-118">Der Name der Zeitreiheneinblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="125a0-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="125a0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="125a0-119">-InputObject</span></span>
<span data-ttu-id="125a0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="125a0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="125a0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="125a0-121">-Name</span></span>
<span data-ttu-id="125a0-122">Der Name des Datensets für Zeitreiheneinblicke, das der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="125a0-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="125a0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="125a0-123">-PassThru</span></span>
<span data-ttu-id="125a0-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="125a0-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="125a0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="125a0-125">-ResourceGroupName</span></span>
<span data-ttu-id="125a0-126">Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="125a0-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="125a0-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="125a0-127">-SubscriptionId</span></span>
<span data-ttu-id="125a0-128">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="125a0-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="125a0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="125a0-129">-Confirm</span></span>
<span data-ttu-id="125a0-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="125a0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="125a0-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="125a0-131">-WhatIf</span></span>
<span data-ttu-id="125a0-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="125a0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="125a0-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="125a0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="125a0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="125a0-134">CommonParameters</span></span>
<span data-ttu-id="125a0-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="125a0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="125a0-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="125a0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="125a0-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="125a0-137">INPUTS</span></span>

### <span data-ttu-id="125a0-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="125a0-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="125a0-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="125a0-139">OUTPUTS</span></span>

### <span data-ttu-id="125a0-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="125a0-140">System.Boolean</span></span>

## <span data-ttu-id="125a0-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="125a0-141">NOTES</span></span>

<span data-ttu-id="125a0-142">ALIASE</span><span class="sxs-lookup"><span data-stu-id="125a0-142">ALIASES</span></span>

<span data-ttu-id="125a0-143">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="125a0-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="125a0-144">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="125a0-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="125a0-145">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="125a0-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="125a0-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="125a0-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="125a0-147">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="125a0-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="125a0-148">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="125a0-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="125a0-149">`[EventSourceName <String>]`: Der Name der Ereignisquelle für Zeitreiheneinblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="125a0-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="125a0-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="125a0-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="125a0-151">`[ReferenceDataSetName <String>]`: Name des Referenzdatensets.</span><span class="sxs-lookup"><span data-stu-id="125a0-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="125a0-152">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="125a0-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="125a0-153">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="125a0-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="125a0-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="125a0-154">RELATED LINKS</span></span>

