---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 32459ad76bb118e97ba29e1730c6006a69b4a3b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949984"
---
# <span data-ttu-id="8d569-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="8d569-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="8d569-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d569-102">SYNOPSIS</span></span>
<span data-ttu-id="8d569-103">Ruft die aktuellen Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="8d569-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="8d569-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d569-104">SYNTAX</span></span>

### <span data-ttu-id="8d569-105">DatabaseObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8d569-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d569-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d569-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d569-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d569-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d569-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d569-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d569-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d569-109">DESCRIPTION</span></span>
<span data-ttu-id="8d569-110">Das Get-AzSqlDatabaseSensitivityClassification-Cmdlet gibt die aktuellen Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Azure SQL zurück.</span><span class="sxs-lookup"><span data-stu-id="8d569-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="8d569-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8d569-111">EXAMPLES</span></span>

### <span data-ttu-id="8d569-112">Beispiel 1: Aktuelle Informationstypen und Vertraulichkeitsbeschriftungen einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8d569-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="8d569-113">Beispiel 2: Aktuelle Informationstypen und Vertraulichkeitsbeschriftungen einer Azure SQL Datenbank mit Piping.</span><span class="sxs-lookup"><span data-stu-id="8d569-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="8d569-114">Beispiel 3: Aktuelle Informationstyp- und Vertraulichkeitsbeschriftung einer bestimmten Spalte einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8d569-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="8d569-115">Beispiel 4: Aktuelle Informationstyp- und Vertraulichkeitsbeschriftung einer bestimmten Spalte einer Azure SQL-Datenbank mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="8d569-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="8d569-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8d569-116">PARAMETERS</span></span>

### <span data-ttu-id="8d569-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d569-117">-AsJob</span></span>
<span data-ttu-id="8d569-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8d569-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d569-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="8d569-119">-ColumnName</span></span>
<span data-ttu-id="8d569-120">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="8d569-120">Name of column.</span></span>

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

### <span data-ttu-id="8d569-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8d569-121">-DatabaseName</span></span>
<span data-ttu-id="8d569-122">Der Name der Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8d569-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="8d569-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="8d569-123">-DatabaseObject</span></span>
<span data-ttu-id="8d569-124">Das SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="8d569-124">The SQL database object.</span></span>

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

### <span data-ttu-id="8d569-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d569-125">-DefaultProfile</span></span>
<span data-ttu-id="8d569-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d569-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d569-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d569-127">-ResourceGroupName</span></span>
<span data-ttu-id="8d569-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8d569-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="8d569-129">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="8d569-129">-SchemaName</span></span>
<span data-ttu-id="8d569-130">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="8d569-130">Name of schema.</span></span>

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

### <span data-ttu-id="8d569-131">-Servername</span><span class="sxs-lookup"><span data-stu-id="8d569-131">-ServerName</span></span>
<span data-ttu-id="8d569-132">SQL Servername.</span><span class="sxs-lookup"><span data-stu-id="8d569-132">SQL server name.</span></span>

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

### <span data-ttu-id="8d569-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="8d569-133">-TableName</span></span>
<span data-ttu-id="8d569-134">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8d569-134">Name of table.</span></span>

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

### <span data-ttu-id="8d569-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d569-135">CommonParameters</span></span>
<span data-ttu-id="8d569-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d569-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d569-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d569-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d569-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8d569-138">INPUTS</span></span>

### <span data-ttu-id="8d569-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8d569-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="8d569-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8d569-140">OUTPUTS</span></span>

### <span data-ttu-id="8d569-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="8d569-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="8d569-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8d569-142">NOTES</span></span>

## <span data-ttu-id="8d569-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8d569-143">RELATED LINKS</span></span>

[<span data-ttu-id="8d569-144">Weitere Informationen zu Azure SQL Datenbankdatenermittlung und -klassifizierung</span><span class="sxs-lookup"><span data-stu-id="8d569-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
