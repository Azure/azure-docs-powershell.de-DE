---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 4d3d88fb5a8cca2343403870233e89b0f2073e8e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166607"
---
# <span data-ttu-id="077b9-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="077b9-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="077b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="077b9-102">SYNOPSIS</span></span>
<span data-ttu-id="077b9-103">Entfernt eine beibehaltene Skript Aktion aus einem HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="077b9-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="077b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="077b9-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="077b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="077b9-105">DESCRIPTION</span></span>
<span data-ttu-id="077b9-106">Das Cmdlet **Remove-AzHDInsightPersistedScriptAction** entfernt eine permanente Skript Aktion aus der Liste der beibehaltenen Skriptaktionen des angegebenen Azure HDInsight-Clusters.</span><span class="sxs-lookup"><span data-stu-id="077b9-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="077b9-107">Das entfernte Skript wird beim Skalieren des Clusters nicht mehr ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="077b9-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="077b9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="077b9-108">EXAMPLES</span></span>

### <span data-ttu-id="077b9-109">Beispiel 1: Entfernen einer Skript Aktion aus der Liste der beibehaltenen Skriptaktionen in einem Cluster</span><span class="sxs-lookup"><span data-stu-id="077b9-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="077b9-110">Dieser Befehl entfernt die Skript Aktion mit dem Namen Skript Action aus der Liste der beibehaltenen Skriptaktionen auf dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="077b9-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="077b9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="077b9-111">PARAMETERS</span></span>

### <span data-ttu-id="077b9-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="077b9-112">-ClusterName</span></span>
<span data-ttu-id="077b9-113">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="077b9-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="077b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="077b9-114">-DefaultProfile</span></span>
<span data-ttu-id="077b9-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="077b9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="077b9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="077b9-116">-Name</span></span>
<span data-ttu-id="077b9-117">Gibt den Namen der beibehaltenen Skript Aktion an, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="077b9-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="077b9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="077b9-118">-ResourceGroupName</span></span>
<span data-ttu-id="077b9-119">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="077b9-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="077b9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="077b9-120">CommonParameters</span></span>
<span data-ttu-id="077b9-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="077b9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="077b9-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="077b9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="077b9-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="077b9-123">INPUTS</span></span>

### <span data-ttu-id="077b9-124">Keine</span><span class="sxs-lookup"><span data-stu-id="077b9-124">None</span></span>

## <span data-ttu-id="077b9-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="077b9-125">OUTPUTS</span></span>

### <span data-ttu-id="077b9-126">System. void</span><span class="sxs-lookup"><span data-stu-id="077b9-126">System.Void</span></span>

## <span data-ttu-id="077b9-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="077b9-127">NOTES</span></span>

## <span data-ttu-id="077b9-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="077b9-128">RELATED LINKS</span></span>

[<span data-ttu-id="077b9-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="077b9-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="077b9-130">Satz-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="077b9-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


