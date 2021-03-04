---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 20a9abc5cfc2ad2cc35bbedcf976daac286abb92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928811"
---
# <span data-ttu-id="30a97-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30a97-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="30a97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30a97-102">SYNOPSIS</span></span>
<span data-ttu-id="30a97-103">Ruft die Zugriffsrichtlinie mit dem angegebenen Namen in der angegebenen Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="30a97-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="30a97-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30a97-104">SYNTAX</span></span>

### <span data-ttu-id="30a97-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="30a97-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="30a97-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="30a97-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="30a97-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="30a97-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="30a97-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30a97-108">DESCRIPTION</span></span>
<span data-ttu-id="30a97-109">Ruft die Zugriffsrichtlinie mit dem angegebenen Namen in der angegebenen Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="30a97-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="30a97-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="30a97-110">EXAMPLES</span></span>

### <span data-ttu-id="30a97-111">Beispiel 1: Auflisten aller Zugriffsrichtlinien in einer angegebenen Umgebung</span><span class="sxs-lookup"><span data-stu-id="30a97-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="30a97-112">Mit diesem Befehl werden alle Zugriffsrichtlinien unter einer angegebenen Umgebung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="30a97-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="30a97-113">Beispiel 2: Erhalten einer angegebenen Zugriffsrichtlinie nach Name</span><span class="sxs-lookup"><span data-stu-id="30a97-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="30a97-114">Dieser Befehl ruft eine angegebene Zugriffsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="30a97-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="30a97-115">Beispiel 3: Erhalten einer angegebenen Zugriffsrichtlinie nach Objekt</span><span class="sxs-lookup"><span data-stu-id="30a97-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="30a97-116">Dieser Befehl ruft eine angegebene Zugriffsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="30a97-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="30a97-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="30a97-117">PARAMETERS</span></span>

### <span data-ttu-id="30a97-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a97-118">-DefaultProfile</span></span>
<span data-ttu-id="30a97-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="30a97-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30a97-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="30a97-120">-EnvironmentName</span></span>
<span data-ttu-id="30a97-121">Der Name der Zeitreiheneinblickumgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="30a97-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="30a97-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30a97-122">-InputObject</span></span>
<span data-ttu-id="30a97-123">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="30a97-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="30a97-124">-Name</span><span class="sxs-lookup"><span data-stu-id="30a97-124">-Name</span></span>
<span data-ttu-id="30a97-125">Der Name der Time Series Insights-Zugriffsrichtlinie, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="30a97-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="30a97-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30a97-126">-ResourceGroupName</span></span>
<span data-ttu-id="30a97-127">Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="30a97-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="30a97-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30a97-128">-SubscriptionId</span></span>
<span data-ttu-id="30a97-129">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="30a97-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="30a97-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a97-130">CommonParameters</span></span>
<span data-ttu-id="30a97-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a97-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a97-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30a97-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a97-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="30a97-133">INPUTS</span></span>

### <span data-ttu-id="30a97-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="30a97-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="30a97-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="30a97-135">OUTPUTS</span></span>

### <span data-ttu-id="30a97-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="30a97-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="30a97-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="30a97-137">NOTES</span></span>

<span data-ttu-id="30a97-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="30a97-138">ALIASES</span></span>

<span data-ttu-id="30a97-139">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="30a97-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="30a97-140">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="30a97-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="30a97-141">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="30a97-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="30a97-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="30a97-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="30a97-143">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="30a97-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="30a97-144">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="30a97-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="30a97-145">`[EventSourceName <String>]`: Der Name der Time Series Insights-Ereignisquelle, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="30a97-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="30a97-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="30a97-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="30a97-147">`[ReferenceDataSetName <String>]`: Name des Bezugsdatensets.</span><span class="sxs-lookup"><span data-stu-id="30a97-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="30a97-148">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="30a97-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="30a97-149">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="30a97-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="30a97-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="30a97-150">RELATED LINKS</span></span>

