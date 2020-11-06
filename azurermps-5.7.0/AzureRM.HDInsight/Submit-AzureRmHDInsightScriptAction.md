---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/submit-azurermhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 866bd8c8189ca727b3893f09370bcca1136e827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504569"
---
# <span data-ttu-id="0b5e4-101">Submit-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="0b5e4-101">Submit-AzureRmHDInsightScriptAction</span></span>

## <span data-ttu-id="0b5e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b5e4-102">SYNOPSIS</span></span>
<span data-ttu-id="0b5e4-103">Sendet eine neue Skript Aktion an einen Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="0b5e4-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b5e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b5e4-104">SYNTAX</span></span>

```
Submit-AzureRmHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b5e4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b5e4-105">DESCRIPTION</span></span>
<span data-ttu-id="0b5e4-106">Das Cmdlet **Submit-AzureRmHDInsightScriptAction** sendet eine neue Skript Aktion an einen Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="0b5e4-106">The **Submit-AzureRmHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="0b5e4-107">Verwenden Sie *PersistOnSuccess* , wenn die Skript Aktion bei jedem Skalieren des Clusters ausgeführt werden soll, sofern die Skript Aktion anfänglich erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="0b5e4-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="0b5e4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b5e4-108">EXAMPLES</span></span>

### <span data-ttu-id="0b5e4-109">Beispiel 1: Übermitteln einer neuen Skript Aktion an einen laufenden HDInsight-Cluster</span><span class="sxs-lookup"><span data-stu-id="0b5e4-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzureRmHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="0b5e4-110">Mit diesem Befehl wird eine Skript Aktion an einen ausgeführten HDInsight-Cluster übermittelt.</span><span class="sxs-lookup"><span data-stu-id="0b5e4-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="0b5e4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b5e4-111">PARAMETERS</span></span>

### <span data-ttu-id="0b5e4-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="0b5e4-112">-ApplicationName</span></span>
<span data-ttu-id="0b5e4-113">Gibt den Anwendungsnamen für die Skript Aktion an.</span><span class="sxs-lookup"><span data-stu-id="0b5e4-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="0b5e4-114">Wenn *ApplicationName* angegeben wird, sollte *PersistOnSuccess* auf false festgelegt werden, Knoten müssen nur edgenode enthalten, und die Anzahl der Skriptaktionen sollte gleich 1 sein.</span><span class="sxs-lookup"><span data-stu-id="0b5e4-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5e4-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="0b5e4-115">-ClusterName</span></span>
<span data-ttu-id="0b5e4-116">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0b5e4-116">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b5e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b5e4-117">-DefaultProfile</span></span>
<span data-ttu-id="0b5e4-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0b5e4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b5e4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0b5e4-119">-Name</span></span>
<span data-ttu-id="0b5e4-120">Gibt den Namen der Skript Aktion an.</span><span class="sxs-lookup"><span data-stu-id="0b5e4-120">Specifies the name of the script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5e4-121">-NodeType</span><span class="sxs-lookup"><span data-stu-id="0b5e4-121">-NodeTypes</span></span>
<span data-ttu-id="0b5e4-122">Gibt die Knotentypen an, für die die Skript Aktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b5e4-122">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases: 
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5e4-123">-Parameter</span><span class="sxs-lookup"><span data-stu-id="0b5e4-123">-Parameters</span></span>
<span data-ttu-id="0b5e4-124">Gibt die Parameter für die Skript Aktion an.</span><span class="sxs-lookup"><span data-stu-id="0b5e4-124">Specifies the parameters for the script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5e4-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="0b5e4-125">-PersistOnSuccess</span></span>
<span data-ttu-id="0b5e4-126">Gibt an, dass die Skript Aktion bei jedem Skalieren des Clusters ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b5e4-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="0b5e4-127">Dieser Parameter Switch wird ignoriert, wenn die Skript Aktion zunächst fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="0b5e4-127">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b5e4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b5e4-128">-ResourceGroupName</span></span>
<span data-ttu-id="0b5e4-129">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0b5e4-129">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b5e4-130">-URI</span><span class="sxs-lookup"><span data-stu-id="0b5e4-130">-Uri</span></span>
<span data-ttu-id="0b5e4-131">Gibt den öffentlichen URI für die Skript Aktion an (ein PowerShell-oder bash-Skript).</span><span class="sxs-lookup"><span data-stu-id="0b5e4-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5e4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b5e4-132">CommonParameters</span></span>
<span data-ttu-id="0b5e4-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b5e4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b5e4-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b5e4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b5e4-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b5e4-135">INPUTS</span></span>

### <span data-ttu-id="0b5e4-136">Keine</span><span class="sxs-lookup"><span data-stu-id="0b5e4-136">None</span></span>
<span data-ttu-id="0b5e4-137">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0b5e4-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b5e4-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b5e4-138">OUTPUTS</span></span>

### <span data-ttu-id="0b5e4-139">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="0b5e4-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="0b5e4-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b5e4-140">NOTES</span></span>

## <span data-ttu-id="0b5e4-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b5e4-141">RELATED LINKS</span></span>

[<span data-ttu-id="0b5e4-142">Add-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="0b5e4-142">Add-AzureRmHDInsightScriptAction</span></span>](./Add-AzureRmHDInsightScriptAction.md)


