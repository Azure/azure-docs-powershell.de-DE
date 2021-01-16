---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/submit-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
ms.openlocfilehash: dfae83e6bd540a83475f02ed95382bebff2ec7a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291976"
---
# <span data-ttu-id="59f59-101">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="59f59-101">Submit-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="59f59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59f59-102">SYNOPSIS</span></span>
<span data-ttu-id="59f59-103">Übermittelt eine neue Skriptaktion an einen Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="59f59-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="59f59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59f59-104">SYNTAX</span></span>

```
Submit-AzHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59f59-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59f59-105">DESCRIPTION</span></span>
<span data-ttu-id="59f59-106">Das **Cmdlet "Submit-AzHDInsightScriptAction"** übermittelt eine neue Skriptaktion an einen Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="59f59-106">The **Submit-AzHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="59f59-107">Verwenden *Sie PersistOnSuccess,* damit die Skriptaktion jedes Mal ausgeführt wird, wenn der Cluster skaliert wird, solange die Skriptaktion anfänglich erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="59f59-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="59f59-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="59f59-108">EXAMPLES</span></span>

### <span data-ttu-id="59f59-109">Beispiel 1: Übermitteln einer neuen Skriptaktion an einen laufenden Cluster "HDInsight"</span><span class="sxs-lookup"><span data-stu-id="59f59-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="59f59-110">Mit diesem Befehl wird eine Skriptaktion an einen laufenden Cluster "HDInsight" übermittelt.</span><span class="sxs-lookup"><span data-stu-id="59f59-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="59f59-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59f59-111">PARAMETERS</span></span>

### <span data-ttu-id="59f59-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="59f59-112">-ApplicationName</span></span>
<span data-ttu-id="59f59-113">Gibt den Anwendungsnamen für die Skriptaktion an.</span><span class="sxs-lookup"><span data-stu-id="59f59-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="59f59-114">Wenn *ApplicationName* angegeben wird, sollte *PersistOnSuccess* auf "False" festgelegt werden, Knoten dürfen nur Edgenode enthalten, und die Skriptaktionsanzahl sollte gleich 1 sein.</span><span class="sxs-lookup"><span data-stu-id="59f59-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59f59-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="59f59-115">-ClusterName</span></span>
<span data-ttu-id="59f59-116">Gibt den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="59f59-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="59f59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f59-117">-DefaultProfile</span></span>
<span data-ttu-id="59f59-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="59f59-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59f59-119">-Name</span><span class="sxs-lookup"><span data-stu-id="59f59-119">-Name</span></span>
<span data-ttu-id="59f59-120">Gibt den Namen der Skriptaktion an.</span><span class="sxs-lookup"><span data-stu-id="59f59-120">Specifies the name of the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59f59-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="59f59-121">-NodeTypes</span></span>
<span data-ttu-id="59f59-122">Gibt die Knotentypen an, für die die Skriptaktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="59f59-122">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59f59-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="59f59-123">-Parameters</span></span>
<span data-ttu-id="59f59-124">Gibt die Parameter für die Skriptaktion an.</span><span class="sxs-lookup"><span data-stu-id="59f59-124">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59f59-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="59f59-125">-PersistOnSuccess</span></span>
<span data-ttu-id="59f59-126">Gibt an, dass die Skriptaktion jedes Mal ausgeführt werden soll, wenn der Cluster skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="59f59-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="59f59-127">Dieser Parameter wird ignoriert, wenn die Skriptaktion anfänglich fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="59f59-127">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f59-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59f59-128">-ResourceGroupName</span></span>
<span data-ttu-id="59f59-129">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="59f59-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="59f59-130">-URI</span><span class="sxs-lookup"><span data-stu-id="59f59-130">-Uri</span></span>
<span data-ttu-id="59f59-131">Gibt den öffentlichen URI für die Skriptaktion an (ein PowerShell- oder Bash-Skript).</span><span class="sxs-lookup"><span data-stu-id="59f59-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59f59-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f59-132">CommonParameters</span></span>
<span data-ttu-id="59f59-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59f59-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f59-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59f59-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f59-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="59f59-135">INPUTS</span></span>

### <span data-ttu-id="59f59-136">System.String</span><span class="sxs-lookup"><span data-stu-id="59f59-136">System.String</span></span>

### <span data-ttu-id="59f59-137">System.URI</span><span class="sxs-lookup"><span data-stu-id="59f59-137">System.Uri</span></span>

### <span data-ttu-id="59f59-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span><span class="sxs-lookup"><span data-stu-id="59f59-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="59f59-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="59f59-139">OUTPUTS</span></span>

### <span data-ttu-id="59f59-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="59f59-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="59f59-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="59f59-141">NOTES</span></span>

## <span data-ttu-id="59f59-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="59f59-142">RELATED LINKS</span></span>

[<span data-ttu-id="59f59-143">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="59f59-143">Add-AzHDInsightScriptAction</span></span>](./Add-AzHDInsightScriptAction.md)


