---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a68604e9701a6ae2c251edf3f2a0935df5ffa94f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650812"
---
# <span data-ttu-id="4da2f-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="4da2f-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="4da2f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4da2f-102">SYNOPSIS</span></span>
<span data-ttu-id="4da2f-103">Listen Sie alle Kusto-Cluster in einer Ressourcengruppe auf, oder rufen Sie einen bestimmten Kusto-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="4da2f-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="4da2f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4da2f-104">SYNTAX</span></span>

### <span data-ttu-id="4da2f-105">ByClusterOrResourceGroupOrSubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="4da2f-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4da2f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4da2f-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4da2f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4da2f-107">DESCRIPTION</span></span>
<span data-ttu-id="4da2f-108">Listen Sie alle Kusto-Cluster in einer Ressourcengruppe auf, oder rufen Sie einen bestimmten Kusto-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="4da2f-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="4da2f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4da2f-109">EXAMPLES</span></span>

### <span data-ttu-id="4da2f-110">Beispiel 1 – Auflisten aller Kusto-Cluster in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4da2f-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="4da2f-111">Geben Sie Folgendes ein: Microsoft. Kusto/Clusters ID:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/Providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup: testrg Name: mykustocluster1 Ort: zentrale US-Kapazität: 3 SKU: D13_v2 ProvisioningState: succeeded-Zustand: Running Tag: {} URI: https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster1.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="4da2f-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net</span></span>

<span data-ttu-id="4da2f-112">Geben Sie Folgendes ein: Microsoft. Kusto/Clusters ID:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/Providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup: testrg Name: mykustocluster2 Ort: zentrale US-Kapazität: 5 SKU: D13_v2 ProvisioningState: succeeded-Zustand: Running Tag: {} URI: https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster2.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="4da2f-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster2.centralus.kusto.windows.net</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="4da2f-113">Der obige Befehl listet alle Kusto-Cluster in der Ressourcengruppe "testrg" auf.</span><span class="sxs-lookup"><span data-stu-id="4da2f-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="4da2f-114">Beispiel 2: Abrufen eines bestimmten Kusto-Clusters anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="4da2f-114">Example 2 - Get a specific Kusto cluster by name</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="4da2f-115">Der obige Befehl gibt den Kusto-Cluster mit dem Namen "mykustocluster" in der Ressourcengruppe "testrg" zurück.</span><span class="sxs-lookup"><span data-stu-id="4da2f-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="4da2f-116">Beispiel 3: Abrufen eines bestimmten Kusto-Clusters nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4da2f-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/clusters/mykustocluster
Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="4da2f-117">Der obige Befehl gibt den Kusto-Cluster mit dem Namen "mykustocluster" in der Ressourcengruppe "testrg" zurück.</span><span class="sxs-lookup"><span data-stu-id="4da2f-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="4da2f-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="4da2f-118">PARAMETERS</span></span>

### <span data-ttu-id="4da2f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da2f-119">-DefaultProfile</span></span>
<span data-ttu-id="4da2f-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4da2f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4da2f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4da2f-121">-Name</span></span>
<span data-ttu-id="4da2f-122">Der Name eines bestimmten Clusters.</span><span class="sxs-lookup"><span data-stu-id="4da2f-122">Name of a specific cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4da2f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4da2f-123">-ResourceGroupName</span></span>
<span data-ttu-id="4da2f-124">Name der Ressourcengruppe, unter der der Benutzer den Cluster abrufen möchte.</span><span class="sxs-lookup"><span data-stu-id="4da2f-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

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

### <span data-ttu-id="4da2f-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4da2f-125">-ResourceId</span></span>
<span data-ttu-id="4da2f-126">Kusto-Cluster-Quell Code.</span><span class="sxs-lookup"><span data-stu-id="4da2f-126">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="4da2f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da2f-127">CommonParameters</span></span>
<span data-ttu-id="4da2f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4da2f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da2f-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4da2f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da2f-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4da2f-130">INPUTS</span></span>

### <span data-ttu-id="4da2f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4da2f-131">System.String</span></span>

## <span data-ttu-id="4da2f-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4da2f-132">OUTPUTS</span></span>

### <span data-ttu-id="4da2f-133">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="4da2f-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="4da2f-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="4da2f-134">NOTES</span></span>

## <span data-ttu-id="4da2f-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4da2f-135">RELATED LINKS</span></span>
