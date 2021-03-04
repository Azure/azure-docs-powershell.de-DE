---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: d5179bd15212e2d5bfa7eb5d903b2c37620ffb23
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938115"
---
# <span data-ttu-id="0c6d9-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="0c6d9-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="0c6d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c6d9-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6d9-103">Fügt einem Clusterkonfigurationsobjekt eine Anpassung des Hadoop-Konfigurationswerts und/oder eine Hive-Bibliotheksanpassung hinzu.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="0c6d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c6d9-104">SYNTAX</span></span>

```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-Spark2Defaults <Hashtable>]
 [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c6d9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c6d9-105">DESCRIPTION</span></span>
<span data-ttu-id="0c6d9-106">Das **Add-AzHDInsightConfigValue-Cmdlet** fügt eine Anpassung des Hadoop-Konfigurationswerts hinzu, z. B. core-site.xml oder hive-site.xml, und/oder eine Anpassung der freigegebenen Hive-Bibliothek an das hdInsight-Konfigurationsobjekt, das vom cmdlet New-AzHDInsightClusterConfig erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-106">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="0c6d9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0c6d9-107">EXAMPLES</span></span>

### <span data-ttu-id="0c6d9-108">Beispiel 1: Hinzufügen eines benutzerdefinierten Konfigurationswerts zum Clusterkonfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="0c6d9-108">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
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

<span data-ttu-id="0c6d9-109">Mit diesem Befehl wird dem Cluster mit dem Namen "your-hadoop-001" ein Hadoop-Konfigurationswert hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-109">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="0c6d9-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0c6d9-110">PARAMETERS</span></span>

### <span data-ttu-id="0c6d9-111">-Config</span><span class="sxs-lookup"><span data-stu-id="0c6d9-111">-Config</span></span>
<span data-ttu-id="0c6d9-112">Gibt das HDInsight-Clusterkonfigurationsobjekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="0c6d9-113">Dieses Objekt wird vom cmdlet New-AzHDInsightClusterConfig erstellt.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-113">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="0c6d9-114">-Core</span><span class="sxs-lookup"><span data-stu-id="0c6d9-114">-Core</span></span>
<span data-ttu-id="0c6d9-115">Gibt die Kernwebsitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-115">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0c6d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c6d9-116">-DefaultProfile</span></span>
<span data-ttu-id="0c6d9-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0c6d9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c6d9-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="0c6d9-118">-HBaseEnv</span></span>
<span data-ttu-id="0c6d9-119">Gibt die HBase Env-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0c6d9-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="0c6d9-120">-HBaseSite</span></span>
<span data-ttu-id="0c6d9-121">Gibt die HBase-Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0c6d9-122">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="0c6d9-122">-Hdfs</span></span>
<span data-ttu-id="0c6d9-123">Gibt die HDFS-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0c6d9-124">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="0c6d9-124">-HiveEnv</span></span>
<span data-ttu-id="0c6d9-125">Gibt die Hive Env-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0c6d9-126">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="0c6d9-126">-HiveSite</span></span>
<span data-ttu-id="0c6d9-127">Gibt die Konfigurationen der Hive-Website dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0c6d9-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="0c6d9-128">-MapRed</span></span>
<span data-ttu-id="0c6d9-129">Gibt die MapRed-Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0c6d9-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="0c6d9-130">-OozieEnv</span></span>
<span data-ttu-id="0c6d9-131">Gibt die Oozie Env-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0c6d9-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="0c6d9-132">-OozieSite</span></span>
<span data-ttu-id="0c6d9-133">Gibt die Oozie-Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0c6d9-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="0c6d9-134">-RServer</span></span>
<span data-ttu-id="0c6d9-135">Gibt die RServer-Konfigurationen an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="0c6d9-136">Gültig nur für RServer-Cluster.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-136">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="0c6d9-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="0c6d9-137">-Spark2Defaults</span></span>
<span data-ttu-id="0c6d9-138">Gibt die Spark2-Standardkonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0c6d9-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="0c6d9-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="0c6d9-140">Gibt die Spark2 Thrift SparkConf-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0c6d9-141">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="0c6d9-141">-SparkDefaults</span></span>
<span data-ttu-id="0c6d9-142">Gibt die Spark Defaults-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0c6d9-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="0c6d9-143">-SparkThriftConf</span></span>
<span data-ttu-id="0c6d9-144">Gibt die Spark Thrift SparkConf-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0c6d9-145">-Storm</span><span class="sxs-lookup"><span data-stu-id="0c6d9-145">-Storm</span></span>
<span data-ttu-id="0c6d9-146">Gibt die Konfigurationen der StormSite dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0c6d9-147">-Tez</span><span class="sxs-lookup"><span data-stu-id="0c6d9-147">-Tez</span></span>
<span data-ttu-id="0c6d9-148">Gibt die Konfigurationen der Tez-Website dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0c6d9-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="0c6d9-149">-WebHCat</span></span>
<span data-ttu-id="0c6d9-150">Gibt die WebHCat-Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0c6d9-151">-Garn</span><span class="sxs-lookup"><span data-stu-id="0c6d9-151">-Yarn</span></span>
<span data-ttu-id="0c6d9-152">Gibt die KONFIGURATIONEN der GARN-Website dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0c6d9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6d9-153">CommonParameters</span></span>
<span data-ttu-id="0c6d9-154">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c6d9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6d9-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c6d9-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6d9-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0c6d9-156">INPUTS</span></span>

### <span data-ttu-id="0c6d9-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="0c6d9-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="0c6d9-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0c6d9-158">OUTPUTS</span></span>

### <span data-ttu-id="0c6d9-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="0c6d9-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="0c6d9-160">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0c6d9-160">NOTES</span></span>

## <span data-ttu-id="0c6d9-161">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0c6d9-161">RELATED LINKS</span></span>

[<span data-ttu-id="0c6d9-162">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="0c6d9-162">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


