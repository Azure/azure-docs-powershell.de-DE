---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 2fe9a418f135471e18f469bf0dcf5ce515de1c2e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924320"
---
# <span data-ttu-id="e4427-101">Remove-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e4427-101">Remove-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="e4427-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4427-102">SYNOPSIS</span></span>
<span data-ttu-id="e4427-103">Löscht die Zugriffsrichtlinie mit dem angegebenen Namen im angegebenen Abonnement, der Ressourcengruppe und der Angegebenen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="e4427-103">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="e4427-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4427-104">SYNTAX</span></span>

### <span data-ttu-id="e4427-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="e4427-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e4427-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e4427-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e4427-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4427-107">DESCRIPTION</span></span>
<span data-ttu-id="e4427-108">Löscht die Zugriffsrichtlinie mit dem angegebenen Namen im angegebenen Abonnement, der Ressourcengruppe und der Angegebenen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="e4427-108">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="e4427-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e4427-109">EXAMPLES</span></span>

### <span data-ttu-id="e4427-110">Beispiel 1: Entfernen einer angegebenen Zugriffsrichtlinie nach Name</span><span class="sxs-lookup"><span data-stu-id="e4427-110">Example 1: Remove a specified access policy by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup

```

<span data-ttu-id="e4427-111">Mit diesem Befehl wird eine angegebene Zugriffsrichtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="e4427-111">This command removes a specified access policy.</span></span>

### <span data-ttu-id="e4427-112">Beispiel 2: Entfernen einer angegebenen Zugriffsrichtlinie nach Objekt</span><span class="sxs-lookup"><span data-stu-id="e4427-112">Example 2: Remove a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -InputObject $policy

```

<span data-ttu-id="e4427-113">Mit diesem Befehl wird eine angegebene Zugriffsrichtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="e4427-113">This command removes a specified access policy.</span></span>

## <span data-ttu-id="e4427-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e4427-114">PARAMETERS</span></span>

### <span data-ttu-id="e4427-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4427-115">-DefaultProfile</span></span>
<span data-ttu-id="e4427-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4427-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4427-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="e4427-117">-EnvironmentName</span></span>
<span data-ttu-id="e4427-118">Der Name der Zeitreiheneinblickumgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e4427-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="e4427-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4427-119">-InputObject</span></span>
<span data-ttu-id="e4427-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e4427-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e4427-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e4427-121">-Name</span></span>
<span data-ttu-id="e4427-122">Der Name der Time Series Insights-Zugriffsrichtlinie, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e4427-122">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4427-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4427-123">-PassThru</span></span>
<span data-ttu-id="e4427-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4427-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e4427-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4427-125">-ResourceGroupName</span></span>
<span data-ttu-id="e4427-126">Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e4427-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="e4427-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4427-127">-SubscriptionId</span></span>
<span data-ttu-id="e4427-128">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e4427-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="e4427-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e4427-129">-Confirm</span></span>
<span data-ttu-id="e4427-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e4427-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4427-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4427-131">-WhatIf</span></span>
<span data-ttu-id="e4427-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4427-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4427-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4427-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4427-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4427-134">CommonParameters</span></span>
<span data-ttu-id="e4427-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4427-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4427-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4427-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4427-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e4427-137">INPUTS</span></span>

### <span data-ttu-id="e4427-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="e4427-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="e4427-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e4427-139">OUTPUTS</span></span>

### <span data-ttu-id="e4427-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e4427-140">System.Boolean</span></span>

## <span data-ttu-id="e4427-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e4427-141">NOTES</span></span>

<span data-ttu-id="e4427-142">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e4427-142">ALIASES</span></span>

<span data-ttu-id="e4427-143">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e4427-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e4427-144">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="e4427-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4427-145">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e4427-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e4427-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="e4427-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e4427-147">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="e4427-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="e4427-148">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="e4427-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="e4427-149">`[EventSourceName <String>]`: Der Name der Time Series Insights-Ereignisquelle, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e4427-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="e4427-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="e4427-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e4427-151">`[ReferenceDataSetName <String>]`: Name des Bezugsdatensets.</span><span class="sxs-lookup"><span data-stu-id="e4427-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="e4427-152">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e4427-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="e4427-153">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e4427-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="e4427-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e4427-154">RELATED LINKS</span></span>

