---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 39bbdf61a5068ea32f1febf66249213264235dfc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173357"
---
# <span data-ttu-id="d078a-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="d078a-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="d078a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d078a-102">SYNOPSIS</span></span>
<span data-ttu-id="d078a-103">Erstellen oder Aktualisieren eines referenzdatensatzes in der angegebenen Umgebung</span><span class="sxs-lookup"><span data-stu-id="d078a-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="d078a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d078a-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d078a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d078a-105">DESCRIPTION</span></span>
<span data-ttu-id="d078a-106">Erstellen oder Aktualisieren eines referenzdatensatzes in der angegebenen Umgebung</span><span class="sxs-lookup"><span data-stu-id="d078a-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="d078a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d078a-107">EXAMPLES</span></span>

### <span data-ttu-id="d078a-108">Beispiel 1: Erstellen eines referenzdatensatzes für eine bestimmte Umgebung</span><span class="sxs-lookup"><span data-stu-id="d078a-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="d078a-109">Dieser Befehl erstellt einen Verweisdaten Satz für eine bestimmte Umgebung.</span><span class="sxs-lookup"><span data-stu-id="d078a-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="d078a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d078a-110">PARAMETERS</span></span>

### <span data-ttu-id="d078a-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="d078a-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="d078a-112">Das Vergleichsverhalten des referenzdatensatzes kann mithilfe dieser Eigenschaft eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d078a-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="d078a-113">Standardmäßig ist der Wert "Ordinal", was bedeutet, dass der Vergleich der Groß-/Kleinschreibung beim Verknüpfen von Referenzdaten mit Ereignissen oder beim Hinzufügen neuer Referenzdaten erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d078a-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="d078a-114">Wenn "OrdinalIgnoreCase" gesetzt ist, wird der Vergleich der Groß-/Kleinschreibung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d078a-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.DataStringComparisonBehavior
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d078a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d078a-115">-DefaultProfile</span></span>
<span data-ttu-id="d078a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d078a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d078a-117">-Umgebungsname</span><span class="sxs-lookup"><span data-stu-id="d078a-117">-EnvironmentName</span></span>
<span data-ttu-id="d078a-118">Der Name der Zeitreihen Einblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d078a-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d078a-119">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="d078a-119">-KeyProperty</span></span>
<span data-ttu-id="d078a-120">Die Liste der Schlüsseleigenschaften für den Verweisdaten Satz.</span><span class="sxs-lookup"><span data-stu-id="d078a-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="d078a-121">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Eigenschaften von keyProperty und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d078a-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetKeyProperty[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d078a-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="d078a-122">-Location</span></span>
<span data-ttu-id="d078a-123">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="d078a-123">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d078a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d078a-124">-Name</span></span>
<span data-ttu-id="d078a-125">Der Name des referenzdatensatzes.</span><span class="sxs-lookup"><span data-stu-id="d078a-125">Name of the reference data set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d078a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d078a-126">-ResourceGroupName</span></span>
<span data-ttu-id="d078a-127">Der Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d078a-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d078a-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d078a-128">-SubscriptionId</span></span>
<span data-ttu-id="d078a-129">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="d078a-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d078a-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="d078a-130">-Tag</span></span>
<span data-ttu-id="d078a-131">Schlüssel-Wert-Paare zusätzlicher Eigenschaften für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="d078a-131">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="d078a-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d078a-132">-Confirm</span></span>
<span data-ttu-id="d078a-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d078a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d078a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d078a-134">-WhatIf</span></span>
<span data-ttu-id="d078a-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d078a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d078a-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d078a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d078a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d078a-137">CommonParameters</span></span>
<span data-ttu-id="d078a-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d078a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d078a-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d078a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d078a-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d078a-140">INPUTS</span></span>

## <span data-ttu-id="d078a-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d078a-141">OUTPUTS</span></span>

### <span data-ttu-id="d078a-142">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="d078a-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="d078a-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="d078a-143">NOTES</span></span>

<span data-ttu-id="d078a-144">Aliase</span><span class="sxs-lookup"><span data-stu-id="d078a-144">ALIASES</span></span>

<span data-ttu-id="d078a-145">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d078a-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d078a-146">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d078a-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d078a-147">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="d078a-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d078a-148">KeyProperty <IReferenceDataSetKeyProperty [] >: die Liste der Schlüsseleigenschaften für den Verweisdaten Satz.</span><span class="sxs-lookup"><span data-stu-id="d078a-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="d078a-149">`[Name <String>]`: Der Name der Schlüsseleigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d078a-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="d078a-150">`[Type <ReferenceDataKeyPropertyType?>]`: Der Typ der Schlüsseleigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d078a-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="d078a-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d078a-151">RELATED LINKS</span></span>

