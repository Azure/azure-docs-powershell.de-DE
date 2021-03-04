---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: 624ca943d9adf7df105fae18a0a4a8ccad2b9b9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934643"
---
# <span data-ttu-id="93019-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="93019-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="93019-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93019-102">SYNOPSIS</span></span>
<span data-ttu-id="93019-103">Gibt Informationen zu Azure SQL virtuellen Cluster zurück.</span><span class="sxs-lookup"><span data-stu-id="93019-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="93019-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93019-104">SYNTAX</span></span>

### <span data-ttu-id="93019-105">GetVirtualClusterByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="93019-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93019-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="93019-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93019-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="93019-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93019-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93019-108">DESCRIPTION</span></span>
<span data-ttu-id="93019-109">Das **Get-AzSqlVirtualCluster-Cmdlet** gibt Informationen zu einem oder mehreren Azure SQL virtuellen Clustern zurück.</span><span class="sxs-lookup"><span data-stu-id="93019-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="93019-110">Geben Sie den Namen eines virtuellen Clusters an, um Informationen nur für diesen Cluster zu sehen.</span><span class="sxs-lookup"><span data-stu-id="93019-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="93019-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="93019-111">EXAMPLES</span></span>

### <span data-ttu-id="93019-112">Beispiel 1: Alle virtuellen Cluster, die einer Ressourcengruppe zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="93019-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
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

<span data-ttu-id="93019-113">Dieser Befehl ruft Informationen zu allen virtuellen Clustern ab, die der Ressourcengruppe ResourceGroup01 zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="93019-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="93019-114">Beispiel 2: Informationen zu bestimmten virtuellen Clustern</span><span class="sxs-lookup"><span data-stu-id="93019-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="93019-115">Dieser Befehl ruft Informationen zum virtuellen Cluster VirtualCluster1 in der Ressourcengruppe ResourceGroup01 ab.</span><span class="sxs-lookup"><span data-stu-id="93019-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="93019-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="93019-116">PARAMETERS</span></span>

### <span data-ttu-id="93019-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93019-117">-DefaultProfile</span></span>
<span data-ttu-id="93019-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93019-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93019-119">-Name</span><span class="sxs-lookup"><span data-stu-id="93019-119">-Name</span></span>
<span data-ttu-id="93019-120">Der Name des virtuellen Clusters.</span><span class="sxs-lookup"><span data-stu-id="93019-120">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="93019-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93019-121">-ResourceGroupName</span></span>
<span data-ttu-id="93019-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="93019-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="93019-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93019-123">-ResourceId</span></span>
<span data-ttu-id="93019-124">Die Ressourcen-ID des zu erhaltende Instanzobjekts</span><span class="sxs-lookup"><span data-stu-id="93019-124">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="93019-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93019-125">CommonParameters</span></span>
<span data-ttu-id="93019-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93019-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93019-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93019-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93019-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="93019-128">INPUTS</span></span>

### <span data-ttu-id="93019-129">Keine</span><span class="sxs-lookup"><span data-stu-id="93019-129">None</span></span>

## <span data-ttu-id="93019-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="93019-130">OUTPUTS</span></span>

### <span data-ttu-id="93019-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="93019-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="93019-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="93019-132">NOTES</span></span>

## <span data-ttu-id="93019-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="93019-133">RELATED LINKS</span></span>
