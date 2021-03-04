---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 983291eda139793b2cc5d0fe5cd213b5d8cd69a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933627"
---
# <span data-ttu-id="ada24-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ada24-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="ada24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ada24-102">SYNOPSIS</span></span>
<span data-ttu-id="ada24-103">Erstellt eine sekundäre Datenbank für eine vorhandene Datenbank und startet die Datenreplikation.</span><span class="sxs-lookup"><span data-stu-id="ada24-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="ada24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ada24-104">SYNTAX</span></span>

### <span data-ttu-id="ada24-105">DtuBasedDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="ada24-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ada24-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="ada24-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ada24-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ada24-107">DESCRIPTION</span></span>
<span data-ttu-id="ada24-108">Das **Cmdlet New-AzSqlDatabaseSecondary** ersetzt das cmdlet Start-AzSqlDatabaseCopy, wenn es zum Einrichten der Georeplikation für eine Datenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ada24-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="ada24-109">Es gibt das Verknüpfungsobjekt für die Georeplikation von der primären in die sekundäre Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="ada24-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="ada24-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ada24-110">EXAMPLES</span></span>

### <span data-ttu-id="ada24-111">Beispiel 1: Einrichten eines aktiven Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="ada24-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="ada24-112">Beispiel 2: Einrichten von active Geo-Replication und Angeben des Namens der Partnerdatenbank, dass er sich vom Quelldatenbanknamen unterscheiden soll</span><span class="sxs-lookup"><span data-stu-id="ada24-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="ada24-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ada24-113">PARAMETERS</span></span>

### <span data-ttu-id="ada24-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="ada24-114">-AllowConnections</span></span>
<span data-ttu-id="ada24-115">Gibt die Leseabsicht der sekundären Azure SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="ada24-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="ada24-116">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="ada24-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ada24-117">Nein</span><span class="sxs-lookup"><span data-stu-id="ada24-117">No</span></span>
- <span data-ttu-id="ada24-118">Alle</span><span class="sxs-lookup"><span data-stu-id="ada24-118">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Replication.Model.AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada24-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ada24-119">-AsJob</span></span>
<span data-ttu-id="ada24-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ada24-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ada24-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="ada24-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="ada24-122">Die Redundanz des Sicherungsspeichers zum Speichern von Sicherungen für die SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ada24-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="ada24-123">Optionen sind: Lokal, Zone und Geo.</span><span class="sxs-lookup"><span data-stu-id="ada24-123">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="ada24-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ada24-124">-DatabaseName</span></span>
<span data-ttu-id="ada24-125">Gibt den Namen der Datenbank an, die als primär fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="ada24-125">Specifies the name of the database to act as primary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ada24-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada24-126">-DefaultProfile</span></span>
<span data-ttu-id="ada24-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ada24-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ada24-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ada24-128">-LicenseType</span></span>
<span data-ttu-id="ada24-129">Der Lizenztyp für die Azure Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ada24-129">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="ada24-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ada24-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="ada24-131">Der Name der zu erstellende sekundären Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ada24-131">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="ada24-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ada24-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="ada24-133">Gibt den Namen der Azure-Ressourcengruppe an, der dieses Cmdlet die sekundäre Datenbank zugibt.</span><span class="sxs-lookup"><span data-stu-id="ada24-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="ada24-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="ada24-134">-PartnerServerName</span></span>
<span data-ttu-id="ada24-135">Gibt den Namen des Azure SQL an, der als sekundäre Datenbankserver fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="ada24-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="ada24-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ada24-136">-ResourceGroupName</span></span>
<span data-ttu-id="ada24-137">Gibt den Namen der Azure-Ressourcengruppe an, der dieses Cmdlet die primäre Datenbank zugibt.</span><span class="sxs-lookup"><span data-stu-id="ada24-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ada24-138">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="ada24-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="ada24-139">Die Rechengenerierung der sekundären Azure Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ada24-139">The compute generation of the Azure Sql Database secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada24-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ada24-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="ada24-141">Gibt den Namen des Poolpools an, in dem die sekundäre Datenbank gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ada24-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada24-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="ada24-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="ada24-143">Gibt den Namen des Dienstziels an, das der sekundären Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ada24-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada24-144">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="ada24-144">-SecondaryType</span></span>
<span data-ttu-id="ada24-145">Der sekundäre Typ der Datenbank, wenn es sich um eine sekundäre Datenbank handelt.</span><span class="sxs-lookup"><span data-stu-id="ada24-145">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="ada24-146">Gültige Werte sind "Geo" und "Named".</span><span class="sxs-lookup"><span data-stu-id="ada24-146">Valid values are Geo and Named.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Named, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada24-147">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="ada24-147">-SecondaryVCore</span></span>
<span data-ttu-id="ada24-148">Die Vcore-Nummern der sekundären Azure Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ada24-148">The Vcore numbers of the Azure Sql Database secondary.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada24-149">-Servername</span><span class="sxs-lookup"><span data-stu-id="ada24-149">-ServerName</span></span>
<span data-ttu-id="ada24-150">Gibt den Namen der SQL Server der primären Datenbank SQL an.</span><span class="sxs-lookup"><span data-stu-id="ada24-150">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ada24-151">-Tags</span><span class="sxs-lookup"><span data-stu-id="ada24-151">-Tags</span></span>
<span data-ttu-id="ada24-152">Gibt die Schlüssel-Wert-Paare in Form einer Hashtabelle an, die dem Link SQL Datenbankreplikation zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ada24-152">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="ada24-153">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="ada24-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada24-154">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ada24-154">-Confirm</span></span>
<span data-ttu-id="ada24-155">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ada24-155">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada24-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ada24-156">-WhatIf</span></span>
<span data-ttu-id="ada24-157">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ada24-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ada24-158">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ada24-158">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada24-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada24-159">CommonParameters</span></span>
<span data-ttu-id="ada24-160">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ada24-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada24-161">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ada24-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada24-162">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ada24-162">INPUTS</span></span>

### <span data-ttu-id="ada24-163">System.String</span><span class="sxs-lookup"><span data-stu-id="ada24-163">System.String</span></span>

## <span data-ttu-id="ada24-164">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ada24-164">OUTPUTS</span></span>

### <span data-ttu-id="ada24-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="ada24-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="ada24-166">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ada24-166">NOTES</span></span>

## <span data-ttu-id="ada24-167">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ada24-167">RELATED LINKS</span></span>

[<span data-ttu-id="ada24-168">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ada24-168">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="ada24-169">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ada24-169">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="ada24-170">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="ada24-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
