---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 72118b8edd5f9816e14a5cfd19abbd5cabaca3dd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003161"
---
# <span data-ttu-id="7868c-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="7868c-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="7868c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7868c-102">SYNOPSIS</span></span>
<span data-ttu-id="7868c-103">Deaktiviert (schließt) Vertraulichkeits Empfehlungen für Spalten in der Azure SQL-Datenbank für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="7868c-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="7868c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7868c-104">SYNTAX</span></span>

### <span data-ttu-id="7868c-105">InputObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7868c-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7868c-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7868c-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7868c-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7868c-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7868c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7868c-108">DESCRIPTION</span></span>
<span data-ttu-id="7868c-109">Mit dem Disable-AzSqlInstanceDatabaseSensitivityRecommendation-Cmdlet werden Vertraulichkeits Empfehlungen für Spalten in der Datenbank Azure SQL Managed instance deaktiviert (geschlossen).</span><span class="sxs-lookup"><span data-stu-id="7868c-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="7868c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7868c-110">EXAMPLES</span></span>

### <span data-ttu-id="7868c-111">Beispiel 1: Deaktivieren Sie die Vertraulichkeits Empfehlungen für eine bestimmte Spalte in einer Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="7868c-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="7868c-112">Beispiel 2: Deaktivieren von Vertraulichkeits Empfehlungen für Spalten mit Vertraulichkeits Empfehlungen in einer Azure SQL-Datenbank mit verwalteten Instanzen mit Piping.</span><span class="sxs-lookup"><span data-stu-id="7868c-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="7868c-113">Beispiel 3: Deaktivieren Sie die Vertraulichkeits Empfehlungen für eine bestimmte Spalte in einer Azure SQL-Datenbank mit verwalteten Instanzen mit Piping.</span><span class="sxs-lookup"><span data-stu-id="7868c-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="7868c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7868c-114">PARAMETERS</span></span>

### <span data-ttu-id="7868c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7868c-115">-AsJob</span></span>
<span data-ttu-id="7868c-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7868c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7868c-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="7868c-117">-ColumnName</span></span>
<span data-ttu-id="7868c-118">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="7868c-118">Name of column.</span></span>

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

### <span data-ttu-id="7868c-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7868c-119">-DatabaseName</span></span>
<span data-ttu-id="7868c-120">Der Name der Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="7868c-120">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="7868c-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="7868c-121">-DatabaseObject</span></span>
<span data-ttu-id="7868c-122">Das Datenbankobjekt der Azure SQL-Instanz</span><span class="sxs-lookup"><span data-stu-id="7868c-122">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="7868c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7868c-123">-DefaultProfile</span></span>
<span data-ttu-id="7868c-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7868c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7868c-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7868c-125">-InputObject</span></span>
<span data-ttu-id="7868c-126">Ein Objekt, das eine Datenbank-Vertraulichkeits Klassifikation für SQL-verwaltete Instanzen darstellt.</span><span class="sxs-lookup"><span data-stu-id="7868c-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="7868c-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7868c-127">-InstanceName</span></span>
<span data-ttu-id="7868c-128">Name der verwalteten Azure SQL-Instanz.</span><span class="sxs-lookup"><span data-stu-id="7868c-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="7868c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7868c-129">-PassThru</span></span>
<span data-ttu-id="7868c-130">Gibt an, ob das Sensitivitäts Klassifikationsmodell am Ende der Cmdlet-Ausführung ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="7868c-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="7868c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7868c-131">-ResourceGroupName</span></span>
<span data-ttu-id="7868c-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7868c-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="7868c-133">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="7868c-133">-SchemaName</span></span>
<span data-ttu-id="7868c-134">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="7868c-134">Name of schema.</span></span>

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

### <span data-ttu-id="7868c-135">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="7868c-135">-TableName</span></span>
<span data-ttu-id="7868c-136">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7868c-136">Name of table.</span></span>

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

### <span data-ttu-id="7868c-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7868c-137">-Confirm</span></span>
<span data-ttu-id="7868c-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7868c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7868c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7868c-139">-WhatIf</span></span>
<span data-ttu-id="7868c-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7868c-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7868c-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7868c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7868c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7868c-142">CommonParameters</span></span>
<span data-ttu-id="7868c-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7868c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7868c-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7868c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7868c-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7868c-145">INPUTS</span></span>

### <span data-ttu-id="7868c-146">Microsoft. Azure. Commands. SQL. dataclassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="7868c-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="7868c-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7868c-147">OUTPUTS</span></span>

### <span data-ttu-id="7868c-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7868c-148">System.Boolean</span></span>

## <span data-ttu-id="7868c-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="7868c-149">NOTES</span></span>

## <span data-ttu-id="7868c-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7868c-150">RELATED LINKS</span></span>

[<span data-ttu-id="7868c-151">Weitere Informationen zur Azure SQL-Datenbankdaten Ermittlung und-Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="7868c-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)