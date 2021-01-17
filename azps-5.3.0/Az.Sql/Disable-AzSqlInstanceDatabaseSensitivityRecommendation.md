---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 72118b8edd5f9816e14a5cfd19abbd5cabaca3dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375317"
---
# <span data-ttu-id="a4016-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="a4016-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="a4016-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4016-102">SYNOPSIS</span></span>
<span data-ttu-id="a4016-103">Deaktiviert (schließt) Vertraulichkeitsempfehlungen für Spalten in der Azure SQL verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="a4016-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="a4016-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4016-104">SYNTAX</span></span>

### <span data-ttu-id="a4016-105">InputObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a4016-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4016-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4016-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4016-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4016-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4016-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4016-108">DESCRIPTION</span></span>
<span data-ttu-id="a4016-109">Das Disable-AzSqlInstanceDatabaseSensitivityRecommendation deaktiviert (schließt) Vertraulichkeitsempfehlungen für Spalten in der Azure SQL Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="a4016-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="a4016-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a4016-110">EXAMPLES</span></span>

### <span data-ttu-id="a4016-111">Beispiel 1: Deaktivieren Sie Vertraulichkeitsempfehlungen für eine bestimmte Spalte in einer Azure SQL verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="a4016-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="a4016-112">Beispiel 2: Deaktivieren Sie Vertraulichkeitsempfehlungen für Spalten, die Vertraulichkeitsempfehlungen in einer Azure SQL Verwaltete Instanzdatenbank mit Piping enthalten.</span><span class="sxs-lookup"><span data-stu-id="a4016-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="a4016-113">Beispiel 3: Deaktivieren sie Vertraulichkeitsempfehlungen für eine bestimmte Spalte in einer Azure SQL Verwaltete Instanzdatenbank mit Piping.</span><span class="sxs-lookup"><span data-stu-id="a4016-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="a4016-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4016-114">PARAMETERS</span></span>

### <span data-ttu-id="a4016-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4016-115">-AsJob</span></span>
<span data-ttu-id="a4016-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a4016-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4016-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="a4016-117">-ColumnName</span></span>
<span data-ttu-id="a4016-118">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="a4016-118">Name of column.</span></span>

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

### <span data-ttu-id="a4016-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a4016-119">-DatabaseName</span></span>
<span data-ttu-id="a4016-120">Der Name der Azure SQL Verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="a4016-120">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="a4016-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="a4016-121">-DatabaseObject</span></span>
<span data-ttu-id="a4016-122">Das Azure SQL verwaltete Instanzdatenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="a4016-122">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="a4016-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4016-123">-DefaultProfile</span></span>
<span data-ttu-id="a4016-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4016-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4016-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4016-125">-InputObject</span></span>
<span data-ttu-id="a4016-126">Ein Objekt, das eine verwaltete SQL A0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="a4016-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="a4016-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a4016-127">-InstanceName</span></span>
<span data-ttu-id="a4016-128">Azure SQL verwalteten Instanznamen.</span><span class="sxs-lookup"><span data-stu-id="a4016-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="a4016-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4016-129">-PassThru</span></span>
<span data-ttu-id="a4016-130">Gibt an, ob das Vertraulichkeitsklassifikationsmodell am Ende der Ausführung des Cmdlets ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4016-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="a4016-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4016-131">-ResourceGroupName</span></span>
<span data-ttu-id="a4016-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a4016-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4016-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a4016-133">-SchemaName</span></span>
<span data-ttu-id="a4016-134">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="a4016-134">Name of schema.</span></span>

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

### <span data-ttu-id="a4016-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="a4016-135">-TableName</span></span>
<span data-ttu-id="a4016-136">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a4016-136">Name of table.</span></span>

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

### <span data-ttu-id="a4016-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4016-137">-Confirm</span></span>
<span data-ttu-id="a4016-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a4016-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4016-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a4016-139">-WhatIf</span></span>
<span data-ttu-id="a4016-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4016-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4016-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4016-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4016-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4016-142">CommonParameters</span></span>
<span data-ttu-id="a4016-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4016-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4016-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4016-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4016-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a4016-145">INPUTS</span></span>

### <span data-ttu-id="a4016-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="a4016-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="a4016-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a4016-147">OUTPUTS</span></span>

### <span data-ttu-id="a4016-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a4016-148">System.Boolean</span></span>

## <span data-ttu-id="a4016-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a4016-149">NOTES</span></span>

## <span data-ttu-id="a4016-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a4016-150">RELATED LINKS</span></span>

[<span data-ttu-id="a4016-151">Weitere Informationen zu Azure SQL Datenbankdatenermittlung und -klassifizierung</span><span class="sxs-lookup"><span data-stu-id="a4016-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)