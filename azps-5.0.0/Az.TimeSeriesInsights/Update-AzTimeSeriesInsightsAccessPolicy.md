---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: e776b0e11fedd0b2903135b9b640c3b704706027
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176201"
---
# <span data-ttu-id="bceae-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bceae-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="bceae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bceae-102">SYNOPSIS</span></span>
<span data-ttu-id="bceae-103">Aktualisiert die Zugriffsrichtlinie mit dem angegebenen Namen im angegebenen Abonnement, in der Ressourcengruppe und in der Umgebung.</span><span class="sxs-lookup"><span data-stu-id="bceae-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="bceae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bceae-104">SYNTAX</span></span>

### <span data-ttu-id="bceae-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="bceae-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bceae-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bceae-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bceae-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bceae-107">DESCRIPTION</span></span>
<span data-ttu-id="bceae-108">Aktualisiert die Zugriffsrichtlinie mit dem angegebenen Namen im angegebenen Abonnement, in der Ressourcengruppe und in der Umgebung.</span><span class="sxs-lookup"><span data-stu-id="bceae-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="bceae-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bceae-109">EXAMPLES</span></span>

### <span data-ttu-id="bceae-110">Beispiel 1: Aktualisieren einer angegebenen Zugriffsrichtlinie nach Namen</span><span class="sxs-lookup"><span data-stu-id="bceae-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="bceae-111">Mit diesem Befehl wird eine bestimmte Zugriffsrichtlinie aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bceae-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="bceae-112">Beispiel 2: Aktualisieren einer angegebenen Zugriffsrichtlinie nach Objekt</span><span class="sxs-lookup"><span data-stu-id="bceae-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="bceae-113">Mit diesem Befehl wird eine bestimmte Zugriffsrichtlinie aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bceae-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="bceae-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="bceae-114">PARAMETERS</span></span>

### <span data-ttu-id="bceae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bceae-115">-DefaultProfile</span></span>
<span data-ttu-id="bceae-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bceae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bceae-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bceae-117">-Description</span></span>
<span data-ttu-id="bceae-118">Eine Beschreibung der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="bceae-118">An description of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bceae-119">-Umgebungsname</span><span class="sxs-lookup"><span data-stu-id="bceae-119">-EnvironmentName</span></span>
<span data-ttu-id="bceae-120">Der Name der Zeitreihen Einblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bceae-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="bceae-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bceae-121">-InputObject</span></span>
<span data-ttu-id="bceae-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="bceae-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bceae-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bceae-123">-Name</span></span>
<span data-ttu-id="bceae-124">Der Name der Zugriffsrichtlinie für Zeitreihen Einblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bceae-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bceae-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bceae-125">-ResourceGroupName</span></span>
<span data-ttu-id="bceae-126">Der Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bceae-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="bceae-127">-Role</span><span class="sxs-lookup"><span data-stu-id="bceae-127">-Role</span></span>
<span data-ttu-id="bceae-128">Die Liste der Rollen, die dem Prinzipal in der Umgebung zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="bceae-128">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bceae-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="bceae-129">-SubscriptionId</span></span>
<span data-ttu-id="bceae-130">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="bceae-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="bceae-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bceae-131">-Confirm</span></span>
<span data-ttu-id="bceae-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bceae-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bceae-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bceae-133">-WhatIf</span></span>
<span data-ttu-id="bceae-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bceae-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bceae-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bceae-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bceae-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bceae-136">CommonParameters</span></span>
<span data-ttu-id="bceae-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bceae-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bceae-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bceae-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bceae-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bceae-139">INPUTS</span></span>

### <span data-ttu-id="bceae-140">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="bceae-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="bceae-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bceae-141">OUTPUTS</span></span>

### <span data-ttu-id="bceae-142">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="bceae-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="bceae-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="bceae-143">NOTES</span></span>

<span data-ttu-id="bceae-144">Aliase</span><span class="sxs-lookup"><span data-stu-id="bceae-144">ALIASES</span></span>

<span data-ttu-id="bceae-145">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bceae-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bceae-146">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bceae-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bceae-147">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="bceae-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bceae-148">Inputobject <ITimeSeriesInsightsIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="bceae-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bceae-149">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="bceae-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="bceae-150">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="bceae-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="bceae-151">`[EventSourceName <String>]`: Der Name der Ereignisquelle für Zeitreihen Einblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bceae-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="bceae-152">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="bceae-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bceae-153">`[ReferenceDataSetName <String>]`: Name des referenzdatensatzes.</span><span class="sxs-lookup"><span data-stu-id="bceae-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="bceae-154">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bceae-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="bceae-155">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="bceae-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="bceae-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bceae-156">RELATED LINKS</span></span>

