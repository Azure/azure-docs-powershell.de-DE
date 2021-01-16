---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: c7d8f46f42b1b42e4831540f5c68706c61ff78cf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360882"
---
# <span data-ttu-id="15ea6-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="15ea6-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="15ea6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="15ea6-103">Ruft die Zugriffsrichtlinie mit dem angegebenen Namen in der angegebenen Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="15ea6-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="15ea6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15ea6-104">SYNTAX</span></span>

### <span data-ttu-id="15ea6-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="15ea6-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="15ea6-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="15ea6-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="15ea6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="15ea6-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="15ea6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15ea6-108">DESCRIPTION</span></span>
<span data-ttu-id="15ea6-109">Ruft die Zugriffsrichtlinie mit dem angegebenen Namen in der angegebenen Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="15ea6-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="15ea6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="15ea6-110">EXAMPLES</span></span>

### <span data-ttu-id="15ea6-111">Beispiel 1: Auflisten aller Zugriffsrichtlinien in einer bestimmten Umgebung</span><span class="sxs-lookup"><span data-stu-id="15ea6-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="15ea6-112">Dieser Befehl listet alle Zugriffsrichtlinien in einer angegebenen Umgebung auf.</span><span class="sxs-lookup"><span data-stu-id="15ea6-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="15ea6-113">Beispiel 2: Erhalten einer angegebenen Zugriffsrichtlinie nach Name</span><span class="sxs-lookup"><span data-stu-id="15ea6-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="15ea6-114">Dieser Befehl ruft eine angegebene Zugriffsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="15ea6-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="15ea6-115">Beispiel 3: Erhalten einer angegebenen Zugriffsrichtlinie nach Objekt</span><span class="sxs-lookup"><span data-stu-id="15ea6-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="15ea6-116">Dieser Befehl ruft eine angegebene Zugriffsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="15ea6-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="15ea6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15ea6-117">PARAMETERS</span></span>

### <span data-ttu-id="15ea6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15ea6-118">-DefaultProfile</span></span>
<span data-ttu-id="15ea6-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="15ea6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15ea6-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="15ea6-120">-EnvironmentName</span></span>
<span data-ttu-id="15ea6-121">Der Name der Zeitreiheneinblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="15ea6-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="15ea6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15ea6-122">-InputObject</span></span>
<span data-ttu-id="15ea6-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="15ea6-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="15ea6-124">-Name</span><span class="sxs-lookup"><span data-stu-id="15ea6-124">-Name</span></span>
<span data-ttu-id="15ea6-125">Der Name der Zugriffsrichtlinie für Zeitreiheneinblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="15ea6-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="15ea6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15ea6-126">-ResourceGroupName</span></span>
<span data-ttu-id="15ea6-127">Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="15ea6-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="15ea6-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15ea6-128">-SubscriptionId</span></span>
<span data-ttu-id="15ea6-129">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="15ea6-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="15ea6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15ea6-130">CommonParameters</span></span>
<span data-ttu-id="15ea6-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15ea6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15ea6-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15ea6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15ea6-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="15ea6-133">INPUTS</span></span>

### <span data-ttu-id="15ea6-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="15ea6-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="15ea6-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="15ea6-135">OUTPUTS</span></span>

### <span data-ttu-id="15ea6-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="15ea6-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="15ea6-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="15ea6-137">NOTES</span></span>

<span data-ttu-id="15ea6-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="15ea6-138">ALIASES</span></span>

<span data-ttu-id="15ea6-139">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="15ea6-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="15ea6-140">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="15ea6-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="15ea6-141">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="15ea6-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="15ea6-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="15ea6-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="15ea6-143">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="15ea6-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="15ea6-144">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="15ea6-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="15ea6-145">`[EventSourceName <String>]`: Der Name der Ereignisquelle für Zeitreiheneinblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="15ea6-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="15ea6-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="15ea6-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="15ea6-147">`[ReferenceDataSetName <String>]`: Name des Referenzdatensets.</span><span class="sxs-lookup"><span data-stu-id="15ea6-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="15ea6-148">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="15ea6-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="15ea6-149">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="15ea6-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="15ea6-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="15ea6-150">RELATED LINKS</span></span>

