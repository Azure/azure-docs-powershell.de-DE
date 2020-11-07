---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: d80e6ddd7fa420b07a0df30c2718d9c4e96123fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825999"
---
# <span data-ttu-id="3740c-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3740c-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="3740c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3740c-102">SYNOPSIS</span></span>
<span data-ttu-id="3740c-103">Erstellt eine Azure SQL-Daten Bank verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="3740c-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="3740c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3740c-104">SYNTAX</span></span>

### <span data-ttu-id="3740c-105">NewByEditionAndComputeGenerationParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3740c-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3740c-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3740c-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3740c-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3740c-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3740c-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="3740c-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3740c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3740c-109">DESCRIPTION</span></span>
<span data-ttu-id="3740c-110">Das Cmdlet **New-AzSqlInstance** erstellt eine verwaltete Azure SQL-Datenbank-Instanz.</span><span class="sxs-lookup"><span data-stu-id="3740c-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="3740c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3740c-111">EXAMPLES</span></span>

### <span data-ttu-id="3740c-112">Beispiel 1: Erstellen einer neuen Instanz</span><span class="sxs-lookup"><span data-stu-id="3740c-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="3740c-113">Dieser Befehl erstellt eine neue Instanz mithilfe des SkuName-Parameters.</span><span class="sxs-lookup"><span data-stu-id="3740c-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="3740c-114">Beispiel 2: Erstellen einer neuen Instanz</span><span class="sxs-lookup"><span data-stu-id="3740c-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="3740c-115">Dieser Befehl erstellt eine neue Instanz mithilfe von Edition-und ComputeGeneration-Parametern.</span><span class="sxs-lookup"><span data-stu-id="3740c-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="3740c-116">Beispiel 3: Erstellen einer neuen Instanz in einem Instanzen Pool mithilfe eines Instanzen Pool Objekts</span><span class="sxs-lookup"><span data-stu-id="3740c-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="3740c-117">Mit diesem Befehl wird eine neue Instanz in einem Instanz Pool mit einem Instanz Pool-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="3740c-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="3740c-118">Beispiel 4: Erstellen einer neuen Instanz in einem Instanzen Pool mithilfe eines Ressourcenbezeichners für einen Instanzen Pool</span><span class="sxs-lookup"><span data-stu-id="3740c-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="3740c-119">Mit diesem Befehl wird eine neue Instanz in einem Instanz Pool mithilfe des Ressourcenbezeichners des Instanzen Pools erstellt.</span><span class="sxs-lookup"><span data-stu-id="3740c-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="3740c-120">Beispiel 5: Erstellen einer neuen Instanz in einem Instanz Pool</span><span class="sxs-lookup"><span data-stu-id="3740c-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="3740c-121">Dieser Befehl erstellt eine neue Instanz in einem Instanzen Pool mit dem Namen instancePool0</span><span class="sxs-lookup"><span data-stu-id="3740c-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="3740c-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="3740c-122">PARAMETERS</span></span>

### <span data-ttu-id="3740c-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="3740c-123">-AdministratorCredential</span></span>
<span data-ttu-id="3740c-124">Die SQL-Authentifizierungsanmeldeinformationen der Instanz.</span><span class="sxs-lookup"><span data-stu-id="3740c-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="3740c-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3740c-125">-AsJob</span></span>
<span data-ttu-id="3740c-126">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3740c-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3740c-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3740c-127">-AssignIdentity</span></span>
<span data-ttu-id="3740c-128">Generieren Sie eine Azure Active Directory-Identität für diese verwaltete Instanz, und weisen Sie Sie für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault zu.</span><span class="sxs-lookup"><span data-stu-id="3740c-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="3740c-129">-Sortierung</span><span class="sxs-lookup"><span data-stu-id="3740c-129">-Collation</span></span>
<span data-ttu-id="3740c-130">Die Sortierung der zu verwendenden Azure SQL-Instanz.</span><span class="sxs-lookup"><span data-stu-id="3740c-130">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="3740c-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="3740c-131">-ComputeGeneration</span></span>
<span data-ttu-id="3740c-132">Die COMPUTE-Generierung für die Instanz.</span><span class="sxs-lookup"><span data-stu-id="3740c-132">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="3740c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3740c-133">-DefaultProfile</span></span>
<span data-ttu-id="3740c-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3740c-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3740c-135">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="3740c-135">-DnsZonePartner</span></span>
<span data-ttu-id="3740c-136">Die Ressourcen-ID des verwalteten Partnerservers, um die dnsZone-Eigenschaft von der Erstellung verwalteter Instanzen zu erben</span><span class="sxs-lookup"><span data-stu-id="3740c-136">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="3740c-137">-Edition</span><span class="sxs-lookup"><span data-stu-id="3740c-137">-Edition</span></span>
<span data-ttu-id="3740c-138">Die Edition für die Instanz.</span><span class="sxs-lookup"><span data-stu-id="3740c-138">The edition for the instance.</span></span>

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

### <span data-ttu-id="3740c-139">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="3740c-139">-InstancePool</span></span>
<span data-ttu-id="3740c-140">Das übergeordnete Objekt des Instanzen Pools.</span><span class="sxs-lookup"><span data-stu-id="3740c-140">The instance pool parent object.</span></span>

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

### <span data-ttu-id="3740c-141">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="3740c-141">-InstancePoolName</span></span>
<span data-ttu-id="3740c-142">Der Instanz Pool, in dem diese Instanz platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3740c-142">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="3740c-143">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="3740c-143">-InstancePoolResourceId</span></span>
<span data-ttu-id="3740c-144">Die Ressourcen-ID des Instanzen Pools.</span><span class="sxs-lookup"><span data-stu-id="3740c-144">The instance pool resource id.</span></span>

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

### <span data-ttu-id="3740c-145">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3740c-145">-LicenseType</span></span>
<span data-ttu-id="3740c-146">Bestimmt den zu verwendenden Lizenztyp.</span><span class="sxs-lookup"><span data-stu-id="3740c-146">Determines which License Type to use.</span></span> <span data-ttu-id="3740c-147">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="3740c-147">Possible values are:</span></span>
- <span data-ttu-id="3740c-148">Grundpr.-Azure Hybrid Benefit (AHB) Discounted Pricing für vorhandene SQL Server-Lizenzbesitzer wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="3740c-148">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="3740c-149">Der Service Preis für verwaltete Instanzen wird für vorhandene SQL Server-Lizenzbesitzer abgezinst.</span><span class="sxs-lookup"><span data-stu-id="3740c-149">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="3740c-150">LicenseIncluded-Azure Hybrid Benefit (AHB) Preisnachlässe für vorhandene SQL Server-Lizenzbesitzer werden nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="3740c-150">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="3740c-151">Der Service Preis für verwaltete Instanzen umfasst eine neue Lizenz für SQL Server-Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="3740c-151">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="3740c-152">-Standort</span><span class="sxs-lookup"><span data-stu-id="3740c-152">-Location</span></span>
<span data-ttu-id="3740c-153">Die Position, an der die Instanz erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3740c-153">The location in which to create the instance</span></span>

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

### <span data-ttu-id="3740c-154">-Name</span><span class="sxs-lookup"><span data-stu-id="3740c-154">-Name</span></span>
<span data-ttu-id="3740c-155">Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="3740c-155">Instance name.</span></span>

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

### <span data-ttu-id="3740c-156">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="3740c-156">-ProxyOverride</span></span>
<span data-ttu-id="3740c-157">Der Verbindungstyp, der für die Verbindung mit der Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3740c-157">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="3740c-158">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="3740c-158">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="3740c-159">Gibt an, ob der öffentliche Daten Endpunkt für die Instanz aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="3740c-159">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="3740c-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3740c-160">-ResourceGroupName</span></span>
<span data-ttu-id="3740c-161">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3740c-161">The name of the resource group.</span></span>

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

### <span data-ttu-id="3740c-162">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3740c-162">-SkuName</span></span>
<span data-ttu-id="3740c-163">Der SKU-Name für die Instanz, beispielsweise "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="3740c-163">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="3740c-164">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="3740c-164">-StorageSizeInGB</span></span>
<span data-ttu-id="3740c-165">Bestimmt, wie viel Speichergröße mit der Instanz verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="3740c-165">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="3740c-166">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="3740c-166">-SubnetId</span></span>
<span data-ttu-id="3740c-167">Die für die Erstellung von Instanzen zu verwendende Subnetz-ID</span><span class="sxs-lookup"><span data-stu-id="3740c-167">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="3740c-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="3740c-168">-Tag</span></span>
<span data-ttu-id="3740c-169">Die Tags, die der Instanz zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3740c-169">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="3740c-170">-Zeitzonen-Nr.</span><span class="sxs-lookup"><span data-stu-id="3740c-170">-TimezoneId</span></span>
<span data-ttu-id="3740c-171">Die Zeit Zonen-ID für die Instanz, die gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3740c-171">The time zone id for the instance to set.</span></span> <span data-ttu-id="3740c-172">Eine Liste der Zeit Zonen-IDs wird über die sys.time_zone_info (Transact-SQL)-Ansicht verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="3740c-172">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="3740c-173">-VCore</span><span class="sxs-lookup"><span data-stu-id="3740c-173">-VCore</span></span>
<span data-ttu-id="3740c-174">Bestimmt, wie viel Vcore mit der Instanz verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="3740c-174">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="3740c-175">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3740c-175">-Confirm</span></span>
<span data-ttu-id="3740c-176">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3740c-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3740c-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3740c-177">-WhatIf</span></span>
<span data-ttu-id="3740c-178">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3740c-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3740c-179">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3740c-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3740c-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3740c-180">CommonParameters</span></span>
<span data-ttu-id="3740c-181">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3740c-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3740c-182">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3740c-182">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3740c-183">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3740c-183">INPUTS</span></span>

### <span data-ttu-id="3740c-184">Keine</span><span class="sxs-lookup"><span data-stu-id="3740c-184">None</span></span>

## <span data-ttu-id="3740c-185">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3740c-185">OUTPUTS</span></span>

### <span data-ttu-id="3740c-186">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="3740c-186">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="3740c-187">Notizen</span><span class="sxs-lookup"><span data-stu-id="3740c-187">NOTES</span></span>

## <span data-ttu-id="3740c-188">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3740c-188">RELATED LINKS</span></span>
