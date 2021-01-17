---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: b5d62e963bdd2f30ab0c5b821854ee46b391376b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458524"
---
# <span data-ttu-id="6f366-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="6f366-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="6f366-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f366-102">SYNOPSIS</span></span>
<span data-ttu-id="6f366-103">Ruft die Aktionen für beibehaltene Skripts für einen Cluster ab und listet sie in chronologischer Reihenfolge auf, oder ruft Details zu einer angegebenen Aktion für beibehaltene Skripts ab.</span><span class="sxs-lookup"><span data-stu-id="6f366-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="6f366-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f366-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f366-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f366-105">DESCRIPTION</span></span>
<span data-ttu-id="6f366-106">Das **Cmdlet "Get-AzHDInsightPersistedScriptAction"** ruft die Aktionen für beibehaltene Skripts für einen Azure -HDInsight-Cluster ab und listet sie in chronologischer Reihenfolge auf oder ruft Details zu einer angegebenen Aktion für beibehaltene Skripts ab.</span><span class="sxs-lookup"><span data-stu-id="6f366-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="6f366-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6f366-107">EXAMPLES</span></span>

### <span data-ttu-id="6f366-108">Beispiel 1: Erhalten der Aktionen für beibehaltene Skripts in einem Cluster</span><span class="sxs-lookup"><span data-stu-id="6f366-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="6f366-109">Dieser Befehl ruft beibehaltene Skriptaktionen für den Cluster namens "Ihr-Hadoop-001" ab.</span><span class="sxs-lookup"><span data-stu-id="6f366-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="6f366-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f366-110">PARAMETERS</span></span>

### <span data-ttu-id="6f366-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6f366-111">-ClusterName</span></span>
<span data-ttu-id="6f366-112">Gibt den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="6f366-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="6f366-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f366-113">-DefaultProfile</span></span>
<span data-ttu-id="6f366-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6f366-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f366-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6f366-115">-Name</span></span>
<span data-ttu-id="6f366-116">Gibt den Namen der Aktion für das beibehaltene Skript an.</span><span class="sxs-lookup"><span data-stu-id="6f366-116">Specifies the name of the persisted script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f366-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f366-117">-ResourceGroupName</span></span>
<span data-ttu-id="6f366-118">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6f366-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6f366-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f366-119">CommonParameters</span></span>
<span data-ttu-id="6f366-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f366-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f366-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f366-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f366-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6f366-122">INPUTS</span></span>

### <span data-ttu-id="6f366-123">Keine</span><span class="sxs-lookup"><span data-stu-id="6f366-123">None</span></span>

## <span data-ttu-id="6f366-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6f366-124">OUTPUTS</span></span>

### <span data-ttu-id="6f366-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="6f366-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="6f366-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6f366-126">NOTES</span></span>

## <span data-ttu-id="6f366-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6f366-127">RELATED LINKS</span></span>

[<span data-ttu-id="6f366-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="6f366-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="6f366-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="6f366-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


