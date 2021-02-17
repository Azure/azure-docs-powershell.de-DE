---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 6affe94fdbfa7a698ad7d666d1847365fc8e25ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164596"
---
# <span data-ttu-id="7e5b1-101">Get-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="7e5b1-101">Get-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="7e5b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e5b1-102">SYNOPSIS</span></span>
<span data-ttu-id="7e5b1-103">Ruft die aktuellen Informationstypen und Vertraulichkeitsbeschriftungen von Spalten im SQL ab.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-103">Gets the current information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="7e5b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e5b1-104">SYNTAX</span></span>

### <span data-ttu-id="7e5b1-105">SqlPoolObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e5b1-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e5b1-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e5b1-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e5b1-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e5b1-107">ColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e5b1-108">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e5b1-108">SqlPoolObjectColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e5b1-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e5b1-109">DESCRIPTION</span></span>
<span data-ttu-id="7e5b1-110">Das Get-AzSynapseSqlPoolSensitivityClassification-Cmdlet gibt die aktuellen Informationstypen und Vertraulichkeitsbeschriftungen von Spalten im Azure Synapse SQL zurück.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-110">The Get-AzSynapseSqlPoolSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure Synapse SQL pool.</span></span>

## <span data-ttu-id="7e5b1-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7e5b1-111">EXAMPLES</span></span>

### <span data-ttu-id="7e5b1-112">Beispiel 1: Aktuelle Informationstypen und Vertraulichkeitsbezeichnungen eines Azure Synapse SQL erhalten.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-112">Example 1: Get current information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
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

### <span data-ttu-id="7e5b1-113">Beispiel 2: Erhalten aktueller Informationstypen und Vertraulichkeitsbeschriftungen eines Azure Synapse SQL pools mit Piping.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-113">Example 2: Get current information types and sensitivity labels of an Azure Synapse SQL pool with Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
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

### <span data-ttu-id="7e5b1-114">Beispiel 3: Erhalten des aktuellen Informationstyps und der Vertraulichkeitsbezeichnung einer bestimmten Spalte eines Azure Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="7e5b1-115">Beispiel 4: Erhalten des aktuellen Informationstyps und der Vertraulichkeitsbezeichnung einer bestimmten Spalte eines Azure Synapse SQL mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="7e5b1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e5b1-116">PARAMETERS</span></span>

### <span data-ttu-id="7e5b1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e5b1-117">-AsJob</span></span>
<span data-ttu-id="7e5b1-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7e5b1-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e5b1-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="7e5b1-119">-ColumnName</span></span>
<span data-ttu-id="7e5b1-120">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e5b1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e5b1-121">-DefaultProfile</span></span>
<span data-ttu-id="7e5b1-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e5b1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e5b1-123">-ResourceGroupName</span></span>
<span data-ttu-id="7e5b1-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e5b1-125">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="7e5b1-125">-SchemaName</span></span>
<span data-ttu-id="7e5b1-126">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-126">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e5b1-127">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="7e5b1-127">-SqlPoolName</span></span>
<span data-ttu-id="7e5b1-128">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e5b1-129">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="7e5b1-129">-SqlPoolObject</span></span>
<span data-ttu-id="7e5b1-130">SQL pool-Eingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-130">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e5b1-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="7e5b1-131">-TableName</span></span>
<span data-ttu-id="7e5b1-132">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-132">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e5b1-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7e5b1-133">-WorkspaceName</span></span>
<span data-ttu-id="7e5b1-134">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e5b1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e5b1-135">CommonParameters</span></span>
<span data-ttu-id="7e5b1-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e5b1-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e5b1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e5b1-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7e5b1-138">INPUTS</span></span>

### <span data-ttu-id="7e5b1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7e5b1-139">System.String</span></span>

### <span data-ttu-id="7e5b1-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7e5b1-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="7e5b1-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7e5b1-141">OUTPUTS</span></span>

### <span data-ttu-id="7e5b1-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="7e5b1-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="7e5b1-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7e5b1-143">NOTES</span></span>

## <span data-ttu-id="7e5b1-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7e5b1-144">RELATED LINKS</span></span>
