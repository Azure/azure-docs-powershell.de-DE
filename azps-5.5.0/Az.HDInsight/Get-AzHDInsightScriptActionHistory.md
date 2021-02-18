---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
ms.openlocfilehash: 0424578473aedb60071e3389e7aaff2b84848f8c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173260"
---
# <span data-ttu-id="655ea-101">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="655ea-101">Get-AzHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="655ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="655ea-102">SYNOPSIS</span></span>
<span data-ttu-id="655ea-103">Ruft den Skriptaktionsverlauf für einen Cluster ab und listet ihn in umgekehrter chronologischer Reihenfolge auf, oder ruft Details einer zuvor ausgeführten Skriptaktion ab.</span><span class="sxs-lookup"><span data-stu-id="655ea-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="655ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="655ea-104">SYNTAX</span></span>

```
Get-AzHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="655ea-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="655ea-105">DESCRIPTION</span></span>
<span data-ttu-id="655ea-106">Das **Cmdlet "Get-AzHDInsightScriptActionHistory"** ruft den Skriptaktionsverlauf für einen Azure -HDInsight-Cluster ab und listet ihn in umgekehrter chronologischer Reihenfolge auf, oder ruft Details einer zuvor ausgeführten Skriptaktion ab.</span><span class="sxs-lookup"><span data-stu-id="655ea-106">The **Get-AzHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="655ea-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="655ea-107">EXAMPLES</span></span>

### <span data-ttu-id="655ea-108">Beispiel 1: Den Verlauf der Ausführung von Skriptaktionen für einen Cluster erhalten</span><span class="sxs-lookup"><span data-stu-id="655ea-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="655ea-109">Dieser Befehl ruft den Verlauf der Skriptaktionen für den Cluster "your-hadoop-001" ab.</span><span class="sxs-lookup"><span data-stu-id="655ea-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="655ea-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="655ea-110">PARAMETERS</span></span>

### <span data-ttu-id="655ea-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="655ea-111">-ClusterName</span></span>
<span data-ttu-id="655ea-112">Gibt den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="655ea-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="655ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="655ea-113">-DefaultProfile</span></span>
<span data-ttu-id="655ea-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="655ea-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="655ea-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="655ea-115">-ResourceGroupName</span></span>
<span data-ttu-id="655ea-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="655ea-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="655ea-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="655ea-117">-ScriptExecutionId</span></span>
<span data-ttu-id="655ea-118">Gibt die Ausführungs-ID der ausgeführten Skriptaktion an.</span><span class="sxs-lookup"><span data-stu-id="655ea-118">Specifies the execution ID of the executed script action.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="655ea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="655ea-119">CommonParameters</span></span>
<span data-ttu-id="655ea-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="655ea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="655ea-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="655ea-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="655ea-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="655ea-122">INPUTS</span></span>

### <span data-ttu-id="655ea-123">Keine</span><span class="sxs-lookup"><span data-stu-id="655ea-123">None</span></span>

## <span data-ttu-id="655ea-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="655ea-124">OUTPUTS</span></span>

### <span data-ttu-id="655ea-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span><span class="sxs-lookup"><span data-stu-id="655ea-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="655ea-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="655ea-126">NOTES</span></span>

## <span data-ttu-id="655ea-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="655ea-127">RELATED LINKS</span></span>
