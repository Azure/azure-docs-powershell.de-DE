---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: 98936051ba3faa06d611fc8509faaa2b26998d29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650811"
---
# <span data-ttu-id="5d75f-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="5d75f-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="5d75f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d75f-102">SYNOPSIS</span></span>
<span data-ttu-id="5d75f-103">Listen Sie alle Kusto-Datenbanken in einem Cluster auf, oder rufen Sie eine bestimmte Kusto-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="5d75f-103">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="5d75f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d75f-104">SYNTAX</span></span>

### <span data-ttu-id="5d75f-105">ByClusterOrResourceGroupOrSubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d75f-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoDatabase -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d75f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5d75f-106">ByResourceId</span></span>
```
Get-AzKustoDatabase [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d75f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5d75f-107">ByInputObject</span></span>
```
Get-AzKustoDatabase [-Name <String>] -InputObject <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d75f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d75f-108">DESCRIPTION</span></span>
<span data-ttu-id="5d75f-109">Listen Sie alle Kusto-Datenbanken in einem Cluster auf, oder rufen Sie eine bestimmte Kusto-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="5d75f-109">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="5d75f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d75f-110">EXAMPLES</span></span>

### <span data-ttu-id="5d75f-111">Beispiel 1: Auflisten aller Kusto-Datenbanken in einem Cluster nach Name</span><span class="sxs-lookup"><span data-stu-id="5d75f-111">Example 1 - List all Kusto databases in a cluster by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster

Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="5d75f-112">Der obige Befehl gibt alle Kusto-Datenbanken im Cluster "mykustocluster" zurück, die in der Ressourcengruppe "testrg" gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="5d75f-112">The above command returns all Kusto databases in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="5d75f-113">Beispiel 2: Auflisten aller Kusto-Datenbanken in einem Cluster durch Piping</span><span class="sxs-lookup"><span data-stu-id="5d75f-113">Example 2 - List all Kusto databases in a cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Get-AzKustoDatabase
Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="5d75f-114">Der obige Befehl erhält den Kusto-Cluster mit dem Namen "mykustocluster", der in der Ressourcengruppe "testrg" mit dem Cmdlet gefunden wurde `Get-AzKustoCluster` , und leitet das Ergebnis an das `Get-AzKustoDatabase` Cmdlet weiter, um alle Datenbanken in diesem Cluster aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="5d75f-114">The above command will get the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and pipe the result to the `Get-AzKustoDatabase` cmdlet to list all databases in that cluster.</span></span>

### <span data-ttu-id="5d75f-115">Beispiel 3: Abrufen einer bestimmten Kusto-Datenbank nach Namen</span><span class="sxs-lookup"><span data-stu-id="5d75f-115">Example 3 - Get a specific Kusto database by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="5d75f-116">Der obige Befehl gibt die Kusto-Datenbank mit dem Namen "mykustodatabase" im Cluster "mykustocluster" zurück, die in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="5d75f-116">The above command returns the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="5d75f-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d75f-117">PARAMETERS</span></span>

### <span data-ttu-id="5d75f-118">-Clustername</span><span class="sxs-lookup"><span data-stu-id="5d75f-118">-ClusterName</span></span>
<span data-ttu-id="5d75f-119">Name des Clusters, unter dem die Datenbank vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5d75f-119">Name of cluster under which the database exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d75f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d75f-120">-DefaultProfile</span></span>
<span data-ttu-id="5d75f-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d75f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d75f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5d75f-122">-InputObject</span></span>
<span data-ttu-id="5d75f-123">Kusto-Clusterobjekt.</span><span class="sxs-lookup"><span data-stu-id="5d75f-123">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d75f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5d75f-124">-Name</span></span>
<span data-ttu-id="5d75f-125">der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5d75f-125">the name of the database.</span></span>

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

### <span data-ttu-id="5d75f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d75f-126">-ResourceGroupName</span></span>
<span data-ttu-id="5d75f-127">Name der Ressourcengruppe, unter der der Benutzer den Cluster abrufen möchte.</span><span class="sxs-lookup"><span data-stu-id="5d75f-127">Name of resource group under which the user wants to retrieve the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d75f-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5d75f-128">-ResourceId</span></span>
<span data-ttu-id="5d75f-129">Kusto-Cluster-Quell Code.</span><span class="sxs-lookup"><span data-stu-id="5d75f-129">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d75f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d75f-130">CommonParameters</span></span>
<span data-ttu-id="5d75f-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d75f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d75f-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d75f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d75f-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d75f-133">INPUTS</span></span>

### <span data-ttu-id="5d75f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5d75f-134">System.String</span></span>

### <span data-ttu-id="5d75f-135">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="5d75f-135">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="5d75f-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d75f-136">OUTPUTS</span></span>

### <span data-ttu-id="5d75f-137">Microsoft. Azure. Commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="5d75f-137">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="5d75f-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d75f-138">NOTES</span></span>

## <span data-ttu-id="5d75f-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d75f-139">RELATED LINKS</span></span>
