---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 0942373dc3ad741f10d5a87d7b4713413f9db4f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947683"
---
# <span data-ttu-id="d3469-101">Get-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="d3469-101">Get-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="d3469-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3469-102">SYNOPSIS</span></span>
<span data-ttu-id="d3469-103">Ruft die aktuellen Informationstypen und Vertraulichkeitsbeschriftungen von Spalten im SQL ab.</span><span class="sxs-lookup"><span data-stu-id="d3469-103">Gets the current information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="d3469-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3469-104">SYNTAX</span></span>

### <span data-ttu-id="d3469-105">SqlPoolObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d3469-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3469-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3469-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3469-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3469-107">ColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3469-108">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3469-108">SqlPoolObjectColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3469-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3469-109">DESCRIPTION</span></span>
<span data-ttu-id="d3469-110">Das Get-AzSynapseSqlPoolSensitivityClassification-Cmdlet gibt die aktuellen Informationstypen und Vertraulichkeitsbeschriftungen von Spalten im Azure Synapse-SQL zurück.</span><span class="sxs-lookup"><span data-stu-id="d3469-110">The Get-AzSynapseSqlPoolSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure Synapse SQL pool.</span></span>

## <span data-ttu-id="d3469-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d3469-111">EXAMPLES</span></span>

### <span data-ttu-id="d3469-112">Beispiel 1: Aktuelle Informationstypen und Vertraulichkeitsbeschriftungen eines Azure Synapse-SQL erhalten.</span><span class="sxs-lookup"><span data-stu-id="d3469-112">Example 1: Get current information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="d3469-113">Beispiel 2: Aktuelle Informationstypen und Vertraulichkeitsbeschriftungen eines Azure Synapse SQL mit Piping.</span><span class="sxs-lookup"><span data-stu-id="d3469-113">Example 2: Get current information types and sensitivity labels of an Azure Synapse SQL pool with Piping.</span></span>
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

### <span data-ttu-id="d3469-114">Beispiel 3: Aktuelle Informationstyp- und Vertraulichkeitsbeschriftung einer bestimmten Spalte eines Azure Synapse-SQL erhalten.</span><span class="sxs-lookup"><span data-stu-id="d3469-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="d3469-115">Beispiel 4: Aktuelle Informationstyp- und Vertraulichkeitsbeschriftung einer bestimmten Spalte eines Azure Synapse-SQL mit Piping.</span><span class="sxs-lookup"><span data-stu-id="d3469-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool using Piping.</span></span>
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

## <span data-ttu-id="d3469-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d3469-116">PARAMETERS</span></span>

### <span data-ttu-id="d3469-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3469-117">-AsJob</span></span>
<span data-ttu-id="d3469-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d3469-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3469-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="d3469-119">-ColumnName</span></span>
<span data-ttu-id="d3469-120">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="d3469-120">Name of column.</span></span>

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

### <span data-ttu-id="d3469-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3469-121">-DefaultProfile</span></span>
<span data-ttu-id="d3469-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3469-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3469-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3469-123">-ResourceGroupName</span></span>
<span data-ttu-id="d3469-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d3469-124">Resource group name.</span></span>

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

### <span data-ttu-id="d3469-125">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="d3469-125">-SchemaName</span></span>
<span data-ttu-id="d3469-126">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="d3469-126">Name of schema.</span></span>

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

### <span data-ttu-id="d3469-127">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="d3469-127">-SqlPoolName</span></span>
<span data-ttu-id="d3469-128">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="d3469-128">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="d3469-129">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="d3469-129">-SqlPoolObject</span></span>
<span data-ttu-id="d3469-130">SQL -Pooleingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d3469-130">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d3469-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="d3469-131">-TableName</span></span>
<span data-ttu-id="d3469-132">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d3469-132">Name of table.</span></span>

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

### <span data-ttu-id="d3469-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d3469-133">-WorkspaceName</span></span>
<span data-ttu-id="d3469-134">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="d3469-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d3469-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3469-135">CommonParameters</span></span>
<span data-ttu-id="d3469-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3469-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3469-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3469-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3469-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d3469-138">INPUTS</span></span>

### <span data-ttu-id="d3469-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d3469-139">System.String</span></span>

### <span data-ttu-id="d3469-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d3469-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d3469-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d3469-141">OUTPUTS</span></span>

### <span data-ttu-id="d3469-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="d3469-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="d3469-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d3469-143">NOTES</span></span>

## <span data-ttu-id="d3469-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d3469-144">RELATED LINKS</span></span>
