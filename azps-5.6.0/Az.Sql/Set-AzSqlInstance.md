---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: a6dd059b7fdab3c2670e3b8902def148d88124d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950547"
---
# <span data-ttu-id="e38ed-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e38ed-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="e38ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e38ed-102">SYNOPSIS</span></span>
<span data-ttu-id="e38ed-103">Legt Eigenschaften für eine verwaltete Azure SQL-Datenbankinstanz fest.</span><span class="sxs-lookup"><span data-stu-id="e38ed-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="e38ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e38ed-104">SYNTAX</span></span>

### <span data-ttu-id="e38ed-105">SetInstanceFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="e38ed-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e38ed-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e38ed-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e38ed-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="e38ed-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-MaintenanceConfigurationId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e38ed-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e38ed-108">DESCRIPTION</span></span>
<span data-ttu-id="e38ed-109">Das **Cmdlet Set-AzSqlInstance** ändert die Eigenschaften einer Azure SQL Datenbank verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="e38ed-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="e38ed-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e38ed-110">EXAMPLES</span></span>

### <span data-ttu-id="e38ed-111">Beispiel 1: Festlegen einer vorhandenen Instanz mit neuen Werten für -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore und -Edition</span><span class="sxs-lookup"><span data-stu-id="e38ed-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition BusinessCritical
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
InstancePoolName         :
```

### <span data-ttu-id="e38ed-112">Beispiel 2: Ändern der vorhandenen Instanzhardwaregenerierung mithilfe eines neuen Werts für -ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="e38ed-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -ComputeGeneration Gen5
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
InstancePoolName         :
```

<span data-ttu-id="e38ed-113">Mit diesem Befehl werden vorhandene Instanzen mit neuen Werten für -AdministratorPassword, -LicenseType, -StorageSizeInGB und -VCore festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e38ed-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="e38ed-114">Beispiel 3: Festlegen vorhandener Instanzen mit neuen Werten für -AdministratorPassword, -LicenseType, -StorageSizeInGB und -VCore für eine Instanz in einem Instanzpool</span><span class="sxs-lookup"><span data-stu-id="e38ed-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolName instancePool0
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
StorageSizeInGB          : 1024
InstancePoolName         : instancePool0
```

<span data-ttu-id="e38ed-115">Mit diesem Befehl werden vorhandene Instanzen mit neuen Werten für -AdministratorPassword, -LicenseType, -StorageSizeInGB und -VCore für eine Instanz in einem Instanzpool festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e38ed-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

### <span data-ttu-id="e38ed-116">Beispiel 4: Aktualisieren der Wartungskonfiguration für vorhandene Instanzen</span><span class="sxs-lookup"><span data-stu-id="e38ed-116">Example 4: Update maintenance configuration for existing instance</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "resourcegroup01" -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2"
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

<span data-ttu-id="e38ed-117">Mit diesem Befehl wird die vorhandene Instanz mit Wartungskonfigurationseinstellungen MI_2</span><span class="sxs-lookup"><span data-stu-id="e38ed-117">This command updates existing instance with maintenance configuration MI_2</span></span>

### <span data-ttu-id="e38ed-118">Beispiel 5: Entfernen der Wartungskonfiguration aus einer vorhandenen Instanz</span><span class="sxs-lookup"><span data-stu-id="e38ed-118">Example 5: Remove maintenance configuration from existing instance</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managediInstance1" -ResourceGroupName "Resourcegroup01" -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_Default"
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
MaintenanceConfigurationId : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_Default
```

<span data-ttu-id="e38ed-119">Dieser Befehl setzt die Wartungskonfiguration auf die Standardeinstellung für vorhandene Instanzen zurück.</span><span class="sxs-lookup"><span data-stu-id="e38ed-119">This command resets maintenance configuration to default for existing instance</span></span>

## <span data-ttu-id="e38ed-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e38ed-120">PARAMETERS</span></span>

### <span data-ttu-id="e38ed-121">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="e38ed-121">-AdministratorPassword</span></span>
<span data-ttu-id="e38ed-122">Das neue SQL Administratorkennwort für die -Instanz.</span><span class="sxs-lookup"><span data-stu-id="e38ed-122">The new SQL administrator password for the instance.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38ed-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e38ed-123">-AsJob</span></span>
<span data-ttu-id="e38ed-124">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e38ed-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e38ed-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e38ed-125">-AssignIdentity</span></span>
<span data-ttu-id="e38ed-126">Generieren und zuweisen Sie eine Azure Active Directory-Identität für diese Instanz für die Verwendung mit wichtigen Verwaltungsdiensten wie Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="e38ed-126">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="e38ed-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="e38ed-127">-ComputeGeneration</span></span>
<span data-ttu-id="e38ed-128">Die Computegenerierung für die -Instanz.</span><span class="sxs-lookup"><span data-stu-id="e38ed-128">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="e38ed-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e38ed-129">-DefaultProfile</span></span>
<span data-ttu-id="e38ed-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e38ed-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e38ed-131">-Edition</span><span class="sxs-lookup"><span data-stu-id="e38ed-131">-Edition</span></span>
<span data-ttu-id="e38ed-132">Die Edition, die der -Instanz zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e38ed-132">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="e38ed-133">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="e38ed-133">-Force</span></span>
<span data-ttu-id="e38ed-134">Bestätigungsmeldung überspringen zum Ausführen der Aktion</span><span class="sxs-lookup"><span data-stu-id="e38ed-134">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="e38ed-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e38ed-135">-InputObject</span></span>
<span data-ttu-id="e38ed-136">Das zu entfernende AzureSqlManagedInstanceModel-Objekt</span><span class="sxs-lookup"><span data-stu-id="e38ed-136">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e38ed-137">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="e38ed-137">-InstancePoolName</span></span>
<span data-ttu-id="e38ed-138">Der Name des Instanzpools.</span><span class="sxs-lookup"><span data-stu-id="e38ed-138">The instance pool name.</span></span>

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

### <span data-ttu-id="e38ed-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e38ed-139">-LicenseType</span></span>
<span data-ttu-id="e38ed-140">Bestimmt, welcher Lizenztyp verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e38ed-140">Determines which License Type to use.</span></span> <span data-ttu-id="e38ed-141">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="e38ed-141">Possible values are:</span></span>
- <span data-ttu-id="e38ed-142">BasePrice – AhB(Azure Hybrid Benefit)-rabattierte Preise für vorhandene SQL Server werden angewendet.</span><span class="sxs-lookup"><span data-stu-id="e38ed-142">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="e38ed-143">Der Servicepreis für verwaltete Instanzen wird für vorhandene Besitzer SQL Server reduziert.</span><span class="sxs-lookup"><span data-stu-id="e38ed-143">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="e38ed-144">LicenseIncluded – Rabattpreise für Azure Hybrid Benefit (AHB) für vorhandene SQL Server Lizenzbesitzer werden nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="e38ed-144">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="e38ed-145">Der Preis für den Dienst für verwaltete Instanzen enthält eine neue SQL Server Lizenzkosten.</span><span class="sxs-lookup"><span data-stu-id="e38ed-145">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="e38ed-146">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e38ed-146">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="e38ed-147">Die Wartungskonfigurations-ID für die verwaltete Sql Azure-Instanz.</span><span class="sxs-lookup"><span data-stu-id="e38ed-147">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="e38ed-148">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="e38ed-148">-MinimalTlsVersion</span></span>
<span data-ttu-id="e38ed-149">Die minimale TLS-Version, die für verwaltete Instanzen erzwungen werden soll</span><span class="sxs-lookup"><span data-stu-id="e38ed-149">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="e38ed-150">-Name</span><span class="sxs-lookup"><span data-stu-id="e38ed-150">-Name</span></span>
<span data-ttu-id="e38ed-151">Instanzname.</span><span class="sxs-lookup"><span data-stu-id="e38ed-151">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38ed-152">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="e38ed-152">-ProxyOverride</span></span>
<span data-ttu-id="e38ed-153">Der Verbindungstyp, der zum Herstellen einer Verbindung mit der -Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e38ed-153">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="e38ed-154">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="e38ed-154">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="e38ed-155">Gibt an, ob der öffentliche Datenendpunkt für die -Instanz aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e38ed-155">Whether or not the public data endpoint is enabled for the instance.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38ed-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e38ed-156">-ResourceGroupName</span></span>
<span data-ttu-id="e38ed-157">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e38ed-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38ed-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e38ed-158">-ResourceId</span></span>
<span data-ttu-id="e38ed-159">Die Ressourcen-ID der zu entfernende Instanz</span><span class="sxs-lookup"><span data-stu-id="e38ed-159">The resource id of instance to remove</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e38ed-160">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="e38ed-160">-StorageSizeInGB</span></span>
<span data-ttu-id="e38ed-161">Bestimmt, wie viel Speichergröße einer Instanz zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="e38ed-161">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="e38ed-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="e38ed-162">-Tag</span></span>
<span data-ttu-id="e38ed-163">Die Tags, die der -Instanz zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e38ed-163">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="e38ed-164">-VCore</span><span class="sxs-lookup"><span data-stu-id="e38ed-164">-VCore</span></span>
<span data-ttu-id="e38ed-165">Bestimmt, wie viel VCore einer Instanz zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="e38ed-165">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="e38ed-166">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e38ed-166">-Confirm</span></span>
<span data-ttu-id="e38ed-167">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e38ed-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e38ed-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e38ed-168">-WhatIf</span></span>
<span data-ttu-id="e38ed-169">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e38ed-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e38ed-170">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e38ed-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e38ed-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e38ed-171">CommonParameters</span></span>
<span data-ttu-id="e38ed-172">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e38ed-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e38ed-173">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e38ed-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e38ed-174">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e38ed-174">INPUTS</span></span>

### <span data-ttu-id="e38ed-175">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="e38ed-175">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="e38ed-176">System.String</span><span class="sxs-lookup"><span data-stu-id="e38ed-176">System.String</span></span>

## <span data-ttu-id="e38ed-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e38ed-177">OUTPUTS</span></span>

### <span data-ttu-id="e38ed-178">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="e38ed-178">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="e38ed-179">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e38ed-179">NOTES</span></span>

## <span data-ttu-id="e38ed-180">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e38ed-180">RELATED LINKS</span></span>
