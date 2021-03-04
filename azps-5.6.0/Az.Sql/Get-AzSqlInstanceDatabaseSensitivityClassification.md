---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: 9a33504fb27d7c1cf623b03f6c4ea8fefb32c85f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943366"
---
# <span data-ttu-id="a5e8f-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="a5e8f-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="a5e8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e8f-103">Ruft die aktuellen Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Azure SQL verwalteten Instanzdatenbank ab.</span><span class="sxs-lookup"><span data-stu-id="a5e8f-103">Gets the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="a5e8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5e8f-104">SYNTAX</span></span>

### <span data-ttu-id="a5e8f-105">DatabaseObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5e8f-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5e8f-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5e8f-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5e8f-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5e8f-107">ColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5e8f-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5e8f-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5e8f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5e8f-109">DESCRIPTION</span></span>
<span data-ttu-id="a5e8f-110">Das Get-AzSqlInstanceDatabaseSensitivityClassification-Cmdlet gibt die aktuellen Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Azure SQL verwaltete Instanzdatenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="a5e8f-110">The Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="a5e8f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a5e8f-111">EXAMPLES</span></span>

### <span data-ttu-id="a5e8f-112">Beispiel 1: Aktuelle Informationstypen und Vertraulichkeitsbeschriftungen einer Azure SQL verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="a5e8f-112">Example 1: Get current information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
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

### <span data-ttu-id="a5e8f-113">Beispiel 2: Aktuelle Informationstypen und Vertraulichkeitsbeschriftungen einer Azure SQL verwaltete Instanzdatenbank mit Piping.</span><span class="sxs-lookup"><span data-stu-id="a5e8f-113">Example 2: Get current information types and sensitivity labels of an Azure SQL managed Instance database with Piping.</span></span>
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

### <span data-ttu-id="a5e8f-114">Beispiel 3: Aktuelle Informationstyp- und Vertraulichkeitsbeschriftung einer bestimmten Spalte einer Azure SQL verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="a5e8f-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database.</span></span>
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

### <span data-ttu-id="a5e8f-115">Beispiel 4: Aktuelle Informationstyp- und Vertraulichkeitsbeschriftung einer bestimmten Spalte einer Azure SQL verwaltete Instanzdatenbank mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="a5e8f-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database using Piping.</span></span>
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

## <span data-ttu-id="a5e8f-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a5e8f-116">PARAMETERS</span></span>

### <span data-ttu-id="a5e8f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5e8f-117">-AsJob</span></span>
<span data-ttu-id="a5e8f-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a5e8f-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5e8f-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="a5e8f-119">-ColumnName</span></span>
<span data-ttu-id="a5e8f-120">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="a5e8f-120">Name of column.</span></span>

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

### <span data-ttu-id="a5e8f-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a5e8f-121">-DatabaseName</span></span>
<span data-ttu-id="a5e8f-122">Der Name der Azure SQL verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="a5e8f-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="a5e8f-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="a5e8f-123">-DatabaseObject</span></span>
<span data-ttu-id="a5e8f-124">Das Azure SQL verwaltete Instanzdatenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="a5e8f-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="a5e8f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e8f-125">-DefaultProfile</span></span>
<span data-ttu-id="a5e8f-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5e8f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5e8f-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a5e8f-127">-InstanceName</span></span>
<span data-ttu-id="a5e8f-128">Azure SQL verwalteten Instanznamen.</span><span class="sxs-lookup"><span data-stu-id="a5e8f-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="a5e8f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5e8f-129">-ResourceGroupName</span></span>
<span data-ttu-id="a5e8f-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a5e8f-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="a5e8f-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a5e8f-131">-SchemaName</span></span>
<span data-ttu-id="a5e8f-132">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="a5e8f-132">Name of schema.</span></span>

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

### <span data-ttu-id="a5e8f-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="a5e8f-133">-TableName</span></span>
<span data-ttu-id="a5e8f-134">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a5e8f-134">Name of table.</span></span>

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

### <span data-ttu-id="a5e8f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e8f-135">CommonParameters</span></span>
<span data-ttu-id="a5e8f-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e8f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e8f-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5e8f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e8f-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a5e8f-138">INPUTS</span></span>

### <span data-ttu-id="a5e8f-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a5e8f-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="a5e8f-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a5e8f-140">OUTPUTS</span></span>

### <span data-ttu-id="a5e8f-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="a5e8f-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="a5e8f-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a5e8f-142">NOTES</span></span>

## <span data-ttu-id="a5e8f-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a5e8f-143">RELATED LINKS</span></span>

[<span data-ttu-id="a5e8f-144">Weitere Informationen zu Azure SQL Datenbankdatenermittlung und -klassifizierung</span><span class="sxs-lookup"><span data-stu-id="a5e8f-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
