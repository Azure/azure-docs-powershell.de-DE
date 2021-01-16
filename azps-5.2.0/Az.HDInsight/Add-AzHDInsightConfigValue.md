---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: 4de1a76d2c9ec2cba7dae67d26f73ef55a5f827f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295739"
---
# <span data-ttu-id="1edb8-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="1edb8-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="1edb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1edb8-102">SYNOPSIS</span></span>
<span data-ttu-id="1edb8-103">Fügt einem Clusterkonfigurationsobjekt eine Anpassung des Werts für die Konfiguration von Hadoop und/oder eine Anpassung der freigegebenen Strukturbibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="1edb8-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="1edb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1edb8-104">SYNTAX</span></span>

```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-Spark2Defaults <Hashtable>]
 [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1edb8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1edb8-105">DESCRIPTION</span></span>
<span data-ttu-id="1edb8-106">Das Cmdlet **"Add-AzHDInsightConfigValue"** fügt dem vom Cmdlet "" erstellten Konfigurationsobjekt "HDIn New-AzHDInsightClusterConfig sight" eine Anpassung des Hadoop-Konfigurationswerts, z. B. core-site.xml oder hive-site.xml, und/oder eine Anpassung der freigegebenen Bibliothek "Strukture" hinzu.</span><span class="sxs-lookup"><span data-stu-id="1edb8-106">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="1edb8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1edb8-107">EXAMPLES</span></span>

### <span data-ttu-id="1edb8-108">Beispiel 1: Hinzufügen eines benutzerdefinierten Konfigurationswerts zum Clusterkonfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="1edb8-108">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightConfigValue `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageAccountContainer
```

<span data-ttu-id="1edb8-109">Dieser Befehl fügt dem Cluster mit dem Namen "your-hadoop-001" einen Wert für die Konfiguration von Hadoop hinzu.</span><span class="sxs-lookup"><span data-stu-id="1edb8-109">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="1edb8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1edb8-110">PARAMETERS</span></span>

### <span data-ttu-id="1edb8-111">-Config</span><span class="sxs-lookup"><span data-stu-id="1edb8-111">-Config</span></span>
<span data-ttu-id="1edb8-112">Gibt das Konfigurationsobjekt für den HDInsight-Cluster an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="1edb8-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="1edb8-113">Dieses Objekt wird vom New-AzHDInsightClusterConfig erstellt.</span><span class="sxs-lookup"><span data-stu-id="1edb8-113">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-114">-Core</span><span class="sxs-lookup"><span data-stu-id="1edb8-114">-Core</span></span>
<span data-ttu-id="1edb8-115">Gibt die Kernwebsitekonfigurationen dieses Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-115">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1edb8-116">-DefaultProfile</span></span>
<span data-ttu-id="1edb8-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1edb8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1edb8-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="1edb8-118">-HBaseEnv</span></span>
<span data-ttu-id="1edb8-119">Gibt die HBase-Env-Konfigurationen dieses Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="1edb8-120">-HBaseSite</span></span>
<span data-ttu-id="1edb8-121">Gibt die Konfigurationen der HBase-Website dieses Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-122">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="1edb8-122">-Hdfs</span></span>
<span data-ttu-id="1edb8-123">Gibt die HDFS-Konfigurationen dieses Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-124">-StruktureEnv</span><span class="sxs-lookup"><span data-stu-id="1edb8-124">-HiveEnv</span></span>
<span data-ttu-id="1edb8-125">Gibt die Strukturenv-Konfigurationen dieses Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-126">-StruktureSite</span><span class="sxs-lookup"><span data-stu-id="1edb8-126">-HiveSite</span></span>
<span data-ttu-id="1edb8-127">Gibt die Konfigurationen der Strukturwebsite dieses Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="1edb8-128">-MapRed</span></span>
<span data-ttu-id="1edb8-129">Gibt die "MapRed Site"-Konfigurationen dieses Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="1edb8-130">-OozieEnv</span></span>
<span data-ttu-id="1edb8-131">Gibt die Konfigurationen von Oozie Env dieses Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="1edb8-132">-OozieSite</span></span>
<span data-ttu-id="1edb8-133">Gibt die Konfigurationen der Oozie-Website dieses Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="1edb8-134">-RServer</span></span>
<span data-ttu-id="1edb8-135">Gibt die RServer-Konfigurationen an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="1edb8-136">Gültig nur für RServer-Cluster.</span><span class="sxs-lookup"><span data-stu-id="1edb8-136">Valid only for RServer clusters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="1edb8-137">-Spark2Defaults</span></span>
<span data-ttu-id="1edb8-138">Gibt die Spark2-Standardkonfigurationen dieses Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="1edb8-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="1edb8-140">Gibt die Spark2-Thrift -SparkConf-Konfigurationen dieses Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-141">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="1edb8-141">-SparkDefaults</span></span>
<span data-ttu-id="1edb8-142">Gibt die Spark-Standardkonfigurationen dieses Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="1edb8-143">-SparkThriftConf</span></span>
<span data-ttu-id="1edb8-144">Gibt die Spark Thrift SparkConf-Konfigurationen dieses Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-145">-Storm</span><span class="sxs-lookup"><span data-stu-id="1edb8-145">-Storm</span></span>
<span data-ttu-id="1edb8-146">Gibt die Konfigurationen von "Storm Site" dieses Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-147">-Tez</span><span class="sxs-lookup"><span data-stu-id="1edb8-147">-Tez</span></span>
<span data-ttu-id="1edb8-148">Gibt die Konfigurationen der Website "Tez" dieses Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="1edb8-149">-WebHCat</span></span>
<span data-ttu-id="1edb8-150">Gibt die WebHCat-Websitekonfigurationen dieses Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-151">-Vorn</span><span class="sxs-lookup"><span data-stu-id="1edb8-151">-Yarn</span></span>
<span data-ttu-id="1edb8-152">Gibt die KONFIGURATIONen der WEBSITE VON MFA für diesen Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="1edb8-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edb8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1edb8-153">CommonParameters</span></span>
<span data-ttu-id="1edb8-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1edb8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1edb8-155">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1edb8-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1edb8-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1edb8-156">INPUTS</span></span>

### <span data-ttu-id="1edb8-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="1edb8-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="1edb8-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1edb8-158">OUTPUTS</span></span>

### <span data-ttu-id="1edb8-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="1edb8-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="1edb8-160">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1edb8-160">NOTES</span></span>

## <span data-ttu-id="1edb8-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1edb8-161">RELATED LINKS</span></span>

[<span data-ttu-id="1edb8-162">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="1edb8-162">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


