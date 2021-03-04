---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: a7c5c9c2008839d4e90dd5f393fbe4acea0f78a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925560"
---
# <span data-ttu-id="f17df-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="f17df-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="f17df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f17df-102">SYNOPSIS</span></span>
<span data-ttu-id="f17df-103">Entfernt eine persistierte Skriptaktion aus einem HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f17df-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="f17df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f17df-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f17df-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f17df-105">DESCRIPTION</span></span>
<span data-ttu-id="f17df-106">Das **Cmdlet Remove-AzHDInsightPersistedScriptAction** entfernt eine persistierte Skriptaktion aus der Liste der beibehaltenen Skriptaktionen des angegebenen Azure HDInsight-Clusters.</span><span class="sxs-lookup"><span data-stu-id="f17df-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="f17df-107">Das entfernte Skript wird nicht mehr ausgeführt, wenn der Cluster skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="f17df-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="f17df-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f17df-108">EXAMPLES</span></span>

### <span data-ttu-id="f17df-109">Beispiel 1: Entfernen einer Skriptaktion aus der Liste der beibehaltenen Skriptaktionen in einem Cluster</span><span class="sxs-lookup"><span data-stu-id="f17df-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="f17df-110">Mit diesem Befehl wird die Skriptaktion "Scriptaction" aus der Liste der beibehaltenen Skriptaktionen im angegebenen Cluster entfernt.</span><span class="sxs-lookup"><span data-stu-id="f17df-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="f17df-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f17df-111">PARAMETERS</span></span>

### <span data-ttu-id="f17df-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f17df-112">-ClusterName</span></span>
<span data-ttu-id="f17df-113">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="f17df-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f17df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f17df-114">-DefaultProfile</span></span>
<span data-ttu-id="f17df-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f17df-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f17df-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f17df-116">-Name</span></span>
<span data-ttu-id="f17df-117">Gibt den Namen der aktion für das beibehaltene Skript an, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f17df-117">Specifies the name of the persisted script action to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f17df-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f17df-118">-ResourceGroupName</span></span>
<span data-ttu-id="f17df-119">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f17df-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f17df-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f17df-120">CommonParameters</span></span>
<span data-ttu-id="f17df-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f17df-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f17df-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f17df-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f17df-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f17df-123">INPUTS</span></span>

### <span data-ttu-id="f17df-124">Keine</span><span class="sxs-lookup"><span data-stu-id="f17df-124">None</span></span>

## <span data-ttu-id="f17df-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f17df-125">OUTPUTS</span></span>

### <span data-ttu-id="f17df-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="f17df-126">System.Void</span></span>

## <span data-ttu-id="f17df-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f17df-127">NOTES</span></span>

## <span data-ttu-id="f17df-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f17df-128">RELATED LINKS</span></span>

[<span data-ttu-id="f17df-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="f17df-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="f17df-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="f17df-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


