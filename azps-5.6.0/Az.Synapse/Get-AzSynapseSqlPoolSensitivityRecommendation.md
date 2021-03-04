---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: d2949bf2d366dc64b0e55b82d0c90979042ea294
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935448"
---
# <span data-ttu-id="7ed77-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="7ed77-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="7ed77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ed77-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed77-103">Ruft die empfohlenen Informationstypen und Vertraulichkeitsbeschriftungen von Spalten im SQL ab.</span><span class="sxs-lookup"><span data-stu-id="7ed77-103">Gets the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="7ed77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ed77-104">SYNTAX</span></span>

### <span data-ttu-id="7ed77-105">SqlPoolObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ed77-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ed77-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ed77-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ed77-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ed77-107">DESCRIPTION</span></span>
<span data-ttu-id="7ed77-108">Das Get-AzSynapseSqlPoolSensitivityRecommendation-Cmdlet gibt die empfohlenen Informationstypen und Vertraulichkeitsbeschriftungen von Spalten im SQL zurück.</span><span class="sxs-lookup"><span data-stu-id="7ed77-108">The Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="7ed77-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7ed77-109">EXAMPLES</span></span>

### <span data-ttu-id="7ed77-110">Beispiel 1: Erhalten Sie empfohlene Informationstypen und Vertraulichkeitsbeschriftungen eines Azure Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="7ed77-110">Example 1: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

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

### <span data-ttu-id="7ed77-111">Beispiel 2: Erhalten Sie empfohlene Informationstypen und Vertraulichkeitsbeschriftungen eines Azure Synapse SQL mit Piping.</span><span class="sxs-lookup"><span data-stu-id="7ed77-111">Example 2: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityRecommendation

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

## <span data-ttu-id="7ed77-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7ed77-112">PARAMETERS</span></span>

### <span data-ttu-id="7ed77-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ed77-113">-AsJob</span></span>
<span data-ttu-id="7ed77-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7ed77-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ed77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed77-115">-DefaultProfile</span></span>
<span data-ttu-id="7ed77-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ed77-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ed77-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ed77-117">-ResourceGroupName</span></span>
<span data-ttu-id="7ed77-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7ed77-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed77-119">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="7ed77-119">-SqlPoolName</span></span>
<span data-ttu-id="7ed77-120">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="7ed77-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed77-121">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="7ed77-121">-SqlPoolObject</span></span>
<span data-ttu-id="7ed77-122">SQL -Pooleingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="7ed77-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed77-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7ed77-123">-WorkspaceName</span></span>
<span data-ttu-id="7ed77-124">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="7ed77-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed77-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed77-125">CommonParameters</span></span>
<span data-ttu-id="7ed77-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ed77-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed77-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ed77-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed77-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7ed77-128">INPUTS</span></span>

### <span data-ttu-id="7ed77-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7ed77-129">System.String</span></span>

### <span data-ttu-id="7ed77-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7ed77-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="7ed77-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7ed77-131">OUTPUTS</span></span>

### <span data-ttu-id="7ed77-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="7ed77-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="7ed77-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7ed77-133">NOTES</span></span>

## <span data-ttu-id="7ed77-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7ed77-134">RELATED LINKS</span></span>
