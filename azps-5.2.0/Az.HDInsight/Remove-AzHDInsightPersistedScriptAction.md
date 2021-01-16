---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 4d3d88fb5a8cca2343403870233e89b0f2073e8e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292018"
---
# <span data-ttu-id="91308-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="91308-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="91308-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91308-102">SYNOPSIS</span></span>
<span data-ttu-id="91308-103">Entfernt eine Aktion für beibehaltenes Skript aus einem HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="91308-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="91308-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91308-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91308-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91308-105">DESCRIPTION</span></span>
<span data-ttu-id="91308-106">Das **Cmdlet "Remove-AzHDInsightPersistedScriptAction"** entfernt eine Aktion für beibehaltenes Skript aus der Liste der beibehaltenen Skriptaktionen des angegebenen Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="91308-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="91308-107">Das entfernte Skript wird nicht mehr ausgeführt, wenn der Cluster skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="91308-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="91308-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="91308-108">EXAMPLES</span></span>

### <span data-ttu-id="91308-109">Beispiel 1: Entfernen einer Skriptaktion aus der Liste der beibehaltenen Skriptaktionen in einem Cluster</span><span class="sxs-lookup"><span data-stu-id="91308-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="91308-110">Mit diesem Befehl wird die Skriptaktion "Scriptaction" aus der Liste der beibehaltenen Skriptaktionen für den angegebenen Cluster entfernt.</span><span class="sxs-lookup"><span data-stu-id="91308-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="91308-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91308-111">PARAMETERS</span></span>

### <span data-ttu-id="91308-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="91308-112">-ClusterName</span></span>
<span data-ttu-id="91308-113">Gibt den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="91308-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="91308-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91308-114">-DefaultProfile</span></span>
<span data-ttu-id="91308-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="91308-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91308-116">-Name</span><span class="sxs-lookup"><span data-stu-id="91308-116">-Name</span></span>
<span data-ttu-id="91308-117">Gibt den Namen der Aktion für das beibehaltene Skript an, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="91308-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="91308-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91308-118">-ResourceGroupName</span></span>
<span data-ttu-id="91308-119">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="91308-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="91308-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91308-120">CommonParameters</span></span>
<span data-ttu-id="91308-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91308-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91308-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91308-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91308-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="91308-123">INPUTS</span></span>

### <span data-ttu-id="91308-124">Keine</span><span class="sxs-lookup"><span data-stu-id="91308-124">None</span></span>

## <span data-ttu-id="91308-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="91308-125">OUTPUTS</span></span>

### <span data-ttu-id="91308-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="91308-126">System.Void</span></span>

## <span data-ttu-id="91308-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="91308-127">NOTES</span></span>

## <span data-ttu-id="91308-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="91308-128">RELATED LINKS</span></span>

[<span data-ttu-id="91308-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="91308-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="91308-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="91308-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


