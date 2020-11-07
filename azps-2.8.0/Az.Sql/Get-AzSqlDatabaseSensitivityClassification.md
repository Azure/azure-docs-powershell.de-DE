---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 50bd23f0c0be638683dae4acb5b43165a8c5b4f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825631"
---
# <span data-ttu-id="9a6ea-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="9a6ea-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="9a6ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a6ea-102">SYNOPSIS</span></span>
<span data-ttu-id="9a6ea-103">Ruft die aktuellen Informationstypen und Vertraulichkeits Bezeichnungen von Spalten in der Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="9a6ea-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="9a6ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a6ea-104">SYNTAX</span></span>

### <span data-ttu-id="9a6ea-105">DatabaseObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9a6ea-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a6ea-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a6ea-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a6ea-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a6ea-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a6ea-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a6ea-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a6ea-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a6ea-109">DESCRIPTION</span></span>
<span data-ttu-id="9a6ea-110">Das Get-AzSqlDatabaseSensitivityClassification-Cmdlet gibt die aktuellen Informationstypen und Vertraulichkeits Bezeichnungen von Spalten in der Azure SQL-Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="9a6ea-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="9a6ea-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a6ea-111">EXAMPLES</span></span>

### <span data-ttu-id="9a6ea-112">Beispiel 1: Abrufen aktueller Informationstypen und Vertraulichkeits Beschriftungen einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9a6ea-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

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

### <span data-ttu-id="9a6ea-113">Beispiel 2: Abrufen aktueller Informationstypen und Vertraulichkeits Beschriftungen einer Azure SQL-Datenbank mit Piping.</span><span class="sxs-lookup"><span data-stu-id="9a6ea-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification

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

### <span data-ttu-id="9a6ea-114">Beispiel 3: Abrufen des aktuellen Informationstyps und der Vertraulichkeits Beschriftung einer bestimmten Spalte einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9a6ea-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

### <span data-ttu-id="9a6ea-115">Beispiel 4: Abrufen des aktuellen Informationstyps und der Vertraulichkeits Beschriftung einer bestimmten Spalte einer Azure SQL-Datenbank mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="9a6ea-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

## <span data-ttu-id="9a6ea-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a6ea-116">PARAMETERS</span></span>

### <span data-ttu-id="9a6ea-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a6ea-117">-AsJob</span></span>
<span data-ttu-id="9a6ea-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9a6ea-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a6ea-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="9a6ea-119">-ColumnName</span></span>
<span data-ttu-id="9a6ea-120">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="9a6ea-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6ea-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9a6ea-121">-DatabaseName</span></span>
<span data-ttu-id="9a6ea-122">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9a6ea-122">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6ea-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="9a6ea-123">-DatabaseObject</span></span>
<span data-ttu-id="9a6ea-124">Das SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="9a6ea-124">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6ea-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a6ea-125">-DefaultProfile</span></span>
<span data-ttu-id="9a6ea-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9a6ea-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a6ea-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a6ea-127">-ResourceGroupName</span></span>
<span data-ttu-id="9a6ea-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9a6ea-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6ea-129">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="9a6ea-129">-SchemaName</span></span>
<span data-ttu-id="9a6ea-130">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="9a6ea-130">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6ea-131">-Servername</span><span class="sxs-lookup"><span data-stu-id="9a6ea-131">-ServerName</span></span>
<span data-ttu-id="9a6ea-132">SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="9a6ea-132">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6ea-133">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="9a6ea-133">-TableName</span></span>
<span data-ttu-id="9a6ea-134">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9a6ea-134">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6ea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a6ea-135">CommonParameters</span></span>
<span data-ttu-id="9a6ea-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a6ea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a6ea-137">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a6ea-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a6ea-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a6ea-138">INPUTS</span></span>

### <span data-ttu-id="9a6ea-139">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9a6ea-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="9a6ea-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a6ea-140">OUTPUTS</span></span>

### <span data-ttu-id="9a6ea-141">Microsoft. Azure. Commands. SQL. dataclassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="9a6ea-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="9a6ea-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a6ea-142">NOTES</span></span>

## <span data-ttu-id="9a6ea-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a6ea-143">RELATED LINKS</span></span>

[<span data-ttu-id="9a6ea-144">Weitere Informationen zur Azure SQL-Datenbankdaten Ermittlung und-Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="9a6ea-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
