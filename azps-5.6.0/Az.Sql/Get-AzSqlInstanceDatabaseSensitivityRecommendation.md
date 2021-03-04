---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 0d40e03b26481b5e974b294533566549646ba628
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943361"
---
# <span data-ttu-id="23d0d-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="23d0d-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="23d0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23d0d-102">SYNOPSIS</span></span>
<span data-ttu-id="23d0d-103">Ruft die empfohlenen Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Azure SQL verwalteten Instanzdatenbank ab.</span><span class="sxs-lookup"><span data-stu-id="23d0d-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="23d0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23d0d-104">SYNTAX</span></span>

### <span data-ttu-id="23d0d-105">DatabaseObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="23d0d-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23d0d-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="23d0d-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23d0d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23d0d-107">DESCRIPTION</span></span>
<span data-ttu-id="23d0d-108">Das Get-AzSqlInstanceDatabaseSensitivityRecommendation-Cmdlet gibt die empfohlenen Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in der Azure SQL verwaltete Instanzdatenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="23d0d-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="23d0d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="23d0d-109">EXAMPLES</span></span>

### <span data-ttu-id="23d0d-110">Beispiel 1: Holen Sie sich empfohlene Informationstypen und Vertraulichkeitsbeschriftungen einer Azure SQL verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="23d0d-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="23d0d-111">Beispiel 2: Erhalten Sie empfohlene Informationstypen und Vertraulichkeitsbeschriftungen einer Azure SQL verwaltete Instanzdatenbank mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="23d0d-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

## <span data-ttu-id="23d0d-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="23d0d-112">PARAMETERS</span></span>

### <span data-ttu-id="23d0d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23d0d-113">-AsJob</span></span>
<span data-ttu-id="23d0d-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="23d0d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23d0d-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="23d0d-115">-DatabaseName</span></span>
<span data-ttu-id="23d0d-116">Der Name der Azure SQL verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="23d0d-116">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="23d0d-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="23d0d-117">-DatabaseObject</span></span>
<span data-ttu-id="23d0d-118">Das Azure SQL verwaltete Instanzdatenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="23d0d-118">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="23d0d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d0d-119">-DefaultProfile</span></span>
<span data-ttu-id="23d0d-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23d0d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23d0d-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="23d0d-121">-InstanceName</span></span>
<span data-ttu-id="23d0d-122">Azure SQL verwalteten Instanznamen.</span><span class="sxs-lookup"><span data-stu-id="23d0d-122">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="23d0d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23d0d-123">-ResourceGroupName</span></span>
<span data-ttu-id="23d0d-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="23d0d-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="23d0d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d0d-125">CommonParameters</span></span>
<span data-ttu-id="23d0d-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23d0d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d0d-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23d0d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d0d-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="23d0d-128">INPUTS</span></span>

### <span data-ttu-id="23d0d-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="23d0d-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="23d0d-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="23d0d-130">OUTPUTS</span></span>

### <span data-ttu-id="23d0d-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="23d0d-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="23d0d-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="23d0d-132">NOTES</span></span>

## <span data-ttu-id="23d0d-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="23d0d-133">RELATED LINKS</span></span>

[<span data-ttu-id="23d0d-134">Weitere Informationen zu Azure SQL Datenbankdatenermittlung und -klassifizierung</span><span class="sxs-lookup"><span data-stu-id="23d0d-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
