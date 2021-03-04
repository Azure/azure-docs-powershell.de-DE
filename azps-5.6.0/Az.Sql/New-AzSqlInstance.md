---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: 9f648f0e2ab15919f3caa849041846570d627df5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927715"
---
# <span data-ttu-id="7e683-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7e683-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="7e683-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e683-102">SYNOPSIS</span></span>
<span data-ttu-id="7e683-103">Erstellt eine verwaltete Azure SQL-Datenbankinstanz.</span><span class="sxs-lookup"><span data-stu-id="7e683-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="7e683-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e683-104">SYNTAX</span></span>

### <span data-ttu-id="7e683-105">NewByEditionAndComputeGenerationParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e683-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e683-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e683-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e683-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e683-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e683-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="7e683-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e683-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e683-109">DESCRIPTION</span></span>
<span data-ttu-id="7e683-110">Das **Cmdlet New-AzSqlInstance** erstellt eine Azure SQL Datenbank verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="7e683-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="7e683-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7e683-111">EXAMPLES</span></span>

### <span data-ttu-id="7e683-112">Beispiel 1: Erstellen einer neuen Instanz</span><span class="sxs-lookup"><span data-stu-id="7e683-112">Example 1: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4 -DnsZonePartner "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/partnerServerForDnsZone"
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
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="7e683-113">Mit diesem Befehl wird mithilfe des SkuName-Parameters eine neue Instanz erstellt.</span><span class="sxs-lookup"><span data-stu-id="7e683-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="7e683-114">Beispiel 2: Erstellen einer neuen Instanz</span><span class="sxs-lookup"><span data-stu-id="7e683-114">Example 2: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="7e683-115">Mit diesem Befehl wird mithilfe der Parameter Edition und ComputeGeneration eine neue Instanz erstellt.</span><span class="sxs-lookup"><span data-stu-id="7e683-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="7e683-116">Beispiel 3: Erstellen einer neuen Instanz in einem Instanzpool mithilfe eines Instanzpoolobjekts</span><span class="sxs-lookup"><span data-stu-id="7e683-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="7e683-117">Mit diesem Befehl wird eine neue Instanz in einem Instanzpool mithilfe eines Instanzpoolobjekts erstellt.</span><span class="sxs-lookup"><span data-stu-id="7e683-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="7e683-118">Beispiel 4: Erstellen einer neuen Instanz in einem Instanzpool mithilfe eines Instanzpoolressourcenbezeichners</span><span class="sxs-lookup"><span data-stu-id="7e683-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
```powershell
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="7e683-119">Mit diesem Befehl wird eine neue Instanz in einem Instanzpool mit dem Ressourcenbezeichner des Instanzpools erstellt.</span><span class="sxs-lookup"><span data-stu-id="7e683-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="7e683-120">Beispiel 5: Erstellen einer neuen Instanz in einem Instanzpool</span><span class="sxs-lookup"><span data-stu-id="7e683-120">Example 5: Create a new instance in an instance pool</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 32 -VCore 2 -ComputeGeneration Gen5 -Edition GeneralPurpose -InstancePoolName instancePool0
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
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 32
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="7e683-121">Mit diesem Befehl wird eine neue Instanz in einem Instanzpool mit Name instancePool0 erstellt.</span><span class="sxs-lookup"><span data-stu-id="7e683-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

### <span data-ttu-id="7e683-122">Beispiel 6: Erstellen einer neuen Instanz mit Wartungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="7e683-122">Example 6: Create a new instance with maintenance configuration</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourcegroup01 -Location "westus" -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -ComputeGeneration Gen5 -Edition GeneralPurpose -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2"
Location                   : westus
Id                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName          : resourcegroup01
ManagedInstanceName        : managedInstance1
Tags                       :
Identity                   :
Sku                        : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName   : managedInstance1.wusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin         : adminLogin1
AdministratorPassword      :
SubnetId                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType                : LicenseIncluded
VCores                     : 8
StorageSizeInGB            : 256
Collation                  : SQL_Latin1_General_CP1_CI_AS
PublicDataEndpointEnabled  : False
ProxyOverride              :
TimezoneId                 : UTC
DnsZonePartner             :
DnsZone                    : ad35cna0mw
InstancePoolName           :
MinimalTlsVersion          :
BackupStorageRedundancy    : Geo
MaintenanceConfigurationId : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2
```

<span data-ttu-id="7e683-123">Mit diesem Befehl wird eine neue Instanz mit Wartungskonfigurationseinstellungen MI_2</span><span class="sxs-lookup"><span data-stu-id="7e683-123">This command creates a new instance with maintenance configuration MI_2</span></span>

## <span data-ttu-id="7e683-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7e683-124">PARAMETERS</span></span>

### <span data-ttu-id="7e683-125">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="7e683-125">-AdministratorCredential</span></span>
<span data-ttu-id="7e683-126">Die SQL Authentifizierungsanmeldeinformationen der -Instanz.</span><span class="sxs-lookup"><span data-stu-id="7e683-126">The SQL authentication credential of the instance.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e683-127">-AsJob</span></span>
<span data-ttu-id="7e683-128">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7e683-128">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7e683-129">-AssignIdentity</span></span>
<span data-ttu-id="7e683-130">Generieren und Zuweisen einer Azure Active Directory-Identität für diese verwaltete Instanz für die Verwendung mit wichtigen Verwaltungsdiensten wie Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="7e683-130">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-131">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="7e683-131">-BackupStorageRedundancy</span></span>
<span data-ttu-id="7e683-132">Die Redundanz des Sicherungsspeichers, die zum Speichern von Sicherungen für die verwaltete Sql Azure-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7e683-132">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="7e683-133">Optionen sind: Lokal, Zone und Geo</span><span class="sxs-lookup"><span data-stu-id="7e683-133">Options are: Local, Zone and Geo</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-134">-Sortierung</span><span class="sxs-lookup"><span data-stu-id="7e683-134">-Collation</span></span>
<span data-ttu-id="7e683-135">Die Sortierung der zu verwendende Azure SQL verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="7e683-135">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="7e683-136">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="7e683-136">-ComputeGeneration</span></span>
<span data-ttu-id="7e683-137">Die Computegenerierung für die -Instanz.</span><span class="sxs-lookup"><span data-stu-id="7e683-137">The compute generation for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e683-138">-DefaultProfile</span></span>
<span data-ttu-id="7e683-139">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e683-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e683-140">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="7e683-140">-DnsZonePartner</span></span>
<span data-ttu-id="7e683-141">Die Ressourcen-ID des Partners Managed Server, von dem die DnsZone-Eigenschaft für die Erstellung verwalteter Instanzen erben soll</span><span class="sxs-lookup"><span data-stu-id="7e683-141">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="7e683-142">-Edition</span><span class="sxs-lookup"><span data-stu-id="7e683-142">-Edition</span></span>
<span data-ttu-id="7e683-143">Die Edition für die -Instanz.</span><span class="sxs-lookup"><span data-stu-id="7e683-143">The edition for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-144">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="7e683-144">-Force</span></span>
<span data-ttu-id="7e683-145">Bestätigungsmeldung überspringen zum Ausführen der Aktion</span><span class="sxs-lookup"><span data-stu-id="7e683-145">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-146">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="7e683-146">-InstancePool</span></span>
<span data-ttu-id="7e683-147">Das übergeordnete Objekt des Instanzpools.</span><span class="sxs-lookup"><span data-stu-id="7e683-147">The instance pool parent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: NewByInstancePoolParentObjectParameterSet
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-148">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="7e683-148">-InstancePoolName</span></span>
<span data-ttu-id="7e683-149">Der Instanzpool zum Platzieren dieser Instanz.</span><span class="sxs-lookup"><span data-stu-id="7e683-149">The instance pool to place this instance in.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-150">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="7e683-150">-InstancePoolResourceId</span></span>
<span data-ttu-id="7e683-151">Die Ressourcen-ID des Instanzpools.</span><span class="sxs-lookup"><span data-stu-id="7e683-151">The instance pool resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByInstancePoolResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-152">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7e683-152">-LicenseType</span></span>
<span data-ttu-id="7e683-153">Bestimmt, welcher Lizenztyp verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e683-153">Determines which License Type to use.</span></span> <span data-ttu-id="7e683-154">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7e683-154">Possible values are:</span></span>
- <span data-ttu-id="7e683-155">BasePrice – AhB(Azure Hybrid Benefit)-rabattierte Preise für vorhandene SQL Server werden angewendet.</span><span class="sxs-lookup"><span data-stu-id="7e683-155">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="7e683-156">Der Servicepreis für verwaltete Instanzen wird für vorhandene Besitzer SQL Server reduziert.</span><span class="sxs-lookup"><span data-stu-id="7e683-156">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="7e683-157">LicenseIncluded – Rabattpreise für Azure Hybrid Benefit (AHB) für vorhandene SQL Server Lizenzbesitzer werden nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="7e683-157">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="7e683-158">Der Preis für den Dienst für verwaltete Instanzen enthält eine neue SQL Server Lizenzkosten.</span><span class="sxs-lookup"><span data-stu-id="7e683-158">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-159">-Location</span><span class="sxs-lookup"><span data-stu-id="7e683-159">-Location</span></span>
<span data-ttu-id="7e683-160">Der Speicherort, an dem die Instanz erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="7e683-160">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-161">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7e683-161">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="7e683-162">Die Wartungskonfigurations-ID für die verwaltete Sql Azure-Instanz.</span><span class="sxs-lookup"><span data-stu-id="7e683-162">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="7e683-163">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="7e683-163">-MinimalTlsVersion</span></span>
<span data-ttu-id="7e683-164">Die minimale TLS-Version, die für verwaltete Instanzen erzwungen werden soll</span><span class="sxs-lookup"><span data-stu-id="7e683-164">The minimal TLS version to enforce for Managed instance</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-165">-Name</span><span class="sxs-lookup"><span data-stu-id="7e683-165">-Name</span></span>
<span data-ttu-id="7e683-166">Instanzname.</span><span class="sxs-lookup"><span data-stu-id="7e683-166">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-167">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="7e683-167">-ProxyOverride</span></span>
<span data-ttu-id="7e683-168">Der Verbindungstyp, der zum Herstellen einer Verbindung mit der -Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7e683-168">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="7e683-169">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="7e683-169">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="7e683-170">Gibt an, ob der öffentliche Datenendpunkt für die -Instanz aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7e683-170">Whether or not the public data endpoint is enabled for the instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e683-171">-ResourceGroupName</span></span>
<span data-ttu-id="7e683-172">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7e683-172">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-173">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7e683-173">-SkuName</span></span>
<span data-ttu-id="7e683-174">Der Name der SKU für die Instanz, z. B. "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="7e683-174">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: System.String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-175">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="7e683-175">-StorageSizeInGB</span></span>
<span data-ttu-id="7e683-176">Bestimmt, wie viel Speichergröße einer Instanz zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="7e683-176">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-177">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7e683-177">-SubnetId</span></span>
<span data-ttu-id="7e683-178">Die Subnetz-ID, die für die Erstellung von Beispielen verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="7e683-178">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e683-179">-Tag</span></span>
<span data-ttu-id="7e683-180">Die Tags, die der Instanz zugeordnet werden sollen</span><span class="sxs-lookup"><span data-stu-id="7e683-180">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e683-181">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="7e683-181">-TimezoneId</span></span>
<span data-ttu-id="7e683-182">Die Zeitzonen-ID für die zu legende Instanz.</span><span class="sxs-lookup"><span data-stu-id="7e683-182">The time zone id for the instance to set.</span></span> <span data-ttu-id="7e683-183">Eine Liste der Zeitzonen-ID wird über die Ansicht sys.time_zone_info (Transact-SQL) verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="7e683-183">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="7e683-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="7e683-184">-VCore</span></span>
<span data-ttu-id="7e683-185">Bestimmt, wie viel VCore einer Instanz zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="7e683-185">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="7e683-186">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7e683-186">-Confirm</span></span>
<span data-ttu-id="7e683-187">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e683-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e683-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e683-188">-WhatIf</span></span>
<span data-ttu-id="7e683-189">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e683-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e683-190">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7e683-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e683-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e683-191">CommonParameters</span></span>
<span data-ttu-id="7e683-192">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e683-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e683-193">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e683-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e683-194">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7e683-194">INPUTS</span></span>

### <span data-ttu-id="7e683-195">Keine</span><span class="sxs-lookup"><span data-stu-id="7e683-195">None</span></span>

## <span data-ttu-id="7e683-196">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7e683-196">OUTPUTS</span></span>

### <span data-ttu-id="7e683-197">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="7e683-197">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="7e683-198">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7e683-198">NOTES</span></span>

## <span data-ttu-id="7e683-199">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7e683-199">RELATED LINKS</span></span>
