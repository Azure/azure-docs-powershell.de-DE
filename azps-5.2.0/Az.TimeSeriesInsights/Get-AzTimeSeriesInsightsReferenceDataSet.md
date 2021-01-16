---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: ed4a3e7c9b53bd481d4d30c4f6a555d8f42c44fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296591"
---
# <span data-ttu-id="64c50-101">Get-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="64c50-101">Get-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="64c50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64c50-102">SYNOPSIS</span></span>
<span data-ttu-id="64c50-103">Ruft das Referenzdatenset mit dem angegebenen Namen in der angegebenen Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="64c50-103">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="64c50-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64c50-104">SYNTAX</span></span>

### <span data-ttu-id="64c50-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="64c50-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="64c50-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="64c50-106">Get</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="64c50-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="64c50-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="64c50-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64c50-108">DESCRIPTION</span></span>
<span data-ttu-id="64c50-109">Ruft das Referenzdatenset mit dem angegebenen Namen in der angegebenen Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="64c50-109">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="64c50-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="64c50-110">EXAMPLES</span></span>

### <span data-ttu-id="64c50-111">Beispiel 1: Auflisten aller Referenzdatensets in der angegebenen Umgebung</span><span class="sxs-lookup"><span data-stu-id="64c50-111">Example 1: List all reference data sets under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
eastus   dstest002 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="64c50-112">Dieser Befehl listet alle Referenzdatensets unter der angegebenen Umgebung auf.</span><span class="sxs-lookup"><span data-stu-id="64c50-112">This command lists all reference data sets under the specified environment.</span></span>

### <span data-ttu-id="64c50-113">Beispiel 2: Erhalten eines angegebenen Bezugsdatensets nach Name</span><span class="sxs-lookup"><span data-stu-id="64c50-113">Example 2: Get a specified reference data set by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="64c50-114">Dieser Befehl ruft ein angegebenes Referenzdatenset ab.</span><span class="sxs-lookup"><span data-stu-id="64c50-114">This command gets a specified reference data set.</span></span>

### <span data-ttu-id="64c50-115">Beispiel 3: Erhalten eines angegebenen Verweisdatensets nach Objekt</span><span class="sxs-lookup"><span data-stu-id="64c50-115">Example 3: Get a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsirdsqwufij 
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

Location Name         Type
-------- ----         ----
eastus2  tsirdsqwufij Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="64c50-116">Dieser Befehl ruft ein angegebenes Referenzdatenset ab.</span><span class="sxs-lookup"><span data-stu-id="64c50-116">This command gets a specified reference data set.</span></span>

## <span data-ttu-id="64c50-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64c50-117">PARAMETERS</span></span>

### <span data-ttu-id="64c50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64c50-118">-DefaultProfile</span></span>
<span data-ttu-id="64c50-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64c50-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64c50-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="64c50-120">-EnvironmentName</span></span>
<span data-ttu-id="64c50-121">Der Name der Zeitreiheneinblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64c50-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c50-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64c50-122">-InputObject</span></span>
<span data-ttu-id="64c50-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="64c50-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64c50-124">-Name</span><span class="sxs-lookup"><span data-stu-id="64c50-124">-Name</span></span>
<span data-ttu-id="64c50-125">Der Name des Datensets für Zeitreiheneinblicke, das der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64c50-125">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c50-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64c50-126">-ResourceGroupName</span></span>
<span data-ttu-id="64c50-127">Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="64c50-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c50-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64c50-128">-SubscriptionId</span></span>
<span data-ttu-id="64c50-129">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="64c50-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c50-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c50-130">CommonParameters</span></span>
<span data-ttu-id="64c50-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64c50-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c50-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64c50-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c50-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="64c50-133">INPUTS</span></span>

### <span data-ttu-id="64c50-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="64c50-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="64c50-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="64c50-135">OUTPUTS</span></span>

### <span data-ttu-id="64c50-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="64c50-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="64c50-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="64c50-137">NOTES</span></span>

<span data-ttu-id="64c50-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="64c50-138">ALIASES</span></span>

<span data-ttu-id="64c50-139">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="64c50-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64c50-140">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="64c50-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64c50-141">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64c50-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64c50-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="64c50-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64c50-143">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="64c50-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="64c50-144">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="64c50-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="64c50-145">`[EventSourceName <String>]`: Der Name der Time Series Insights-Ereignisquelle, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64c50-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="64c50-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="64c50-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64c50-147">`[ReferenceDataSetName <String>]`: Name des Referenzdatensets.</span><span class="sxs-lookup"><span data-stu-id="64c50-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="64c50-148">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="64c50-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="64c50-149">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="64c50-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="64c50-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="64c50-150">RELATED LINKS</span></span>

