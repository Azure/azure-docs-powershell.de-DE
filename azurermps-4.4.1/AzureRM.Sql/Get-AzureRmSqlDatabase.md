---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabase.md
ms.openlocfilehash: 9ae96035a4257826ac92dc6dbae75282debf08a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504710"
---
# <span data-ttu-id="09330-101">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="09330-101">Get-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="09330-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09330-102">SYNOPSIS</span></span>
<span data-ttu-id="09330-103">Ruft mindestens eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="09330-103">Gets one or more databases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09330-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09330-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09330-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09330-105">DESCRIPTION</span></span>
<span data-ttu-id="09330-106">Das Cmdlet " **Get-AzureRmSqlDatabase** " Ruft eine oder mehrere Azure SQL-Datenbanken von einem Azure SQL-Daten Bank Server ab.</span><span class="sxs-lookup"><span data-stu-id="09330-106">The **Get-AzureRmSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>

<span data-ttu-id="09330-107">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="09330-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="09330-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09330-108">EXAMPLES</span></span>

### <span data-ttu-id="09330-109">Beispiel 1: Abrufen aller Datenbanken auf einem Server</span><span class="sxs-lookup"><span data-stu-id="09330-109">Example 1: Get all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

<span data-ttu-id="09330-110">Dieser Befehl ruft alle Datenbanken auf dem Server mit dem Namen SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="09330-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="09330-111">Beispiel 2: Abrufen einer Datenbank nach Name auf einem Server</span><span class="sxs-lookup"><span data-stu-id="09330-111">Example 2: Get a database by name on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02"
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

<span data-ttu-id="09330-112">Dieser Befehl ruft eine Datenbank mit dem Namen Database02 von einem Server mit dem Namen SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="09330-112">This command gets a database named Database02 from a server named Server01.</span></span>

## <span data-ttu-id="09330-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="09330-113">PARAMETERS</span></span>

### <span data-ttu-id="09330-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="09330-114">-DatabaseName</span></span>
<span data-ttu-id="09330-115">Gibt den Namen der Datenbank an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="09330-115">Specifies the name of the database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09330-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09330-116">-ResourceGroupName</span></span>
<span data-ttu-id="09330-117">Gibt den Namen der Ressourcengruppe an, der der Datenbankserver zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="09330-117">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="09330-118">-Servername</span><span class="sxs-lookup"><span data-stu-id="09330-118">-ServerName</span></span>
<span data-ttu-id="09330-119">Gibt den Namen des Servers an, dem die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="09330-119">Specifies the name of the server to which the database is assigned.</span></span>

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

### <span data-ttu-id="09330-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="09330-120">-Confirm</span></span>
<span data-ttu-id="09330-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09330-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09330-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09330-122">-WhatIf</span></span>
<span data-ttu-id="09330-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09330-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09330-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09330-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09330-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09330-125">-DefaultProfile</span></span>
<span data-ttu-id="09330-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09330-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09330-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09330-127">CommonParameters</span></span>
<span data-ttu-id="09330-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09330-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09330-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09330-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09330-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09330-130">INPUTS</span></span>

## <span data-ttu-id="09330-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09330-131">OUTPUTS</span></span>

### <span data-ttu-id="09330-132">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="09330-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="09330-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="09330-133">NOTES</span></span>

## <span data-ttu-id="09330-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09330-134">RELATED LINKS</span></span>

[<span data-ttu-id="09330-135">Neu – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="09330-135">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="09330-136">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="09330-136">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="09330-137">Lebenslauf-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="09330-137">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="09330-138">Satz-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="09330-138">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="09330-139">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="09330-139">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)


