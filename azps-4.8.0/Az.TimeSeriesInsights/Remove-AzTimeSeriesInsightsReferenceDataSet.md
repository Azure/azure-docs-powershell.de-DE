---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 56173c8ca384c817912395a536583fb26e9dfa76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165420"
---
# <span data-ttu-id="81970-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="81970-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="81970-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81970-102">SYNOPSIS</span></span>
<span data-ttu-id="81970-103">Löscht den Verweisdaten Satz mit dem angegebenen Namen im angegebenen Abonnement, in der Ressourcengruppe und in der Umgebung.</span><span class="sxs-lookup"><span data-stu-id="81970-103">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="81970-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81970-104">SYNTAX</span></span>

### <span data-ttu-id="81970-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="81970-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="81970-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="81970-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="81970-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81970-107">DESCRIPTION</span></span>
<span data-ttu-id="81970-108">Löscht den Verweisdaten Satz mit dem angegebenen Namen im angegebenen Abonnement, in der Ressourcengruppe und in der Umgebung.</span><span class="sxs-lookup"><span data-stu-id="81970-108">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="81970-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81970-109">EXAMPLES</span></span>

### <span data-ttu-id="81970-110">Beispiel 1: Entfernen eines angegebenen Verweisdaten Satzes nach Name</span><span class="sxs-lookup"><span data-stu-id="81970-110">Example 1: Remove a specified reference data set by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup

```

<span data-ttu-id="81970-111">Mit diesem Befehl wird ein angegebener Verweisdaten Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="81970-111">This command removes a specified reference data set.</span></span>

### <span data-ttu-id="81970-112">Beispiel 2: Entfernen einer angegebenen Verweisdaten Gruppe nach Objekt</span><span class="sxs-lookup"><span data-stu-id="81970-112">Example 2: Remove a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

```

<span data-ttu-id="81970-113">Mit diesem Befehl wird ein angegebener Verweisdaten Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="81970-113">This command removes a specified reference data set.</span></span>

## <span data-ttu-id="81970-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="81970-114">PARAMETERS</span></span>

### <span data-ttu-id="81970-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81970-115">-DefaultProfile</span></span>
<span data-ttu-id="81970-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81970-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81970-117">-Umgebungsname</span><span class="sxs-lookup"><span data-stu-id="81970-117">-EnvironmentName</span></span>
<span data-ttu-id="81970-118">Der Name der Zeitreihen Einblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="81970-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="81970-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="81970-119">-InputObject</span></span>
<span data-ttu-id="81970-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="81970-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="81970-121">-Name</span><span class="sxs-lookup"><span data-stu-id="81970-121">-Name</span></span>
<span data-ttu-id="81970-122">Der Name der Zeitreihen Einblicke-Referenzdatensatz, der der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="81970-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81970-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81970-123">-PassThru</span></span>
<span data-ttu-id="81970-124">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="81970-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="81970-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81970-125">-ResourceGroupName</span></span>
<span data-ttu-id="81970-126">Der Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="81970-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="81970-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="81970-127">-SubscriptionId</span></span>
<span data-ttu-id="81970-128">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="81970-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="81970-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="81970-129">-Confirm</span></span>
<span data-ttu-id="81970-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="81970-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81970-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81970-131">-WhatIf</span></span>
<span data-ttu-id="81970-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="81970-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81970-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="81970-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81970-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81970-134">CommonParameters</span></span>
<span data-ttu-id="81970-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81970-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81970-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81970-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81970-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81970-137">INPUTS</span></span>

### <span data-ttu-id="81970-138">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="81970-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="81970-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81970-139">OUTPUTS</span></span>

### <span data-ttu-id="81970-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="81970-140">System.Boolean</span></span>

## <span data-ttu-id="81970-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="81970-141">NOTES</span></span>

<span data-ttu-id="81970-142">Aliase</span><span class="sxs-lookup"><span data-stu-id="81970-142">ALIASES</span></span>

<span data-ttu-id="81970-143">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81970-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="81970-144">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="81970-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="81970-145">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="81970-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="81970-146">Inputobject <ITimeSeriesInsightsIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="81970-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="81970-147">`[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="81970-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="81970-148">`[EnvironmentName <String>]`: Name der Umgebung</span><span class="sxs-lookup"><span data-stu-id="81970-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="81970-149">`[EventSourceName <String>]`: Der Name der Ereignisquelle für Zeitreihen Einblicke, die der angegebenen Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="81970-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="81970-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="81970-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="81970-151">`[ReferenceDataSetName <String>]`: Name des referenzdatensatzes.</span><span class="sxs-lookup"><span data-stu-id="81970-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="81970-152">`[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="81970-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="81970-153">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="81970-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="81970-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81970-154">RELATED LINKS</span></span>

