---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: fe8cffb4ab9d79828795cc1148a3c109cfbfdddb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163409"
---
# <span data-ttu-id="05d94-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="05d94-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="05d94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05d94-102">SYNOPSIS</span></span>
<span data-ttu-id="05d94-103">Ruft die aktuellen Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Azure SQL Instanzdatenbank ab.</span><span class="sxs-lookup"><span data-stu-id="05d94-103">Gets the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="05d94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05d94-104">SYNTAX</span></span>

### <span data-ttu-id="05d94-105">DatabaseObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="05d94-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05d94-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="05d94-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05d94-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="05d94-107">ColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05d94-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="05d94-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05d94-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05d94-109">DESCRIPTION</span></span>
<span data-ttu-id="05d94-110">Das Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet gibt die aktuellen Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Azure SQL Verwaltete Instanzdatenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="05d94-110">The Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="05d94-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="05d94-111">EXAMPLES</span></span>

### <span data-ttu-id="05d94-112">Beispiel 1: Aktuelle Informationstypen und Vertraulichkeitsbezeichnungen einer Azure SQL Instanzdatenbank erhalten.</span><span class="sxs-lookup"><span data-stu-id="05d94-112">Example 1: Get current information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="05d94-113">Beispiel 2: Aktuelle Informationstypen und Vertraulichkeitsbeschriftungen einer Azure SQL Verwaltete Instanzdatenbank mit Piping erhalten.</span><span class="sxs-lookup"><span data-stu-id="05d94-113">Example 2: Get current information types and sensitivity labels of an Azure SQL managed Instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="05d94-114">Beispiel 3: Erhalten des aktuellen Informationstyps und der Vertraulichkeitsbezeichnung einer bestimmten Spalte einer Azure SQL Verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="05d94-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="05d94-115">Beispiel 4: Erhalten des aktuellen Informationstyps und der Vertraulichkeitsbezeichnung einer bestimmten Spalte einer Azure SQL Instanzdatenbank mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="05d94-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

## <span data-ttu-id="05d94-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05d94-116">PARAMETERS</span></span>

### <span data-ttu-id="05d94-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05d94-117">-AsJob</span></span>
<span data-ttu-id="05d94-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="05d94-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05d94-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="05d94-119">-ColumnName</span></span>
<span data-ttu-id="05d94-120">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="05d94-120">Name of column.</span></span>

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

### <span data-ttu-id="05d94-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="05d94-121">-DatabaseName</span></span>
<span data-ttu-id="05d94-122">Der Name der Azure SQL Verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="05d94-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="05d94-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="05d94-123">-DatabaseObject</span></span>
<span data-ttu-id="05d94-124">Das Azure SQL verwaltete Instanzdatenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="05d94-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="05d94-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05d94-125">-DefaultProfile</span></span>
<span data-ttu-id="05d94-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05d94-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05d94-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="05d94-127">-InstanceName</span></span>
<span data-ttu-id="05d94-128">Azure SQL verwalteten Instanznamen.</span><span class="sxs-lookup"><span data-stu-id="05d94-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="05d94-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05d94-129">-ResourceGroupName</span></span>
<span data-ttu-id="05d94-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="05d94-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="05d94-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="05d94-131">-SchemaName</span></span>
<span data-ttu-id="05d94-132">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="05d94-132">Name of schema.</span></span>

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

### <span data-ttu-id="05d94-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="05d94-133">-TableName</span></span>
<span data-ttu-id="05d94-134">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="05d94-134">Name of table.</span></span>

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

### <span data-ttu-id="05d94-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05d94-135">CommonParameters</span></span>
<span data-ttu-id="05d94-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05d94-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05d94-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05d94-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05d94-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="05d94-138">INPUTS</span></span>

### <span data-ttu-id="05d94-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="05d94-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="05d94-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="05d94-140">OUTPUTS</span></span>

### <span data-ttu-id="05d94-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="05d94-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="05d94-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="05d94-142">NOTES</span></span>

## <span data-ttu-id="05d94-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="05d94-143">RELATED LINKS</span></span>

[<span data-ttu-id="05d94-144">Weitere Informationen zu Azure SQL Datenbankdatenermittlung und -klassifizierung</span><span class="sxs-lookup"><span data-stu-id="05d94-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
