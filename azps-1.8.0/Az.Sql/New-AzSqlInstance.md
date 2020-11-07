---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: bfa1785004e13400395bd6a6fc93bdec29a69809
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659097"
---
# <span data-ttu-id="29e91-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="29e91-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="29e91-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29e91-102">SYNOPSIS</span></span>
<span data-ttu-id="29e91-103">Erstellt eine Azure SQL-Daten Bank verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="29e91-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="29e91-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29e91-104">SYNTAX</span></span>

### <span data-ttu-id="29e91-105">NewByEditionAndComputeGenerationParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="29e91-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29e91-106">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="29e91-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29e91-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29e91-107">DESCRIPTION</span></span>
<span data-ttu-id="29e91-108">Das Cmdlet **New-AzSqlInstance** erstellt eine verwaltete Azure SQL-Datenbank-Instanz.</span><span class="sxs-lookup"><span data-stu-id="29e91-108">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="29e91-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29e91-109">EXAMPLES</span></span>

### <span data-ttu-id="29e91-110">Beispiel 1: Erstellen einer neuen Instanz</span><span class="sxs-lookup"><span data-stu-id="29e91-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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
```

<span data-ttu-id="29e91-111">Mit diesem Befehl wird eine neue Instanz mithilfe von Edition-und ComputeGeneration-Parametern erstellt.</span><span class="sxs-lookup"><span data-stu-id="29e91-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="29e91-112">Beispiel 2: Erstellen einer neuen Instanz</span><span class="sxs-lookup"><span data-stu-id="29e91-112">Example 2: Create a new instance</span></span>
```
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
```

<span data-ttu-id="29e91-113">Dieser Befehl erstellt eine neue Instanz mithilfe von Edition-und ComputeGeneration-Parametern.</span><span class="sxs-lookup"><span data-stu-id="29e91-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="29e91-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="29e91-114">PARAMETERS</span></span>

### <span data-ttu-id="29e91-115">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="29e91-115">-AdministratorCredential</span></span>
<span data-ttu-id="29e91-116">Die SQL-Authentifizierungsanmeldeinformationen der Instanz.</span><span class="sxs-lookup"><span data-stu-id="29e91-116">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="29e91-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29e91-117">-AsJob</span></span>
<span data-ttu-id="29e91-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="29e91-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29e91-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="29e91-119">-AssignIdentity</span></span>
<span data-ttu-id="29e91-120">Generieren Sie eine Azure Active Directory-Identität für diese verwaltete Instanz, und weisen Sie Sie für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault zu.</span><span class="sxs-lookup"><span data-stu-id="29e91-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="29e91-121">-Sortierung</span><span class="sxs-lookup"><span data-stu-id="29e91-121">-Collation</span></span>
<span data-ttu-id="29e91-122">Die Sortierung der zu verwendenden Azure SQL-Instanz.</span><span class="sxs-lookup"><span data-stu-id="29e91-122">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="29e91-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="29e91-123">-ComputeGeneration</span></span>
<span data-ttu-id="29e91-124">Die COMPUTE-Generierung für die Instanz.</span><span class="sxs-lookup"><span data-stu-id="29e91-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="29e91-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29e91-125">-DefaultProfile</span></span>
<span data-ttu-id="29e91-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="29e91-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29e91-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="29e91-127">-Edition</span></span>
<span data-ttu-id="29e91-128">Die Edition für die Instanz.</span><span class="sxs-lookup"><span data-stu-id="29e91-128">The edition for the instance.</span></span>

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

### <span data-ttu-id="29e91-129">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="29e91-129">-LicenseType</span></span>
<span data-ttu-id="29e91-130">Bestimmt den zu verwendenden Lizenztyp.</span><span class="sxs-lookup"><span data-stu-id="29e91-130">Determines which License Type to use.</span></span> <span data-ttu-id="29e91-131">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="29e91-131">Possible values are:</span></span>
- <span data-ttu-id="29e91-132">Grundpr.-Azure Hybrid Benefit (AHB) Discounted Pricing für vorhandene SQL Server-Lizenzbesitzer wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="29e91-132">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="29e91-133">Der Service Preis für verwaltete Instanzen wird für vorhandene SQL Server-Lizenzbesitzer abgezinst.</span><span class="sxs-lookup"><span data-stu-id="29e91-133">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="29e91-134">LicenseIncluded-Azure Hybrid Benefit (AHB) Preisnachlässe für vorhandene SQL Server-Lizenzbesitzer werden nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="29e91-134">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="29e91-135">Der Service Preis für verwaltete Instanzen umfasst eine neue Lizenz für SQL Server-Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="29e91-135">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29e91-136">-Standort</span><span class="sxs-lookup"><span data-stu-id="29e91-136">-Location</span></span>
<span data-ttu-id="29e91-137">Die Position, an der die Instanz erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="29e91-137">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29e91-138">-Name</span><span class="sxs-lookup"><span data-stu-id="29e91-138">-Name</span></span>
<span data-ttu-id="29e91-139">Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="29e91-139">Instance name.</span></span>

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

### <span data-ttu-id="29e91-140">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="29e91-140">-ProxyOverride</span></span>
<span data-ttu-id="29e91-141">Der Verbindungstyp, der für die Verbindung mit der Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="29e91-141">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="29e91-142">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="29e91-142">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="29e91-143">Gibt an, ob der öffentliche Daten Endpunkt für die Instanz aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="29e91-143">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="29e91-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29e91-144">-ResourceGroupName</span></span>
<span data-ttu-id="29e91-145">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="29e91-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29e91-146">-SkuName</span><span class="sxs-lookup"><span data-stu-id="29e91-146">-SkuName</span></span>
<span data-ttu-id="29e91-147">Der SKU-Name für die Instanz, beispielsweise "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="29e91-147">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="29e91-148">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="29e91-148">-StorageSizeInGB</span></span>
<span data-ttu-id="29e91-149">Bestimmt, wie viel Speichergröße mit der Instanz verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="29e91-149">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="29e91-150">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="29e91-150">-SubnetId</span></span>
<span data-ttu-id="29e91-151">Die für die Erstellung von Instanzen zu verwendende Subnetz-ID</span><span class="sxs-lookup"><span data-stu-id="29e91-151">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29e91-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="29e91-152">-Tag</span></span>
<span data-ttu-id="29e91-153">Die Tags, die der Instanz zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="29e91-153">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="29e91-154">-Zeitzonen-Nr.</span><span class="sxs-lookup"><span data-stu-id="29e91-154">-TimezoneId</span></span>
<span data-ttu-id="29e91-155">Die Zeit Zonen-ID für die Instanz, die gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="29e91-155">The time zone id for the instance to set.</span></span> <span data-ttu-id="29e91-156">Eine Liste der Zeit Zonen-IDs wird über die sys.time_zone_info (Transact-SQL)-Ansicht verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="29e91-156">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="29e91-157">-VCore</span><span class="sxs-lookup"><span data-stu-id="29e91-157">-VCore</span></span>
<span data-ttu-id="29e91-158">Bestimmt, wie viel Vcore mit der Instanz verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="29e91-158">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="29e91-159">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29e91-159">-Confirm</span></span>
<span data-ttu-id="29e91-160">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29e91-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29e91-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29e91-161">-WhatIf</span></span>
<span data-ttu-id="29e91-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29e91-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29e91-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29e91-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29e91-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e91-164">CommonParameters</span></span>
<span data-ttu-id="29e91-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29e91-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e91-166">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29e91-166">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e91-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29e91-167">INPUTS</span></span>

### <span data-ttu-id="29e91-168">Keine</span><span class="sxs-lookup"><span data-stu-id="29e91-168">None</span></span>

## <span data-ttu-id="29e91-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29e91-169">OUTPUTS</span></span>

### <span data-ttu-id="29e91-170">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="29e91-170">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="29e91-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="29e91-171">NOTES</span></span>

## <span data-ttu-id="29e91-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29e91-172">RELATED LINKS</span></span>
