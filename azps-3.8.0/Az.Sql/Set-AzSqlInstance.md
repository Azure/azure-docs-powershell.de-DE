---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: e17c6b226f7ed4fe17842c93d03828d53c0bb22c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845172"
---
# <span data-ttu-id="fe0a1-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fe0a1-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="fe0a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fe0a1-102">SYNOPSIS</span></span>
<span data-ttu-id="fe0a1-103">Legt Eigenschaften für eine Azure SQL-Daten Bank verwaltete Instanz fest.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="fe0a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe0a1-104">SYNTAX</span></span>

### <span data-ttu-id="fe0a1-105">SetInstanceFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe0a1-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe0a1-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="fe0a1-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe0a1-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="fe0a1-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe0a1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe0a1-108">DESCRIPTION</span></span>
<span data-ttu-id="fe0a1-109">Das Cmdlet " **Satz-AzSqlInstance** " ändert die Eigenschaften einer Azure SQL-Datenbank-verwalteten Instanz.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="fe0a1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe0a1-110">EXAMPLES</span></span>

### <span data-ttu-id="fe0a1-111">Beispiel 1: Einrichten einer vorhandenen Instanz mit neuen Werten für-Administrator Password,-LicenseType,-StorageSizeInGB,-Vcore und-Edition</span><span class="sxs-lookup"><span data-stu-id="fe0a1-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
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

### <span data-ttu-id="fe0a1-112">Beispiel 2: Ändern der vorhandenen Instanzen Hardware Generierung mithilfe des neuen Werts für-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="fe0a1-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
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

<span data-ttu-id="fe0a1-113">Dieser Befehl legt die vorhandene Instanz mit neuen Werten für-Administrator Password,-LicenseType,-StorageSizeInGB und-Vcore fest.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="fe0a1-114">Beispiel 3: Setzen einer vorhandenen Instanz mit neuen Werten für-Administrator Password,-LicenseType,-StorageSizeInGB und-Vcore für eine Instanz innerhalb eines Instanzen Pools</span><span class="sxs-lookup"><span data-stu-id="fe0a1-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="fe0a1-115">Dieser Befehl legt die vorhandene Instanz mit neuen Werten für-Administrator Password,-LicenseType,-StorageSizeInGB und-Vcore für eine Instanz innerhalb eines Instanzen Pools fest.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="fe0a1-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe0a1-116">PARAMETERS</span></span>

### <span data-ttu-id="fe0a1-117">-Administrator Password</span><span class="sxs-lookup"><span data-stu-id="fe0a1-117">-AdministratorPassword</span></span>
<span data-ttu-id="fe0a1-118">Das neue SQL-Administratorkennwort für die Instanz.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-118">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="fe0a1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe0a1-119">-AsJob</span></span>
<span data-ttu-id="fe0a1-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fe0a1-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe0a1-121">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="fe0a1-121">-AssignIdentity</span></span>
<span data-ttu-id="fe0a1-122">Generieren Sie eine Azure Active Directory-Identität für diese Instanz, und weisen Sie Sie für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault zu.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="fe0a1-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="fe0a1-123">-ComputeGeneration</span></span>
<span data-ttu-id="fe0a1-124">Die COMPUTE-Generierung für die Instanz.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="fe0a1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe0a1-125">-DefaultProfile</span></span>
<span data-ttu-id="fe0a1-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe0a1-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="fe0a1-127">-Edition</span></span>
<span data-ttu-id="fe0a1-128">Die Edition, die der Instanz zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="fe0a1-129">-Force</span><span class="sxs-lookup"><span data-stu-id="fe0a1-129">-Force</span></span>
<span data-ttu-id="fe0a1-130">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="fe0a1-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="fe0a1-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fe0a1-131">-InputObject</span></span>
<span data-ttu-id="fe0a1-132">Das zu entfernende AzureSqlManagedInstanceModel-Objekt</span><span class="sxs-lookup"><span data-stu-id="fe0a1-132">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="fe0a1-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="fe0a1-133">-InstancePoolName</span></span>
<span data-ttu-id="fe0a1-134">Der Name des Instanz Pools.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-134">The instance pool name.</span></span>

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

### <span data-ttu-id="fe0a1-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fe0a1-135">-LicenseType</span></span>
<span data-ttu-id="fe0a1-136">Bestimmt den zu verwendenden Lizenztyp.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-136">Determines which License Type to use.</span></span> <span data-ttu-id="fe0a1-137">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="fe0a1-137">Possible values are:</span></span>
- <span data-ttu-id="fe0a1-138">Grundpr.-Azure Hybrid Benefit (AHB) Discounted Pricing für vorhandene SQL Server-Lizenzbesitzer wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="fe0a1-139">Der Service Preis für verwaltete Instanzen wird für vorhandene SQL Server-Lizenzbesitzer abgezinst.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="fe0a1-140">LicenseIncluded-Azure Hybrid Benefit (AHB) Preisnachlässe für vorhandene SQL Server-Lizenzbesitzer werden nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="fe0a1-141">Der Service Preis für verwaltete Instanzen umfasst eine neue Lizenz für SQL Server-Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="fe0a1-142">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="fe0a1-142">-MinimalTlsVersion</span></span>
<span data-ttu-id="fe0a1-143">Die minimale TLS-Version, die für verwaltete Instanzen erzwungen werden soll</span><span class="sxs-lookup"><span data-stu-id="fe0a1-143">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="fe0a1-144">-Name</span><span class="sxs-lookup"><span data-stu-id="fe0a1-144">-Name</span></span>
<span data-ttu-id="fe0a1-145">Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-145">Instance name.</span></span>

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

### <span data-ttu-id="fe0a1-146">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="fe0a1-146">-ProxyOverride</span></span>
<span data-ttu-id="fe0a1-147">Der Verbindungstyp, der für die Verbindung mit der Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-147">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="fe0a1-148">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="fe0a1-148">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="fe0a1-149">Gibt an, ob der öffentliche Daten Endpunkt für die Instanz aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-149">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="fe0a1-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe0a1-150">-ResourceGroupName</span></span>
<span data-ttu-id="fe0a1-151">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="fe0a1-152">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fe0a1-152">-ResourceId</span></span>
<span data-ttu-id="fe0a1-153">Die Ressourcen-ID der zu entfernenden Instanz</span><span class="sxs-lookup"><span data-stu-id="fe0a1-153">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="fe0a1-154">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="fe0a1-154">-StorageSizeInGB</span></span>
<span data-ttu-id="fe0a1-155">Bestimmt, wie viel Speichergröße mit der Instanz verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-155">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="fe0a1-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="fe0a1-156">-Tag</span></span>
<span data-ttu-id="fe0a1-157">Die Tags, die der Instanz zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-157">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="fe0a1-158">-VCore</span><span class="sxs-lookup"><span data-stu-id="fe0a1-158">-VCore</span></span>
<span data-ttu-id="fe0a1-159">Bestimmt, wie viel Vcore mit der Instanz verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-159">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="fe0a1-160">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fe0a1-160">-Confirm</span></span>
<span data-ttu-id="fe0a1-161">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe0a1-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe0a1-162">-WhatIf</span></span>
<span data-ttu-id="fe0a1-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe0a1-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe0a1-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe0a1-165">CommonParameters</span></span>
<span data-ttu-id="fe0a1-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe0a1-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe0a1-167">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe0a1-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe0a1-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fe0a1-168">INPUTS</span></span>

### <span data-ttu-id="fe0a1-169">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="fe0a1-169">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="fe0a1-170">System. String</span><span class="sxs-lookup"><span data-stu-id="fe0a1-170">System.String</span></span>

## <span data-ttu-id="fe0a1-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fe0a1-171">OUTPUTS</span></span>

### <span data-ttu-id="fe0a1-172">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="fe0a1-172">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="fe0a1-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="fe0a1-173">NOTES</span></span>

## <span data-ttu-id="fe0a1-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fe0a1-174">RELATED LINKS</span></span>
