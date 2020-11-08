---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 7dbced00ee2e39c536765bd16a19fbe7a66e291b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175358"
---
# <span data-ttu-id="4184b-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="4184b-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="4184b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4184b-102">SYNOPSIS</span></span>
<span data-ttu-id="4184b-103">Aktualisiert den Verweisdaten Satz mit dem angegebenen Namen im angegebenen Abonnement, in der Ressourcengruppe und in der Umgebung.</span><span class="sxs-lookup"><span data-stu-id="4184b-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="4184b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4184b-104">SYNTAX</span></span>

### <span data-ttu-id="4184b-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="4184b-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4184b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4184b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4184b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4184b-107">DESCRIPTION</span></span>
<span data-ttu-id="4184b-108">Aktualisiert den Verweisdaten Satz mit dem angegebenen Namen im angegebenen Abonnement, in der Ressourcengruppe und in der Umgebung.</span><span class="sxs-lookup"><span data-stu-id="4184b-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="4184b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4184b-109">EXAMPLES</span></span>

### <span data-ttu-id="4184b-110">Beispiel 1: Aktualisieren eines angegebenen Verweisdaten Satzes nach Name</span><span class="sxs-lookup"><span data-stu-id="4184b-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="4184b-111">Mit diesem Befehl wird ein angegebener Verweisdaten Satz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4184b-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="4184b-112">Beispiel 2: Aktualisieren eines angegebenen Verweisdatasets nach Objekt</span><span class="sxs-lookup"><span data-stu-id="4184b-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="4184b-113">Mit diesem Befehl wird ein angegebener Verweisdaten Satz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4184b-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="4184b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4184b-114">PARAMETERS</span></span>

### <span data-ttu-id="4184b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4184b-115">-DefaultProfile</span></span>
<span data-ttu-id="4184b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4184b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4184b-117">-Umgebungsname</span><span class="sxs-lookup"><span data-stu-id="4184b-117">-EnvironmentName</span></span>
<span data-ttu-id="4184b-118">Der Name der Zeitreihen Einblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4184b-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="4184b-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4184b-119">-InputObject</span></span>
<span data-ttu-id="4184b-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="4184b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4184b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4184b-121">-Name</span></span>
<span data-ttu-id="4184b-122">Der Name der Zeitreihen Einblicke-Referenzdatensatz, der der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4184b-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4184b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4184b-123">-ResourceGroupName</span></span>
<span data-ttu-id="4184b-124">Der Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4184b-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="4184b-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="4184b-125">-SubscriptionId</span></span>
<span data-ttu-id="4184b-126">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="4184b-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="4184b-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="4184b-127">-Tag</span></span>
<span data-ttu-id="4184b-128">Schlüssel-Wert-Paare zusätzlicher Eigenschaften für den Verweisdaten Satz.</span><span class="sxs-lookup"><span data-stu-id="4184b-128">Key-value pairs of additional properties for the reference data set.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4184b-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4184b-129">-Confirm</span></span>
<span data-ttu-id="4184b-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4184b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4184b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4184b-131">-WhatIf</span></span>
<span data-ttu-id="4184b-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4184b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4184b-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4184b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4184b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4184b-134">CommonParameters</span></span>
<span data-ttu-id="4184b-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4184b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4184b-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4184b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4184b-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4184b-137">INPUTS</span></span>

### <span data-ttu-id="4184b-138">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="4184b-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="4184b-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4184b-139">OUTPUTS</span></span>

### <span data-ttu-id="4184b-140">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="4184b-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="4184b-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="4184b-141">NOTES</span></span>

<span data-ttu-id="4184b-142">Aliase</span><span class="sxs-lookup"><span data-stu-id="4184b-142">ALIASES</span></span>

<span data-ttu-id="4184b-143">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4184b-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4184b-144">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4184b-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4184b-145">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="4184b-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4184b-146">Inputobject <ITimeSeriesInsightsIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="4184b-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4184b-147">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="4184b-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="4184b-148">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="4184b-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="4184b-149">`[EventSourceName <String>]`: Der Name der Ereignisquelle für Zeitreihen Einblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4184b-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="4184b-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="4184b-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4184b-151">`[ReferenceDataSetName <String>]`: Name des referenzdatensatzes.</span><span class="sxs-lookup"><span data-stu-id="4184b-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="4184b-152">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4184b-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="4184b-153">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="4184b-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="4184b-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4184b-154">RELATED LINKS</span></span>

