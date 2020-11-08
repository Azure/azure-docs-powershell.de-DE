---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: f7dbffffe9a51d35ced8861894373322898fd0f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997170"
---
# <span data-ttu-id="61c3f-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="61c3f-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="61c3f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61c3f-102">SYNOPSIS</span></span>
<span data-ttu-id="61c3f-103">Erstellt eine sekundäre Datenbank für eine vorhandene Datenbank und startet die Datenreplikation.</span><span class="sxs-lookup"><span data-stu-id="61c3f-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="61c3f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61c3f-104">SYNTAX</span></span>

### <span data-ttu-id="61c3f-105">DtuBasedDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="61c3f-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61c3f-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="61c3f-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61c3f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61c3f-107">DESCRIPTION</span></span>
<span data-ttu-id="61c3f-108">Das Cmdlet **New-AzSqlDatabaseSecondary** ersetzt das Start-AzSqlDatabaseCopy-Cmdlet, wenn es für die Einrichtung der Geo-Replikation für eine Datenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61c3f-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="61c3f-109">Sie gibt das Objekt für die Geo-Replikationsverknüpfung von der primären zur sekundären Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="61c3f-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="61c3f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61c3f-110">EXAMPLES</span></span>

### <span data-ttu-id="61c3f-111">1: Einrichten einer aktiven Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="61c3f-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="61c3f-112">2: Einrichten einer aktiven Geo-Replication und angeben des Partnerdaten Banknamens, der sich von dem Namen der Quelldatenbank unterscheiden soll</span><span class="sxs-lookup"><span data-stu-id="61c3f-112">2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="61c3f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="61c3f-113">PARAMETERS</span></span>

### <span data-ttu-id="61c3f-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="61c3f-114">-AllowConnections</span></span>
<span data-ttu-id="61c3f-115">Gibt die Lese Absicht der sekundären Azure SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="61c3f-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="61c3f-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="61c3f-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="61c3f-117">Nein</span><span class="sxs-lookup"><span data-stu-id="61c3f-117">No</span></span>
- <span data-ttu-id="61c3f-118">Alle</span><span class="sxs-lookup"><span data-stu-id="61c3f-118">All</span></span>

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

### <span data-ttu-id="61c3f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61c3f-119">-AsJob</span></span>
<span data-ttu-id="61c3f-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="61c3f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61c3f-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="61c3f-121">-DatabaseName</span></span>
<span data-ttu-id="61c3f-122">Gibt den Namen der Datenbank an, die als primäre Datenbank fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="61c3f-122">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="61c3f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61c3f-123">-DefaultProfile</span></span>
<span data-ttu-id="61c3f-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="61c3f-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61c3f-125">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="61c3f-125">-LicenseType</span></span>
<span data-ttu-id="61c3f-126">Der Lizenztyp für die Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="61c3f-126">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="61c3f-127">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="61c3f-127">-PartnerDatabaseName</span></span>
<span data-ttu-id="61c3f-128">Der Name der sekundären Datenbank, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="61c3f-128">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="61c3f-129">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61c3f-129">-PartnerResourceGroupName</span></span>
<span data-ttu-id="61c3f-130">Gibt den Namen der Azure-Ressourcengruppe an, der das Cmdlet die sekundäre Datenbank zuweist.</span><span class="sxs-lookup"><span data-stu-id="61c3f-130">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="61c3f-131">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="61c3f-131">-PartnerServerName</span></span>
<span data-ttu-id="61c3f-132">Gibt den Namen des Azure SQL-Datenbankservers an, der als sekundär fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="61c3f-132">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="61c3f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61c3f-133">-ResourceGroupName</span></span>
<span data-ttu-id="61c3f-134">Gibt den Namen der Azure-Ressourcengruppe an, der dieses Cmdlet die primäre Datenbank zuweist.</span><span class="sxs-lookup"><span data-stu-id="61c3f-134">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="61c3f-135">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="61c3f-135">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="61c3f-136">Die COMPUTE-Generierung der Azure SQL-Datenbank sekundär.</span><span class="sxs-lookup"><span data-stu-id="61c3f-136">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="61c3f-137">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="61c3f-137">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="61c3f-138">Gibt den Namen des elastischen Pools an, in dem die sekundäre Datenbank abgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="61c3f-138">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="61c3f-139">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="61c3f-139">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="61c3f-140">Gibt den Namen des Dienst Ziels an, das der sekundären Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="61c3f-140">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="61c3f-141">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="61c3f-141">-SecondaryVCore</span></span>
<span data-ttu-id="61c3f-142">Die Vcore-Nummern der Azure SQL-Datenbank sekundär.</span><span class="sxs-lookup"><span data-stu-id="61c3f-142">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="61c3f-143">-Servername</span><span class="sxs-lookup"><span data-stu-id="61c3f-143">-ServerName</span></span>
<span data-ttu-id="61c3f-144">Gibt den Namen des SQL-Servers der primären SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="61c3f-144">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="61c3f-145">-Tags</span><span class="sxs-lookup"><span data-stu-id="61c3f-145">-Tags</span></span>
<span data-ttu-id="61c3f-146">Gibt die Schlüssel-Wert-Paare in Form einer Hashtabelle an, die mit der SQL-Datenbank-Replikationsverknüpfung verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="61c3f-146">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="61c3f-147">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="61c3f-147">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="61c3f-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="61c3f-148">-Confirm</span></span>
<span data-ttu-id="61c3f-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="61c3f-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61c3f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61c3f-150">-WhatIf</span></span>
<span data-ttu-id="61c3f-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61c3f-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61c3f-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61c3f-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61c3f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61c3f-153">CommonParameters</span></span>
<span data-ttu-id="61c3f-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61c3f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61c3f-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61c3f-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61c3f-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61c3f-156">INPUTS</span></span>

### <span data-ttu-id="61c3f-157">System. String</span><span class="sxs-lookup"><span data-stu-id="61c3f-157">System.String</span></span>

## <span data-ttu-id="61c3f-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61c3f-158">OUTPUTS</span></span>

### <span data-ttu-id="61c3f-159">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="61c3f-159">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="61c3f-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="61c3f-160">NOTES</span></span>

## <span data-ttu-id="61c3f-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61c3f-161">RELATED LINKS</span></span>

[<span data-ttu-id="61c3f-162">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="61c3f-162">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="61c3f-163">Satz-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="61c3f-163">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="61c3f-164">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="61c3f-164">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
