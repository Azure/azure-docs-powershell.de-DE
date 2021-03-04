---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: fac62ac0e75587e19a9ba0a5e99461693ce31c0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922288"
---
# <span data-ttu-id="29411-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="29411-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="29411-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29411-102">SYNOPSIS</span></span>
<span data-ttu-id="29411-103">Legt die Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Azure SQL verwalteten Instanzdatenbank fest.</span><span class="sxs-lookup"><span data-stu-id="29411-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="29411-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29411-104">SYNTAX</span></span>

### <span data-ttu-id="29411-105">ClassificationObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="29411-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29411-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="29411-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29411-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="29411-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29411-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29411-108">DESCRIPTION</span></span>
<span data-ttu-id="29411-109">Das Set-AzSqlInstanceDatabaseSensitivityClassification-Cmdlet legt die Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Azure SQL verwalteten Instanzdatenbank fest.</span><span class="sxs-lookup"><span data-stu-id="29411-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="29411-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29411-110">EXAMPLES</span></span>

### <span data-ttu-id="29411-111">Beispiel 1: Festlegen von Informationstyp und Vertraulichkeitsbeschriftung einer Spalte in einer Azure SQL verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="29411-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="29411-112">Beispiel 2: Festlegen empfohlener Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in einer Azure SQL verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="29411-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="29411-113">Beispiel 3: Festlegen von Informationstyp und Vertraulichkeitsbeschriftung einer Spalte in einer Azure SQL verwaltete Instanzdatenbank mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="29411-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="29411-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="29411-114">PARAMETERS</span></span>

### <span data-ttu-id="29411-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29411-115">-AsJob</span></span>
<span data-ttu-id="29411-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="29411-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29411-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="29411-117">-ClassificationObject</span></span>
<span data-ttu-id="29411-118">Ein Objekt, das eine SQL Verwaltete Instanz-Datenbanksensitivitätsklassifizierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="29411-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="29411-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="29411-119">-ColumnName</span></span>
<span data-ttu-id="29411-120">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="29411-120">Name of column.</span></span>

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

### <span data-ttu-id="29411-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="29411-121">-DatabaseName</span></span>
<span data-ttu-id="29411-122">Der Name der Azure SQL verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="29411-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="29411-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="29411-123">-DatabaseObject</span></span>
<span data-ttu-id="29411-124">Das Azure SQL verwaltete Instanzdatenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="29411-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="29411-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29411-125">-DefaultProfile</span></span>
<span data-ttu-id="29411-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29411-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29411-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="29411-127">-InformationType</span></span>
<span data-ttu-id="29411-128">Ein Name, der den Informationstyp der in der Spalte gespeicherten Daten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="29411-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="29411-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="29411-129">-InstanceName</span></span>
<span data-ttu-id="29411-130">Azure SQL verwalteten Instanznamen.</span><span class="sxs-lookup"><span data-stu-id="29411-130">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="29411-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29411-131">-PassThru</span></span>
<span data-ttu-id="29411-132">Gibt an, ob das Vertraulichkeitsklassifizierungsmodell am Ende der Cmdletausführung ausgegeben werden soll</span><span class="sxs-lookup"><span data-stu-id="29411-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="29411-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29411-133">-ResourceGroupName</span></span>
<span data-ttu-id="29411-134">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="29411-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="29411-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="29411-135">-SchemaName</span></span>
<span data-ttu-id="29411-136">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="29411-136">Name of schema.</span></span>

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

### <span data-ttu-id="29411-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="29411-137">-SensitivityLabel</span></span>
<span data-ttu-id="29411-138">Ein Name, der die Vertraulichkeit der in der Spalte gespeicherten Daten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="29411-138">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="29411-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="29411-139">-TableName</span></span>
<span data-ttu-id="29411-140">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="29411-140">Name of table.</span></span>

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

### <span data-ttu-id="29411-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29411-141">-Confirm</span></span>
<span data-ttu-id="29411-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29411-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29411-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29411-143">-WhatIf</span></span>
<span data-ttu-id="29411-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29411-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29411-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29411-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29411-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29411-146">CommonParameters</span></span>
<span data-ttu-id="29411-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29411-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29411-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29411-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29411-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29411-149">INPUTS</span></span>

### <span data-ttu-id="29411-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="29411-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="29411-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29411-151">OUTPUTS</span></span>

### <span data-ttu-id="29411-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="29411-152">System.Boolean</span></span>

## <span data-ttu-id="29411-153">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="29411-153">NOTES</span></span>

## <span data-ttu-id="29411-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="29411-154">RELATED LINKS</span></span>

[<span data-ttu-id="29411-155">Weitere Informationen zu Azure SQL Datenbankdatenermittlung und -klassifizierung</span><span class="sxs-lookup"><span data-stu-id="29411-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
