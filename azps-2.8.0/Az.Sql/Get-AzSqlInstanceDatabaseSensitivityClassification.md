---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: 89190f171ec9634e13eaa56499f6eca87e75ccf5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825548"
---
# <span data-ttu-id="ecba6-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="ecba6-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="ecba6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ecba6-102">SYNOPSIS</span></span>
<span data-ttu-id="ecba6-103">Ruft die aktuellen Informationstypen und Vertraulichkeits Bezeichnungen von Spalten in der Azure SQL-Instanzdatenbank für verwaltete Datenbanken ab.</span><span class="sxs-lookup"><span data-stu-id="ecba6-103">Gets the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="ecba6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecba6-104">SYNTAX</span></span>

### <span data-ttu-id="ecba6-105">DatabaseObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ecba6-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecba6-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecba6-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecba6-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecba6-107">ColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecba6-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecba6-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecba6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ecba6-109">DESCRIPTION</span></span>
<span data-ttu-id="ecba6-110">Das Get-AzSqlInstanceDatabaseSensitivityClassification-Cmdlet gibt die aktuellen Informationstypen und Vertraulichkeits Bezeichnungen von Spalten in der Azure SQL-Instanzdatenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="ecba6-110">The Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="ecba6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ecba6-111">EXAMPLES</span></span>

### <span data-ttu-id="ecba6-112">Beispiel 1: Abrufen aktueller Informationstypen und Vertraulichkeits Beschriftungen einer Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="ecba6-112">Example 1: Get current information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="ecba6-113">Beispiel 2: Abrufen aktueller Informationstypen und Vertraulichkeits Beschriftungen einer Azure SQL-Datenbank mit verwalteten Instanzen mit Piping.</span><span class="sxs-lookup"><span data-stu-id="ecba6-113">Example 2: Get current information types and sensitivity labels of an Azure SQL managed Instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="ecba6-114">Beispiel 3: Abrufen des aktuellen Informationstyps und der Vertraulichkeits Beschriftung einer bestimmten Spalte einer Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="ecba6-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

### <span data-ttu-id="ecba6-115">Beispiel 4: Abrufen des aktuellen Informationstyps und der Vertraulichkeits Beschriftung einer bestimmten Spalte einer Azure SQL-Datenbank mit verwalteten Instanzen mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="ecba6-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

## <span data-ttu-id="ecba6-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecba6-116">PARAMETERS</span></span>

### <span data-ttu-id="ecba6-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecba6-117">-AsJob</span></span>
<span data-ttu-id="ecba6-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ecba6-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ecba6-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="ecba6-119">-ColumnName</span></span>
<span data-ttu-id="ecba6-120">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="ecba6-120">Name of column.</span></span>

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

### <span data-ttu-id="ecba6-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ecba6-121">-DatabaseName</span></span>
<span data-ttu-id="ecba6-122">Der Name der Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="ecba6-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="ecba6-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="ecba6-123">-DatabaseObject</span></span>
<span data-ttu-id="ecba6-124">Das Datenbankobjekt der Azure SQL-Instanz</span><span class="sxs-lookup"><span data-stu-id="ecba6-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecba6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecba6-125">-DefaultProfile</span></span>
<span data-ttu-id="ecba6-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ecba6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecba6-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ecba6-127">-InstanceName</span></span>
<span data-ttu-id="ecba6-128">Name der verwalteten Azure SQL-Instanz.</span><span class="sxs-lookup"><span data-stu-id="ecba6-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="ecba6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecba6-129">-ResourceGroupName</span></span>
<span data-ttu-id="ecba6-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ecba6-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="ecba6-131">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="ecba6-131">-SchemaName</span></span>
<span data-ttu-id="ecba6-132">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="ecba6-132">Name of schema.</span></span>

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

### <span data-ttu-id="ecba6-133">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="ecba6-133">-TableName</span></span>
<span data-ttu-id="ecba6-134">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ecba6-134">Name of table.</span></span>

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

### <span data-ttu-id="ecba6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecba6-135">CommonParameters</span></span>
<span data-ttu-id="ecba6-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecba6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecba6-137">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecba6-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecba6-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ecba6-138">INPUTS</span></span>

### <span data-ttu-id="ecba6-139">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ecba6-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="ecba6-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ecba6-140">OUTPUTS</span></span>

### <span data-ttu-id="ecba6-141">Microsoft. Azure. Commands. SQL. dataclassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="ecba6-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="ecba6-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="ecba6-142">NOTES</span></span>

## <span data-ttu-id="ecba6-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ecba6-143">RELATED LINKS</span></span>

[<span data-ttu-id="ecba6-144">Weitere Informationen zur Azure SQL-Datenbankdaten Ermittlung und-Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="ecba6-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
