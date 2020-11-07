---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: e39239b7434d61642ad5fcfc1f487ac5bbc5829a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659101"
---
# <span data-ttu-id="f345d-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f345d-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="f345d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f345d-102">SYNOPSIS</span></span>
<span data-ttu-id="f345d-103">Erstellt eine sekundäre Datenbank für eine vorhandene Datenbank und startet die Datenreplikation.</span><span class="sxs-lookup"><span data-stu-id="f345d-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="f345d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f345d-104">SYNTAX</span></span>

### <span data-ttu-id="f345d-105">DtuBasedDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="f345d-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-LicenseType <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f345d-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="f345d-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f345d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f345d-107">DESCRIPTION</span></span>
<span data-ttu-id="f345d-108">Das Cmdlet **New-AzSqlDatabaseSecondary** ersetzt das Start-AzSqlDatabaseCopy-Cmdlet, wenn es für die Einrichtung der Geo-Replikation für eine Datenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f345d-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="f345d-109">Sie gibt das Objekt für die Geo-Replikationsverknüpfung von der primären zur sekundären Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="f345d-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="f345d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f345d-110">EXAMPLES</span></span>

### <span data-ttu-id="f345d-111">1: Einrichten einer aktiven Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="f345d-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="f345d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f345d-112">PARAMETERS</span></span>

### <span data-ttu-id="f345d-113">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="f345d-113">-AllowConnections</span></span>
<span data-ttu-id="f345d-114">Gibt die Lese Absicht der sekundären Azure SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="f345d-114">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="f345d-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f345d-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f345d-116">Nein</span><span class="sxs-lookup"><span data-stu-id="f345d-116">No</span></span>
- <span data-ttu-id="f345d-117">Alle</span><span class="sxs-lookup"><span data-stu-id="f345d-117">All</span></span>

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

### <span data-ttu-id="f345d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f345d-118">-AsJob</span></span>
<span data-ttu-id="f345d-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f345d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f345d-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f345d-120">-DatabaseName</span></span>
<span data-ttu-id="f345d-121">Gibt den Namen der Datenbank an, die als primäre Datenbank fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="f345d-121">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="f345d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f345d-122">-DefaultProfile</span></span>
<span data-ttu-id="f345d-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f345d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f345d-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f345d-124">-LicenseType</span></span>
<span data-ttu-id="f345d-125">Der Lizenztyp für die Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f345d-125">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="f345d-126">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f345d-126">-PartnerResourceGroupName</span></span>
<span data-ttu-id="f345d-127">Gibt den Namen der Azure-Ressourcengruppe an, der das Cmdlet die sekundäre Datenbank zuweist.</span><span class="sxs-lookup"><span data-stu-id="f345d-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="f345d-128">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="f345d-128">-PartnerServerName</span></span>
<span data-ttu-id="f345d-129">Gibt den Namen des Azure SQL-Datenbankservers an, der als sekundär fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="f345d-129">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="f345d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f345d-130">-ResourceGroupName</span></span>
<span data-ttu-id="f345d-131">Gibt den Namen der Azure-Ressourcengruppe an, der dieses Cmdlet die primäre Datenbank zuweist.</span><span class="sxs-lookup"><span data-stu-id="f345d-131">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="f345d-132">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="f345d-132">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="f345d-133">Die COMPUTE-Generierung der Azure SQL-Datenbank sekundär.</span><span class="sxs-lookup"><span data-stu-id="f345d-133">The compute generation of teh Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="f345d-134">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f345d-134">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="f345d-135">Gibt den Namen des elastischen Pools an, in dem die sekundäre Datenbank abgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f345d-135">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="f345d-136">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="f345d-136">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="f345d-137">Gibt den Namen des Dienst Ziels an, das der sekundären Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f345d-137">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="f345d-138">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="f345d-138">-SecondaryVCore</span></span>
<span data-ttu-id="f345d-139">Die Vcore-Nummern der Azure SQL-Datenbank sekundär.</span><span class="sxs-lookup"><span data-stu-id="f345d-139">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="f345d-140">-Servername</span><span class="sxs-lookup"><span data-stu-id="f345d-140">-ServerName</span></span>
<span data-ttu-id="f345d-141">Gibt den Namen des SQL-Servers der primären SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="f345d-141">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="f345d-142">-Tags</span><span class="sxs-lookup"><span data-stu-id="f345d-142">-Tags</span></span>
<span data-ttu-id="f345d-143">Gibt die Schlüssel-Wert-Paare in Form einer Hashtabelle an, die mit der SQL-Datenbank-Replikationsverknüpfung verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="f345d-143">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="f345d-144">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="f345d-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f345d-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f345d-145">-Confirm</span></span>
<span data-ttu-id="f345d-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f345d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f345d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f345d-147">-WhatIf</span></span>
<span data-ttu-id="f345d-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f345d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f345d-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f345d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f345d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f345d-150">CommonParameters</span></span>
<span data-ttu-id="f345d-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f345d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f345d-152">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f345d-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f345d-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f345d-153">INPUTS</span></span>

### <span data-ttu-id="f345d-154">System. String</span><span class="sxs-lookup"><span data-stu-id="f345d-154">System.String</span></span>

## <span data-ttu-id="f345d-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f345d-155">OUTPUTS</span></span>

### <span data-ttu-id="f345d-156">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="f345d-156">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="f345d-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="f345d-157">NOTES</span></span>

## <span data-ttu-id="f345d-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f345d-158">RELATED LINKS</span></span>

[<span data-ttu-id="f345d-159">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f345d-159">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="f345d-160">Satz-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f345d-160">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="f345d-161">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="f345d-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
