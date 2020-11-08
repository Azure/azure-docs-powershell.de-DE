---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: bd12fd2067c931f05266ed1ed24fb5666ead59a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175868"
---
# <span data-ttu-id="f3274-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="f3274-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="f3274-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3274-102">SYNOPSIS</span></span>
<span data-ttu-id="f3274-103">Gibt Informationen zu Azure SQL Virtual Cluster zurück.</span><span class="sxs-lookup"><span data-stu-id="f3274-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="f3274-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3274-104">SYNTAX</span></span>

### <span data-ttu-id="f3274-105">GetVirtualClusterByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="f3274-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3274-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f3274-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3274-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3274-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3274-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3274-108">DESCRIPTION</span></span>
<span data-ttu-id="f3274-109">Das Cmdlet " **Get-AzSqlVirtualCluster** " gibt Informationen zu einem oder mehreren virtuellen Azure SQL-Clustern zurück.</span><span class="sxs-lookup"><span data-stu-id="f3274-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="f3274-110">Geben Sie den Namen eines virtuellen Clusters an, um Informationen nur für diesen Cluster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f3274-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="f3274-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3274-111">EXAMPLES</span></span>

### <span data-ttu-id="f3274-112">Beispiel 1: Abrufen aller virtuellen Cluster, die einer Ressourcengruppe zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="f3274-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
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

<span data-ttu-id="f3274-113">Dieser Befehl ruft Informationen zu allen virtuellen Clustern ab, die der Ressourcengruppe ResourceGroup01 zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f3274-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="f3274-114">Beispiel 2: Abrufen von Informationen zu einem bestimmten virtuellen Cluster</span><span class="sxs-lookup"><span data-stu-id="f3274-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="f3274-115">Dieser Befehl ruft Informationen zum virtuellen Cluster VirtualCluster1 in der Ressourcengruppe ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f3274-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="f3274-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3274-116">PARAMETERS</span></span>

### <span data-ttu-id="f3274-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3274-117">-DefaultProfile</span></span>
<span data-ttu-id="f3274-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3274-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3274-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f3274-119">-Name</span></span>
<span data-ttu-id="f3274-120">Der Name des virtuellen Clusters.</span><span class="sxs-lookup"><span data-stu-id="f3274-120">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="f3274-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3274-121">-ResourceGroupName</span></span>
<span data-ttu-id="f3274-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f3274-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="f3274-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f3274-123">-ResourceId</span></span>
<span data-ttu-id="f3274-124">Die Ressourcen-ID des abzurufenden Instanzen Objekts.</span><span class="sxs-lookup"><span data-stu-id="f3274-124">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="f3274-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3274-125">CommonParameters</span></span>
<span data-ttu-id="f3274-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3274-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3274-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3274-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3274-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3274-128">INPUTS</span></span>

### <span data-ttu-id="f3274-129">Keine</span><span class="sxs-lookup"><span data-stu-id="f3274-129">None</span></span>

## <span data-ttu-id="f3274-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3274-130">OUTPUTS</span></span>

### <span data-ttu-id="f3274-131">Microsoft. Azure. Commands. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="f3274-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="f3274-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3274-132">NOTES</span></span>

## <span data-ttu-id="f3274-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3274-133">RELATED LINKS</span></span>
