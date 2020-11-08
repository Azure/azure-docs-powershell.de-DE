---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: bb9ae3ba225c67a98b6c3588e1dc0c63f02170ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176876"
---
# <span data-ttu-id="66189-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="66189-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="66189-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66189-102">SYNOPSIS</span></span>
<span data-ttu-id="66189-103">Erstellt eine Azure SQL-Daten Bank verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="66189-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="66189-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66189-104">SYNTAX</span></span>

### <span data-ttu-id="66189-105">NewByEditionAndComputeGenerationParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="66189-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66189-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66189-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66189-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66189-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66189-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="66189-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66189-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66189-109">DESCRIPTION</span></span>
<span data-ttu-id="66189-110">Das Cmdlet **New-AzSqlInstance** erstellt eine verwaltete Azure SQL-Datenbank-Instanz.</span><span class="sxs-lookup"><span data-stu-id="66189-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="66189-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66189-111">EXAMPLES</span></span>

### <span data-ttu-id="66189-112">Beispiel 1: Erstellen einer neuen Instanz</span><span class="sxs-lookup"><span data-stu-id="66189-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="66189-113">Dieser Befehl erstellt eine neue Instanz mithilfe des SkuName-Parameters.</span><span class="sxs-lookup"><span data-stu-id="66189-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="66189-114">Beispiel 2: Erstellen einer neuen Instanz</span><span class="sxs-lookup"><span data-stu-id="66189-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="66189-115">Dieser Befehl erstellt eine neue Instanz mithilfe von Edition-und ComputeGeneration-Parametern.</span><span class="sxs-lookup"><span data-stu-id="66189-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="66189-116">Beispiel 3: Erstellen einer neuen Instanz in einem Instanzen Pool mithilfe eines Instanzen Pool Objekts</span><span class="sxs-lookup"><span data-stu-id="66189-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="66189-117">Mit diesem Befehl wird eine neue Instanz in einem Instanz Pool mit einem Instanz Pool-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="66189-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="66189-118">Beispiel 4: Erstellen einer neuen Instanz in einem Instanzen Pool mithilfe eines Ressourcenbezeichners für einen Instanzen Pool</span><span class="sxs-lookup"><span data-stu-id="66189-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="66189-119">Mit diesem Befehl wird eine neue Instanz in einem Instanz Pool mithilfe des Ressourcenbezeichners des Instanzen Pools erstellt.</span><span class="sxs-lookup"><span data-stu-id="66189-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="66189-120">Beispiel 5: Erstellen einer neuen Instanz in einem Instanz Pool</span><span class="sxs-lookup"><span data-stu-id="66189-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="66189-121">Dieser Befehl erstellt eine neue Instanz in einem Instanzen Pool mit dem Namen instancePool0</span><span class="sxs-lookup"><span data-stu-id="66189-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="66189-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="66189-122">PARAMETERS</span></span>

### <span data-ttu-id="66189-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="66189-123">-AdministratorCredential</span></span>
<span data-ttu-id="66189-124">Die SQL-Authentifizierungsanmeldeinformationen der Instanz.</span><span class="sxs-lookup"><span data-stu-id="66189-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="66189-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66189-125">-AsJob</span></span>
<span data-ttu-id="66189-126">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="66189-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66189-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="66189-127">-AssignIdentity</span></span>
<span data-ttu-id="66189-128">Generieren Sie eine Azure Active Directory-Identität für diese verwaltete Instanz, und weisen Sie Sie für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault zu.</span><span class="sxs-lookup"><span data-stu-id="66189-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="66189-129">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="66189-129">-BackupStorageRedundancy</span></span>
<span data-ttu-id="66189-130">Die Backup-Speicherredundanz, die zum Speichern von Sicherungen für die verwaltete SQL Azure-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="66189-130">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="66189-131">Optionen sind: lokal, Zone und Geo</span><span class="sxs-lookup"><span data-stu-id="66189-131">Options are: Local, Zone and Geo</span></span>

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

### <span data-ttu-id="66189-132">-Sortierung</span><span class="sxs-lookup"><span data-stu-id="66189-132">-Collation</span></span>
<span data-ttu-id="66189-133">Die Sortierung der zu verwendenden Azure SQL-Instanz.</span><span class="sxs-lookup"><span data-stu-id="66189-133">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="66189-134">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="66189-134">-ComputeGeneration</span></span>
<span data-ttu-id="66189-135">Die COMPUTE-Generierung für die Instanz.</span><span class="sxs-lookup"><span data-stu-id="66189-135">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="66189-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66189-136">-DefaultProfile</span></span>
<span data-ttu-id="66189-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66189-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66189-138">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="66189-138">-DnsZonePartner</span></span>
<span data-ttu-id="66189-139">Die Ressourcen-ID des verwalteten Partnerservers, um die dnsZone-Eigenschaft von der Erstellung verwalteter Instanzen zu erben</span><span class="sxs-lookup"><span data-stu-id="66189-139">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="66189-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="66189-140">-Edition</span></span>
<span data-ttu-id="66189-141">Die Edition für die Instanz.</span><span class="sxs-lookup"><span data-stu-id="66189-141">The edition for the instance.</span></span>

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

### <span data-ttu-id="66189-142">-Force</span><span class="sxs-lookup"><span data-stu-id="66189-142">-Force</span></span>
<span data-ttu-id="66189-143">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="66189-143">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="66189-144">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="66189-144">-InstancePool</span></span>
<span data-ttu-id="66189-145">Das übergeordnete Objekt des Instanzen Pools.</span><span class="sxs-lookup"><span data-stu-id="66189-145">The instance pool parent object.</span></span>

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

### <span data-ttu-id="66189-146">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="66189-146">-InstancePoolName</span></span>
<span data-ttu-id="66189-147">Der Instanz Pool, in dem diese Instanz platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="66189-147">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="66189-148">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="66189-148">-InstancePoolResourceId</span></span>
<span data-ttu-id="66189-149">Die Ressourcen-ID des Instanzen Pools.</span><span class="sxs-lookup"><span data-stu-id="66189-149">The instance pool resource id.</span></span>

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

### <span data-ttu-id="66189-150">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="66189-150">-LicenseType</span></span>
<span data-ttu-id="66189-151">Bestimmt den zu verwendenden Lizenztyp.</span><span class="sxs-lookup"><span data-stu-id="66189-151">Determines which License Type to use.</span></span> <span data-ttu-id="66189-152">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="66189-152">Possible values are:</span></span>
- <span data-ttu-id="66189-153">Grundpr.-Azure Hybrid Benefit (AHB) Discounted Pricing für vorhandene SQL Server-Lizenzbesitzer wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="66189-153">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="66189-154">Der Service Preis für verwaltete Instanzen wird für vorhandene SQL Server-Lizenzbesitzer abgezinst.</span><span class="sxs-lookup"><span data-stu-id="66189-154">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="66189-155">LicenseIncluded-Azure Hybrid Benefit (AHB) Preisnachlässe für vorhandene SQL Server-Lizenzbesitzer werden nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="66189-155">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="66189-156">Der Service Preis für verwaltete Instanzen umfasst eine neue Lizenz für SQL Server-Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="66189-156">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="66189-157">-Standort</span><span class="sxs-lookup"><span data-stu-id="66189-157">-Location</span></span>
<span data-ttu-id="66189-158">Die Position, an der die Instanz erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66189-158">The location in which to create the instance</span></span>

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

### <span data-ttu-id="66189-159">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="66189-159">-MinimalTlsVersion</span></span>
<span data-ttu-id="66189-160">Die minimale TLS-Version, die für verwaltete Instanzen erzwungen werden soll</span><span class="sxs-lookup"><span data-stu-id="66189-160">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="66189-161">-Name</span><span class="sxs-lookup"><span data-stu-id="66189-161">-Name</span></span>
<span data-ttu-id="66189-162">Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="66189-162">Instance name.</span></span>

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

### <span data-ttu-id="66189-163">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="66189-163">-ProxyOverride</span></span>
<span data-ttu-id="66189-164">Der Verbindungstyp, der für die Verbindung mit der Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="66189-164">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="66189-165">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="66189-165">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="66189-166">Gibt an, ob der öffentliche Daten Endpunkt für die Instanz aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="66189-166">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="66189-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66189-167">-ResourceGroupName</span></span>
<span data-ttu-id="66189-168">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="66189-168">The name of the resource group.</span></span>

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

### <span data-ttu-id="66189-169">-SkuName</span><span class="sxs-lookup"><span data-stu-id="66189-169">-SkuName</span></span>
<span data-ttu-id="66189-170">Der SKU-Name für die Instanz, beispielsweise "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="66189-170">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="66189-171">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="66189-171">-StorageSizeInGB</span></span>
<span data-ttu-id="66189-172">Bestimmt, wie viel Speichergröße mit der Instanz verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="66189-172">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="66189-173">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="66189-173">-SubnetId</span></span>
<span data-ttu-id="66189-174">Die für die Erstellung von Instanzen zu verwendende Subnetz-ID</span><span class="sxs-lookup"><span data-stu-id="66189-174">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="66189-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="66189-175">-Tag</span></span>
<span data-ttu-id="66189-176">Die Tags, die der Instanz zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="66189-176">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="66189-177">-Zeitzonen-Nr.</span><span class="sxs-lookup"><span data-stu-id="66189-177">-TimezoneId</span></span>
<span data-ttu-id="66189-178">Die Zeit Zonen-ID für die Instanz, die gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66189-178">The time zone id for the instance to set.</span></span> <span data-ttu-id="66189-179">Eine Liste der Zeit Zonen-IDs wird über die sys.time_zone_info (Transact-SQL)-Ansicht verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="66189-179">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="66189-180">-VCore</span><span class="sxs-lookup"><span data-stu-id="66189-180">-VCore</span></span>
<span data-ttu-id="66189-181">Bestimmt, wie viel Vcore mit der Instanz verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="66189-181">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="66189-182">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66189-182">-Confirm</span></span>
<span data-ttu-id="66189-183">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66189-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66189-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66189-184">-WhatIf</span></span>
<span data-ttu-id="66189-185">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66189-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66189-186">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66189-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66189-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66189-187">CommonParameters</span></span>
<span data-ttu-id="66189-188">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66189-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66189-189">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66189-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66189-190">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66189-190">INPUTS</span></span>

### <span data-ttu-id="66189-191">Keine</span><span class="sxs-lookup"><span data-stu-id="66189-191">None</span></span>

## <span data-ttu-id="66189-192">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66189-192">OUTPUTS</span></span>

### <span data-ttu-id="66189-193">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="66189-193">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="66189-194">Notizen</span><span class="sxs-lookup"><span data-stu-id="66189-194">NOTES</span></span>

## <span data-ttu-id="66189-195">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66189-195">RELATED LINKS</span></span>
