---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: fa187bad03027f1c0dd3e1c38e8b05dfb9257f05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825923"
---
# <span data-ttu-id="ece56-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="ece56-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="ece56-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ece56-102">SYNOPSIS</span></span>
<span data-ttu-id="ece56-103">Entfernt die Informationstypen und Vertraulichkeits Bezeichnungen von Spalten in der Azure SQL-Instanzdatenbank für verwaltete Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="ece56-103">Removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="ece56-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ece56-104">SYNTAX</span></span>

### <span data-ttu-id="ece56-105">ClassificationObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ece56-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece56-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece56-106">ColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece56-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece56-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ece56-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ece56-108">DESCRIPTION</span></span>
<span data-ttu-id="ece56-109">Das Remove-AzSqlInstanceDatabaseSensitivityClassification-Cmdlet entfernt die Informationstypen und Vertraulichkeits Bezeichnungen von Spalten in der Azure SQL-Instanzdatenbank für verwaltete Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="ece56-109">The Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="ece56-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ece56-110">EXAMPLES</span></span>

### <span data-ttu-id="ece56-111">Beispiel 1: Entfernen des Informationstyps und der Vertraulichkeits Beschriftung einer Spalte in einer Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="ece56-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="ece56-112">Beispiel 2: Entfernen der aktuellen Informationstypen und Vertraulichkeits Beschriftungen von Spalten in einer Azure SQL-Datenbank mit verwalteten Instanzen mit Piping.</span><span class="sxs-lookup"><span data-stu-id="ece56-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Remove-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="ece56-113">Beispiel 3: Entfernen des Informationstyps und der Vertraulichkeits Beschriftung einer Spalte in einer Azure SQL-Datenbank mit verwalteten Instanzen mit Piping.</span><span class="sxs-lookup"><span data-stu-id="ece56-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="ece56-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ece56-114">PARAMETERS</span></span>

### <span data-ttu-id="ece56-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ece56-115">-AsJob</span></span>
<span data-ttu-id="ece56-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ece56-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ece56-117">-Classificationobject</span><span class="sxs-lookup"><span data-stu-id="ece56-117">-ClassificationObject</span></span>
<span data-ttu-id="ece56-118">Ein Objekt, das eine Datenbank-Vertraulichkeits Klassifikation für SQL-verwaltete Instanzen darstellt.</span><span class="sxs-lookup"><span data-stu-id="ece56-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="ece56-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="ece56-119">-ColumnName</span></span>
<span data-ttu-id="ece56-120">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="ece56-120">Name of column.</span></span>

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

### <span data-ttu-id="ece56-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ece56-121">-DatabaseName</span></span>
<span data-ttu-id="ece56-122">Der Name der Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="ece56-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="ece56-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="ece56-123">-DatabaseObject</span></span>
<span data-ttu-id="ece56-124">Das Datenbankobjekt der Azure SQL-Instanz</span><span class="sxs-lookup"><span data-stu-id="ece56-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="ece56-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece56-125">-DefaultProfile</span></span>
<span data-ttu-id="ece56-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ece56-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ece56-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ece56-127">-InstanceName</span></span>
<span data-ttu-id="ece56-128">Name der verwalteten Azure SQL-Instanz.</span><span class="sxs-lookup"><span data-stu-id="ece56-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="ece56-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ece56-129">-PassThru</span></span>
<span data-ttu-id="ece56-130">Gibt an, ob das Sensitivitäts Klassifikationsmodell am Ende der Cmdlet-Ausführung ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="ece56-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="ece56-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ece56-131">-ResourceGroupName</span></span>
<span data-ttu-id="ece56-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ece56-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="ece56-133">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="ece56-133">-SchemaName</span></span>
<span data-ttu-id="ece56-134">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="ece56-134">Name of schema.</span></span>

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

### <span data-ttu-id="ece56-135">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="ece56-135">-TableName</span></span>
<span data-ttu-id="ece56-136">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ece56-136">Name of table.</span></span>

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

### <span data-ttu-id="ece56-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ece56-137">-Confirm</span></span>
<span data-ttu-id="ece56-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ece56-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ece56-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece56-139">-WhatIf</span></span>
<span data-ttu-id="ece56-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ece56-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ece56-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ece56-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ece56-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece56-142">CommonParameters</span></span>
<span data-ttu-id="ece56-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ece56-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece56-144">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ece56-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece56-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ece56-145">INPUTS</span></span>

### <span data-ttu-id="ece56-146">Microsoft. Azure. Commands. SQL. dataclassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="ece56-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="ece56-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ece56-147">OUTPUTS</span></span>

### <span data-ttu-id="ece56-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ece56-148">System.Boolean</span></span>

## <span data-ttu-id="ece56-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="ece56-149">NOTES</span></span>

## <span data-ttu-id="ece56-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ece56-150">RELATED LINKS</span></span>

[<span data-ttu-id="ece56-151">Weitere Informationen zur Azure SQL-Datenbankdaten Ermittlung und-Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="ece56-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
