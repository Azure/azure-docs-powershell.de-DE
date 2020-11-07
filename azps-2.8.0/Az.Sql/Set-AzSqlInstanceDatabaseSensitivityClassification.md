---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: c476f19f8c2ab8af334f92e75b67aeee151793fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825840"
---
# <span data-ttu-id="9ab66-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="9ab66-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="9ab66-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ab66-102">SYNOPSIS</span></span>
<span data-ttu-id="9ab66-103">Legt die Informationstypen und Vertraulichkeits Beschriftungen von Spalten in der Azure SQL-Datenbank für verwaltete Instanzen fest.</span><span class="sxs-lookup"><span data-stu-id="9ab66-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="9ab66-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ab66-104">SYNTAX</span></span>

### <span data-ttu-id="9ab66-105">ClassificationObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ab66-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ab66-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ab66-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ab66-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ab66-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ab66-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ab66-108">DESCRIPTION</span></span>
<span data-ttu-id="9ab66-109">Das Set-AzSqlInstanceDatabaseSensitivityClassification-Cmdlet legt die Informationstypen und Vertraulichkeits Beschriftungen von Spalten in der Azure SQL-Instanzdatenbank für verwaltete Instanzen fest.</span><span class="sxs-lookup"><span data-stu-id="9ab66-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="9ab66-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ab66-110">EXAMPLES</span></span>

### <span data-ttu-id="9ab66-111">Beispiel 1: Einrichten des Informationstyps und der Vertraulichkeits Beschriftung einer Spalte in einer Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="9ab66-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="9ab66-112">Beispiel 2: setzen Sie Empfohlene Informationstypen und Vertraulichkeits Beschriftungen von Spalten in einer Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="9ab66-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="9ab66-113">Beispiel 3: setzen Sie den Informationstyp und die Vertraulichkeits Beschriftung einer Spalte in einer Azure SQL-Datenbank mit verwalteten Instanzen mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="9ab66-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="9ab66-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ab66-114">PARAMETERS</span></span>

### <span data-ttu-id="9ab66-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ab66-115">-AsJob</span></span>
<span data-ttu-id="9ab66-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9ab66-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ab66-117">-Classificationobject</span><span class="sxs-lookup"><span data-stu-id="9ab66-117">-ClassificationObject</span></span>
<span data-ttu-id="9ab66-118">Ein Objekt, das eine Datenbank-Vertraulichkeits Klassifikation für SQL-verwaltete Instanzen darstellt.</span><span class="sxs-lookup"><span data-stu-id="9ab66-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ab66-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="9ab66-119">-ColumnName</span></span>
<span data-ttu-id="9ab66-120">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="9ab66-120">Name of column.</span></span>

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

### <span data-ttu-id="9ab66-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9ab66-121">-DatabaseName</span></span>
<span data-ttu-id="9ab66-122">Der Name der Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="9ab66-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="9ab66-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="9ab66-123">-DatabaseObject</span></span>
<span data-ttu-id="9ab66-124">Das Datenbankobjekt der Azure SQL-Instanz</span><span class="sxs-lookup"><span data-stu-id="9ab66-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ab66-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ab66-125">-DefaultProfile</span></span>
<span data-ttu-id="9ab66-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9ab66-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ab66-127">-Informationtype</span><span class="sxs-lookup"><span data-stu-id="9ab66-127">-InformationType</span></span>
<span data-ttu-id="9ab66-128">Ein Name, der den Informationstyp der in der Spalte gespeicherten Daten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9ab66-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="9ab66-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9ab66-129">-InstanceName</span></span>
<span data-ttu-id="9ab66-130">Name der verwalteten Azure SQL-Instanz.</span><span class="sxs-lookup"><span data-stu-id="9ab66-130">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="9ab66-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ab66-131">-PassThru</span></span>
<span data-ttu-id="9ab66-132">Gibt an, ob das Sensitivitäts Klassifikationsmodell am Ende der Cmdlet-Ausführung ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ab66-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="9ab66-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ab66-133">-ResourceGroupName</span></span>
<span data-ttu-id="9ab66-134">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9ab66-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="9ab66-135">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="9ab66-135">-SchemaName</span></span>
<span data-ttu-id="9ab66-136">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="9ab66-136">Name of schema.</span></span>

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

### <span data-ttu-id="9ab66-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="9ab66-137">-SensitivityLabel</span></span>
<span data-ttu-id="9ab66-138">Ein Name, der die Vertraulichkeit der in der Spalte gespeicherten Daten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9ab66-138">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="9ab66-139">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="9ab66-139">-TableName</span></span>
<span data-ttu-id="9ab66-140">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9ab66-140">Name of table.</span></span>

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

### <span data-ttu-id="9ab66-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ab66-141">-Confirm</span></span>
<span data-ttu-id="9ab66-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ab66-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ab66-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ab66-143">-WhatIf</span></span>
<span data-ttu-id="9ab66-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ab66-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ab66-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ab66-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ab66-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab66-146">CommonParameters</span></span>
<span data-ttu-id="9ab66-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ab66-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab66-148">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ab66-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab66-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ab66-149">INPUTS</span></span>

### <span data-ttu-id="9ab66-150">Microsoft. Azure. Commands. SQL. dataclassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="9ab66-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="9ab66-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ab66-151">OUTPUTS</span></span>

### <span data-ttu-id="9ab66-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ab66-152">System.Boolean</span></span>

## <span data-ttu-id="9ab66-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ab66-153">NOTES</span></span>

## <span data-ttu-id="9ab66-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ab66-154">RELATED LINKS</span></span>

[<span data-ttu-id="9ab66-155">Weitere Informationen zur Azure SQL-Datenbankdaten Ermittlung und-Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="9ab66-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
