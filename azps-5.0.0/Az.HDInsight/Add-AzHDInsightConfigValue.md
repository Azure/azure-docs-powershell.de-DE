---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: 4de1a76d2c9ec2cba7dae67d26f73ef55a5f827f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175597"
---
# <span data-ttu-id="2d766-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="2d766-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="2d766-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d766-102">SYNOPSIS</span></span>
<span data-ttu-id="2d766-103">Fügt einem Cluster Konfigurationsobjekt eine Anpassung der Hadoop-Konfigurationswerte und/oder eine freigegebene Hive-Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d766-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="2d766-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d766-104">SYNTAX</span></span>

```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-Spark2Defaults <Hashtable>]
 [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d766-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d766-105">DESCRIPTION</span></span>
<span data-ttu-id="2d766-106">Das Cmdlet **Add-AzHDInsightConfigValue** fügt eine Anpassung des Hadoop-Konfigurationswerts, wie core-site.xml oder hive-site.xml, und/oder eine Anpassung der freigegebenen Struktur Bibliothek an das vom New-AzHDInsightClusterConfig-Cmdlet erstellte HDInsight-Konfigurationsobjekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d766-106">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="2d766-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d766-107">EXAMPLES</span></span>

### <span data-ttu-id="2d766-108">Beispiel 1: Hinzufügen eines benutzerdefinierten Konfigurationswerts zum Cluster-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="2d766-108">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
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

<span data-ttu-id="2d766-109">Dieser Befehl fügt dem Cluster mit dem Namen "Your-Hadoop-001" einen Hadoop-Konfigurationswert hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d766-109">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="2d766-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d766-110">PARAMETERS</span></span>

### <span data-ttu-id="2d766-111">-Config</span><span class="sxs-lookup"><span data-stu-id="2d766-111">-Config</span></span>
<span data-ttu-id="2d766-112">Gibt das HDInsight-Cluster Konfigurationsobjekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2d766-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="2d766-113">Dieses Objekt wird vom New-AzHDInsightClusterConfig-Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="2d766-113">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="2d766-114">-Core</span><span class="sxs-lookup"><span data-stu-id="2d766-114">-Core</span></span>
<span data-ttu-id="2d766-115">Gibt die grundlegenden Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2d766-115">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d766-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d766-116">-DefaultProfile</span></span>
<span data-ttu-id="2d766-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2d766-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d766-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="2d766-118">-HBaseEnv</span></span>
<span data-ttu-id="2d766-119">Gibt die HBAs-env-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2d766-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d766-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="2d766-120">-HBaseSite</span></span>
<span data-ttu-id="2d766-121">Gibt die HBAs-Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2d766-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d766-122">-HDFS</span><span class="sxs-lookup"><span data-stu-id="2d766-122">-Hdfs</span></span>
<span data-ttu-id="2d766-123">Gibt die HDFS-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2d766-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d766-124">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="2d766-124">-HiveEnv</span></span>
<span data-ttu-id="2d766-125">Gibt die Struktur env-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2d766-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d766-126">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="2d766-126">-HiveSite</span></span>
<span data-ttu-id="2d766-127">Gibt die Struktur Website-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2d766-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d766-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="2d766-128">-MapRed</span></span>
<span data-ttu-id="2d766-129">Gibt die MapRed-Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2d766-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d766-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="2d766-130">-OozieEnv</span></span>
<span data-ttu-id="2d766-131">Gibt die Oozie env-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2d766-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d766-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="2d766-132">-OozieSite</span></span>
<span data-ttu-id="2d766-133">Gibt die Oozie-Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2d766-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d766-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="2d766-134">-RServer</span></span>
<span data-ttu-id="2d766-135">Gibt die RServer-Konfigurationen an.</span><span class="sxs-lookup"><span data-stu-id="2d766-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="2d766-136">Nur für RServer-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="2d766-136">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="2d766-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="2d766-137">-Spark2Defaults</span></span>
<span data-ttu-id="2d766-138">Gibt die Spark2-Standardkonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2d766-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d766-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="2d766-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="2d766-140">Gibt die Spark2 Thrift SparkConf-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2d766-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d766-141">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="2d766-141">-SparkDefaults</span></span>
<span data-ttu-id="2d766-142">Gibt die Standardkonfigurationen für Sparks dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2d766-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d766-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="2d766-143">-SparkThriftConf</span></span>
<span data-ttu-id="2d766-144">Gibt die Spark Thrift SparkConf-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2d766-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d766-145">-Storm</span><span class="sxs-lookup"><span data-stu-id="2d766-145">-Storm</span></span>
<span data-ttu-id="2d766-146">Gibt die Sturm Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2d766-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d766-147">-TEZ</span><span class="sxs-lookup"><span data-stu-id="2d766-147">-Tez</span></span>
<span data-ttu-id="2d766-148">Gibt die TEZ-Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2d766-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d766-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="2d766-149">-WebHCat</span></span>
<span data-ttu-id="2d766-150">Gibt die WebHCat-Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2d766-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d766-151">-Garn</span><span class="sxs-lookup"><span data-stu-id="2d766-151">-Yarn</span></span>
<span data-ttu-id="2d766-152">Gibt die Garn Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2d766-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d766-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d766-153">CommonParameters</span></span>
<span data-ttu-id="2d766-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d766-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d766-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d766-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d766-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d766-156">INPUTS</span></span>

### <span data-ttu-id="2d766-157">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="2d766-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="2d766-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d766-158">OUTPUTS</span></span>

### <span data-ttu-id="2d766-159">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="2d766-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="2d766-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d766-160">NOTES</span></span>

## <span data-ttu-id="2d766-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d766-161">RELATED LINKS</span></span>

[<span data-ttu-id="2d766-162">Neu – AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="2d766-162">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


