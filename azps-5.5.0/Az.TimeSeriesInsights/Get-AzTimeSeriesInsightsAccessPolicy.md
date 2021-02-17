---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: c7d8f46f42b1b42e4831540f5c68706c61ff78cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149852"
---
# <span data-ttu-id="00f1d-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="00f1d-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="00f1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="00f1d-103">Ruft die Zugriffsrichtlinie mit dem angegebenen Namen in der angegebenen Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="00f1d-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="00f1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00f1d-104">SYNTAX</span></span>

### <span data-ttu-id="00f1d-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="00f1d-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="00f1d-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="00f1d-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="00f1d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="00f1d-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="00f1d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00f1d-108">DESCRIPTION</span></span>
<span data-ttu-id="00f1d-109">Ruft die Zugriffsrichtlinie mit dem angegebenen Namen in der angegebenen Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="00f1d-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="00f1d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="00f1d-110">EXAMPLES</span></span>

### <span data-ttu-id="00f1d-111">Beispiel 1: Auflisten aller Zugriffsrichtlinien in einer bestimmten Umgebung</span><span class="sxs-lookup"><span data-stu-id="00f1d-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="00f1d-112">Dieser Befehl listet alle Zugriffsrichtlinien in einer angegebenen Umgebung auf.</span><span class="sxs-lookup"><span data-stu-id="00f1d-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="00f1d-113">Beispiel 2: Erhalten einer angegebenen Zugriffsrichtlinie nach Name</span><span class="sxs-lookup"><span data-stu-id="00f1d-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="00f1d-114">Dieser Befehl ruft eine angegebene Zugriffsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="00f1d-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="00f1d-115">Beispiel 3: Erhalten einer angegebenen Zugriffsrichtlinie nach Objekt</span><span class="sxs-lookup"><span data-stu-id="00f1d-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="00f1d-116">Dieser Befehl ruft eine angegebene Zugriffsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="00f1d-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="00f1d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00f1d-117">PARAMETERS</span></span>

### <span data-ttu-id="00f1d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f1d-118">-DefaultProfile</span></span>
<span data-ttu-id="00f1d-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00f1d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00f1d-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="00f1d-120">-EnvironmentName</span></span>
<span data-ttu-id="00f1d-121">Der Name der Zeitreiheneinblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="00f1d-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="00f1d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00f1d-122">-InputObject</span></span>
<span data-ttu-id="00f1d-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="00f1d-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="00f1d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="00f1d-124">-Name</span></span>
<span data-ttu-id="00f1d-125">Der Name der Zugriffsrichtlinie für Zeitreiheneinblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="00f1d-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f1d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f1d-126">-ResourceGroupName</span></span>
<span data-ttu-id="00f1d-127">Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="00f1d-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="00f1d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00f1d-128">-SubscriptionId</span></span>
<span data-ttu-id="00f1d-129">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="00f1d-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="00f1d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f1d-130">CommonParameters</span></span>
<span data-ttu-id="00f1d-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00f1d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f1d-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00f1d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f1d-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="00f1d-133">INPUTS</span></span>

### <span data-ttu-id="00f1d-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="00f1d-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="00f1d-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="00f1d-135">OUTPUTS</span></span>

### <span data-ttu-id="00f1d-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="00f1d-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="00f1d-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="00f1d-137">NOTES</span></span>

<span data-ttu-id="00f1d-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="00f1d-138">ALIASES</span></span>

<span data-ttu-id="00f1d-139">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="00f1d-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="00f1d-140">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="00f1d-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="00f1d-141">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="00f1d-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="00f1d-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="00f1d-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="00f1d-143">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="00f1d-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="00f1d-144">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="00f1d-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="00f1d-145">`[EventSourceName <String>]`: Der Name der Time Series Insights-Ereignisquelle, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="00f1d-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="00f1d-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="00f1d-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="00f1d-147">`[ReferenceDataSetName <String>]`: Name des Referenzdatensets.</span><span class="sxs-lookup"><span data-stu-id="00f1d-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="00f1d-148">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="00f1d-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="00f1d-149">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="00f1d-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="00f1d-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="00f1d-150">RELATED LINKS</span></span>

