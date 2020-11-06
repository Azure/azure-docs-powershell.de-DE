---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 22b74b3dcd76577d7c864a3779d12c8474c431a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478873"
---
# <span data-ttu-id="9b1aa-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9b1aa-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="9b1aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9b1aa-102">SYNOPSIS</span></span>
<span data-ttu-id="9b1aa-103">Erstellt eine Datenbank oder eine elastische Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b1aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b1aa-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b1aa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b1aa-105">DESCRIPTION</span></span>
<span data-ttu-id="9b1aa-106">Das Cmdlet **New-AzureRmSqlDatabase** erstellt eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-106">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>

<span data-ttu-id="9b1aa-107">Sie können auch eine elastische Datenbank erstellen, indem Sie den *ElasticPoolName* -Parameter auf einen vorhandenen elastischen Pool festlegen.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-107">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="9b1aa-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b1aa-108">EXAMPLES</span></span>

### <span data-ttu-id="9b1aa-109">Beispiel 1: Erstellen einer Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="9b1aa-109">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="9b1aa-110">Mit diesem Befehl wird eine Datenbank mit dem Namen Database01 auf dem Server Server01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-110">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="9b1aa-111">Beispiel 2: Erstellen einer elastischen Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="9b1aa-111">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="9b1aa-112">Dieser Befehl erstellt eine Datenbank mit dem Namen database01 im elastischen Pool mit dem Namen ElasticPool01 auf Server Server01.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-112">This command creates a database named Database01 in the elastic pool named ElasticPool01 on server Server01.</span></span>

## <span data-ttu-id="9b1aa-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b1aa-113">PARAMETERS</span></span>

### <span data-ttu-id="9b1aa-114">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="9b1aa-114">-CatalogCollation</span></span>
<span data-ttu-id="9b1aa-115">Gibt den Namen der SQL-Datenbankkatalog Sortierung an.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-115">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="9b1aa-116">-Collation</span><span class="sxs-lookup"><span data-stu-id="9b1aa-116">-CollationName</span></span>
<span data-ttu-id="9b1aa-117">Gibt den Namen der SQL-Datenbanksortierung an.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-117">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="9b1aa-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9b1aa-118">-DatabaseName</span></span>
<span data-ttu-id="9b1aa-119">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-119">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1aa-120">-Edition</span><span class="sxs-lookup"><span data-stu-id="9b1aa-120">-Edition</span></span>
<span data-ttu-id="9b1aa-121">Gibt die Edition an, die der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-121">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="9b1aa-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9b1aa-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9b1aa-123">Standard</span><span class="sxs-lookup"><span data-stu-id="9b1aa-123">Default</span></span>
- <span data-ttu-id="9b1aa-124">Keine</span><span class="sxs-lookup"><span data-stu-id="9b1aa-124">None</span></span>
- <span data-ttu-id="9b1aa-125">Premium</span><span class="sxs-lookup"><span data-stu-id="9b1aa-125">Premium</span></span>
- <span data-ttu-id="9b1aa-126">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="9b1aa-126">Basic</span></span>
- <span data-ttu-id="9b1aa-127">Standard</span><span class="sxs-lookup"><span data-stu-id="9b1aa-127">Standard</span></span>
- <span data-ttu-id="9b1aa-128">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="9b1aa-128">DataWarehouse</span></span>
- <span data-ttu-id="9b1aa-129">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="9b1aa-129">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1aa-130">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="9b1aa-130">-ElasticPoolName</span></span>
<span data-ttu-id="9b1aa-131">Gibt den Namen des elastischen Pools an, in dem die Datenbank abgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-131">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="9b1aa-132">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="9b1aa-132">-MaxSizeBytes</span></span>
<span data-ttu-id="9b1aa-133">Gibt die maximale Größe der Datenbank in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-133">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1aa-134">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="9b1aa-134">-ReadScale</span></span>
<span data-ttu-id="9b1aa-135">Die Option zum Lesen der Skalierung, die der Azure SQL-Datenbank zugewiesen werden soll. (Aktiviert/deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="9b1aa-135">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1aa-136">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="9b1aa-136">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="9b1aa-137">Gibt den Namen des Dienst Ziels an, das der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-137">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="9b1aa-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b1aa-138">-ResourceGroupName</span></span>
<span data-ttu-id="9b1aa-139">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-139">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9b1aa-140">-Samplename</span><span class="sxs-lookup"><span data-stu-id="9b1aa-140">-SampleName</span></span>
<span data-ttu-id="9b1aa-141">Der Name des Beispiel Schemas, das beim Erstellen dieser Datenbank angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-141">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1aa-142">-Servername</span><span class="sxs-lookup"><span data-stu-id="9b1aa-142">-ServerName</span></span>
<span data-ttu-id="9b1aa-143">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-143">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="9b1aa-144">-Tags</span><span class="sxs-lookup"><span data-stu-id="9b1aa-144">-Tags</span></span>
<span data-ttu-id="9b1aa-145">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren in Form einer Hashtabelle an, die dieses Cmdlet der neuen Datenbank zuordnet.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-145">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="9b1aa-146">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9b1aa-146">For example:</span></span>

<span data-ttu-id="9b1aa-147">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="9b1aa-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9b1aa-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9b1aa-148">-Confirm</span></span>
<span data-ttu-id="9b1aa-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b1aa-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b1aa-150">-WhatIf</span></span>
<span data-ttu-id="9b1aa-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b1aa-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b1aa-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b1aa-153">-DefaultProfile</span></span>
<span data-ttu-id="9b1aa-154">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b1aa-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b1aa-155">CommonParameters</span></span>
<span data-ttu-id="9b1aa-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b1aa-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b1aa-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b1aa-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b1aa-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9b1aa-158">INPUTS</span></span>

## <span data-ttu-id="9b1aa-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9b1aa-159">OUTPUTS</span></span>

### <span data-ttu-id="9b1aa-160">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9b1aa-160">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="9b1aa-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="9b1aa-161">NOTES</span></span>

## <span data-ttu-id="9b1aa-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9b1aa-162">RELATED LINKS</span></span>

[<span data-ttu-id="9b1aa-163">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9b1aa-163">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="9b1aa-164">Neu – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9b1aa-164">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="9b1aa-165">Neu – AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="9b1aa-165">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="9b1aa-166">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9b1aa-166">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="9b1aa-167">Lebenslauf-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9b1aa-167">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="9b1aa-168">Satz-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9b1aa-168">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="9b1aa-169">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9b1aa-169">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="9b1aa-170">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="9b1aa-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
