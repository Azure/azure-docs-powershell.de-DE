---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: 33272012d81160a055bcd5d1eb0ef617787eed1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650814"
---
# <span data-ttu-id="5f0ff-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="5f0ff-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="5f0ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f0ff-102">SYNOPSIS</span></span>
<span data-ttu-id="5f0ff-103">Erstellt eine neue Kusto-Datenbank in einem vorhandenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-103">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="5f0ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f0ff-104">SYNTAX</span></span>

### <span data-ttu-id="5f0ff-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f0ff-105">ByNameAndResourceGroup (Default)</span></span>
```
New-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f0ff-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f0ff-106">ByResourceId</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f0ff-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5f0ff-107">ByInputObject</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-InputObject] <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f0ff-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f0ff-108">DESCRIPTION</span></span>
<span data-ttu-id="5f0ff-109">Erstellt eine neue Kusto-Datenbank in einem vorhandenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-109">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="5f0ff-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f0ff-110">EXAMPLES</span></span>

### <span data-ttu-id="5f0ff-111">Beispiel 1: Erstellen einer neuen Kusto-Datenbank nach Namen</span><span class="sxs-lookup"><span data-stu-id="5f0ff-111">Example 1 - Create a new Kusto database by name</span></span>

```
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 4 -HotCachePeriodInDays 2

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 4
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="5f0ff-112">Der obige Befehl erstellt eine neue Kusto-Datenbank mit dem Namen "mykustodatabase" im vorhandenen Cluster "mykustocluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-112">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="5f0ff-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f0ff-113">PARAMETERS</span></span>

### <span data-ttu-id="5f0ff-114">-Clustername</span><span class="sxs-lookup"><span data-stu-id="5f0ff-114">-ClusterName</span></span>
<span data-ttu-id="5f0ff-115">Name des Clusters, unter dem Sie die Datenbank erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-115">Name of cluster under which you want to create the database.</span></span>

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

### <span data-ttu-id="5f0ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f0ff-116">-DefaultProfile</span></span>
<span data-ttu-id="5f0ff-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f0ff-118">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="5f0ff-118">-HotCachePeriodInDays</span></span>
<span data-ttu-id="5f0ff-119">Die Anzahl der Tage der Daten, die im Cache für schnelle Abfragen aufbewahrt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-119">The number of days of data that should be kept in cache for fast queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0ff-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5f0ff-120">-InputObject</span></span>
<span data-ttu-id="5f0ff-121">Kusto-Clusterobjekt.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-121">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0ff-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5f0ff-122">-Name</span></span>
<span data-ttu-id="5f0ff-123">Der Name der zu erstellende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-123">Name of the database to be created.</span></span>

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

### <span data-ttu-id="5f0ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f0ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="5f0ff-125">Der Name der Ressourcengruppe, unter der der Cluster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="5f0ff-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5f0ff-126">-ResourceId</span></span>
<span data-ttu-id="5f0ff-127">Kusto-Cluster-Quell Code.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="5f0ff-128">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="5f0ff-128">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="5f0ff-129">Die Anzahl der Tage, die Daten aufbewahrt werden sollen, bevor Sie nicht mehr auf Abfragen zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-129">The number of days data should be kept before it stops being accessible to queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0ff-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5f0ff-130">-Confirm</span></span>
<span data-ttu-id="5f0ff-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f0ff-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f0ff-132">-WhatIf</span></span>
<span data-ttu-id="5f0ff-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f0ff-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f0ff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f0ff-135">CommonParameters</span></span>
<span data-ttu-id="5f0ff-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f0ff-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f0ff-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f0ff-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f0ff-138">INPUTS</span></span>

### <span data-ttu-id="5f0ff-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5f0ff-139">System.String</span></span>

### <span data-ttu-id="5f0ff-140">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="5f0ff-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="5f0ff-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f0ff-141">OUTPUTS</span></span>

### <span data-ttu-id="5f0ff-142">Microsoft. Azure. Commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="5f0ff-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="5f0ff-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f0ff-143">NOTES</span></span>

## <span data-ttu-id="5f0ff-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f0ff-144">RELATED LINKS</span></span>
