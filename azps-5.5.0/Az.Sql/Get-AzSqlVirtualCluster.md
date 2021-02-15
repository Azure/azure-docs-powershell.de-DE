---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: bd12fd2067c931f05266ed1ed24fb5666ead59a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145660"
---
# <span data-ttu-id="dba4b-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="dba4b-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="dba4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dba4b-102">SYNOPSIS</span></span>
<span data-ttu-id="dba4b-103">Gibt Informationen zum virtuellen Azure SQL Cluster zurück.</span><span class="sxs-lookup"><span data-stu-id="dba4b-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="dba4b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dba4b-104">SYNTAX</span></span>

### <span data-ttu-id="dba4b-105">GetVirtualClusterByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="dba4b-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dba4b-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dba4b-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dba4b-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="dba4b-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dba4b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dba4b-108">DESCRIPTION</span></span>
<span data-ttu-id="dba4b-109">Das **Cmdlet "Get-AzSqlVirtualCluster"** gibt Informationen zu einem oder mehreren virtuellen Clustern SQL Azure zurück.</span><span class="sxs-lookup"><span data-stu-id="dba4b-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="dba4b-110">Geben Sie den Namen eines virtuellen Cluster an, um nur Informationen für diesen Cluster zu sehen.</span><span class="sxs-lookup"><span data-stu-id="dba4b-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="dba4b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dba4b-111">EXAMPLES</span></span>

### <span data-ttu-id="dba4b-112">Beispiel 1: Alle virtuellen Cluster einer Ressourcengruppe zugewiesen bekommen</span><span class="sxs-lookup"><span data-stu-id="dba4b-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
```powershell
PS C:> Get-AzSqlVirtualCluster -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster2
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster2
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name2

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster3
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster3
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name3
```

<span data-ttu-id="dba4b-113">Dieser Befehl ruft Informationen zu allen virtuellen Clustern ab, die der Ressourcengruppe "ResourceGroup01" zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="dba4b-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="dba4b-114">Beispiel 2: Erhalten von Informationen zu einem bestimmten virtuellen Cluster</span><span class="sxs-lookup"><span data-stu-id="dba4b-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="dba4b-115">Dieser Befehl ruft Informationen über den virtuellen Cluster "VirtualCluster1" in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="dba4b-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="dba4b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dba4b-116">PARAMETERS</span></span>

### <span data-ttu-id="dba4b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba4b-117">-DefaultProfile</span></span>
<span data-ttu-id="dba4b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dba4b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dba4b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dba4b-119">-Name</span></span>
<span data-ttu-id="dba4b-120">Der Name des virtuellen Cluster.</span><span class="sxs-lookup"><span data-stu-id="dba4b-120">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dba4b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dba4b-121">-ResourceGroupName</span></span>
<span data-ttu-id="dba4b-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dba4b-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dba4b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dba4b-123">-ResourceId</span></span>
<span data-ttu-id="dba4b-124">Die Ressourcen-ID des zu erhaltende Instanzobjekts</span><span class="sxs-lookup"><span data-stu-id="dba4b-124">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dba4b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba4b-125">CommonParameters</span></span>
<span data-ttu-id="dba4b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dba4b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba4b-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dba4b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba4b-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dba4b-128">INPUTS</span></span>

### <span data-ttu-id="dba4b-129">Keine</span><span class="sxs-lookup"><span data-stu-id="dba4b-129">None</span></span>

## <span data-ttu-id="dba4b-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dba4b-130">OUTPUTS</span></span>

### <span data-ttu-id="dba4b-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="dba4b-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="dba4b-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dba4b-132">NOTES</span></span>

## <span data-ttu-id="dba4b-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dba4b-133">RELATED LINKS</span></span>
