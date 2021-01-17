---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: c594a9bf247355201bc08e438af1d9dff8cd3f7d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460608"
---
# <span data-ttu-id="74fc7-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="74fc7-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="74fc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74fc7-102">SYNOPSIS</span></span>
<span data-ttu-id="74fc7-103">Entfernt die Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Azure SQL verwalteten Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="74fc7-103">Removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="74fc7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74fc7-104">SYNTAX</span></span>

### <span data-ttu-id="74fc7-105">ClassificationObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="74fc7-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74fc7-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="74fc7-106">ColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74fc7-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="74fc7-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74fc7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74fc7-108">DESCRIPTION</span></span>
<span data-ttu-id="74fc7-109">Das Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet entfernt die Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Azure SQL Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="74fc7-109">The Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="74fc7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="74fc7-110">EXAMPLES</span></span>

### <span data-ttu-id="74fc7-111">Beispiel 1: Entfernen des Informationstyps und der Vertraulichkeitsbezeichnung einer Spalte in einer Azure SQL Verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="74fc7-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="74fc7-112">Beispiel 2: Entfernen der aktuellen Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in einer Azure SQL Verwaltete Instanzdatenbank mit Piping.</span><span class="sxs-lookup"><span data-stu-id="74fc7-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Remove-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="74fc7-113">Beispiel 3: Entfernen des Informationstyps und der Vertraulichkeitsbeschriftung einer Spalte in einer Azure SQL Verwaltete Instanzdatenbank mit Piping.</span><span class="sxs-lookup"><span data-stu-id="74fc7-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="74fc7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74fc7-114">PARAMETERS</span></span>

### <span data-ttu-id="74fc7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74fc7-115">-AsJob</span></span>
<span data-ttu-id="74fc7-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="74fc7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74fc7-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="74fc7-117">-ClassificationObject</span></span>
<span data-ttu-id="74fc7-118">Ein Objekt, das eine verwaltete SQL A0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="74fc7-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="74fc7-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="74fc7-119">-ColumnName</span></span>
<span data-ttu-id="74fc7-120">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="74fc7-120">Name of column.</span></span>

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

### <span data-ttu-id="74fc7-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="74fc7-121">-DatabaseName</span></span>
<span data-ttu-id="74fc7-122">Der Name der Azure SQL Verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="74fc7-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="74fc7-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="74fc7-123">-DatabaseObject</span></span>
<span data-ttu-id="74fc7-124">Das Azure SQL verwaltete Instanzdatenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="74fc7-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="74fc7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74fc7-125">-DefaultProfile</span></span>
<span data-ttu-id="74fc7-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74fc7-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74fc7-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="74fc7-127">-InstanceName</span></span>
<span data-ttu-id="74fc7-128">Azure SQL verwalteten Instanznamen.</span><span class="sxs-lookup"><span data-stu-id="74fc7-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="74fc7-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74fc7-129">-PassThru</span></span>
<span data-ttu-id="74fc7-130">Gibt an, ob das Vertraulichkeitsklassifikationsmodell am Ende der Ausführung des Cmdlets ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="74fc7-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="74fc7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74fc7-131">-ResourceGroupName</span></span>
<span data-ttu-id="74fc7-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="74fc7-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="74fc7-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="74fc7-133">-SchemaName</span></span>
<span data-ttu-id="74fc7-134">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="74fc7-134">Name of schema.</span></span>

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

### <span data-ttu-id="74fc7-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="74fc7-135">-TableName</span></span>
<span data-ttu-id="74fc7-136">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="74fc7-136">Name of table.</span></span>

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

### <span data-ttu-id="74fc7-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74fc7-137">-Confirm</span></span>
<span data-ttu-id="74fc7-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74fc7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74fc7-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="74fc7-139">-WhatIf</span></span>
<span data-ttu-id="74fc7-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74fc7-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74fc7-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74fc7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74fc7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74fc7-142">CommonParameters</span></span>
<span data-ttu-id="74fc7-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74fc7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74fc7-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74fc7-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74fc7-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="74fc7-145">INPUTS</span></span>

### <span data-ttu-id="74fc7-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="74fc7-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="74fc7-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="74fc7-147">OUTPUTS</span></span>

### <span data-ttu-id="74fc7-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="74fc7-148">System.Boolean</span></span>

## <span data-ttu-id="74fc7-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="74fc7-149">NOTES</span></span>

## <span data-ttu-id="74fc7-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="74fc7-150">RELATED LINKS</span></span>

[<span data-ttu-id="74fc7-151">Weitere Informationen zu Azure SQL Datenbankdatenermittlung und -klassifizierung</span><span class="sxs-lookup"><span data-stu-id="74fc7-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
