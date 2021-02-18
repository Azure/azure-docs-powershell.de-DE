---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: f524c8b30f609cb2fef3fb3f59550078b26b11b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175121"
---
# <span data-ttu-id="9472e-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="9472e-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="9472e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9472e-102">SYNOPSIS</span></span>
<span data-ttu-id="9472e-103">Legt die Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Azure SQL Instanzdatenbank fest.</span><span class="sxs-lookup"><span data-stu-id="9472e-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="9472e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9472e-104">SYNTAX</span></span>

### <span data-ttu-id="9472e-105">ClassificationObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9472e-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9472e-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9472e-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9472e-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9472e-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9472e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9472e-108">DESCRIPTION</span></span>
<span data-ttu-id="9472e-109">Das Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet legt die Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Azure SQL Instanzdatenbank fest.</span><span class="sxs-lookup"><span data-stu-id="9472e-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="9472e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9472e-110">EXAMPLES</span></span>

### <span data-ttu-id="9472e-111">Beispiel 1: Festlegen des Informationstyps und der Vertraulichkeitsbezeichnung einer Spalte in einer Azure SQL Verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="9472e-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="9472e-112">Beispiel 2: Festlegen empfohlener Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in einer Azure SQL Verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="9472e-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="9472e-113">Beispiel 3: Festlegen des Informationstyps und der Vertraulichkeitsbezeichnung einer Spalte in einer Azure SQL verwalteten Instanzdatenbank mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="9472e-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="9472e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9472e-114">PARAMETERS</span></span>

### <span data-ttu-id="9472e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9472e-115">-AsJob</span></span>
<span data-ttu-id="9472e-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9472e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9472e-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="9472e-117">-ClassificationObject</span></span>
<span data-ttu-id="9472e-118">Ein Objekt, das eine verwaltete SQL A0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="9472e-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="9472e-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="9472e-119">-ColumnName</span></span>
<span data-ttu-id="9472e-120">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="9472e-120">Name of column.</span></span>

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

### <span data-ttu-id="9472e-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9472e-121">-DatabaseName</span></span>
<span data-ttu-id="9472e-122">Der Name der Azure SQL Verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="9472e-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="9472e-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="9472e-123">-DatabaseObject</span></span>
<span data-ttu-id="9472e-124">Das Azure SQL verwaltete Instanzdatenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="9472e-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="9472e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9472e-125">-DefaultProfile</span></span>
<span data-ttu-id="9472e-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9472e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9472e-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="9472e-127">-InformationType</span></span>
<span data-ttu-id="9472e-128">Ein Name, der den Informationstyp der in der Spalte gespeicherten Daten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9472e-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="9472e-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9472e-129">-InstanceName</span></span>
<span data-ttu-id="9472e-130">Azure SQL verwalteten Instanznamen.</span><span class="sxs-lookup"><span data-stu-id="9472e-130">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="9472e-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9472e-131">-PassThru</span></span>
<span data-ttu-id="9472e-132">Gibt an, ob das Vertraulichkeitsklassifikationsmodell am Ende der Ausführung des Cmdlets ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9472e-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="9472e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9472e-133">-ResourceGroupName</span></span>
<span data-ttu-id="9472e-134">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9472e-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="9472e-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9472e-135">-SchemaName</span></span>
<span data-ttu-id="9472e-136">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="9472e-136">Name of schema.</span></span>

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

### <span data-ttu-id="9472e-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="9472e-137">-SensitivityLabel</span></span>
<span data-ttu-id="9472e-138">Ein Name, der die Vertraulichkeit der in der Spalte gespeicherten Daten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9472e-138">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="9472e-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="9472e-139">-TableName</span></span>
<span data-ttu-id="9472e-140">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9472e-140">Name of table.</span></span>

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

### <span data-ttu-id="9472e-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9472e-141">-Confirm</span></span>
<span data-ttu-id="9472e-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9472e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9472e-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9472e-143">-WhatIf</span></span>
<span data-ttu-id="9472e-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9472e-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9472e-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9472e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9472e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9472e-146">CommonParameters</span></span>
<span data-ttu-id="9472e-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9472e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9472e-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9472e-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9472e-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9472e-149">INPUTS</span></span>

### <span data-ttu-id="9472e-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="9472e-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="9472e-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9472e-151">OUTPUTS</span></span>

### <span data-ttu-id="9472e-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9472e-152">System.Boolean</span></span>

## <span data-ttu-id="9472e-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9472e-153">NOTES</span></span>

## <span data-ttu-id="9472e-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9472e-154">RELATED LINKS</span></span>

[<span data-ttu-id="9472e-155">Weitere Informationen zu Azure SQL Datenbankdatenermittlung und -klassifizierung</span><span class="sxs-lookup"><span data-stu-id="9472e-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
