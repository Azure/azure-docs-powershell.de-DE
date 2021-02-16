---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/submit-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
ms.openlocfilehash: 3cbd73075445bdcf65efafb266476c522dc4b1ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153089"
---
# <span data-ttu-id="22368-101">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="22368-101">Submit-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="22368-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22368-102">SYNOPSIS</span></span>
<span data-ttu-id="22368-103">Übermittelt eine neue Skriptaktion an einen Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="22368-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="22368-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22368-104">SYNTAX</span></span>

```
Submit-AzHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22368-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22368-105">DESCRIPTION</span></span>
<span data-ttu-id="22368-106">Das **Cmdlet "Submit-AzHDInsightScriptAction"** übermittelt eine neue Skriptaktion an einen Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="22368-106">The **Submit-AzHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="22368-107">Verwenden *Sie PersistOnSuccess,* damit die Skriptaktion jedes Mal ausgeführt wird, wenn der Cluster skaliert wird, solange die Skriptaktion anfänglich erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="22368-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="22368-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="22368-108">EXAMPLES</span></span>

### <span data-ttu-id="22368-109">Beispiel 1: Übermitteln einer neuen Skriptaktion an einen laufenden Cluster "HDInsight"</span><span class="sxs-lookup"><span data-stu-id="22368-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="22368-110">Mit diesem Befehl wird eine Skriptaktion an einen laufenden Cluster "HDInsight" übermittelt.</span><span class="sxs-lookup"><span data-stu-id="22368-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="22368-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22368-111">PARAMETERS</span></span>

### <span data-ttu-id="22368-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="22368-112">-ApplicationName</span></span>
<span data-ttu-id="22368-113">Gibt den Anwendungsnamen für die Skriptaktion an.</span><span class="sxs-lookup"><span data-stu-id="22368-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="22368-114">Wenn *ApplicationName* angegeben wird, sollte *PersistOnSuccess* auf "False" festgelegt werden, Knoten dürfen nur Edgenode enthalten, und die Skriptaktionsanzahl sollte gleich 1 sein.</span><span class="sxs-lookup"><span data-stu-id="22368-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

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

### <span data-ttu-id="22368-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="22368-115">-ClusterName</span></span>
<span data-ttu-id="22368-116">Gibt den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="22368-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="22368-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22368-117">-DefaultProfile</span></span>
<span data-ttu-id="22368-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="22368-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22368-119">-Name</span><span class="sxs-lookup"><span data-stu-id="22368-119">-Name</span></span>
<span data-ttu-id="22368-120">Gibt den Namen der Skriptaktion an.</span><span class="sxs-lookup"><span data-stu-id="22368-120">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="22368-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="22368-121">-NodeTypes</span></span>
<span data-ttu-id="22368-122">Gibt die Knotentypen an, für die die Skriptaktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="22368-122">Specifies the node types on which to run the script action.</span></span>

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

### <span data-ttu-id="22368-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="22368-123">-Parameters</span></span>
<span data-ttu-id="22368-124">Gibt die Parameter für die Skriptaktion an.</span><span class="sxs-lookup"><span data-stu-id="22368-124">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="22368-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="22368-125">-PersistOnSuccess</span></span>
<span data-ttu-id="22368-126">Gibt an, dass die Skriptaktion jedes Mal ausgeführt werden soll, wenn der Cluster skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="22368-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="22368-127">Dieser Parameter wird ignoriert, wenn die Skriptaktion anfänglich fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="22368-127">This switch parameter is ignored if the script action initially fails.</span></span>

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

### <span data-ttu-id="22368-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22368-128">-ResourceGroupName</span></span>
<span data-ttu-id="22368-129">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="22368-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="22368-130">-URI</span><span class="sxs-lookup"><span data-stu-id="22368-130">-Uri</span></span>
<span data-ttu-id="22368-131">Gibt den öffentlichen URI für die Skriptaktion an (ein PowerShell- oder Bash-Skript).</span><span class="sxs-lookup"><span data-stu-id="22368-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="22368-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22368-132">CommonParameters</span></span>
<span data-ttu-id="22368-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22368-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22368-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22368-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22368-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="22368-135">INPUTS</span></span>

### <span data-ttu-id="22368-136">System.String</span><span class="sxs-lookup"><span data-stu-id="22368-136">System.String</span></span>

### <span data-ttu-id="22368-137">System.URI</span><span class="sxs-lookup"><span data-stu-id="22368-137">System.Uri</span></span>

### <span data-ttu-id="22368-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span><span class="sxs-lookup"><span data-stu-id="22368-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="22368-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="22368-139">OUTPUTS</span></span>

### <span data-ttu-id="22368-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="22368-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="22368-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="22368-141">NOTES</span></span>

## <span data-ttu-id="22368-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="22368-142">RELATED LINKS</span></span>

[<span data-ttu-id="22368-143">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="22368-143">Add-AzHDInsightScriptAction</span></span>](./Add-AzHDInsightScriptAction.md)


