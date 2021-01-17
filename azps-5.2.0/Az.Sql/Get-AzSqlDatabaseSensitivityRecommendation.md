---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f002dca1c91ada808acc81108d3f06e9376a8b3f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372012"
---
# <span data-ttu-id="63a19-101">Get-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="63a19-101">Get-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="63a19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63a19-102">SYNOPSIS</span></span>
<span data-ttu-id="63a19-103">Ruft die empfohlenen Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="63a19-103">Gets the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="63a19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63a19-104">SYNTAX</span></span>

### <span data-ttu-id="63a19-105">DatabaseObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="63a19-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63a19-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="63a19-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63a19-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63a19-107">DESCRIPTION</span></span>
<span data-ttu-id="63a19-108">Das Get-AzSqlDatabaseSensitivityRecommendation cmdlet gibt die empfohlenen Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="63a19-108">The Get-AzSqlDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="63a19-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="63a19-109">EXAMPLES</span></span>

### <span data-ttu-id="63a19-110">Beispiel 1: Erhalten empfohlener Informationstypen und Vertraulichkeitsbeschriftungen einer Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="63a19-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="63a19-111">Beispiel 2: Erhalten empfohlener Informationstypen und Vertraulichkeitsbeschriftungen einer Azure SQL mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="63a19-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="63a19-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63a19-112">PARAMETERS</span></span>

### <span data-ttu-id="63a19-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63a19-113">-AsJob</span></span>
<span data-ttu-id="63a19-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="63a19-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63a19-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="63a19-115">-DatabaseName</span></span>
<span data-ttu-id="63a19-116">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="63a19-116">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="63a19-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="63a19-117">-DatabaseObject</span></span>
<span data-ttu-id="63a19-118">Das SQL Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="63a19-118">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63a19-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63a19-119">-DefaultProfile</span></span>
<span data-ttu-id="63a19-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63a19-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63a19-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63a19-121">-ResourceGroupName</span></span>
<span data-ttu-id="63a19-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="63a19-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="63a19-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="63a19-123">-ServerName</span></span>
<span data-ttu-id="63a19-124">SQL Servername.</span><span class="sxs-lookup"><span data-stu-id="63a19-124">SQL server name.</span></span>

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

### <span data-ttu-id="63a19-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63a19-125">CommonParameters</span></span>
<span data-ttu-id="63a19-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63a19-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63a19-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63a19-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63a19-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="63a19-128">INPUTS</span></span>

### <span data-ttu-id="63a19-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="63a19-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="63a19-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="63a19-130">OUTPUTS</span></span>

### <span data-ttu-id="63a19-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="63a19-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="63a19-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="63a19-132">NOTES</span></span>

## <span data-ttu-id="63a19-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="63a19-133">RELATED LINKS</span></span>

[<span data-ttu-id="63a19-134">Weitere Informationen zu Azure SQL Datenbankdatenermittlung und -klassifizierung</span><span class="sxs-lookup"><span data-stu-id="63a19-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
