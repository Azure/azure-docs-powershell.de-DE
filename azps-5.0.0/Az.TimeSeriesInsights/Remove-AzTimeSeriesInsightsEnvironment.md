---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 8b56475d2510099b7873fa444a0dc78497aeb729
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179948"
---
# <span data-ttu-id="ee16a-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="ee16a-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="ee16a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ee16a-102">SYNOPSIS</span></span>
<span data-ttu-id="ee16a-103">Löscht die Umgebung mit dem angegebenen Namen in der angegebenen Abonnement-und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ee16a-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="ee16a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee16a-104">SYNTAX</span></span>

### <span data-ttu-id="ee16a-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="ee16a-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ee16a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ee16a-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ee16a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee16a-107">DESCRIPTION</span></span>
<span data-ttu-id="ee16a-108">Löscht die Umgebung mit dem angegebenen Namen in der angegebenen Abonnement-und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ee16a-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="ee16a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee16a-109">EXAMPLES</span></span>

### <span data-ttu-id="ee16a-110">Beispiel 1: Entfernen einer Zeitreihen Einblicke-Umgebung nach Namen</span><span class="sxs-lookup"><span data-stu-id="ee16a-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="ee16a-111">Mit diesem Befehl wird eine Zeitreihen Einblicke-Umgebung entfernt.</span><span class="sxs-lookup"><span data-stu-id="ee16a-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="ee16a-112">Beispiel 2: Entfernen einer Zeitreihen Einblicke-Umgebung nach Objekt</span><span class="sxs-lookup"><span data-stu-id="ee16a-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="ee16a-113">Mit diesem Befehl wird eine Zeitreihen Einblicke-Umgebung entfernt.</span><span class="sxs-lookup"><span data-stu-id="ee16a-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="ee16a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee16a-114">PARAMETERS</span></span>

### <span data-ttu-id="ee16a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee16a-115">-DefaultProfile</span></span>
<span data-ttu-id="ee16a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ee16a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee16a-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ee16a-117">-InputObject</span></span>
<span data-ttu-id="ee16a-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ee16a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ee16a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ee16a-119">-Name</span></span>
<span data-ttu-id="ee16a-120">Der Name der Zeitreihen Einblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ee16a-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="ee16a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee16a-121">-PassThru</span></span>
<span data-ttu-id="ee16a-122">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="ee16a-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ee16a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee16a-123">-ResourceGroupName</span></span>
<span data-ttu-id="ee16a-124">Der Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ee16a-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="ee16a-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="ee16a-125">-SubscriptionId</span></span>
<span data-ttu-id="ee16a-126">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="ee16a-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="ee16a-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ee16a-127">-Confirm</span></span>
<span data-ttu-id="ee16a-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ee16a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee16a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee16a-129">-WhatIf</span></span>
<span data-ttu-id="ee16a-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ee16a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee16a-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee16a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee16a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee16a-132">CommonParameters</span></span>
<span data-ttu-id="ee16a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee16a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee16a-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee16a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee16a-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ee16a-135">INPUTS</span></span>

### <span data-ttu-id="ee16a-136">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="ee16a-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="ee16a-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ee16a-137">OUTPUTS</span></span>

### <span data-ttu-id="ee16a-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ee16a-138">System.Boolean</span></span>

## <span data-ttu-id="ee16a-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="ee16a-139">NOTES</span></span>

<span data-ttu-id="ee16a-140">Aliase</span><span class="sxs-lookup"><span data-stu-id="ee16a-140">ALIASES</span></span>

<span data-ttu-id="ee16a-141">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee16a-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ee16a-142">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ee16a-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ee16a-143">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="ee16a-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ee16a-144">Inputobject <ITimeSeriesInsightsIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="ee16a-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ee16a-145">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="ee16a-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="ee16a-146">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="ee16a-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="ee16a-147">`[EventSourceName <String>]`: Der Name der Ereignisquelle für Zeitreihen Einblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ee16a-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="ee16a-148">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="ee16a-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ee16a-149">`[ReferenceDataSetName <String>]`: Name des referenzdatensatzes.</span><span class="sxs-lookup"><span data-stu-id="ee16a-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="ee16a-150">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ee16a-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="ee16a-151">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="ee16a-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="ee16a-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ee16a-152">RELATED LINKS</span></span>

