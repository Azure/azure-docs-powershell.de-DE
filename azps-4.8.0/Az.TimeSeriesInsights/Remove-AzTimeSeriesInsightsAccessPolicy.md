---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 2a6c58729d08c5bd060434c7a21720f87a3f7de3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173353"
---
# <span data-ttu-id="2135d-101">Remove-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2135d-101">Remove-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="2135d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2135d-102">SYNOPSIS</span></span>
<span data-ttu-id="2135d-103">Löscht die Zugriffsrichtlinie mit dem angegebenen Namen im angegebenen Abonnement, in der Ressourcengruppe und in der Umgebung</span><span class="sxs-lookup"><span data-stu-id="2135d-103">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="2135d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2135d-104">SYNTAX</span></span>

### <span data-ttu-id="2135d-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="2135d-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2135d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2135d-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2135d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2135d-107">DESCRIPTION</span></span>
<span data-ttu-id="2135d-108">Löscht die Zugriffsrichtlinie mit dem angegebenen Namen im angegebenen Abonnement, in der Ressourcengruppe und in der Umgebung</span><span class="sxs-lookup"><span data-stu-id="2135d-108">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="2135d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2135d-109">EXAMPLES</span></span>

### <span data-ttu-id="2135d-110">Beispiel 1: Entfernen einer angegebenen Zugriffsrichtlinie nach Namen</span><span class="sxs-lookup"><span data-stu-id="2135d-110">Example 1: Remove a specified access policy by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup

```

<span data-ttu-id="2135d-111">Mit diesem Befehl wird eine angegebene Zugriffsrichtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="2135d-111">This command removes a specified access policy.</span></span>

### <span data-ttu-id="2135d-112">Beispiel 2: Entfernen einer angegebenen Zugriffsrichtlinie nach Objekt</span><span class="sxs-lookup"><span data-stu-id="2135d-112">Example 2: Remove a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -InputObject $policy

```

<span data-ttu-id="2135d-113">Mit diesem Befehl wird eine angegebene Zugriffsrichtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="2135d-113">This command removes a specified access policy.</span></span>

## <span data-ttu-id="2135d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2135d-114">PARAMETERS</span></span>

### <span data-ttu-id="2135d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2135d-115">-DefaultProfile</span></span>
<span data-ttu-id="2135d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2135d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2135d-117">-Umgebungsname</span><span class="sxs-lookup"><span data-stu-id="2135d-117">-EnvironmentName</span></span>
<span data-ttu-id="2135d-118">Der Name der Zeitreihen Einblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2135d-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="2135d-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2135d-119">-InputObject</span></span>
<span data-ttu-id="2135d-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2135d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2135d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2135d-121">-Name</span></span>
<span data-ttu-id="2135d-122">Der Name der Zugriffsrichtlinie für Zeitreihen Einblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2135d-122">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="2135d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2135d-123">-PassThru</span></span>
<span data-ttu-id="2135d-124">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="2135d-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2135d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2135d-125">-ResourceGroupName</span></span>
<span data-ttu-id="2135d-126">Der Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2135d-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="2135d-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2135d-127">-SubscriptionId</span></span>
<span data-ttu-id="2135d-128">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="2135d-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="2135d-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2135d-129">-Confirm</span></span>
<span data-ttu-id="2135d-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2135d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2135d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2135d-131">-WhatIf</span></span>
<span data-ttu-id="2135d-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2135d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2135d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2135d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2135d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2135d-134">CommonParameters</span></span>
<span data-ttu-id="2135d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2135d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2135d-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2135d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2135d-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2135d-137">INPUTS</span></span>

### <span data-ttu-id="2135d-138">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="2135d-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="2135d-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2135d-139">OUTPUTS</span></span>

### <span data-ttu-id="2135d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2135d-140">System.Boolean</span></span>

## <span data-ttu-id="2135d-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="2135d-141">NOTES</span></span>

<span data-ttu-id="2135d-142">Aliase</span><span class="sxs-lookup"><span data-stu-id="2135d-142">ALIASES</span></span>

<span data-ttu-id="2135d-143">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2135d-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2135d-144">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2135d-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2135d-145">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="2135d-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2135d-146">Inputobject <ITimeSeriesInsightsIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="2135d-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2135d-147">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2135d-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="2135d-148">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="2135d-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="2135d-149">`[EventSourceName <String>]`: Der Name der Ereignisquelle für Zeitreihen Einblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2135d-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="2135d-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="2135d-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2135d-151">`[ReferenceDataSetName <String>]`: Name des referenzdatensatzes.</span><span class="sxs-lookup"><span data-stu-id="2135d-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="2135d-152">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2135d-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="2135d-153">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="2135d-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="2135d-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2135d-154">RELATED LINKS</span></span>

