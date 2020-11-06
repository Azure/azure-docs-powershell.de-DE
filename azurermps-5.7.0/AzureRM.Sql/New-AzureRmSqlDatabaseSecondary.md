---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: b23128d2ef55e971f20569e251601b410b218ec2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476466"
---
# <span data-ttu-id="365ba-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="365ba-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="365ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="365ba-102">SYNOPSIS</span></span>
<span data-ttu-id="365ba-103">Erstellt eine sekundäre Datenbank für eine vorhandene Datenbank und startet die Datenreplikation.</span><span class="sxs-lookup"><span data-stu-id="365ba-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="365ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="365ba-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="365ba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="365ba-105">DESCRIPTION</span></span>
<span data-ttu-id="365ba-106">Das Cmdlet **New-AzureRMSqlDatabaseSecondary** ersetzt das Start-AzureSqlDatabaseCopy-Cmdlet, wenn es für die Einrichtung der Geo-Replikation für eine Datenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="365ba-106">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="365ba-107">Sie gibt das Objekt für die Geo-Replikationsverknüpfung von der primären zur sekundären Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="365ba-107">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="365ba-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="365ba-108">EXAMPLES</span></span>

### <span data-ttu-id="365ba-109">1: Einrichten einer aktiven Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="365ba-109">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="365ba-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="365ba-110">PARAMETERS</span></span>

### <span data-ttu-id="365ba-111">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="365ba-111">-AllowConnections</span></span>
<span data-ttu-id="365ba-112">Gibt die Lese Absicht der sekundären Azure SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="365ba-112">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="365ba-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="365ba-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="365ba-114">Nein</span><span class="sxs-lookup"><span data-stu-id="365ba-114">No</span></span>
- <span data-ttu-id="365ba-115">Alle</span><span class="sxs-lookup"><span data-stu-id="365ba-115">All</span></span>

```yaml
Type: AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ba-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="365ba-116">-AsJob</span></span>
<span data-ttu-id="365ba-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="365ba-117">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ba-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="365ba-118">-DatabaseName</span></span>
<span data-ttu-id="365ba-119">Gibt den Namen der Datenbank an, die als primäre Datenbank fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="365ba-119">Specifies the name of the database to act as primary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365ba-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="365ba-120">-DefaultProfile</span></span>
<span data-ttu-id="365ba-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="365ba-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ba-122">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="365ba-122">-PartnerResourceGroupName</span></span>
<span data-ttu-id="365ba-123">Gibt den Namen der Azure-Ressourcengruppe an, der das Cmdlet die sekundäre Datenbank zuweist.</span><span class="sxs-lookup"><span data-stu-id="365ba-123">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ba-124">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="365ba-124">-PartnerServerName</span></span>
<span data-ttu-id="365ba-125">Gibt den Namen des Azure SQL-Datenbankservers an, der als sekundär fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="365ba-125">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="365ba-126">-ResourceGroupName</span></span>
<span data-ttu-id="365ba-127">Gibt den Namen der Azure-Ressourcengruppe an, der dieses Cmdlet die primäre Datenbank zuweist.</span><span class="sxs-lookup"><span data-stu-id="365ba-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365ba-128">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="365ba-128">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="365ba-129">Gibt den Namen des elastischen Pools an, in dem die sekundäre Datenbank abgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="365ba-129">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ba-130">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="365ba-130">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="365ba-131">Gibt den Namen des Dienst Ziels an, das der sekundären Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="365ba-131">Specifies the name of the service objective to assign to the secondary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ba-132">-Servername</span><span class="sxs-lookup"><span data-stu-id="365ba-132">-ServerName</span></span>
<span data-ttu-id="365ba-133">Gibt den Namen des SQL-Servers der primären SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="365ba-133">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365ba-134">-Tags</span><span class="sxs-lookup"><span data-stu-id="365ba-134">-Tags</span></span>
<span data-ttu-id="365ba-135">Gibt die Schlüssel-Wert-Paare in Form einer Hashtabelle an, die mit der SQL-Datenbank-Replikationsverknüpfung verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="365ba-135">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="365ba-136">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="365ba-136">For example:</span></span>

<span data-ttu-id="365ba-137">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="365ba-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ba-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="365ba-138">-Confirm</span></span>
<span data-ttu-id="365ba-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="365ba-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ba-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="365ba-140">-WhatIf</span></span>
<span data-ttu-id="365ba-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="365ba-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="365ba-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="365ba-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ba-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="365ba-143">CommonParameters</span></span>
<span data-ttu-id="365ba-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="365ba-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="365ba-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="365ba-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="365ba-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="365ba-146">INPUTS</span></span>

### <span data-ttu-id="365ba-147">Keine</span><span class="sxs-lookup"><span data-stu-id="365ba-147">None</span></span>
<span data-ttu-id="365ba-148">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="365ba-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="365ba-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="365ba-149">OUTPUTS</span></span>

### <span data-ttu-id="365ba-150">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="365ba-150">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>
<span data-ttu-id="365ba-151">Dieses Cmdlet gibt **ReplicationLink** -Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="365ba-151">This cmdlet returns **ReplicationLink** objects.</span></span>

## <span data-ttu-id="365ba-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="365ba-152">NOTES</span></span>

## <span data-ttu-id="365ba-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="365ba-153">RELATED LINKS</span></span>

[<span data-ttu-id="365ba-154">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="365ba-154">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="365ba-155">Satz-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="365ba-155">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="365ba-156">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="365ba-156">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
