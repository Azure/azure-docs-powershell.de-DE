---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: ba8229bcddf27a2a14d50efc2cbd32e6e47015c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659219"
---
# <span data-ttu-id="2db4c-101">Get-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="2db4c-101">Get-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="2db4c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2db4c-102">SYNOPSIS</span></span>
<span data-ttu-id="2db4c-103">Ruft die empfohlenen Informationstypen und Vertraulichkeits Bezeichnungen von Spalten in der Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="2db4c-103">Gets the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="2db4c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2db4c-104">SYNTAX</span></span>

### <span data-ttu-id="2db4c-105">DatabaseObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2db4c-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2db4c-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="2db4c-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2db4c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2db4c-107">DESCRIPTION</span></span>
<span data-ttu-id="2db4c-108">Das Get-AzSqlDatabaseSensitivityRecommendation-Cmdlet gibt die empfohlenen Informationstypen und Vertraulichkeits Bezeichnungen von Spalten in der Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="2db4c-108">The Get-AzSqlDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="2db4c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2db4c-109">EXAMPLES</span></span>

### <span data-ttu-id="2db4c-110">Beispiel 1: Abrufen empfohlener Informationstypen und Vertraulichkeits Beschriftungen einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2db4c-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="2db4c-111">Beispiel 2: Abrufen empfohlener Informationstypen und Vertraulichkeits Beschriftungen einer Azure SQL-Datenbank mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="2db4c-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

## <span data-ttu-id="2db4c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2db4c-112">PARAMETERS</span></span>

### <span data-ttu-id="2db4c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2db4c-113">-AsJob</span></span>
<span data-ttu-id="2db4c-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2db4c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2db4c-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2db4c-115">-DatabaseName</span></span>
<span data-ttu-id="2db4c-116">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2db4c-116">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db4c-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="2db4c-117">-DatabaseObject</span></span>
<span data-ttu-id="2db4c-118">Das SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="2db4c-118">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2db4c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db4c-119">-DefaultProfile</span></span>
<span data-ttu-id="2db4c-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2db4c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2db4c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2db4c-121">-ResourceGroupName</span></span>
<span data-ttu-id="2db4c-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2db4c-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db4c-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="2db4c-123">-ServerName</span></span>
<span data-ttu-id="2db4c-124">SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="2db4c-124">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db4c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db4c-125">CommonParameters</span></span>
<span data-ttu-id="2db4c-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2db4c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db4c-127">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2db4c-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db4c-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2db4c-128">INPUTS</span></span>

### <span data-ttu-id="2db4c-129">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2db4c-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="2db4c-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2db4c-130">OUTPUTS</span></span>

### <span data-ttu-id="2db4c-131">Microsoft. Azure. Commands. SQL. dataclassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="2db4c-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="2db4c-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="2db4c-132">NOTES</span></span>

## <span data-ttu-id="2db4c-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2db4c-133">RELATED LINKS</span></span>

[<span data-ttu-id="2db4c-134">Weitere Informationen zur Azure SQL-Datenbankdaten Ermittlung und-Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="2db4c-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
