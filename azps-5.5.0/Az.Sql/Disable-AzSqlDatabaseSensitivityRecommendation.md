---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f9a8ab299571e4e04f3061773d19b920f52d22a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163452"
---
# <span data-ttu-id="691e0-101">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="691e0-101">Disable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="691e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="691e0-102">SYNOPSIS</span></span>
<span data-ttu-id="691e0-103">Deaktiviert (schließt) Vertraulichkeitsempfehlungen für Spalten in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="691e0-103">Disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="691e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="691e0-104">SYNTAX</span></span>

### <span data-ttu-id="691e0-105">InputObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="691e0-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="691e0-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="691e0-106">ColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="691e0-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="691e0-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="691e0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="691e0-108">DESCRIPTION</span></span>
<span data-ttu-id="691e0-109">Das Disable-AzSqlDatabaseSensitivityRecommendation deaktiviert (schließt) Vertraulichkeitsempfehlungen für Spalten in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="691e0-109">The Disable-AzSqlDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="691e0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="691e0-110">EXAMPLES</span></span>

### <span data-ttu-id="691e0-111">Beispiel 1: Deaktivieren von Vertraulichkeitsempfehlungen für eine bestimmte Spalte in einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="691e0-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Disable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="691e0-112">Beispiel 2: Deaktivieren Sie Vertraulichkeitsempfehlungen für Spalten, die Vertraulichkeitsempfehlungen in einer Azure SQL mithilfe von Piping enthalten.</span><span class="sxs-lookup"><span data-stu-id="691e0-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation
```

### <span data-ttu-id="691e0-113">Beispiel 3: Deaktivieren von Vertraulichkeitsempfehlungen für eine bestimmte Spalte in einer Azure SQL mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="691e0-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="691e0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="691e0-114">PARAMETERS</span></span>

### <span data-ttu-id="691e0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="691e0-115">-AsJob</span></span>
<span data-ttu-id="691e0-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="691e0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="691e0-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="691e0-117">-ColumnName</span></span>
<span data-ttu-id="691e0-118">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="691e0-118">Name of column.</span></span>

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

### <span data-ttu-id="691e0-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="691e0-119">-DatabaseName</span></span>
<span data-ttu-id="691e0-120">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="691e0-120">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="691e0-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="691e0-121">-DatabaseObject</span></span>
<span data-ttu-id="691e0-122">Das SQL Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="691e0-122">The SQL database object.</span></span>

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

### <span data-ttu-id="691e0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="691e0-123">-DefaultProfile</span></span>
<span data-ttu-id="691e0-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="691e0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="691e0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="691e0-125">-InputObject</span></span>
<span data-ttu-id="691e0-126">Ein Objekt, das eine SQL A0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="691e0-126">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="691e0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="691e0-127">-PassThru</span></span>
<span data-ttu-id="691e0-128">Gibt an, ob das Vertraulichkeitsklassifikationsmodell am Ende der Ausführung des Cmdlets ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="691e0-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="691e0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="691e0-129">-ResourceGroupName</span></span>
<span data-ttu-id="691e0-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="691e0-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="691e0-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="691e0-131">-SchemaName</span></span>
<span data-ttu-id="691e0-132">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="691e0-132">Name of schema.</span></span>

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

### <span data-ttu-id="691e0-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="691e0-133">-ServerName</span></span>
<span data-ttu-id="691e0-134">SQL Servername.</span><span class="sxs-lookup"><span data-stu-id="691e0-134">SQL server name.</span></span>

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

### <span data-ttu-id="691e0-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="691e0-135">-TableName</span></span>
<span data-ttu-id="691e0-136">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="691e0-136">Name of table.</span></span>

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

### <span data-ttu-id="691e0-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="691e0-137">-Confirm</span></span>
<span data-ttu-id="691e0-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="691e0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="691e0-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="691e0-139">-WhatIf</span></span>
<span data-ttu-id="691e0-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="691e0-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="691e0-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="691e0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="691e0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="691e0-142">CommonParameters</span></span>
<span data-ttu-id="691e0-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="691e0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="691e0-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="691e0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="691e0-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="691e0-145">INPUTS</span></span>

### <span data-ttu-id="691e0-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="691e0-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="691e0-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="691e0-147">OUTPUTS</span></span>

### <span data-ttu-id="691e0-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="691e0-148">System.Boolean</span></span>

## <span data-ttu-id="691e0-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="691e0-149">NOTES</span></span>

## <span data-ttu-id="691e0-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="691e0-150">RELATED LINKS</span></span>

[<span data-ttu-id="691e0-151">Weitere Informationen zu Azure SQL Datenbankdatenermittlung und -klassifizierung</span><span class="sxs-lookup"><span data-stu-id="691e0-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)