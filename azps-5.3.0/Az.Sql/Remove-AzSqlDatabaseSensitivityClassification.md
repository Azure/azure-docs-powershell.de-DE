---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 15da7969c5e47376e04bb78a02ff611c9326b947
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460636"
---
# <span data-ttu-id="f548f-101">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="f548f-101">Remove-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="f548f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f548f-102">SYNOPSIS</span></span>
<span data-ttu-id="f548f-103">Entfernt die Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f548f-103">Removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="f548f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f548f-104">SYNTAX</span></span>

### <span data-ttu-id="f548f-105">ClassificationObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f548f-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f548f-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f548f-106">ColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f548f-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f548f-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f548f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f548f-108">DESCRIPTION</span></span>
<span data-ttu-id="f548f-109">Das Remove-AzSqlDatabaseSensitivityClassification cmdlet entfernt die Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f548f-109">The Remove-AzSqlDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="f548f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f548f-110">EXAMPLES</span></span>

### <span data-ttu-id="f548f-111">Beispiel 1: Entfernen des Informationstyps und der Vertraulichkeitsbezeichnung einer Spalte in einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f548f-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="f548f-112">Beispiel 2: Entfernen aktueller Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in einer Azure SQL mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="f548f-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="f548f-113">Beispiel 3: Entfernen des Informationstyps und der Vertraulichkeitsbeschriftung einer Spalte in einer Azure SQL mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="f548f-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="f548f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f548f-114">PARAMETERS</span></span>

### <span data-ttu-id="f548f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f548f-115">-AsJob</span></span>
<span data-ttu-id="f548f-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f548f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f548f-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="f548f-117">-ClassificationObject</span></span>
<span data-ttu-id="f548f-118">Ein Objekt, das eine SQL A0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="f548f-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="f548f-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="f548f-119">-ColumnName</span></span>
<span data-ttu-id="f548f-120">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="f548f-120">Name of column.</span></span>

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

### <span data-ttu-id="f548f-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f548f-121">-DatabaseName</span></span>
<span data-ttu-id="f548f-122">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f548f-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="f548f-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="f548f-123">-DatabaseObject</span></span>
<span data-ttu-id="f548f-124">Das SQL Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="f548f-124">The SQL database object.</span></span>

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

### <span data-ttu-id="f548f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f548f-125">-DefaultProfile</span></span>
<span data-ttu-id="f548f-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f548f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f548f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f548f-127">-PassThru</span></span>
<span data-ttu-id="f548f-128">Gibt an, ob das Vertraulichkeitsklassifikationsmodell am Ende der Ausführung des Cmdlets ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f548f-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="f548f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f548f-129">-ResourceGroupName</span></span>
<span data-ttu-id="f548f-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f548f-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="f548f-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="f548f-131">-SchemaName</span></span>
<span data-ttu-id="f548f-132">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="f548f-132">Name of schema.</span></span>

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

### <span data-ttu-id="f548f-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f548f-133">-ServerName</span></span>
<span data-ttu-id="f548f-134">SQL Servername.</span><span class="sxs-lookup"><span data-stu-id="f548f-134">SQL server name.</span></span>

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

### <span data-ttu-id="f548f-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="f548f-135">-TableName</span></span>
<span data-ttu-id="f548f-136">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f548f-136">Name of table.</span></span>

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

### <span data-ttu-id="f548f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f548f-137">-Confirm</span></span>
<span data-ttu-id="f548f-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f548f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f548f-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f548f-139">-WhatIf</span></span>
<span data-ttu-id="f548f-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f548f-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f548f-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f548f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f548f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f548f-142">CommonParameters</span></span>
<span data-ttu-id="f548f-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f548f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f548f-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f548f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f548f-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f548f-145">INPUTS</span></span>

### <span data-ttu-id="f548f-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="f548f-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="f548f-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f548f-147">OUTPUTS</span></span>

### <span data-ttu-id="f548f-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f548f-148">System.Boolean</span></span>

## <span data-ttu-id="f548f-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f548f-149">NOTES</span></span>

## <span data-ttu-id="f548f-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f548f-150">RELATED LINKS</span></span>

[<span data-ttu-id="f548f-151">Weitere Informationen zu Azure SQL Datenbankdatenermittlung und -klassifizierung</span><span class="sxs-lookup"><span data-stu-id="f548f-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
