---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: 05d01d776f03ec3bbfe4e9bf6bd438ba8f002afb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819428"
---
# <span data-ttu-id="f7165-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="f7165-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="f7165-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7165-102">SYNOPSIS</span></span>
<span data-ttu-id="f7165-103">Aktualisieren einer vorhandenen Kusto-Datenbank</span><span class="sxs-lookup"><span data-stu-id="f7165-103">Update an existing Kusto database.</span></span>

## <span data-ttu-id="f7165-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7165-104">SYNTAX</span></span>

### <span data-ttu-id="f7165-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="f7165-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7165-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f7165-106">ByResourceId</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7165-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f7165-107">ByInputObject</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>]
 [-InputObject] <PSKustoDatabase> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7165-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7165-108">DESCRIPTION</span></span>
<span data-ttu-id="f7165-109">Aktualisieren einer vorhandenen Kusto-Datenbank</span><span class="sxs-lookup"><span data-stu-id="f7165-109">Update an existing Kusto database.</span></span>

## <span data-ttu-id="f7165-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7165-110">EXAMPLES</span></span>

### <span data-ttu-id="f7165-111">Beispiel 1 – Aktualisieren einer vorhandenen Datenbank nach Namen</span><span class="sxs-lookup"><span data-stu-id="f7165-111">Example 1 - Update an existing database by name</span></span>

```
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="f7165-112">Der obige Befehl aktualisiert den Soft-Deletion-Zeitraum der Kusto-Datenbank "mykustodatabase" im Cluster "mykustocluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="f7165-112">The above command updates the soft deletion period of the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="f7165-113">Beispiel 2 – Aktualisieren einer vorhandenen Datenbank durch Piping</span><span class="sxs-lookup"><span data-stu-id="f7165-113">Example 2 - Update an existing database by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Update-AzKustoDatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="f7165-114">Der obige Befehl ruft die Kusto-Datenbank "mykustodatabase" im Cluster "mykustocluster" ab, die in der Ressourcengruppe "testrg" mithilfe des `Get-AzKustoDatabase` Cmdlets gefunden wird, und führt dann das Ergebnis aus, um `Update-AzKustoDatabase` den Soft-Deletion-Zeitraum der Datenbank auf fünf Tage zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f7165-114">The above command gets the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Update-AzKustoDatabase` to update the database's soft deletion period to five days.</span></span>

## <span data-ttu-id="f7165-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7165-115">PARAMETERS</span></span>

### <span data-ttu-id="f7165-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="f7165-116">-ClusterName</span></span>
<span data-ttu-id="f7165-117">Name des Clusters, unter dem die Datenbank vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="f7165-117">Name of cluster under which the database exists</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7165-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7165-118">-DefaultProfile</span></span>
<span data-ttu-id="f7165-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7165-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7165-120">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="f7165-120">-HotCachePeriodInDays</span></span>
<span data-ttu-id="f7165-121">Die Anzahl der Tage, die Daten im Cache für schnelle Abfragen aufbewahrt werden sollten</span><span class="sxs-lookup"><span data-stu-id="f7165-121">The number of days that data should be kept in cache for fast queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7165-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f7165-122">-InputObject</span></span>
<span data-ttu-id="f7165-123">Kusto-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="f7165-123">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7165-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f7165-124">-Name</span></span>
<span data-ttu-id="f7165-125">Name der zu aktualisierende Datenbank</span><span class="sxs-lookup"><span data-stu-id="f7165-125">Name of the database to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7165-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7165-126">-ResourceGroupName</span></span>
<span data-ttu-id="f7165-127">Der Name der Ressourcengruppe, unter der der Cluster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f7165-127">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7165-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f7165-128">-ResourceId</span></span>
<span data-ttu-id="f7165-129">Kusto-Datenbank-Quell Code.</span><span class="sxs-lookup"><span data-stu-id="f7165-129">Kusto database ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7165-130">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="f7165-130">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="f7165-131">Die Anzahl von Tagen, die Daten aufbewahrt werden sollen, bevor Sie nicht mehr auf Abfragen zugreifen können</span><span class="sxs-lookup"><span data-stu-id="f7165-131">The number of days that data should be kept before it stops being accessible to queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7165-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f7165-132">-Confirm</span></span>
<span data-ttu-id="f7165-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7165-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7165-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7165-134">-WhatIf</span></span>
<span data-ttu-id="f7165-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7165-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7165-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7165-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7165-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7165-137">CommonParameters</span></span>
<span data-ttu-id="f7165-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7165-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7165-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7165-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7165-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7165-140">INPUTS</span></span>

### <span data-ttu-id="f7165-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f7165-141">System.String</span></span>

### <span data-ttu-id="f7165-142">Microsoft. Azure. Commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="f7165-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="f7165-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7165-143">OUTPUTS</span></span>

### <span data-ttu-id="f7165-144">Microsoft. Azure. Commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="f7165-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="f7165-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7165-145">NOTES</span></span>

## <span data-ttu-id="f7165-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7165-146">RELATED LINKS</span></span>
