---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: e21bf168093d2589321d6952ca45af7e9f8c0cbe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846771"
---
# <span data-ttu-id="5c5de-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="5c5de-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="5c5de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5c5de-102">SYNOPSIS</span></span>
<span data-ttu-id="5c5de-103">Aktiviert Vertraulichkeits Empfehlungen für Spalten (Empfehlungen sind standardmäßig für alle Spalten aktiviert) in der Azure SQL-Instanzdatenbank für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="5c5de-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="5c5de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c5de-104">SYNTAX</span></span>

### <span data-ttu-id="5c5de-105">InputObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5c5de-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c5de-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c5de-106">ColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c5de-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c5de-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c5de-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c5de-108">DESCRIPTION</span></span>
<span data-ttu-id="5c5de-109">Das Enable-AzSqlInstanceDatabaseSensitivityRecommendation-Cmdlet ermöglicht Vertraulichkeits Empfehlungen für Spalten in der Azure SQL-Datenbank für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="5c5de-109">The Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="5c5de-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c5de-110">EXAMPLES</span></span>

### <span data-ttu-id="5c5de-111">Beispiel 1: Aktivieren von Vertraulichkeits Empfehlungen für eine bestimmte Spalte in einer Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="5c5de-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Enable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="5c5de-112">Beispiel 2: Aktivieren von Vertraulichkeits Empfehlungen für eine bestimmte Spalte in einer Azure SQL-Datenbank mit verwalteten Instanzen mit Piping.</span><span class="sxs-lookup"><span data-stu-id="5c5de-112">Example 2: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="5c5de-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c5de-113">PARAMETERS</span></span>

### <span data-ttu-id="5c5de-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c5de-114">-AsJob</span></span>
<span data-ttu-id="5c5de-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5c5de-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c5de-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="5c5de-116">-ColumnName</span></span>
<span data-ttu-id="5c5de-117">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="5c5de-117">Name of column.</span></span>

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

### <span data-ttu-id="5c5de-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c5de-118">-DatabaseName</span></span>
<span data-ttu-id="5c5de-119">Der Name der Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="5c5de-119">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="5c5de-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="5c5de-120">-DatabaseObject</span></span>
<span data-ttu-id="5c5de-121">Das Datenbankobjekt der Azure SQL-Instanz</span><span class="sxs-lookup"><span data-stu-id="5c5de-121">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="5c5de-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c5de-122">-DefaultProfile</span></span>
<span data-ttu-id="5c5de-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5c5de-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c5de-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5c5de-124">-InputObject</span></span>
<span data-ttu-id="5c5de-125">Ein Objekt, das eine Datenbank-Vertraulichkeits Klassifikation für SQL-verwaltete Instanzen darstellt.</span><span class="sxs-lookup"><span data-stu-id="5c5de-125">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="5c5de-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="5c5de-126">-InstanceName</span></span>
<span data-ttu-id="5c5de-127">Name der verwalteten Azure SQL-Instanz.</span><span class="sxs-lookup"><span data-stu-id="5c5de-127">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="5c5de-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c5de-128">-PassThru</span></span>
<span data-ttu-id="5c5de-129">Gibt an, ob das Sensitivitäts Klassifikationsmodell am Ende der Cmdlet-Ausführung ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c5de-129">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="5c5de-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c5de-130">-ResourceGroupName</span></span>
<span data-ttu-id="5c5de-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5c5de-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="5c5de-132">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="5c5de-132">-SchemaName</span></span>
<span data-ttu-id="5c5de-133">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="5c5de-133">Name of schema.</span></span>

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

### <span data-ttu-id="5c5de-134">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="5c5de-134">-TableName</span></span>
<span data-ttu-id="5c5de-135">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5c5de-135">Name of table.</span></span>

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

### <span data-ttu-id="5c5de-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5c5de-136">-Confirm</span></span>
<span data-ttu-id="5c5de-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5c5de-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c5de-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c5de-138">-WhatIf</span></span>
<span data-ttu-id="5c5de-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c5de-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c5de-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c5de-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c5de-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c5de-141">CommonParameters</span></span>
<span data-ttu-id="5c5de-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c5de-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c5de-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c5de-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c5de-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5c5de-144">INPUTS</span></span>

### <span data-ttu-id="5c5de-145">Microsoft. Azure. Commands. SQL. dataclassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="5c5de-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="5c5de-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5c5de-146">OUTPUTS</span></span>

### <span data-ttu-id="5c5de-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c5de-147">System.Boolean</span></span>

## <span data-ttu-id="5c5de-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="5c5de-148">NOTES</span></span>

## <span data-ttu-id="5c5de-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5c5de-149">RELATED LINKS</span></span>

[<span data-ttu-id="5c5de-150">Weitere Informationen zur Azure SQL-Datenbankdaten Ermittlung und-Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="5c5de-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)