---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 2f7d9421ada70946f18322828c138eca186df5c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948371"
---
# <span data-ttu-id="1a0d8-101">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="1a0d8-101">Disable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="1a0d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a0d8-102">SYNOPSIS</span></span>
<span data-ttu-id="1a0d8-103">Deaktiviert (schließt) Vertraulichkeitsempfehlungen für Spalten in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-103">Disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="1a0d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a0d8-104">SYNTAX</span></span>

### <span data-ttu-id="1a0d8-105">InputObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1a0d8-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a0d8-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a0d8-106">ColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a0d8-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a0d8-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a0d8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a0d8-108">DESCRIPTION</span></span>
<span data-ttu-id="1a0d8-109">Das Disable-AzSqlDatabaseSensitivityRecommendation-Cmdlet deaktiviert (schließt) Vertraulichkeitsempfehlungen für Spalten in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-109">The Disable-AzSqlDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="1a0d8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a0d8-110">EXAMPLES</span></span>

### <span data-ttu-id="1a0d8-111">Beispiel 1: Deaktivieren von Vertraulichkeitsempfehlungen für eine bestimmte Spalte in einer Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Disable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="1a0d8-112">Beispiel 2: Deaktivieren von Vertraulichkeitsempfehlungen für Spalten mit Vertraulichkeitsempfehlungen in einer Azure SQL mit Piping.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation
```

### <span data-ttu-id="1a0d8-113">Beispiel 3: Deaktivieren von Vertraulichkeitsempfehlungen für eine bestimmte Spalte in einer Azure SQL mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="1a0d8-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1a0d8-114">PARAMETERS</span></span>

### <span data-ttu-id="1a0d8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a0d8-115">-AsJob</span></span>
<span data-ttu-id="1a0d8-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1a0d8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a0d8-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="1a0d8-117">-ColumnName</span></span>
<span data-ttu-id="1a0d8-118">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-118">Name of column.</span></span>

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

### <span data-ttu-id="1a0d8-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1a0d8-119">-DatabaseName</span></span>
<span data-ttu-id="1a0d8-120">Der Name der Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-120">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="1a0d8-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="1a0d8-121">-DatabaseObject</span></span>
<span data-ttu-id="1a0d8-122">Das SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-122">The SQL database object.</span></span>

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

### <span data-ttu-id="1a0d8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a0d8-123">-DefaultProfile</span></span>
<span data-ttu-id="1a0d8-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a0d8-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a0d8-125">-InputObject</span></span>
<span data-ttu-id="1a0d8-126">Ein Objekt, das eine SQL Datenbanksensitivitätsklassifizierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-126">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="1a0d8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a0d8-127">-PassThru</span></span>
<span data-ttu-id="1a0d8-128">Gibt an, ob das Vertraulichkeitsklassifizierungsmodell am Ende der Cmdletausführung ausgegeben werden soll</span><span class="sxs-lookup"><span data-stu-id="1a0d8-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="1a0d8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a0d8-129">-ResourceGroupName</span></span>
<span data-ttu-id="1a0d8-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="1a0d8-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="1a0d8-131">-SchemaName</span></span>
<span data-ttu-id="1a0d8-132">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-132">Name of schema.</span></span>

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

### <span data-ttu-id="1a0d8-133">-Servername</span><span class="sxs-lookup"><span data-stu-id="1a0d8-133">-ServerName</span></span>
<span data-ttu-id="1a0d8-134">SQL Servername.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-134">SQL server name.</span></span>

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

### <span data-ttu-id="1a0d8-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="1a0d8-135">-TableName</span></span>
<span data-ttu-id="1a0d8-136">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-136">Name of table.</span></span>

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

### <span data-ttu-id="1a0d8-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1a0d8-137">-Confirm</span></span>
<span data-ttu-id="1a0d8-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a0d8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a0d8-139">-WhatIf</span></span>
<span data-ttu-id="1a0d8-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a0d8-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a0d8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a0d8-142">CommonParameters</span></span>
<span data-ttu-id="1a0d8-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a0d8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a0d8-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a0d8-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a0d8-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a0d8-145">INPUTS</span></span>

### <span data-ttu-id="1a0d8-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="1a0d8-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="1a0d8-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a0d8-147">OUTPUTS</span></span>

### <span data-ttu-id="1a0d8-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1a0d8-148">System.Boolean</span></span>

## <span data-ttu-id="1a0d8-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1a0d8-149">NOTES</span></span>

## <span data-ttu-id="1a0d8-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1a0d8-150">RELATED LINKS</span></span>

[<span data-ttu-id="1a0d8-151">Weitere Informationen zu Azure SQL Datenbankdatenermittlung und -klassifizierung</span><span class="sxs-lookup"><span data-stu-id="1a0d8-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)