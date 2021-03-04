---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 89fa39a5e6e1bb2ded61c41dd553b6d7d0473d4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924304"
---
# <span data-ttu-id="54880-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="54880-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="54880-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54880-102">SYNOPSIS</span></span>
<span data-ttu-id="54880-103">Löscht die Umgebung mit dem angegebenen Namen in der angegebenen Abonnement- und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="54880-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="54880-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54880-104">SYNTAX</span></span>

### <span data-ttu-id="54880-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="54880-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="54880-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="54880-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="54880-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54880-107">DESCRIPTION</span></span>
<span data-ttu-id="54880-108">Löscht die Umgebung mit dem angegebenen Namen in der angegebenen Abonnement- und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="54880-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="54880-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54880-109">EXAMPLES</span></span>

### <span data-ttu-id="54880-110">Beispiel 1: Entfernen einer Umgebung für Zeitreiheneinblicke nach Name</span><span class="sxs-lookup"><span data-stu-id="54880-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="54880-111">Mit diesem Befehl wird eine Umgebung für Zeitreiheneinblicke entfernt.</span><span class="sxs-lookup"><span data-stu-id="54880-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="54880-112">Beispiel 2: Entfernen einer Umgebung für Zeitreiheneinblicke nach Objekt</span><span class="sxs-lookup"><span data-stu-id="54880-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="54880-113">Mit diesem Befehl wird eine Umgebung für Zeitreiheneinblicke entfernt.</span><span class="sxs-lookup"><span data-stu-id="54880-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="54880-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="54880-114">PARAMETERS</span></span>

### <span data-ttu-id="54880-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54880-115">-DefaultProfile</span></span>
<span data-ttu-id="54880-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54880-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54880-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54880-117">-InputObject</span></span>
<span data-ttu-id="54880-118">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="54880-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="54880-119">-Name</span><span class="sxs-lookup"><span data-stu-id="54880-119">-Name</span></span>
<span data-ttu-id="54880-120">Der Name der Zeitreiheneinblickumgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="54880-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="54880-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54880-121">-PassThru</span></span>
<span data-ttu-id="54880-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54880-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="54880-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54880-123">-ResourceGroupName</span></span>
<span data-ttu-id="54880-124">Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="54880-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="54880-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54880-125">-SubscriptionId</span></span>
<span data-ttu-id="54880-126">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="54880-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="54880-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="54880-127">-Confirm</span></span>
<span data-ttu-id="54880-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54880-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54880-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54880-129">-WhatIf</span></span>
<span data-ttu-id="54880-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54880-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54880-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54880-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54880-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54880-132">CommonParameters</span></span>
<span data-ttu-id="54880-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54880-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54880-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54880-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54880-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54880-135">INPUTS</span></span>

### <span data-ttu-id="54880-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="54880-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="54880-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54880-137">OUTPUTS</span></span>

### <span data-ttu-id="54880-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="54880-138">System.Boolean</span></span>

## <span data-ttu-id="54880-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="54880-139">NOTES</span></span>

<span data-ttu-id="54880-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="54880-140">ALIASES</span></span>

<span data-ttu-id="54880-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="54880-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="54880-142">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="54880-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="54880-143">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="54880-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="54880-144">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="54880-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="54880-145">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="54880-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="54880-146">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="54880-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="54880-147">`[EventSourceName <String>]`: Der Name der Time Series Insights-Ereignisquelle, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="54880-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="54880-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="54880-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="54880-149">`[ReferenceDataSetName <String>]`: Name des Bezugsdatensets.</span><span class="sxs-lookup"><span data-stu-id="54880-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="54880-150">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="54880-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="54880-151">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="54880-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="54880-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="54880-152">RELATED LINKS</span></span>

