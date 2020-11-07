---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: d5923be20fd893aefee4e9a5789c2f6f57f20fbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826108"
---
# <span data-ttu-id="7abf2-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="7abf2-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="7abf2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7abf2-102">SYNOPSIS</span></span>
<span data-ttu-id="7abf2-103">Ruft die empfohlenen Informationstypen und Vertraulichkeits Bezeichnungen von Spalten in der Azure SQL-Datenbank für verwaltete Instanzen ab.</span><span class="sxs-lookup"><span data-stu-id="7abf2-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="7abf2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7abf2-104">SYNTAX</span></span>

### <span data-ttu-id="7abf2-105">DatabaseObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7abf2-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7abf2-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="7abf2-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7abf2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7abf2-107">DESCRIPTION</span></span>
<span data-ttu-id="7abf2-108">Das Get-AzSqlInstanceDatabaseSensitivityRecommendation-Cmdlet gibt die empfohlenen Informationstypen und Vertraulichkeits Bezeichnungen von Spalten in der Datenbank Azure SQL Managed instance zurück.</span><span class="sxs-lookup"><span data-stu-id="7abf2-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="7abf2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7abf2-109">EXAMPLES</span></span>

### <span data-ttu-id="7abf2-110">Beispiel 1: Abrufen empfohlener Informationstypen und Vertraulichkeits Beschriftungen einer Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="7abf2-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="7abf2-111">Beispiel 2: Abrufen empfohlener Informationstypen und Vertraulichkeits Beschriftungen einer Azure SQL-Datenbank mit verwalteten Instanzen mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="7abf2-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

## <span data-ttu-id="7abf2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7abf2-112">PARAMETERS</span></span>

### <span data-ttu-id="7abf2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7abf2-113">-AsJob</span></span>
<span data-ttu-id="7abf2-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7abf2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7abf2-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7abf2-115">-DatabaseName</span></span>
<span data-ttu-id="7abf2-116">Der Name der Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="7abf2-116">The name of the Azure SQL managed instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7abf2-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="7abf2-117">-DatabaseObject</span></span>
<span data-ttu-id="7abf2-118">Das Datenbankobjekt der Azure SQL-Instanz</span><span class="sxs-lookup"><span data-stu-id="7abf2-118">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7abf2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7abf2-119">-DefaultProfile</span></span>
<span data-ttu-id="7abf2-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7abf2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7abf2-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7abf2-121">-InstanceName</span></span>
<span data-ttu-id="7abf2-122">Name der verwalteten Azure SQL-Instanz.</span><span class="sxs-lookup"><span data-stu-id="7abf2-122">Azure SQL managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7abf2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7abf2-123">-ResourceGroupName</span></span>
<span data-ttu-id="7abf2-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7abf2-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7abf2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7abf2-125">CommonParameters</span></span>
<span data-ttu-id="7abf2-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7abf2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7abf2-127">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7abf2-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7abf2-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7abf2-128">INPUTS</span></span>

### <span data-ttu-id="7abf2-129">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7abf2-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="7abf2-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7abf2-130">OUTPUTS</span></span>

### <span data-ttu-id="7abf2-131">Microsoft. Azure. Commands. SQL. dataclassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="7abf2-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="7abf2-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="7abf2-132">NOTES</span></span>

## <span data-ttu-id="7abf2-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7abf2-133">RELATED LINKS</span></span>

[<span data-ttu-id="7abf2-134">Weitere Informationen zur Azure SQL-Datenbankdaten Ermittlung und-Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="7abf2-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
