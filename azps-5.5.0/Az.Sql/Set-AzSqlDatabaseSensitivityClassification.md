---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 4409825b758d34e656b18a198aefd0da32824fcd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145580"
---
# <span data-ttu-id="4a4dd-101">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="4a4dd-101">Set-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="4a4dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a4dd-102">SYNOPSIS</span></span>
<span data-ttu-id="4a4dd-103">Legt die Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-103">Sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="4a4dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a4dd-104">SYNTAX</span></span>

### <span data-ttu-id="4a4dd-105">ClassificationObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4a4dd-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a4dd-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a4dd-106">ColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a4dd-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a4dd-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a4dd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a4dd-108">DESCRIPTION</span></span>
<span data-ttu-id="4a4dd-109">Das Set-AzSqlDatabaseSensitivityClassification cmdlet legt die Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-109">The Set-AzSqlDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="4a4dd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a4dd-110">EXAMPLES</span></span>

### <span data-ttu-id="4a4dd-111">Beispiel 1: Festlegen des Informationstyps und der Vertraulichkeitsbezeichnung einer Spalte in einer Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL database.</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="4a4dd-112">Beispiel 2: Festlegen empfohlener Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in einer Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="4a4dd-113">Beispiel 3: Festlegen des Informationstyps und der Vertraulichkeitsbezeichnung einer Spalte in einer Azure SQL mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="4a4dd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a4dd-114">PARAMETERS</span></span>

### <span data-ttu-id="4a4dd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a4dd-115">-AsJob</span></span>
<span data-ttu-id="4a4dd-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4a4dd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a4dd-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="4a4dd-117">-ClassificationObject</span></span>
<span data-ttu-id="4a4dd-118">Ein Objekt, das eine SQL A0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-118">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a4dd-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="4a4dd-119">-ColumnName</span></span>
<span data-ttu-id="4a4dd-120">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-120">Name of column.</span></span>

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

### <span data-ttu-id="4a4dd-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a4dd-121">-DatabaseName</span></span>
<span data-ttu-id="4a4dd-122">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="4a4dd-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="4a4dd-123">-DatabaseObject</span></span>
<span data-ttu-id="4a4dd-124">Das SQL Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-124">The SQL database object.</span></span>

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

### <span data-ttu-id="4a4dd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a4dd-125">-DefaultProfile</span></span>
<span data-ttu-id="4a4dd-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a4dd-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="4a4dd-127">-InformationType</span></span>
<span data-ttu-id="4a4dd-128">Ein Name, der den Informationstyp der in der Spalte gespeicherten Daten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-128">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a4dd-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a4dd-129">-PassThru</span></span>
<span data-ttu-id="4a4dd-130">Gibt an, ob das Vertraulichkeitsklassifikationsmodell am Ende der Ausführung des Cmdlets ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="4a4dd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a4dd-131">-ResourceGroupName</span></span>
<span data-ttu-id="4a4dd-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="4a4dd-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="4a4dd-133">-SchemaName</span></span>
<span data-ttu-id="4a4dd-134">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-134">Name of schema.</span></span>

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

### <span data-ttu-id="4a4dd-135">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="4a4dd-135">-SensitivityLabel</span></span>
<span data-ttu-id="4a4dd-136">Ein Name, der die Vertraulichkeit der in der Spalte gespeicherten Daten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-136">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a4dd-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4a4dd-137">-ServerName</span></span>
<span data-ttu-id="4a4dd-138">SQL Servername.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-138">SQL server name.</span></span>

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

### <span data-ttu-id="4a4dd-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="4a4dd-139">-TableName</span></span>
<span data-ttu-id="4a4dd-140">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-140">Name of table.</span></span>

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

### <span data-ttu-id="4a4dd-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a4dd-141">-Confirm</span></span>
<span data-ttu-id="4a4dd-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a4dd-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4a4dd-143">-WhatIf</span></span>
<span data-ttu-id="4a4dd-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a4dd-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a4dd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a4dd-146">CommonParameters</span></span>
<span data-ttu-id="4a4dd-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a4dd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a4dd-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a4dd-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a4dd-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a4dd-149">INPUTS</span></span>

### <span data-ttu-id="4a4dd-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="4a4dd-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="4a4dd-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a4dd-151">OUTPUTS</span></span>

### <span data-ttu-id="4a4dd-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4a4dd-152">System.Boolean</span></span>

## <span data-ttu-id="4a4dd-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4a4dd-153">NOTES</span></span>

## <span data-ttu-id="4a4dd-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4a4dd-154">RELATED LINKS</span></span>

[<span data-ttu-id="4a4dd-155">Weitere Informationen zu Azure SQL Datenbankdatenermittlung und -klassifizierung</span><span class="sxs-lookup"><span data-stu-id="4a4dd-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
