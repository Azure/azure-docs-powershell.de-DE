---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: f16e6f2dcbcf3ebd16926784ca84eef02740df7b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163196"
---
# <span data-ttu-id="38c84-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="38c84-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="38c84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38c84-102">SYNOPSIS</span></span>
<span data-ttu-id="38c84-103">Legt Eigenschaften für eine verwaltete Azure SQL-Datenbankinstanz fest.</span><span class="sxs-lookup"><span data-stu-id="38c84-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="38c84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38c84-104">SYNTAX</span></span>

### <span data-ttu-id="38c84-105">SetInstanceFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="38c84-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38c84-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="38c84-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38c84-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="38c84-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-MaintenanceConfigurationId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38c84-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38c84-108">DESCRIPTION</span></span>
<span data-ttu-id="38c84-109">Das **Cmdlet "Set-AzSqlInstance"** ändert die Eigenschaften einer Azure SQL-Datenbank-verwalteten Instanz.</span><span class="sxs-lookup"><span data-stu-id="38c84-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="38c84-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38c84-110">EXAMPLES</span></span>

### <span data-ttu-id="38c84-111">Beispiel 1: Festlegen einer vorhandenen Instanz mit neuen Werten für -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore und -Edition</span><span class="sxs-lookup"><span data-stu-id="38c84-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
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

### <span data-ttu-id="38c84-112">Beispiel 2: Ändern der vorhandenen Instanzhardwaregenerierung mit einem neuen Wert für "-ComputeGeneration"</span><span class="sxs-lookup"><span data-stu-id="38c84-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
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

<span data-ttu-id="38c84-113">Mit diesem Befehl wird eine vorhandene Instanz mit neuen Werten für "-AdministratorPassword", "-LicenseType", "-StorageSizeInGB" und "-VCore" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="38c84-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="38c84-114">Beispiel 3: Festlegen einer vorhandenen Instanz mit neuen Werten für "-AdministratorPassword", "-LicenseType", "-StorageSizeInGB" und "-VCore" für eine Instanz in einem Instanzpool</span><span class="sxs-lookup"><span data-stu-id="38c84-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="38c84-115">Dieser Befehl legt eine vorhandene Instanz mithilfe neuer Werte für "-AdministratorPassword", "-LicenseType", "-StorageSizeInGB" und "-VCore" für eine Instanz in einem Instanzpool fest.</span><span class="sxs-lookup"><span data-stu-id="38c84-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="38c84-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38c84-116">PARAMETERS</span></span>

### <span data-ttu-id="38c84-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="38c84-117">-AdministratorPassword</span></span>
<span data-ttu-id="38c84-118">Das neue SQL Administratorkennwort für die Instanz.</span><span class="sxs-lookup"><span data-stu-id="38c84-118">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="38c84-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38c84-119">-AsJob</span></span>
<span data-ttu-id="38c84-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="38c84-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38c84-121">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="38c84-121">-AssignIdentity</span></span>
<span data-ttu-id="38c84-122">Generieren und zuweisen Sie eine Azure Active Directory-Identität für diese Instanz zur Verwendung mit Schlüsselverwaltungsdiensten wie Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="38c84-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="38c84-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="38c84-123">-ComputeGeneration</span></span>
<span data-ttu-id="38c84-124">Die Rechengenerierung für die Instanz.</span><span class="sxs-lookup"><span data-stu-id="38c84-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="38c84-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c84-125">-DefaultProfile</span></span>
<span data-ttu-id="38c84-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38c84-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38c84-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="38c84-127">-Edition</span></span>
<span data-ttu-id="38c84-128">Die Edition, die der Instanz zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="38c84-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="38c84-129">-Force</span><span class="sxs-lookup"><span data-stu-id="38c84-129">-Force</span></span>
<span data-ttu-id="38c84-130">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="38c84-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="38c84-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38c84-131">-InputObject</span></span>
<span data-ttu-id="38c84-132">Das zu entfernende AzureSqlManagedInstanceModel-Objekt</span><span class="sxs-lookup"><span data-stu-id="38c84-132">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="38c84-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="38c84-133">-InstancePoolName</span></span>
<span data-ttu-id="38c84-134">Der Name des Instanzpools.</span><span class="sxs-lookup"><span data-stu-id="38c84-134">The instance pool name.</span></span>

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

### <span data-ttu-id="38c84-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="38c84-135">-LicenseType</span></span>
<span data-ttu-id="38c84-136">Bestimmt, welcher Lizenztyp verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="38c84-136">Determines which License Type to use.</span></span> <span data-ttu-id="38c84-137">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="38c84-137">Possible values are:</span></span>
- <span data-ttu-id="38c84-138">BasePrice – Reduzierte Preise für Azure Hybrid Benefit (AHB) für vorhandene SQL Server Lizenzbesitzer werden angewendet.</span><span class="sxs-lookup"><span data-stu-id="38c84-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="38c84-139">Der Dienstpreis für verwaltete Instanzen wird für vorhandene Besitzer SQL Server Instanz vergünstigt.</span><span class="sxs-lookup"><span data-stu-id="38c84-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="38c84-140">LicenseIncluded – Rabatte für Azure Hybrid Benefit (AHB) für vorhandene SQL Server lizenzbesitzer werden nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="38c84-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="38c84-141">Der Preis für verwaltete Instanzdienste enthält eine neue SQL Server Lizenzkosten.</span><span class="sxs-lookup"><span data-stu-id="38c84-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="38c84-142">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="38c84-142">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="38c84-143">Die Wartungskonfigurations-ID für die verwaltete Sql Azure-Instanz.</span><span class="sxs-lookup"><span data-stu-id="38c84-143">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="38c84-144">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="38c84-144">-MinimalTlsVersion</span></span>
<span data-ttu-id="38c84-145">Die minimale TLS-Version, die für verwaltete Instanzen erzwungen werden soll</span><span class="sxs-lookup"><span data-stu-id="38c84-145">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="38c84-146">-Name</span><span class="sxs-lookup"><span data-stu-id="38c84-146">-Name</span></span>
<span data-ttu-id="38c84-147">Instanzname.</span><span class="sxs-lookup"><span data-stu-id="38c84-147">Instance name.</span></span>

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

### <span data-ttu-id="38c84-148">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="38c84-148">-ProxyOverride</span></span>
<span data-ttu-id="38c84-149">Der Verbindungstyp, der zum Herstellen einer Verbindung mit der Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="38c84-149">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="38c84-150">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="38c84-150">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="38c84-151">Gibt an, ob der öffentliche Datenendpunkt für die Instanz aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="38c84-151">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="38c84-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38c84-152">-ResourceGroupName</span></span>
<span data-ttu-id="38c84-153">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="38c84-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="38c84-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38c84-154">-ResourceId</span></span>
<span data-ttu-id="38c84-155">Die Ressourcen-ID der zu entfernende Instanz</span><span class="sxs-lookup"><span data-stu-id="38c84-155">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="38c84-156">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="38c84-156">-StorageSizeInGB</span></span>
<span data-ttu-id="38c84-157">Bestimmt, wie viel Speichergröße einer Instanz zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="38c84-157">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="38c84-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="38c84-158">-Tag</span></span>
<span data-ttu-id="38c84-159">Die Tags, die der Instanz zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="38c84-159">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="38c84-160">-VCore</span><span class="sxs-lookup"><span data-stu-id="38c84-160">-VCore</span></span>
<span data-ttu-id="38c84-161">Bestimmt, wie viel VCore einer Instanz zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="38c84-161">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="38c84-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38c84-162">-Confirm</span></span>
<span data-ttu-id="38c84-163">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="38c84-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38c84-164">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="38c84-164">-WhatIf</span></span>
<span data-ttu-id="38c84-165">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38c84-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38c84-166">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38c84-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38c84-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c84-167">CommonParameters</span></span>
<span data-ttu-id="38c84-168">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38c84-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c84-169">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38c84-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c84-170">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38c84-170">INPUTS</span></span>

### <span data-ttu-id="38c84-171">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="38c84-171">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="38c84-172">System.String</span><span class="sxs-lookup"><span data-stu-id="38c84-172">System.String</span></span>

## <span data-ttu-id="38c84-173">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38c84-173">OUTPUTS</span></span>

### <span data-ttu-id="38c84-174">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="38c84-174">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="38c84-175">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="38c84-175">NOTES</span></span>

## <span data-ttu-id="38c84-176">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="38c84-176">RELATED LINKS</span></span>
