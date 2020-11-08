---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0809415ea5dfff687c69089e1aeda60c9f3b00ee
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005926"
---
# <span data-ttu-id="1c333-101">Add-AzureHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="1c333-101">Add-AzureHDInsightScriptAction</span></span>

## <span data-ttu-id="1c333-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c333-102">SYNOPSIS</span></span>
<span data-ttu-id="1c333-103">Fügt eine HDInsight-Skript Aktion hinzu.</span><span class="sxs-lookup"><span data-stu-id="1c333-103">Adds an HDInsight script action.</span></span>

## <span data-ttu-id="1c333-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c333-104">SYNTAX</span></span>

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c333-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c333-105">DESCRIPTION</span></span>
<span data-ttu-id="1c333-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="1c333-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="1c333-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="1c333-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="1c333-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1c333-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="1c333-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="1c333-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="1c333-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="1c333-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="1c333-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1c333-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="1c333-112">Das Cmdlet **Add-AzureHDInsightScriptAction** bietet Azure-HDInsight-Funktionen, die zum Installieren zusätzlicher Software oder zum Ändern der Konfiguration von Anwendungen verwendet werden, die in einem Hadoop-Cluster mithilfe von Windows PowerShell-Skripts ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1c333-112">The **Add-AzureHDInsightScriptAction** cmdlet provides Azure HDInsight functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell scripts.</span></span>

<span data-ttu-id="1c333-113">Eine Skript Aktion wird auf den Clusterknoten ausgeführt, wenn HDInsight-Cluster bereitgestellt werden, und Sie werden ausgeführt, nachdem die Knoten im Cluster die HDInsight-Konfiguration abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="1c333-113">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="1c333-114">Die Skript Aktion wird unter Systemadministratorkonto Privilegien ausgeführt und bietet vollständige Zugriffsrechte für die Clusterknoten.</span><span class="sxs-lookup"><span data-stu-id="1c333-114">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="1c333-115">Sie können jedem Cluster eine Liste von Skriptaktionen zur Verfügung stellen, die in einer bestimmten Reihenfolge ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1c333-115">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="1c333-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c333-116">EXAMPLES</span></span>

### <span data-ttu-id="1c333-117">Beispiel 1: Hinzufügen einer Skript Aktion zu einem Cluster</span><span class="sxs-lookup"><span data-stu-id="1c333-117">Example 1: Add a script action to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="1c333-118">Der erste Befehl verwendet das Cmdlet **New-AzureHDInsightClusterConfig** , um eine HDInsight-Cluster Konfiguration zu erstellen, und speichert Sie dann in der $config-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1c333-118">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="1c333-119">Der zweite Befehl verwendet das Cmdlet **Add-AzureHDInsightScriptAction** , um die Skript Aktion mit dem Namen TestScriptAction zu $config hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1c333-119">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the script action named TestScriptAction to $Config.</span></span>

<span data-ttu-id="1c333-120">Der endgültige Befehl verwendet das Cmdlet **New-AzureHDInsightCluster** zum Erstellen eines neuen HDInsight-Clusters, der die in $config gespeicherte Skript Aktion ausführt.</span><span class="sxs-lookup"><span data-stu-id="1c333-120">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster that runs the script action stored in $Config.</span></span>

### <span data-ttu-id="1c333-121">Beispiel 2: Hinzufügen mehrerer Skriptaktionen zu einem Cluster</span><span class="sxs-lookup"><span data-stu-id="1c333-121">Example 2: Add multiple script actions to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="1c333-122">Der erste Befehl verwendet das Cmdlet **New-AzureHDInsightClusterConfig** , um eine HDInsight-Cluster Konfiguration zu erstellen, und speichert Sie dann in der $config-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1c333-122">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="1c333-123">Der zweite Befehl verwendet das Cmdlet **Add-AzureHDInsightScriptAction** , um die angegebene Skript Aktion zu $config hinzuzufügen, und verwendet dann den Pipelineoperator, um $config an **Add-AzureHDInsightScriptAction** ein zweites Mal zu übergeben, um $config eine zweite Skript Aktion hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1c333-123">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the specified script action to $Config, and then uses the pipeline operator to pass $Config to **Add-AzureHDInsightScriptAction** a second time to add a second script action to $Config.</span></span>

<span data-ttu-id="1c333-124">Der endgültige Befehl verwendet das Cmdlet **New-AzureHDInsightCluster** zum Erstellen eines Clusters, in dem die Skriptaktionen in $config ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1c333-124">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a cluster that runs the script actions in $Config.</span></span>

## <span data-ttu-id="1c333-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c333-125">PARAMETERS</span></span>

### <span data-ttu-id="1c333-126">-ClusterRoleCollection</span><span class="sxs-lookup"><span data-stu-id="1c333-126">-ClusterRoleCollection</span></span>
<span data-ttu-id="1c333-127">Gibt die Knoten an, für die ein Skript ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c333-127">Specifies the nodes for which to run a script.</span></span>
<span data-ttu-id="1c333-128">Die zulässigen Werte für diesen Parameter sind: HeadNode oder datanode.</span><span class="sxs-lookup"><span data-stu-id="1c333-128">The acceptable values for this parameter are: HeadNode or DataNode.</span></span>

<span data-ttu-id="1c333-129">Sie können einen oder beide Werte angeben.</span><span class="sxs-lookup"><span data-stu-id="1c333-129">You can specify one value or both values.</span></span>

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c333-130">-Config</span><span class="sxs-lookup"><span data-stu-id="1c333-130">-Config</span></span>
<span data-ttu-id="1c333-131">Gibt ein Configuration-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="1c333-131">Specifies a configuration object.</span></span>
<span data-ttu-id="1c333-132">Dieses Cmdlet fügt dem Objekt, das dieser Parameter angibt, Skript Aktionsinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="1c333-132">This cmdlet adds script action information to the object that this parameter specifies.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c333-133">-Name</span><span class="sxs-lookup"><span data-stu-id="1c333-133">-Name</span></span>
<span data-ttu-id="1c333-134">Gibt den Namen einer Skript Aktion an.</span><span class="sxs-lookup"><span data-stu-id="1c333-134">Specifies the name of a script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c333-135">-Parameter</span><span class="sxs-lookup"><span data-stu-id="1c333-135">-Parameters</span></span>
<span data-ttu-id="1c333-136">Gibt die Parameter an, die für eine Skript Aktion erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1c333-136">Specifies the parameters that are required by a script action.</span></span>

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

### <span data-ttu-id="1c333-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="1c333-137">-Profile</span></span>
<span data-ttu-id="1c333-138">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="1c333-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1c333-139">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="1c333-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c333-140">-URI</span><span class="sxs-lookup"><span data-stu-id="1c333-140">-Uri</span></span>
<span data-ttu-id="1c333-141">Gibt den URI-Speicherort eines Skripts an, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c333-141">Specifies the URI location of a script to run.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c333-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c333-142">CommonParameters</span></span>
<span data-ttu-id="1c333-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c333-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c333-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c333-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c333-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c333-145">INPUTS</span></span>

## <span data-ttu-id="1c333-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c333-146">OUTPUTS</span></span>

## <span data-ttu-id="1c333-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c333-147">NOTES</span></span>

## <span data-ttu-id="1c333-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c333-148">RELATED LINKS</span></span>

[<span data-ttu-id="1c333-149">Neu – AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1c333-149">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="1c333-150">Neu – AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="1c333-150">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


