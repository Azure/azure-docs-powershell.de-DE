---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: c5c7cdffc8b329fdff426f48f60869ca6821f32d
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401350"
---
# <span data-ttu-id="38f17-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="38f17-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="38f17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38f17-102">SYNOPSIS</span></span>
<span data-ttu-id="38f17-103">Listen Sie alle "Kusto"-Cluster in einer Ressourcengruppe auf, oder erhalten Sie einen bestimmten Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="38f17-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="38f17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38f17-104">SYNTAX</span></span>

### <span data-ttu-id="38f17-105">ByClusterOrResourceGroupOrSubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="38f17-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="38f17-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="38f17-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38f17-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38f17-107">DESCRIPTION</span></span>
<span data-ttu-id="38f17-108">Listen Sie alle "Kusto"-Cluster in einer Ressourcengruppe auf, oder erhalten Sie einen bestimmten Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="38f17-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="38f17-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38f17-109">EXAMPLES</span></span>

### <span data-ttu-id="38f17-110">Beispiel 1: Auflisten aller Kusto-Cluster in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="38f17-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="38f17-111">Typ: Microsoft.Kusto/Cluster-ID: /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Cluster/mykustocluster1 ResourceGroup : testrg Name: mykustocluster1 Location: Central US Capacity : 3 SKU : D13_v2 ProvisioningState : Succeeded State : Running Tag : {} Uri : `https://mykustocluster1.centralus.kusto.windows.net` DataIngestionUri : `https://ingest-mykustocluster1.centralus.kusto.windows.net`</span><span class="sxs-lookup"><span data-stu-id="38f17-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : `https://mykustocluster1.centralus.kusto.windows.net` DataIngestionUri  : `https://ingest-mykustocluster1.centralus.kusto.windows.net`</span></span>

<span data-ttu-id="38f17-112">Typ: Microsoft.Kusto/Cluster-ID: /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Cluster/mykustocluster2 ResourceGroup : testrg Name: mykustocluster2 Location: Central US Capacity : 5 SKU : D13_v2 ProvisioningState : Succeeded State : Running Tag : {} Uri : `https://mykustocluster2.centralus.kusto.windows.net` DataIngestionUri : `https://ingest-mykustocluster2.centralus.kusto.windows.net`</span><span class="sxs-lookup"><span data-stu-id="38f17-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : `https://mykustocluster2.centralus.kusto.windows.net` DataIngestionUri  : `https://ingest-mykustocluster2.centralus.kusto.windows.net`</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="38f17-113">Der oben aufgeführte Befehl listet alle Kusto-Cluster in der Ressourcengruppe "testrg" auf.</span><span class="sxs-lookup"><span data-stu-id="38f17-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="38f17-114">Beispiel 2: Erhalten eines bestimmten Kusto-Clusters nach Name</span><span class="sxs-lookup"><span data-stu-id="38f17-114">Example 2 - Get a specific Kusto cluster by name</span></span>

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

<span data-ttu-id="38f17-115">Der oben aufgeführte Befehl gibt den Cluster "Kusto" mit dem Namen "mykustocluster" in der Ressourcengruppe "testrg" zurück.</span><span class="sxs-lookup"><span data-stu-id="38f17-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="38f17-116">Beispiel 3: Erhalten eines bestimmten Kusto-Clusters nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="38f17-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

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

<span data-ttu-id="38f17-117">Der oben aufgeführte Befehl gibt den Cluster "Kusto" mit dem Namen "mykustocluster" in der Ressourcengruppe "testrg" zurück.</span><span class="sxs-lookup"><span data-stu-id="38f17-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="38f17-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38f17-118">PARAMETERS</span></span>

### <span data-ttu-id="38f17-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f17-119">-DefaultProfile</span></span>
<span data-ttu-id="38f17-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38f17-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38f17-121">-Name</span><span class="sxs-lookup"><span data-stu-id="38f17-121">-Name</span></span>
<span data-ttu-id="38f17-122">Name eines bestimmten Cluster.</span><span class="sxs-lookup"><span data-stu-id="38f17-122">Name of a specific cluster.</span></span>

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

### <span data-ttu-id="38f17-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38f17-123">-ResourceGroupName</span></span>
<span data-ttu-id="38f17-124">Name der Ressourcengruppe, unter der der Benutzer den Cluster abrufen möchte.</span><span class="sxs-lookup"><span data-stu-id="38f17-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

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

### <span data-ttu-id="38f17-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38f17-125">-ResourceId</span></span>
<span data-ttu-id="38f17-126">Ressourcen-ID des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="38f17-126">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="38f17-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f17-127">CommonParameters</span></span>
<span data-ttu-id="38f17-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f17-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f17-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38f17-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f17-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38f17-130">INPUTS</span></span>

### <span data-ttu-id="38f17-131">System.String</span><span class="sxs-lookup"><span data-stu-id="38f17-131">System.String</span></span>

## <span data-ttu-id="38f17-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38f17-132">OUTPUTS</span></span>

### <span data-ttu-id="38f17-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="38f17-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="38f17-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="38f17-134">NOTES</span></span>

## <span data-ttu-id="38f17-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="38f17-135">RELATED LINKS</span></span>
