---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 0b0934ffe9a5721ff08438ca7a24d97e2b4a34cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177187"
---
# <span data-ttu-id="c3711-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c3711-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="c3711-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3711-102">SYNOPSIS</span></span>
<span data-ttu-id="c3711-103">Erstellt eine sekundäre Datenbank für eine vorhandene Datenbank und startet die Datenreplikation.</span><span class="sxs-lookup"><span data-stu-id="c3711-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="c3711-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3711-104">SYNTAX</span></span>

### <span data-ttu-id="c3711-105">DtuBasedDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3711-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3711-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="c3711-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3711-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3711-107">DESCRIPTION</span></span>
<span data-ttu-id="c3711-108">Das Cmdlet **New-AzSqlDatabaseSecondary** ersetzt das Start-AzSqlDatabaseCopy-Cmdlet, wenn es für die Einrichtung der Geo-Replikation für eine Datenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3711-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="c3711-109">Sie gibt das Objekt für die Geo-Replikationsverknüpfung von der primären zur sekundären Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="c3711-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="c3711-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3711-110">EXAMPLES</span></span>

### <span data-ttu-id="c3711-111">Beispiel 1: Einrichten einer aktiven Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="c3711-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="c3711-112">Beispiel 2: Einrichten einer aktiven Geo-Replication und angeben des Partnerdaten Banknamens, der sich von dem Namen der Quelldatenbank unterscheiden soll</span><span class="sxs-lookup"><span data-stu-id="c3711-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="c3711-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3711-113">PARAMETERS</span></span>

### <span data-ttu-id="c3711-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="c3711-114">-AllowConnections</span></span>
<span data-ttu-id="c3711-115">Gibt die Lese Absicht der sekundären Azure SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="c3711-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="c3711-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3711-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c3711-117">Nein</span><span class="sxs-lookup"><span data-stu-id="c3711-117">No</span></span>
- <span data-ttu-id="c3711-118">Alle</span><span class="sxs-lookup"><span data-stu-id="c3711-118">All</span></span>

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

### <span data-ttu-id="c3711-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3711-119">-AsJob</span></span>
<span data-ttu-id="c3711-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c3711-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3711-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="c3711-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="c3711-122">Die Backup-Speicherredundanz, die zum Speichern von Sicherungen für die SQL-Datenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3711-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="c3711-123">Die Optionen sind: local, Zone und Geo.</span><span class="sxs-lookup"><span data-stu-id="c3711-123">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="c3711-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c3711-124">-DatabaseName</span></span>
<span data-ttu-id="c3711-125">Gibt den Namen der Datenbank an, die als primäre Datenbank fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="c3711-125">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="c3711-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3711-126">-DefaultProfile</span></span>
<span data-ttu-id="c3711-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c3711-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3711-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c3711-128">-LicenseType</span></span>
<span data-ttu-id="c3711-129">Der Lizenztyp für die Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c3711-129">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="c3711-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c3711-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="c3711-131">Der Name der sekundären Datenbank, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3711-131">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="c3711-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3711-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="c3711-133">Gibt den Namen der Azure-Ressourcengruppe an, der das Cmdlet die sekundäre Datenbank zuweist.</span><span class="sxs-lookup"><span data-stu-id="c3711-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="c3711-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="c3711-134">-PartnerServerName</span></span>
<span data-ttu-id="c3711-135">Gibt den Namen des Azure SQL-Datenbankservers an, der als sekundär fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="c3711-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="c3711-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3711-136">-ResourceGroupName</span></span>
<span data-ttu-id="c3711-137">Gibt den Namen der Azure-Ressourcengruppe an, der dieses Cmdlet die primäre Datenbank zuweist.</span><span class="sxs-lookup"><span data-stu-id="c3711-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="c3711-138">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="c3711-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="c3711-139">Die COMPUTE-Generierung der Azure SQL-Datenbank sekundär.</span><span class="sxs-lookup"><span data-stu-id="c3711-139">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="c3711-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c3711-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="c3711-141">Gibt den Namen des elastischen Pools an, in dem die sekundäre Datenbank abgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3711-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="c3711-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="c3711-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="c3711-143">Gibt den Namen des Dienst Ziels an, das der sekundären Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3711-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="c3711-144">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="c3711-144">-SecondaryVCore</span></span>
<span data-ttu-id="c3711-145">Die Vcore-Nummern der Azure SQL-Datenbank sekundär.</span><span class="sxs-lookup"><span data-stu-id="c3711-145">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="c3711-146">-Servername</span><span class="sxs-lookup"><span data-stu-id="c3711-146">-ServerName</span></span>
<span data-ttu-id="c3711-147">Gibt den Namen des SQL-Servers der primären SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="c3711-147">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="c3711-148">-Tags</span><span class="sxs-lookup"><span data-stu-id="c3711-148">-Tags</span></span>
<span data-ttu-id="c3711-149">Gibt die Schlüssel-Wert-Paare in Form einer Hashtabelle an, die mit der SQL-Datenbank-Replikationsverknüpfung verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3711-149">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="c3711-150">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="c3711-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c3711-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3711-151">-Confirm</span></span>
<span data-ttu-id="c3711-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3711-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3711-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3711-153">-WhatIf</span></span>
<span data-ttu-id="c3711-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3711-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3711-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3711-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3711-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3711-156">CommonParameters</span></span>
<span data-ttu-id="c3711-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3711-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3711-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3711-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3711-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3711-159">INPUTS</span></span>

### <span data-ttu-id="c3711-160">System. String</span><span class="sxs-lookup"><span data-stu-id="c3711-160">System.String</span></span>

## <span data-ttu-id="c3711-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3711-161">OUTPUTS</span></span>

### <span data-ttu-id="c3711-162">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="c3711-162">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="c3711-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3711-163">NOTES</span></span>

## <span data-ttu-id="c3711-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3711-164">RELATED LINKS</span></span>

[<span data-ttu-id="c3711-165">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c3711-165">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="c3711-166">Satz-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c3711-166">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="c3711-167">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="c3711-167">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
