---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: ed4a3e7c9b53bd481d4d30c4f6a555d8f42c44fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178113"
---
# <span data-ttu-id="0037e-101">Get-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="0037e-101">Get-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="0037e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0037e-102">SYNOPSIS</span></span>
<span data-ttu-id="0037e-103">Ruft den Verweisdaten Satz mit dem angegebenen Namen in der angegebenen Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="0037e-103">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="0037e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0037e-104">SYNTAX</span></span>

### <span data-ttu-id="0037e-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="0037e-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0037e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="0037e-106">Get</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0037e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0037e-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0037e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0037e-108">DESCRIPTION</span></span>
<span data-ttu-id="0037e-109">Ruft den Verweisdaten Satz mit dem angegebenen Namen in der angegebenen Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="0037e-109">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="0037e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0037e-110">EXAMPLES</span></span>

### <span data-ttu-id="0037e-111">Beispiel 1: Auflisten aller Verweisdaten Sätze unter der angegebenen Umgebung</span><span class="sxs-lookup"><span data-stu-id="0037e-111">Example 1: List all reference data sets under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
eastus   dstest002 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="0037e-112">Dieser Befehl listet alle Referenzdatensätze in der angegebenen Umgebung auf.</span><span class="sxs-lookup"><span data-stu-id="0037e-112">This command lists all reference data sets under the specified environment.</span></span>

### <span data-ttu-id="0037e-113">Beispiel 2: Abrufen eines angegebenen Verweisdaten Satzes nach Name</span><span class="sxs-lookup"><span data-stu-id="0037e-113">Example 2: Get a specified reference data set by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="0037e-114">Dieser Befehl ruft einen angegebenen Verweisdaten Satz ab.</span><span class="sxs-lookup"><span data-stu-id="0037e-114">This command gets a specified reference data set.</span></span>

### <span data-ttu-id="0037e-115">Beispiel 3: Abrufen eines angegebenen Verweisdaten Satzes nach Objekt</span><span class="sxs-lookup"><span data-stu-id="0037e-115">Example 3: Get a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsirdsqwufij 
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

Location Name         Type
-------- ----         ----
eastus2  tsirdsqwufij Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="0037e-116">Dieser Befehl ruft einen angegebenen Verweisdaten Satz ab.</span><span class="sxs-lookup"><span data-stu-id="0037e-116">This command gets a specified reference data set.</span></span>

## <span data-ttu-id="0037e-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="0037e-117">PARAMETERS</span></span>

### <span data-ttu-id="0037e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0037e-118">-DefaultProfile</span></span>
<span data-ttu-id="0037e-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0037e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0037e-120">-Umgebungsname</span><span class="sxs-lookup"><span data-stu-id="0037e-120">-EnvironmentName</span></span>
<span data-ttu-id="0037e-121">Der Name der Zeitreihen Einblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0037e-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="0037e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0037e-122">-InputObject</span></span>
<span data-ttu-id="0037e-123">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0037e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0037e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0037e-124">-Name</span></span>
<span data-ttu-id="0037e-125">Der Name der Zeitreihen Einblicke-Referenzdatensatz, der der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0037e-125">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="0037e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0037e-126">-ResourceGroupName</span></span>
<span data-ttu-id="0037e-127">Der Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0037e-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="0037e-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="0037e-128">-SubscriptionId</span></span>
<span data-ttu-id="0037e-129">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="0037e-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="0037e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0037e-130">CommonParameters</span></span>
<span data-ttu-id="0037e-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0037e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0037e-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0037e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0037e-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0037e-133">INPUTS</span></span>

### <span data-ttu-id="0037e-134">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="0037e-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="0037e-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0037e-135">OUTPUTS</span></span>

### <span data-ttu-id="0037e-136">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="0037e-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="0037e-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="0037e-137">NOTES</span></span>

<span data-ttu-id="0037e-138">Aliase</span><span class="sxs-lookup"><span data-stu-id="0037e-138">ALIASES</span></span>

<span data-ttu-id="0037e-139">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0037e-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0037e-140">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0037e-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0037e-141">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="0037e-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0037e-142">Inputobject <ITimeSeriesInsightsIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="0037e-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0037e-143">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="0037e-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="0037e-144">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="0037e-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="0037e-145">`[EventSourceName <String>]`: Der Name der Ereignisquelle für Zeitreihen Einblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0037e-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="0037e-146">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="0037e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0037e-147">`[ReferenceDataSetName <String>]`: Name des referenzdatensatzes.</span><span class="sxs-lookup"><span data-stu-id="0037e-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="0037e-148">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0037e-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="0037e-149">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="0037e-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="0037e-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0037e-150">RELATED LINKS</span></span>

