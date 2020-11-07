---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 226910b81da287c04adb05574b77713e97c6a045
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662396"
---
# <span data-ttu-id="1152e-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1152e-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="1152e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1152e-102">SYNOPSIS</span></span>
<span data-ttu-id="1152e-103">Erstellt eine sekundäre Datenbank für eine vorhandene Datenbank und startet die Datenreplikation.</span><span class="sxs-lookup"><span data-stu-id="1152e-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1152e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1152e-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1152e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1152e-105">DESCRIPTION</span></span>
<span data-ttu-id="1152e-106">Das Cmdlet **New-AzureRMSqlDatabaseSecondary** ersetzt das Start-AzureSqlDatabaseCopy-Cmdlet, wenn es für die Einrichtung der Geo-Replikation für eine Datenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1152e-106">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="1152e-107">Sie gibt das Objekt für die Geo-Replikationsverknüpfung von der primären zur sekundären Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="1152e-107">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="1152e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1152e-108">EXAMPLES</span></span>

### <span data-ttu-id="1152e-109">1: Einrichten einer aktiven Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="1152e-109">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="1152e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1152e-110">PARAMETERS</span></span>

### <span data-ttu-id="1152e-111">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="1152e-111">-AllowConnections</span></span>
<span data-ttu-id="1152e-112">Gibt die Lese Absicht der sekundären Azure SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="1152e-112">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="1152e-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1152e-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1152e-114">Nein</span><span class="sxs-lookup"><span data-stu-id="1152e-114">No</span></span>
- <span data-ttu-id="1152e-115">Alle</span><span class="sxs-lookup"><span data-stu-id="1152e-115">All</span></span>

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

### <span data-ttu-id="1152e-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1152e-116">-DatabaseName</span></span>
<span data-ttu-id="1152e-117">Gibt den Namen der Datenbank an, die als primäre Datenbank fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="1152e-117">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="1152e-118">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1152e-118">-PartnerResourceGroupName</span></span>
<span data-ttu-id="1152e-119">Gibt den Namen der Azure-Ressourcengruppe an, der das Cmdlet die sekundäre Datenbank zuweist.</span><span class="sxs-lookup"><span data-stu-id="1152e-119">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="1152e-120">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="1152e-120">-PartnerServerName</span></span>
<span data-ttu-id="1152e-121">Gibt den Namen des Azure SQL-Datenbankservers an, der als sekundär fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="1152e-121">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="1152e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1152e-122">-ResourceGroupName</span></span>
<span data-ttu-id="1152e-123">Gibt den Namen der Azure-Ressourcengruppe an, der dieses Cmdlet die primäre Datenbank zuweist.</span><span class="sxs-lookup"><span data-stu-id="1152e-123">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="1152e-124">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="1152e-124">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="1152e-125">Gibt den Namen des elastischen Pools an, in dem die sekundäre Datenbank abgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1152e-125">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="1152e-126">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="1152e-126">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="1152e-127">Gibt den Namen des Dienst Ziels an, das der sekundären Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1152e-127">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="1152e-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="1152e-128">-ServerName</span></span>
<span data-ttu-id="1152e-129">Gibt den Namen des SQL-Servers der primären SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="1152e-129">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="1152e-130">-Tags</span><span class="sxs-lookup"><span data-stu-id="1152e-130">-Tags</span></span>
<span data-ttu-id="1152e-131">Gibt die Schlüssel-Wert-Paare in Form einer Hashtabelle an, die mit der SQL-Datenbank-Replikationsverknüpfung verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="1152e-131">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="1152e-132">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1152e-132">For example:</span></span>

<span data-ttu-id="1152e-133">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="1152e-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1152e-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1152e-134">-Confirm</span></span>
<span data-ttu-id="1152e-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1152e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1152e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1152e-136">-WhatIf</span></span>
<span data-ttu-id="1152e-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1152e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1152e-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1152e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1152e-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1152e-139">-DefaultProfile</span></span>
<span data-ttu-id="1152e-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1152e-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1152e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1152e-141">CommonParameters</span></span>
<span data-ttu-id="1152e-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1152e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1152e-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1152e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1152e-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1152e-144">INPUTS</span></span>

## <span data-ttu-id="1152e-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1152e-145">OUTPUTS</span></span>

### <span data-ttu-id="1152e-146">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="1152e-146">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>
<span data-ttu-id="1152e-147">Dieses Cmdlet gibt **ReplicationLink** -Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="1152e-147">This cmdlet returns **ReplicationLink** objects.</span></span>

## <span data-ttu-id="1152e-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="1152e-148">NOTES</span></span>

## <span data-ttu-id="1152e-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1152e-149">RELATED LINKS</span></span>

[<span data-ttu-id="1152e-150">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1152e-150">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="1152e-151">Satz-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1152e-151">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="1152e-152">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="1152e-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
