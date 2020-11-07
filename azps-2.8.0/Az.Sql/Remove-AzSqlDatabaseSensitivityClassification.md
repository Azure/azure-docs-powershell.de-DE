---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: d60eff325b0240591fc3360276447861560860ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825956"
---
# <span data-ttu-id="ed5b6-101">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="ed5b6-101">Remove-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="ed5b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed5b6-102">SYNOPSIS</span></span>
<span data-ttu-id="ed5b6-103">Entfernt die Informationstypen und Vertraulichkeits Beschriftungen von Spalten in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-103">Removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="ed5b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed5b6-104">SYNTAX</span></span>

### <span data-ttu-id="ed5b6-105">ClassificationObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed5b6-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed5b6-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed5b6-106">ColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed5b6-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed5b6-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed5b6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed5b6-108">DESCRIPTION</span></span>
<span data-ttu-id="ed5b6-109">Das Remove-AzSqlDatabaseSensitivityClassification-Cmdlet entfernt die Informationstypen und Vertraulichkeits Bezeichnungen von Spalten in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-109">The Remove-AzSqlDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="ed5b6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed5b6-110">EXAMPLES</span></span>

### <span data-ttu-id="ed5b6-111">Beispiel 1: Entfernen des Informationstyps und der Vertraulichkeits Beschriftung einer Spalte in einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="ed5b6-112">Beispiel 2: Entfernen Sie aktuelle Informationstypen und Vertraulichkeits Beschriftungen von Spalten in einer Azure SQL-Datenbank mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="ed5b6-113">Beispiel 3: Entfernen des Informationstyps und der Vertraulichkeits Beschriftung einer Spalte in einer Azure SQL-Datenbank mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="ed5b6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed5b6-114">PARAMETERS</span></span>

### <span data-ttu-id="ed5b6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed5b6-115">-AsJob</span></span>
<span data-ttu-id="ed5b6-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ed5b6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed5b6-117">-Classificationobject</span><span class="sxs-lookup"><span data-stu-id="ed5b6-117">-ClassificationObject</span></span>
<span data-ttu-id="ed5b6-118">Ein Objekt, das eine SQL-Datenbank-Vertraulichkeits Klassifikation darstellt.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="ed5b6-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="ed5b6-119">-ColumnName</span></span>
<span data-ttu-id="ed5b6-120">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-120">Name of column.</span></span>

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

### <span data-ttu-id="ed5b6-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ed5b6-121">-DatabaseName</span></span>
<span data-ttu-id="ed5b6-122">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="ed5b6-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="ed5b6-123">-DatabaseObject</span></span>
<span data-ttu-id="ed5b6-124">Das SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-124">The SQL database object.</span></span>

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

### <span data-ttu-id="ed5b6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed5b6-125">-DefaultProfile</span></span>
<span data-ttu-id="ed5b6-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed5b6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed5b6-127">-PassThru</span></span>
<span data-ttu-id="ed5b6-128">Gibt an, ob das Sensitivitäts Klassifikationsmodell am Ende der Cmdlet-Ausführung ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="ed5b6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed5b6-129">-ResourceGroupName</span></span>
<span data-ttu-id="ed5b6-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="ed5b6-131">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="ed5b6-131">-SchemaName</span></span>
<span data-ttu-id="ed5b6-132">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-132">Name of schema.</span></span>

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

### <span data-ttu-id="ed5b6-133">-Servername</span><span class="sxs-lookup"><span data-stu-id="ed5b6-133">-ServerName</span></span>
<span data-ttu-id="ed5b6-134">SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-134">SQL server name.</span></span>

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

### <span data-ttu-id="ed5b6-135">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="ed5b6-135">-TableName</span></span>
<span data-ttu-id="ed5b6-136">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-136">Name of table.</span></span>

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

### <span data-ttu-id="ed5b6-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ed5b6-137">-Confirm</span></span>
<span data-ttu-id="ed5b6-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed5b6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed5b6-139">-WhatIf</span></span>
<span data-ttu-id="ed5b6-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed5b6-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed5b6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed5b6-142">CommonParameters</span></span>
<span data-ttu-id="ed5b6-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed5b6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed5b6-144">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed5b6-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed5b6-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed5b6-145">INPUTS</span></span>

### <span data-ttu-id="ed5b6-146">Microsoft. Azure. Commands. SQL. dataclassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="ed5b6-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="ed5b6-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed5b6-147">OUTPUTS</span></span>

### <span data-ttu-id="ed5b6-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed5b6-148">System.Boolean</span></span>

## <span data-ttu-id="ed5b6-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed5b6-149">NOTES</span></span>

## <span data-ttu-id="ed5b6-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed5b6-150">RELATED LINKS</span></span>

[<span data-ttu-id="ed5b6-151">Weitere Informationen zur Azure SQL-Datenbankdaten Ermittlung und-Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="ed5b6-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
