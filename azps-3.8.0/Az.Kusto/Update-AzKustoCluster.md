---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 0b5e066255a0757c7aaafb6aee6c4ca37d03c7fa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995819"
---
# <span data-ttu-id="815c2-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="815c2-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="815c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="815c2-102">SYNOPSIS</span></span>
<span data-ttu-id="815c2-103">Aktualisieren eines vorhandenen Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="815c2-103">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="815c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="815c2-104">SYNTAX</span></span>

### <span data-ttu-id="815c2-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="815c2-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>] [-Capacity <Int32>]
 [-Tier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="815c2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="815c2-106">ByResourceId</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="815c2-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="815c2-107">ByInputObject</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-InputObject] <PSKustoCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="815c2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="815c2-108">DESCRIPTION</span></span>
<span data-ttu-id="815c2-109">Aktualisieren eines vorhandenen Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="815c2-109">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="815c2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="815c2-110">EXAMPLES</span></span>

### <span data-ttu-id="815c2-111">Beispiel 1 – Aktualisieren eines vorhandenen Clusters anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="815c2-111">Example 1 - Update an existing cluster by name</span></span>

```
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Sku D14_v2

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Sku               : D14_v2
Capacity          : 5
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="815c2-112">Der obige Befehl aktualisiert die Ebene des Kusto-Clusters "mykustocluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="815c2-112">The above command updates the tier of the Kusto cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="815c2-113">Beispiel 2 – Aktualisieren eines vorhandenen Clusters durch Piping</span><span class="sxs-lookup"><span data-stu-id="815c2-113">Example 2 - Update an existing cluster by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Update-AzKustoCluster -Sku D14_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D14_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="815c2-114">Der obige Befehl ruft den Kusto-Cluster "mykustocluster" ab, der in der Ressourcengruppe "testrg" mit dem Cmdlet gefunden wird `Get-AzKustoCluster` , und leitet dann das Ergebnis an, um `Update-AzKustoCluster` die Ebene des Clusters auf "Standard" zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="815c2-114">The above command gets the Kusto cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Update-AzKustoCluster` to update the cluster's tier to "standard".</span></span>

## <span data-ttu-id="815c2-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="815c2-115">PARAMETERS</span></span>

### <span data-ttu-id="815c2-116">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="815c2-116">-Capacity</span></span>
<span data-ttu-id="815c2-117">Die Instanznummer des VM.</span><span class="sxs-lookup"><span data-stu-id="815c2-117">The instance number of the VM.</span></span>

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

### <span data-ttu-id="815c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="815c2-118">-DefaultProfile</span></span>
<span data-ttu-id="815c2-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="815c2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="815c2-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="815c2-120">-InputObject</span></span>
<span data-ttu-id="815c2-121">Kusto-Clusterobjekt.</span><span class="sxs-lookup"><span data-stu-id="815c2-121">Kusto cluster object.</span></span>

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

### <span data-ttu-id="815c2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="815c2-122">-Name</span></span>
<span data-ttu-id="815c2-123">Der Name des Clusters, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="815c2-123">Name of cluster to be updated.</span></span>

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

### <span data-ttu-id="815c2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="815c2-124">-ResourceGroupName</span></span>
<span data-ttu-id="815c2-125">Der Name der Ressourcengruppe, unter der der Cluster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="815c2-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="815c2-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="815c2-126">-ResourceId</span></span>
<span data-ttu-id="815c2-127">Kusto-Cluster-Quell Code.</span><span class="sxs-lookup"><span data-stu-id="815c2-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="815c2-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="815c2-128">-SkuName</span></span>
<span data-ttu-id="815c2-129">Name der SKU, die zum Erstellen des Clusters verwendet wird</span><span class="sxs-lookup"><span data-stu-id="815c2-129">Name of the Sku used to create the cluster</span></span>

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

### <span data-ttu-id="815c2-130">-Tier</span><span class="sxs-lookup"><span data-stu-id="815c2-130">-Tier</span></span>
<span data-ttu-id="815c2-131">Name der zum Erstellen des Clusters verwendeten Ebene</span><span class="sxs-lookup"><span data-stu-id="815c2-131">Name of the Tier used to create the cluster</span></span>

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

### <span data-ttu-id="815c2-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="815c2-132">-Confirm</span></span>
<span data-ttu-id="815c2-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="815c2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="815c2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="815c2-134">-WhatIf</span></span>
<span data-ttu-id="815c2-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="815c2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="815c2-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="815c2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="815c2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="815c2-137">CommonParameters</span></span>
<span data-ttu-id="815c2-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="815c2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="815c2-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="815c2-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="815c2-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="815c2-140">INPUTS</span></span>

### <span data-ttu-id="815c2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="815c2-141">System.String</span></span>

### <span data-ttu-id="815c2-142">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="815c2-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="815c2-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="815c2-143">OUTPUTS</span></span>

### <span data-ttu-id="815c2-144">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="815c2-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="815c2-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="815c2-145">NOTES</span></span>

## <span data-ttu-id="815c2-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="815c2-146">RELATED LINKS</span></span>
