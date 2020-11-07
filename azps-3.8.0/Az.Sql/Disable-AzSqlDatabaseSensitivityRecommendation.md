---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f9a8ab299571e4e04f3061773d19b920f52d22a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846644"
---
# <span data-ttu-id="edf80-101">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="edf80-101">Disable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="edf80-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="edf80-102">SYNOPSIS</span></span>
<span data-ttu-id="edf80-103">Deaktiviert (Kündigungen) Vertraulichkeits Empfehlungen für Spalten in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="edf80-103">Disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="edf80-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="edf80-104">SYNTAX</span></span>

### <span data-ttu-id="edf80-105">InputObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="edf80-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edf80-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="edf80-106">ColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edf80-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="edf80-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edf80-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edf80-108">DESCRIPTION</span></span>
<span data-ttu-id="edf80-109">Das Disable-AzSqlDatabaseSensitivityRecommendation-Cmdlet deaktiviert Vertraulichkeits Empfehlungen für Spalten in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="edf80-109">The Disable-AzSqlDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="edf80-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="edf80-110">EXAMPLES</span></span>

### <span data-ttu-id="edf80-111">Beispiel 1: Deaktivieren von Vertraulichkeits Empfehlungen für eine bestimmte Spalte in einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="edf80-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Disable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="edf80-112">Beispiel 2: Deaktivieren Sie die Vertraulichkeits Empfehlungen für Spalten, die in einer Azure SQL-Datenbank mithilfe von Piping Vertraulichkeits Empfehlungen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="edf80-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation
```

### <span data-ttu-id="edf80-113">Beispiel 3: Deaktivieren von Vertraulichkeits Empfehlungen für eine bestimmte Spalte in einer Azure SQL-Datenbank mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="edf80-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="edf80-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="edf80-114">PARAMETERS</span></span>

### <span data-ttu-id="edf80-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="edf80-115">-AsJob</span></span>
<span data-ttu-id="edf80-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="edf80-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="edf80-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="edf80-117">-ColumnName</span></span>
<span data-ttu-id="edf80-118">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="edf80-118">Name of column.</span></span>

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

### <span data-ttu-id="edf80-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="edf80-119">-DatabaseName</span></span>
<span data-ttu-id="edf80-120">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="edf80-120">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="edf80-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="edf80-121">-DatabaseObject</span></span>
<span data-ttu-id="edf80-122">Das SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="edf80-122">The SQL database object.</span></span>

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

### <span data-ttu-id="edf80-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edf80-123">-DefaultProfile</span></span>
<span data-ttu-id="edf80-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="edf80-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edf80-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="edf80-125">-InputObject</span></span>
<span data-ttu-id="edf80-126">Ein Objekt, das eine SQL-Datenbank-Vertraulichkeits Klassifikation darstellt.</span><span class="sxs-lookup"><span data-stu-id="edf80-126">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="edf80-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edf80-127">-PassThru</span></span>
<span data-ttu-id="edf80-128">Gibt an, ob das Sensitivitäts Klassifikationsmodell am Ende der Cmdlet-Ausführung ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="edf80-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="edf80-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edf80-129">-ResourceGroupName</span></span>
<span data-ttu-id="edf80-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="edf80-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="edf80-131">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="edf80-131">-SchemaName</span></span>
<span data-ttu-id="edf80-132">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="edf80-132">Name of schema.</span></span>

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

### <span data-ttu-id="edf80-133">-Servername</span><span class="sxs-lookup"><span data-stu-id="edf80-133">-ServerName</span></span>
<span data-ttu-id="edf80-134">SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="edf80-134">SQL server name.</span></span>

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

### <span data-ttu-id="edf80-135">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="edf80-135">-TableName</span></span>
<span data-ttu-id="edf80-136">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="edf80-136">Name of table.</span></span>

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

### <span data-ttu-id="edf80-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="edf80-137">-Confirm</span></span>
<span data-ttu-id="edf80-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="edf80-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edf80-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edf80-139">-WhatIf</span></span>
<span data-ttu-id="edf80-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="edf80-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="edf80-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="edf80-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edf80-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edf80-142">CommonParameters</span></span>
<span data-ttu-id="edf80-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edf80-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edf80-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="edf80-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edf80-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="edf80-145">INPUTS</span></span>

### <span data-ttu-id="edf80-146">Microsoft. Azure. Commands. SQL. dataclassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="edf80-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="edf80-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="edf80-147">OUTPUTS</span></span>

### <span data-ttu-id="edf80-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="edf80-148">System.Boolean</span></span>

## <span data-ttu-id="edf80-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="edf80-149">NOTES</span></span>

## <span data-ttu-id="edf80-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="edf80-150">RELATED LINKS</span></span>

[<span data-ttu-id="edf80-151">Weitere Informationen zur Azure SQL-Datenbankdaten Ermittlung und-Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="edf80-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)