---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: e21bf168093d2589321d6952ca45af7e9f8c0cbe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372027"
---
# <span data-ttu-id="99658-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="99658-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="99658-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99658-102">SYNOPSIS</span></span>
<span data-ttu-id="99658-103">Aktiviert Vertraulichkeitsempfehlungen für Spalten (Empfehlungen sind standardmäßig für alle Spalten aktiviert) in der Azure SQL Verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="99658-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="99658-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99658-104">SYNTAX</span></span>

### <span data-ttu-id="99658-105">InputObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="99658-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99658-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="99658-106">ColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99658-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="99658-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99658-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99658-108">DESCRIPTION</span></span>
<span data-ttu-id="99658-109">Das Enable-AzSqlInstanceDatabaseSensitivityRecommendation ermöglicht Vertraulichkeitsempfehlungen für Spalten in der Azure SQL Verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="99658-109">The Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="99658-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="99658-110">EXAMPLES</span></span>

### <span data-ttu-id="99658-111">Beispiel 1: Aktivieren von Vertraulichkeitsempfehlungen für eine bestimmte Spalte in einer Azure SQL verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="99658-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Enable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="99658-112">Beispiel 2: Aktivieren von Vertraulichkeitsempfehlungen für eine bestimmte Spalte in einer Azure SQL Verwaltete Instanzdatenbank mit Piping.</span><span class="sxs-lookup"><span data-stu-id="99658-112">Example 2: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="99658-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99658-113">PARAMETERS</span></span>

### <span data-ttu-id="99658-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99658-114">-AsJob</span></span>
<span data-ttu-id="99658-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="99658-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99658-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="99658-116">-ColumnName</span></span>
<span data-ttu-id="99658-117">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="99658-117">Name of column.</span></span>

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

### <span data-ttu-id="99658-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="99658-118">-DatabaseName</span></span>
<span data-ttu-id="99658-119">Der Name der Azure SQL Verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="99658-119">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="99658-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="99658-120">-DatabaseObject</span></span>
<span data-ttu-id="99658-121">Das Azure SQL verwaltete Instanzdatenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="99658-121">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="99658-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99658-122">-DefaultProfile</span></span>
<span data-ttu-id="99658-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99658-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99658-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99658-124">-InputObject</span></span>
<span data-ttu-id="99658-125">Ein Objekt, das eine verwaltete SQL A0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="99658-125">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99658-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="99658-126">-InstanceName</span></span>
<span data-ttu-id="99658-127">Azure SQL verwalteten Instanznamen.</span><span class="sxs-lookup"><span data-stu-id="99658-127">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="99658-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99658-128">-PassThru</span></span>
<span data-ttu-id="99658-129">Gibt an, ob das Vertraulichkeitsklassifikationsmodell am Ende der Ausführung des Cmdlets ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="99658-129">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="99658-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99658-130">-ResourceGroupName</span></span>
<span data-ttu-id="99658-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="99658-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="99658-132">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="99658-132">-SchemaName</span></span>
<span data-ttu-id="99658-133">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="99658-133">Name of schema.</span></span>

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

### <span data-ttu-id="99658-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="99658-134">-TableName</span></span>
<span data-ttu-id="99658-135">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="99658-135">Name of table.</span></span>

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

### <span data-ttu-id="99658-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99658-136">-Confirm</span></span>
<span data-ttu-id="99658-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="99658-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99658-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="99658-138">-WhatIf</span></span>
<span data-ttu-id="99658-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99658-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99658-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="99658-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99658-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99658-141">CommonParameters</span></span>
<span data-ttu-id="99658-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99658-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99658-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99658-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99658-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="99658-144">INPUTS</span></span>

### <span data-ttu-id="99658-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="99658-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="99658-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="99658-146">OUTPUTS</span></span>

### <span data-ttu-id="99658-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="99658-147">System.Boolean</span></span>

## <span data-ttu-id="99658-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="99658-148">NOTES</span></span>

## <span data-ttu-id="99658-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="99658-149">RELATED LINKS</span></span>

[<span data-ttu-id="99658-150">Weitere Informationen zu Azure SQL Datenbankdatenermittlung und -klassifizierung</span><span class="sxs-lookup"><span data-stu-id="99658-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)