---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 68e889f4da9555a4dc4ca7217bce65121d3a62c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375261"
---
# <span data-ttu-id="279dd-101">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="279dd-101">Enable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="279dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="279dd-102">SYNOPSIS</span></span>
<span data-ttu-id="279dd-103">Aktiviert Vertraulichkeitsempfehlungen für Spalten in der Datenbank (Empfehlungen sind standardmäßig für alle Spalten aktiviert).</span><span class="sxs-lookup"><span data-stu-id="279dd-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the database.</span></span>

## <span data-ttu-id="279dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="279dd-104">SYNTAX</span></span>

### <span data-ttu-id="279dd-105">InputObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="279dd-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279dd-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="279dd-106">ColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279dd-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="279dd-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="279dd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="279dd-108">DESCRIPTION</span></span>
<span data-ttu-id="279dd-109">Das Enable-AzSqlDatabaseSensitivityRecommendation ermöglicht Vertraulichkeitsempfehlungen für Spalten in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="279dd-109">The Enable-AzSqlDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="279dd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="279dd-110">EXAMPLES</span></span>

### <span data-ttu-id="279dd-111">Beispiel 1: Aktivieren von Vertraulichkeitsempfehlungen für eine bestimmte Spalte in einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="279dd-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Enable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="279dd-112">Beispiel 2: Aktivieren von Vertraulichkeitsempfehlungen für eine bestimmte Spalte von Azure SQL mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="279dd-112">Example 2: Enable sensitivity recommendations on a given column Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Enable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="279dd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="279dd-113">PARAMETERS</span></span>

### <span data-ttu-id="279dd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="279dd-114">-AsJob</span></span>
<span data-ttu-id="279dd-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="279dd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="279dd-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="279dd-116">-ColumnName</span></span>
<span data-ttu-id="279dd-117">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="279dd-117">Name of column.</span></span>

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

### <span data-ttu-id="279dd-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="279dd-118">-DatabaseName</span></span>
<span data-ttu-id="279dd-119">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="279dd-119">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="279dd-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="279dd-120">-DatabaseObject</span></span>
<span data-ttu-id="279dd-121">Das SQL Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="279dd-121">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="279dd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="279dd-122">-DefaultProfile</span></span>
<span data-ttu-id="279dd-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="279dd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="279dd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="279dd-124">-InputObject</span></span>
<span data-ttu-id="279dd-125">Ein Objekt, das eine SQL A0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="279dd-125">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="279dd-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="279dd-126">-PassThru</span></span>
<span data-ttu-id="279dd-127">Gibt an, ob das Vertraulichkeitsklassifikationsmodell am Ende der Ausführung des Cmdlets ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="279dd-127">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="279dd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="279dd-128">-ResourceGroupName</span></span>
<span data-ttu-id="279dd-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="279dd-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="279dd-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="279dd-130">-SchemaName</span></span>
<span data-ttu-id="279dd-131">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="279dd-131">Name of schema.</span></span>

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

### <span data-ttu-id="279dd-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="279dd-132">-ServerName</span></span>
<span data-ttu-id="279dd-133">SQL Servername.</span><span class="sxs-lookup"><span data-stu-id="279dd-133">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="279dd-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="279dd-134">-TableName</span></span>
<span data-ttu-id="279dd-135">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="279dd-135">Name of table.</span></span>

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

### <span data-ttu-id="279dd-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="279dd-136">-Confirm</span></span>
<span data-ttu-id="279dd-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="279dd-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="279dd-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="279dd-138">-WhatIf</span></span>
<span data-ttu-id="279dd-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="279dd-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="279dd-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="279dd-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="279dd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="279dd-141">CommonParameters</span></span>
<span data-ttu-id="279dd-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="279dd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="279dd-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="279dd-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="279dd-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="279dd-144">INPUTS</span></span>

### <span data-ttu-id="279dd-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="279dd-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="279dd-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="279dd-146">OUTPUTS</span></span>

### <span data-ttu-id="279dd-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="279dd-147">System.Boolean</span></span>

## <span data-ttu-id="279dd-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="279dd-148">NOTES</span></span>

## <span data-ttu-id="279dd-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="279dd-149">RELATED LINKS</span></span>

[<span data-ttu-id="279dd-150">Weitere Informationen zu Azure SQL Datenbankdatenermittlung und -klassifizierung</span><span class="sxs-lookup"><span data-stu-id="279dd-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)