---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: 3d36c94ebcc1b733559f9fb4075fb20e4ec67144
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662883"
---
# <span data-ttu-id="9435b-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9435b-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="9435b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9435b-102">SYNOPSIS</span></span>
<span data-ttu-id="9435b-103">Legt Eigenschaften für eine Datenbank fest oder verschiebt eine vorhandene Datenbank in einen elastischen Pool.</span><span class="sxs-lookup"><span data-stu-id="9435b-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9435b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9435b-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9435b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9435b-105">DESCRIPTION</span></span>
<span data-ttu-id="9435b-106">Das Cmdlet " **Set-AzureRmSqlDatabase** " legt Eigenschaften für eine Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="9435b-106">The **Set-AzureRmSqlDatabase** cmdlet sets properties for an Azure SQL database.</span></span>
<span data-ttu-id="9435b-107">Darüber hinaus können Sie den *ElasticPoolName* -Parameter angeben, um eine Datenbank in einen elastischen Pool zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="9435b-107">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span>
<span data-ttu-id="9435b-108">Wenn sich eine Datenbank bereits in einem elastischen Pool befindet, können Sie den *RequestedServiceObjectiveName* -Parameter verwenden, um eine Leistungsstufe zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="9435b-108">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to assign a performance level.</span></span>

## <span data-ttu-id="9435b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9435b-109">EXAMPLES</span></span>

### <span data-ttu-id="9435b-110">Beispiel 1: Aktualisieren einer Datenbank auf eine Standard-S2-Datenbank</span><span class="sxs-lookup"><span data-stu-id="9435b-110">Example 1: Update a database to a Standard S2 database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S2"
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
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S2
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="9435b-111">Mit diesem Befehl wird eine Datenbank mit dem Namen database01 in eine Standard-S2-Datenbank auf einem Server mit dem Namen Server01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9435b-111">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="9435b-112">Beispiel 2: Hinzufügen einer Datenbank zu einem elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="9435b-112">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
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
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="9435b-113">Dieser Befehl fügt dem elastischen Pool mit dem Namen ElasticPool01, der auf dem Server mit dem Namen Server01 gehostet wird, eine Datenbank mit dem Namen database01 hinzu.</span><span class="sxs-lookup"><span data-stu-id="9435b-113">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

## <span data-ttu-id="9435b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9435b-114">PARAMETERS</span></span>

### <span data-ttu-id="9435b-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9435b-115">-DatabaseName</span></span>
<span data-ttu-id="9435b-116">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="9435b-116">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9435b-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="9435b-117">-Edition</span></span>
<span data-ttu-id="9435b-118">Gibt die Edition für die Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="9435b-118">Specifies the edition for the database.</span></span>
<span data-ttu-id="9435b-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9435b-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9435b-120">Keine</span><span class="sxs-lookup"><span data-stu-id="9435b-120">None</span></span>
- <span data-ttu-id="9435b-121">Premium</span><span class="sxs-lookup"><span data-stu-id="9435b-121">Premium</span></span>
- <span data-ttu-id="9435b-122">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="9435b-122">Basic</span></span>
- <span data-ttu-id="9435b-123">Standard</span><span class="sxs-lookup"><span data-stu-id="9435b-123">Standard</span></span>
- <span data-ttu-id="9435b-124">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="9435b-124">DataWarehouse</span></span>
- <span data-ttu-id="9435b-125">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="9435b-125">Free</span></span>

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

### <span data-ttu-id="9435b-126">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="9435b-126">-ElasticPoolName</span></span>
<span data-ttu-id="9435b-127">Gibt den Namen des elastischen Pools an, in dem die Datenbank verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9435b-127">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="9435b-128">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="9435b-128">-MaxSizeBytes</span></span>
<span data-ttu-id="9435b-129">Gibt die neue maximale Größe für die Datenbank in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="9435b-129">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="9435b-130">Sie können entweder diesen Parameter oder *MaxSizeGB* angeben.</span><span class="sxs-lookup"><span data-stu-id="9435b-130">You can specify either this parameter or *MaxSizeGB*.</span></span>
<span data-ttu-id="9435b-131">Lesen Sie den *MaxSizeGB* -Parameter für akzeptable Werte pro Edition.</span><span class="sxs-lookup"><span data-stu-id="9435b-131">See the *MaxSizeGB* parameter for acceptable values per edition.</span></span>

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

### <span data-ttu-id="9435b-132">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="9435b-132">-ReadScale</span></span>
<span data-ttu-id="9435b-133">Die Option zum Lesen der Skalierung, die der Azure SQL-Datenbank zugewiesen werden soll. (Aktiviert/deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="9435b-133">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="9435b-134">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="9435b-134">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="9435b-135">Gibt den Namen des Dienst Ziels an, das der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9435b-135">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="9435b-136">Informationen zu den Dienst Zielen finden Sie unter [Azure SQL-Datenbankdienst Ebenen und Leistungsstufen](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in der Microsoft Developer Network Library.</span><span class="sxs-lookup"><span data-stu-id="9435b-136">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="9435b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9435b-137">-ResourceGroupName</span></span>
<span data-ttu-id="9435b-138">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9435b-138">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9435b-139">-Servername</span><span class="sxs-lookup"><span data-stu-id="9435b-139">-ServerName</span></span>
<span data-ttu-id="9435b-140">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="9435b-140">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="9435b-141">-Tags</span><span class="sxs-lookup"><span data-stu-id="9435b-141">-Tags</span></span>
<span data-ttu-id="9435b-142">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="9435b-142">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9435b-143">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9435b-143">For example:</span></span>

<span data-ttu-id="9435b-144">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="9435b-144">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9435b-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9435b-145">-Confirm</span></span>
<span data-ttu-id="9435b-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9435b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9435b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9435b-147">-WhatIf</span></span>
<span data-ttu-id="9435b-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9435b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9435b-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9435b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9435b-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9435b-150">-DefaultProfile</span></span>
<span data-ttu-id="9435b-151">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9435b-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9435b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9435b-152">CommonParameters</span></span>
<span data-ttu-id="9435b-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9435b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9435b-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9435b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9435b-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9435b-155">INPUTS</span></span>

## <span data-ttu-id="9435b-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9435b-156">OUTPUTS</span></span>

### <span data-ttu-id="9435b-157">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9435b-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="9435b-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="9435b-158">NOTES</span></span>

## <span data-ttu-id="9435b-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9435b-159">RELATED LINKS</span></span>

[<span data-ttu-id="9435b-160">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9435b-160">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="9435b-161">Neu – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9435b-161">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="9435b-162">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9435b-162">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="9435b-163">Lebenslauf-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9435b-163">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="9435b-164">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9435b-164">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="9435b-165">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="9435b-165">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
