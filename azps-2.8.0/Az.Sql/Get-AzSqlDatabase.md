---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
ms.openlocfilehash: bcaa1c5d57fea979e227fa8890cac6ac0b3f8a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825332"
---
# <span data-ttu-id="e9b07-101">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9b07-101">Get-AzSqlDatabase</span></span>

## <span data-ttu-id="e9b07-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9b07-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b07-103">Ruft mindestens eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="e9b07-103">Gets one or more databases.</span></span>

## <span data-ttu-id="e9b07-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9b07-104">SYNTAX</span></span>

```
Get-AzSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9b07-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9b07-105">DESCRIPTION</span></span>
<span data-ttu-id="e9b07-106">Das Cmdlet " **Get-AzSqlDatabase** " Ruft eine oder mehrere Azure SQL-Datenbanken von einem Azure SQL-Daten Bank Server ab.</span><span class="sxs-lookup"><span data-stu-id="e9b07-106">The **Get-AzSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>
<span data-ttu-id="e9b07-107">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9b07-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e9b07-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9b07-108">EXAMPLES</span></span>

### <span data-ttu-id="e9b07-109">Beispiel 1: Abrufen aller Datenbanken auf einem Server</span><span class="sxs-lookup"><span data-stu-id="e9b07-109">Example 1: Get all databases on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : master
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
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

<span data-ttu-id="e9b07-110">Dieser Befehl ruft alle Datenbanken auf dem Server mit dem Namen SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="e9b07-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="e9b07-111">Beispiel 2: Abrufen einer Datenbank nach Name auf einem Server</span><span class="sxs-lookup"><span data-stu-id="e9b07-111">Example 2: Get a database by name on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
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

<span data-ttu-id="e9b07-112">Dieser Befehl ruft eine Datenbank mit dem Namen Database02 von einem Server mit dem Namen SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="e9b07-112">This command gets a database named Database02 from a server named Server01.</span></span>

### <span data-ttu-id="e9b07-113">Beispiel 3: Abrufen aller Datenbanken auf einem Server mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="e9b07-113">Example 3: Get all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database*"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
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

<span data-ttu-id="e9b07-114">Dieser Befehl ruft alle Datenbanken auf dem Server mit dem Namen "Server01" ab, die mit "Datenbank" beginnen.</span><span class="sxs-lookup"><span data-stu-id="e9b07-114">This command gets all databases on the server named server01 that start with "database".</span></span>

## <span data-ttu-id="e9b07-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9b07-115">PARAMETERS</span></span>

### <span data-ttu-id="e9b07-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e9b07-116">-DatabaseName</span></span>
<span data-ttu-id="e9b07-117">Gibt den Namen der Datenbank an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9b07-117">Specifies the name of the database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e9b07-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b07-118">-DefaultProfile</span></span>
<span data-ttu-id="e9b07-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e9b07-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9b07-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9b07-120">-ResourceGroupName</span></span>
<span data-ttu-id="e9b07-121">Gibt den Namen der Ressourcengruppe an, der der Datenbankserver zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e9b07-121">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="e9b07-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="e9b07-122">-ServerName</span></span>
<span data-ttu-id="e9b07-123">Gibt den Namen des Servers an, dem die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e9b07-123">Specifies the name of the server to which the database is assigned.</span></span>

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

### <span data-ttu-id="e9b07-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e9b07-124">-Confirm</span></span>
<span data-ttu-id="e9b07-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9b07-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9b07-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9b07-126">-WhatIf</span></span>
<span data-ttu-id="e9b07-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9b07-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9b07-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e9b07-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9b07-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b07-129">CommonParameters</span></span>
<span data-ttu-id="e9b07-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9b07-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b07-131">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9b07-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b07-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9b07-132">INPUTS</span></span>

### <span data-ttu-id="e9b07-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e9b07-133">System.String</span></span>

## <span data-ttu-id="e9b07-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9b07-134">OUTPUTS</span></span>

### <span data-ttu-id="e9b07-135">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e9b07-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="e9b07-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9b07-136">NOTES</span></span>

## <span data-ttu-id="e9b07-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9b07-137">RELATED LINKS</span></span>

[<span data-ttu-id="e9b07-138">Neu – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9b07-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="e9b07-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9b07-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="e9b07-140">Lebenslauf-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9b07-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="e9b07-141">Satz-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9b07-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="e9b07-142">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9b07-142">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)


