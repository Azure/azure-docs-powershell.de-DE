---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/submit-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
ms.openlocfilehash: ef1c06c475b5de4984abf7859f033d68ad7d9dfa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651026"
---
# <span data-ttu-id="ce036-101">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="ce036-101">Submit-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="ce036-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ce036-102">SYNOPSIS</span></span>
<span data-ttu-id="ce036-103">Sendet eine neue Skript Aktion an einen Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="ce036-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ce036-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce036-104">SYNTAX</span></span>

```
Submit-AzHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce036-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce036-105">DESCRIPTION</span></span>
<span data-ttu-id="ce036-106">Das Cmdlet **Submit-AzHDInsightScriptAction** sendet eine neue Skript Aktion an einen Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="ce036-106">The **Submit-AzHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="ce036-107">Verwenden Sie *PersistOnSuccess* , wenn die Skript Aktion bei jedem Skalieren des Clusters ausgeführt werden soll, sofern die Skript Aktion anfänglich erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="ce036-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="ce036-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce036-108">EXAMPLES</span></span>

### <span data-ttu-id="ce036-109">Beispiel 1: Übermitteln einer neuen Skript Aktion an einen laufenden HDInsight-Cluster</span><span class="sxs-lookup"><span data-stu-id="ce036-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="ce036-110">Mit diesem Befehl wird eine Skript Aktion an einen ausgeführten HDInsight-Cluster übermittelt.</span><span class="sxs-lookup"><span data-stu-id="ce036-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="ce036-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce036-111">PARAMETERS</span></span>

### <span data-ttu-id="ce036-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="ce036-112">-ApplicationName</span></span>
<span data-ttu-id="ce036-113">Gibt den Anwendungsnamen für die Skript Aktion an.</span><span class="sxs-lookup"><span data-stu-id="ce036-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="ce036-114">Wenn *ApplicationName* angegeben wird, sollte *PersistOnSuccess* auf false festgelegt werden, Knoten müssen nur edgenode enthalten, und die Anzahl der Skriptaktionen sollte gleich 1 sein.</span><span class="sxs-lookup"><span data-stu-id="ce036-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

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

### <span data-ttu-id="ce036-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ce036-115">-ClusterName</span></span>
<span data-ttu-id="ce036-116">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="ce036-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ce036-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce036-117">-DefaultProfile</span></span>
<span data-ttu-id="ce036-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ce036-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce036-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ce036-119">-Name</span></span>
<span data-ttu-id="ce036-120">Gibt den Namen der Skript Aktion an.</span><span class="sxs-lookup"><span data-stu-id="ce036-120">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="ce036-121">-NodeType</span><span class="sxs-lookup"><span data-stu-id="ce036-121">-NodeTypes</span></span>
<span data-ttu-id="ce036-122">Gibt die Knotentypen an, für die die Skript Aktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce036-122">Specifies the node types on which to run the script action.</span></span>

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

### <span data-ttu-id="ce036-123">-Parameter</span><span class="sxs-lookup"><span data-stu-id="ce036-123">-Parameters</span></span>
<span data-ttu-id="ce036-124">Gibt die Parameter für die Skript Aktion an.</span><span class="sxs-lookup"><span data-stu-id="ce036-124">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="ce036-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="ce036-125">-PersistOnSuccess</span></span>
<span data-ttu-id="ce036-126">Gibt an, dass die Skript Aktion bei jedem Skalieren des Clusters ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce036-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="ce036-127">Dieser Parameter Switch wird ignoriert, wenn die Skript Aktion zunächst fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="ce036-127">This switch parameter is ignored if the script action initially fails.</span></span>

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

### <span data-ttu-id="ce036-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce036-128">-ResourceGroupName</span></span>
<span data-ttu-id="ce036-129">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ce036-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ce036-130">-URI</span><span class="sxs-lookup"><span data-stu-id="ce036-130">-Uri</span></span>
<span data-ttu-id="ce036-131">Gibt den öffentlichen URI für die Skript Aktion an (ein PowerShell-oder bash-Skript).</span><span class="sxs-lookup"><span data-stu-id="ce036-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="ce036-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce036-132">CommonParameters</span></span>
<span data-ttu-id="ce036-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce036-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce036-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce036-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce036-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ce036-135">INPUTS</span></span>

### <span data-ttu-id="ce036-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ce036-136">System.String</span></span>

### <span data-ttu-id="ce036-137">System. Uri</span><span class="sxs-lookup"><span data-stu-id="ce036-137">System.Uri</span></span>

### <span data-ttu-id="ce036-138">Microsoft. Azure. Commands. HDInsight. Models. Management. RuntimeScriptActionClusterNodeType []</span><span class="sxs-lookup"><span data-stu-id="ce036-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="ce036-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ce036-139">OUTPUTS</span></span>

### <span data-ttu-id="ce036-140">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="ce036-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="ce036-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce036-141">NOTES</span></span>

## <span data-ttu-id="ce036-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ce036-142">RELATED LINKS</span></span>

[<span data-ttu-id="ce036-143">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="ce036-143">Add-AzHDInsightScriptAction</span></span>](./Add-AzHDInsightScriptAction.md)


