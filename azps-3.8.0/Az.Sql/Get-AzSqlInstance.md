---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
ms.openlocfilehash: 8758cc8045856f66799144200c173ac766d8cbdb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003906"
---
# <span data-ttu-id="83084-101">Get-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="83084-101">Get-AzSqlInstance</span></span>

## <span data-ttu-id="83084-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83084-102">SYNOPSIS</span></span>
<span data-ttu-id="83084-103">Gibt Informationen zu Azure SQL-Datenbankinstanz zurück.</span><span class="sxs-lookup"><span data-stu-id="83084-103">Returns information about Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="83084-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83084-104">SYNTAX</span></span>

### <span data-ttu-id="83084-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="83084-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstance [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83084-106">ListByInstancePoolObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83084-106">ListByInstancePoolObjectParameterSet</span></span>
```
Get-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83084-107">ListByInstancePoolResourceIdentiferParameterSet</span><span class="sxs-lookup"><span data-stu-id="83084-107">ListByInstancePoolResourceIdentiferParameterSet</span></span>
```
Get-AzSqlInstance [-InstancePoolResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83084-108">GetByManagedInstanceResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="83084-108">GetByManagedInstanceResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstance [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83084-109">ListByInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="83084-109">ListByInstancePoolParameterSet</span></span>
```
Get-AzSqlInstance [-InstancePoolName] <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83084-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83084-110">DESCRIPTION</span></span>
<span data-ttu-id="83084-111">Das Cmdlet " **Get-AzSqlInstance** " gibt Informationen zu mindestens einem Azure SQL-verwalteten Instanzen zurück.</span><span class="sxs-lookup"><span data-stu-id="83084-111">The **Get-AzSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="83084-112">Geben Sie den Namen einer Instanz an, um Informationen nur für diese Instanz anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="83084-112">Specify the name of an instance to see information for only that instance.</span></span>

## <span data-ttu-id="83084-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83084-113">EXAMPLES</span></span>

### <span data-ttu-id="83084-114">Beispiel 1: Abrufen aller Instanzen, die einer Ressourcengruppe zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="83084-114">Example 1: Get all instances assigned to a resource group</span></span>
```powershell
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
```

<span data-ttu-id="83084-115">Dieser Befehl ruft Informationen zu allen Instanzen ab, die der Ressourcengruppe ResourceGroup01 zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="83084-115">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="83084-116">Beispiel 2: Abrufen von Informationen zu einer Instanz</span><span class="sxs-lookup"><span data-stu-id="83084-116">Example 2: Get information about an  instance</span></span>
```powershell
PS C:\> Get-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
```

<span data-ttu-id="83084-117">Dieser Befehl ruft Informationen zur Instanz mit dem Namen managedInstance1 ab.</span><span class="sxs-lookup"><span data-stu-id="83084-117">This command gets information about the instance named managedInstance1.</span></span>

### <span data-ttu-id="83084-118">Beispiel 3: Abrufen aller Instanzen, die einer Ressourcengruppe zugeordnet sind, mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="83084-118">Example 3: Get all instances assigned to a resource group using filtering</span></span>
```powershell
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "managedInstance*"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
```

<span data-ttu-id="83084-119">Dieser Befehl ruft Informationen zu allen Instanzen ab, die der Ressourcengruppen-ResourceGroup01 zugeordnet sind, die mit "managedInstance" beginnen.</span><span class="sxs-lookup"><span data-stu-id="83084-119">This command gets information about all instances assigned to the resource group ResourceGroup01 that start with "managedInstance".</span></span>

### <span data-ttu-id="83084-120">Beispiel 4: Abrufen aller Instanzen innerhalb eines Instanzen Pools</span><span class="sxs-lookup"><span data-stu-id="83084-120">Example 4: Get all instances within an instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstancePoolName "instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="83084-121">Dieser Befehl ruft Informationen zu allen Instanzen innerhalb des Instanz Pools "instancePool0" ab.</span><span class="sxs-lookup"><span data-stu-id="83084-121">This command gets information about all instances within the instance pool "instancePool0".</span></span>

### <span data-ttu-id="83084-122">Beispiel 5: Abrufen aller Instanzen innerhalb eines Instanzen Pools mit dem Instanz Pool Objekt</span><span class="sxs-lookup"><span data-stu-id="83084-122">Example 5: Get all instances within an instance pool using instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName "ResourceGroup01" -Name "instancePool0"
PS C:\> Get-AzSqlInstance -InstancePool $instancePool
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="83084-123">Dieser Befehl ruft Informationen zu allen Instanzen innerhalb des Instanz Pools "instancePool0" ab.</span><span class="sxs-lookup"><span data-stu-id="83084-123">This command gets information about all instances within the instance pool "instancePool0".</span></span>

### <span data-ttu-id="83084-124">Beispiel 6: Abrufen aller Instanzen innerhalb eines Instanzen Pools unter Verwendung des Ressourcenbezeichners des Instanz Pools</span><span class="sxs-lookup"><span data-stu-id="83084-124">Example 6: Get all instances within an instance pool using instance pool resource identifier</span></span>
```powershell
PS C:\> Get-AzSqlInstance -InstancePoolResourceIdentifier "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="83084-125">Dieser Befehl ruft Informationen zu allen Instanzen innerhalb des Instanz Pools "instancePool0" ab.</span><span class="sxs-lookup"><span data-stu-id="83084-125">This command gets information about all instances within the instance pool "instancePool0".</span></span>

### <span data-ttu-id="83084-126">Beispiel 7: Abrufen einer verwalteten Instanz mithilfe Ihres Ressourcenbezeichners</span><span class="sxs-lookup"><span data-stu-id="83084-126">Example 7: Get a managed instance using its resource identifier</span></span>
```powershell
PS C:\> Get-AzSqlInstance -ResourceIdentifier "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="83084-127">Dieser Befehl ruft Informationen zur Instanz mit dem Namen managedInstance1 ab.</span><span class="sxs-lookup"><span data-stu-id="83084-127">This command gets information about the instance named managedInstance1.</span></span>

## <span data-ttu-id="83084-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="83084-128">PARAMETERS</span></span>

### <span data-ttu-id="83084-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83084-129">-DefaultProfile</span></span>
<span data-ttu-id="83084-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83084-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83084-131">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="83084-131">-InstancePool</span></span>
<span data-ttu-id="83084-132">Das übergeordnete Objekt des Instanzen Pools.</span><span class="sxs-lookup"><span data-stu-id="83084-132">The instance pool parent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: ListByInstancePoolObjectParameterSet
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83084-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="83084-133">-InstancePoolName</span></span>
<span data-ttu-id="83084-134">Der Name des Instanzen Pools.</span><span class="sxs-lookup"><span data-stu-id="83084-134">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83084-135">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="83084-135">-InstancePoolResourceId</span></span>
<span data-ttu-id="83084-136">Der Ressourcenbezeichner des Instanz Pools.</span><span class="sxs-lookup"><span data-stu-id="83084-136">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolResourceIdentiferParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83084-137">-Name</span><span class="sxs-lookup"><span data-stu-id="83084-137">-Name</span></span>
<span data-ttu-id="83084-138">SQL-Instanzenname</span><span class="sxs-lookup"><span data-stu-id="83084-138">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: InstanceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83084-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83084-139">-ResourceGroupName</span></span>
<span data-ttu-id="83084-140">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="83084-140">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83084-141">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="83084-141">-ResourceId</span></span>
<span data-ttu-id="83084-142">Der Ressourcenbezeichner für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="83084-142">The managed instance resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByManagedInstanceResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83084-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83084-143">CommonParameters</span></span>
<span data-ttu-id="83084-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83084-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83084-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83084-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83084-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83084-146">INPUTS</span></span>

### <span data-ttu-id="83084-147">Keine</span><span class="sxs-lookup"><span data-stu-id="83084-147">None</span></span>

## <span data-ttu-id="83084-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83084-148">OUTPUTS</span></span>

### <span data-ttu-id="83084-149">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="83084-149">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="83084-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="83084-150">NOTES</span></span>

## <span data-ttu-id="83084-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83084-151">RELATED LINKS</span></span>
