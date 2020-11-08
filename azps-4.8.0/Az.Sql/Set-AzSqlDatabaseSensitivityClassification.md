---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 4409825b758d34e656b18a198aefd0da32824fcd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166000"
---
# <span data-ttu-id="7ea0a-101">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="7ea0a-101">Set-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="7ea0a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ea0a-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea0a-103">Legt die Informationstypen und Vertraulichkeits Beschriftungen von Spalten in der Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-103">Sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="7ea0a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ea0a-104">SYNTAX</span></span>

### <span data-ttu-id="7ea0a-105">ClassificationObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ea0a-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ea0a-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ea0a-106">ColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ea0a-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ea0a-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ea0a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ea0a-108">DESCRIPTION</span></span>
<span data-ttu-id="7ea0a-109">Das Set-AzSqlDatabaseSensitivityClassification-Cmdlet legt die Informationstypen und Vertraulichkeits Beschriftungen von Spalten in der Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-109">The Set-AzSqlDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="7ea0a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ea0a-110">EXAMPLES</span></span>

### <span data-ttu-id="7ea0a-111">Beispiel 1: Einrichten des Informationstyps und der Vertraulichkeits Beschriftung einer Spalte in einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL database.</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="7ea0a-112">Beispiel 2: setzen Sie Empfohlene Informationstypen und Vertraulichkeits Beschriftungen von Spalten in einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="7ea0a-113">Beispiel 3: setzen Sie den Informationstyp und die Vertraulichkeits Beschriftung einer Spalte in einer Azure SQL-Datenbank mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="7ea0a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ea0a-114">PARAMETERS</span></span>

### <span data-ttu-id="7ea0a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ea0a-115">-AsJob</span></span>
<span data-ttu-id="7ea0a-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7ea0a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ea0a-117">-Classificationobject</span><span class="sxs-lookup"><span data-stu-id="7ea0a-117">-ClassificationObject</span></span>
<span data-ttu-id="7ea0a-118">Ein Objekt, das eine SQL-Datenbank-Vertraulichkeits Klassifikation darstellt.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="7ea0a-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="7ea0a-119">-ColumnName</span></span>
<span data-ttu-id="7ea0a-120">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-120">Name of column.</span></span>

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

### <span data-ttu-id="7ea0a-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7ea0a-121">-DatabaseName</span></span>
<span data-ttu-id="7ea0a-122">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="7ea0a-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="7ea0a-123">-DatabaseObject</span></span>
<span data-ttu-id="7ea0a-124">Das SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-124">The SQL database object.</span></span>

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

### <span data-ttu-id="7ea0a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea0a-125">-DefaultProfile</span></span>
<span data-ttu-id="7ea0a-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ea0a-127">-Informationtype</span><span class="sxs-lookup"><span data-stu-id="7ea0a-127">-InformationType</span></span>
<span data-ttu-id="7ea0a-128">Ein Name, der den Informationstyp der in der Spalte gespeicherten Daten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="7ea0a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ea0a-129">-PassThru</span></span>
<span data-ttu-id="7ea0a-130">Gibt an, ob das Sensitivitäts Klassifikationsmodell am Ende der Cmdlet-Ausführung ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="7ea0a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea0a-131">-ResourceGroupName</span></span>
<span data-ttu-id="7ea0a-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="7ea0a-133">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="7ea0a-133">-SchemaName</span></span>
<span data-ttu-id="7ea0a-134">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-134">Name of schema.</span></span>

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

### <span data-ttu-id="7ea0a-135">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="7ea0a-135">-SensitivityLabel</span></span>
<span data-ttu-id="7ea0a-136">Ein Name, der die Vertraulichkeit der in der Spalte gespeicherten Daten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-136">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="7ea0a-137">-Servername</span><span class="sxs-lookup"><span data-stu-id="7ea0a-137">-ServerName</span></span>
<span data-ttu-id="7ea0a-138">SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-138">SQL server name.</span></span>

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

### <span data-ttu-id="7ea0a-139">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="7ea0a-139">-TableName</span></span>
<span data-ttu-id="7ea0a-140">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-140">Name of table.</span></span>

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

### <span data-ttu-id="7ea0a-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7ea0a-141">-Confirm</span></span>
<span data-ttu-id="7ea0a-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ea0a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ea0a-143">-WhatIf</span></span>
<span data-ttu-id="7ea0a-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ea0a-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ea0a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea0a-146">CommonParameters</span></span>
<span data-ttu-id="7ea0a-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ea0a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea0a-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ea0a-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea0a-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ea0a-149">INPUTS</span></span>

### <span data-ttu-id="7ea0a-150">Microsoft. Azure. Commands. SQL. dataclassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="7ea0a-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="7ea0a-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ea0a-151">OUTPUTS</span></span>

### <span data-ttu-id="7ea0a-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ea0a-152">System.Boolean</span></span>

## <span data-ttu-id="7ea0a-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ea0a-153">NOTES</span></span>

## <span data-ttu-id="7ea0a-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ea0a-154">RELATED LINKS</span></span>

[<span data-ttu-id="7ea0a-155">Weitere Informationen zur Azure SQL-Datenbankdaten Ermittlung und-Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="7ea0a-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
