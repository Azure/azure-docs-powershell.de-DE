---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: ef809acdf8b78eb0d1203a901b3b44028c79733e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296200"
---
# <span data-ttu-id="04315-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="04315-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="04315-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04315-102">SYNOPSIS</span></span>
<span data-ttu-id="04315-103">Erstellt eine verwaltete Azure SQL-Datenbankinstanz.</span><span class="sxs-lookup"><span data-stu-id="04315-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="04315-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04315-104">SYNTAX</span></span>

### <span data-ttu-id="04315-105">NewByEditionAndComputeGenerationParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="04315-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04315-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04315-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04315-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04315-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04315-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="04315-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04315-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04315-109">DESCRIPTION</span></span>
<span data-ttu-id="04315-110">Das **Cmdlet "New-AzSqlInstance"** erstellt eine Azure SQL-Datenbank-verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="04315-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="04315-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="04315-111">EXAMPLES</span></span>

### <span data-ttu-id="04315-112">Beispiel 1: Erstellen einer neuen Instanz</span><span class="sxs-lookup"><span data-stu-id="04315-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="04315-113">Dieser Befehl erstellt mithilfe des Parameters "SkuName" eine neue Instanz.</span><span class="sxs-lookup"><span data-stu-id="04315-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="04315-114">Beispiel 2: Erstellen einer neuen Instanz</span><span class="sxs-lookup"><span data-stu-id="04315-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="04315-115">Dieser Befehl erstellt mithilfe der Parameter "Edition" und "ComputeGeneration" eine neue Instanz.</span><span class="sxs-lookup"><span data-stu-id="04315-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="04315-116">Beispiel 3: Erstellen einer neuen Instanz in einem Instanzpool mithilfe eines Instanzpoolobjekts</span><span class="sxs-lookup"><span data-stu-id="04315-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="04315-117">Mit diesem Befehl wird mithilfe eines Instanzpoolobjekts eine neue Instanz in einem Instanzpool erstellt.</span><span class="sxs-lookup"><span data-stu-id="04315-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="04315-118">Beispiel 4: Erstellen einer neuen Instanz in einem Instanzpool mithilfe eines Ressourcenbezeichners für den Instanzpool</span><span class="sxs-lookup"><span data-stu-id="04315-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="04315-119">Mit diesem Befehl wird mithilfe des Ressourcenbezeichners des Instanzpools eine neue Instanz in einem Instanzpool erstellt.</span><span class="sxs-lookup"><span data-stu-id="04315-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="04315-120">Beispiel 5: Erstellen einer neuen Instanz in einem Instanzpool</span><span class="sxs-lookup"><span data-stu-id="04315-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="04315-121">Mit diesem Befehl wird eine neue Instanz in einem Instanzpool mit Name instancePool0 erstellt.</span><span class="sxs-lookup"><span data-stu-id="04315-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="04315-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04315-122">PARAMETERS</span></span>

### <span data-ttu-id="04315-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="04315-123">-AdministratorCredential</span></span>
<span data-ttu-id="04315-124">Die SQL Authentifizierungsanmeldeinformationen der Instanz.</span><span class="sxs-lookup"><span data-stu-id="04315-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="04315-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04315-125">-AsJob</span></span>
<span data-ttu-id="04315-126">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="04315-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04315-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="04315-127">-AssignIdentity</span></span>
<span data-ttu-id="04315-128">Generieren und zuweisen Sie eine Azure Active Directory-Identität für diese verwaltete Instanz zur Verwendung mit Schlüsselverwaltungsdiensten wie Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="04315-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="04315-129">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="04315-129">-BackupStorageRedundancy</span></span>
<span data-ttu-id="04315-130">Die Sicherungsspeicherredundanz, die zum Speichern von Sicherungen für die sql Azure Managed Instance verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="04315-130">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="04315-131">Optionen sind: Lokal, Zone und Geo</span><span class="sxs-lookup"><span data-stu-id="04315-131">Options are: Local, Zone and Geo</span></span>

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

### <span data-ttu-id="04315-132">-Collation</span><span class="sxs-lookup"><span data-stu-id="04315-132">-Collation</span></span>
<span data-ttu-id="04315-133">Die Sortierung der zu verwendende Azure SQL verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="04315-133">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="04315-134">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="04315-134">-ComputeGeneration</span></span>
<span data-ttu-id="04315-135">Die Rechengenerierung für die Instanz.</span><span class="sxs-lookup"><span data-stu-id="04315-135">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="04315-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04315-136">-DefaultProfile</span></span>
<span data-ttu-id="04315-137">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04315-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04315-138">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="04315-138">-DnsZonePartner</span></span>
<span data-ttu-id="04315-139">Die Ressourcen-ID des vom Partner verwalteten Servers, von dem die Eigenschaft "DnsZone" für die Erstellung verwalteter Instanzen geerbt werden soll</span><span class="sxs-lookup"><span data-stu-id="04315-139">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="04315-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="04315-140">-Edition</span></span>
<span data-ttu-id="04315-141">Die Edition für die Instanz.</span><span class="sxs-lookup"><span data-stu-id="04315-141">The edition for the instance.</span></span>

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

### <span data-ttu-id="04315-142">-Force</span><span class="sxs-lookup"><span data-stu-id="04315-142">-Force</span></span>
<span data-ttu-id="04315-143">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="04315-143">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="04315-144">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="04315-144">-InstancePool</span></span>
<span data-ttu-id="04315-145">Das übergeordnete Objekt des Instanzpools.</span><span class="sxs-lookup"><span data-stu-id="04315-145">The instance pool parent object.</span></span>

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

### <span data-ttu-id="04315-146">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="04315-146">-InstancePoolName</span></span>
<span data-ttu-id="04315-147">Der Instanzpool, in dem diese Instanz zu platzieren ist.</span><span class="sxs-lookup"><span data-stu-id="04315-147">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="04315-148">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="04315-148">-InstancePoolResourceId</span></span>
<span data-ttu-id="04315-149">Die Ressourcen-ID des Instanzpools.</span><span class="sxs-lookup"><span data-stu-id="04315-149">The instance pool resource id.</span></span>

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

### <span data-ttu-id="04315-150">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="04315-150">-LicenseType</span></span>
<span data-ttu-id="04315-151">Bestimmt, welcher Lizenztyp verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="04315-151">Determines which License Type to use.</span></span> <span data-ttu-id="04315-152">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="04315-152">Possible values are:</span></span>
- <span data-ttu-id="04315-153">BasePrice – Reduzierte Preise für Azure Hybrid Benefit (AHB) für vorhandene SQL Server Lizenzbesitzer werden angewendet.</span><span class="sxs-lookup"><span data-stu-id="04315-153">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="04315-154">Der Dienstpreis für verwaltete Instanzen wird für vorhandene Besitzer SQL Server Instanz vergünstigt.</span><span class="sxs-lookup"><span data-stu-id="04315-154">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="04315-155">LicenseIncluded – Rabatte für Azure Hybrid Benefit (AHB) für vorhandene SQL Server Lizenzbesitzer werden nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="04315-155">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="04315-156">Der Preis für verwaltete Instanzdienste enthält eine neue SQL Server Lizenzkosten.</span><span class="sxs-lookup"><span data-stu-id="04315-156">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="04315-157">-Location</span><span class="sxs-lookup"><span data-stu-id="04315-157">-Location</span></span>
<span data-ttu-id="04315-158">Der Speicherort, an dem die Instanz erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="04315-158">The location in which to create the instance</span></span>

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

### <span data-ttu-id="04315-159">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="04315-159">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="04315-160">Die Wartungskonfigurations-ID für die verwaltete Sql Azure-Instanz.</span><span class="sxs-lookup"><span data-stu-id="04315-160">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="04315-161">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="04315-161">-MinimalTlsVersion</span></span>
<span data-ttu-id="04315-162">Die minimale TLS-Version, die für verwaltete Instanzen erzwungen werden soll</span><span class="sxs-lookup"><span data-stu-id="04315-162">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="04315-163">-Name</span><span class="sxs-lookup"><span data-stu-id="04315-163">-Name</span></span>
<span data-ttu-id="04315-164">Instanzname.</span><span class="sxs-lookup"><span data-stu-id="04315-164">Instance name.</span></span>

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

### <span data-ttu-id="04315-165">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="04315-165">-ProxyOverride</span></span>
<span data-ttu-id="04315-166">Der Verbindungstyp, der zum Herstellen einer Verbindung mit der Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="04315-166">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="04315-167">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="04315-167">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="04315-168">Gibt an, ob der öffentliche Datenendpunkt für die Instanz aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="04315-168">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="04315-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04315-169">-ResourceGroupName</span></span>
<span data-ttu-id="04315-170">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="04315-170">The name of the resource group.</span></span>

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

### <span data-ttu-id="04315-171">-SkuName</span><span class="sxs-lookup"><span data-stu-id="04315-171">-SkuName</span></span>
<span data-ttu-id="04315-172">Der Name der SKU für die Instanz, z. B. "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="04315-172">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="04315-173">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="04315-173">-StorageSizeInGB</span></span>
<span data-ttu-id="04315-174">Bestimmt, wie viel Speichergröße einer Instanz zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="04315-174">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="04315-175">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="04315-175">-SubnetId</span></span>
<span data-ttu-id="04315-176">Die Subnetz-ID, die für die Instanzerstellung verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="04315-176">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="04315-177">-Tag</span><span class="sxs-lookup"><span data-stu-id="04315-177">-Tag</span></span>
<span data-ttu-id="04315-178">Die Tags, die der Instanz zugeordnet werden sollen</span><span class="sxs-lookup"><span data-stu-id="04315-178">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="04315-179">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="04315-179">-TimezoneId</span></span>
<span data-ttu-id="04315-180">Die Zeitzonen-ID für die zu festlegende Instanz.</span><span class="sxs-lookup"><span data-stu-id="04315-180">The time zone id for the instance to set.</span></span> <span data-ttu-id="04315-181">Eine Liste der Zeitzonen-IDs wird in der sys.time_zone_info (Transact-SQL) verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="04315-181">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="04315-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="04315-182">-VCore</span></span>
<span data-ttu-id="04315-183">Bestimmt, wie viel VCore einer Instanz zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="04315-183">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="04315-184">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04315-184">-Confirm</span></span>
<span data-ttu-id="04315-185">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="04315-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04315-186">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="04315-186">-WhatIf</span></span>
<span data-ttu-id="04315-187">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04315-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04315-188">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04315-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04315-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04315-189">CommonParameters</span></span>
<span data-ttu-id="04315-190">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04315-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04315-191">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04315-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04315-192">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="04315-192">INPUTS</span></span>

### <span data-ttu-id="04315-193">Keine</span><span class="sxs-lookup"><span data-stu-id="04315-193">None</span></span>

## <span data-ttu-id="04315-194">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="04315-194">OUTPUTS</span></span>

### <span data-ttu-id="04315-195">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="04315-195">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="04315-196">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="04315-196">NOTES</span></span>

## <span data-ttu-id="04315-197">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="04315-197">RELATED LINKS</span></span>
