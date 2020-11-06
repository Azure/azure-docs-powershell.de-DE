---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightconfigvalues
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
ms.openlocfilehash: 75d68b98d93168d69db4d5120dde41ca1a8f8f2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482934"
---
# <span data-ttu-id="88a8b-101">Add-AzureRmHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="88a8b-101">Add-AzureRmHDInsightConfigValues</span></span>

## <span data-ttu-id="88a8b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="88a8b-103">Fügt einem Cluster Konfigurationsobjekt eine Anpassung der Hadoop-Konfigurationswerte und/oder eine freigegebene Hive-Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="88a8b-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88a8b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88a8b-104">SYNTAX</span></span>

### <span data-ttu-id="88a8b-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="88a8b-105">Spark1</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88a8b-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="88a8b-106">Spark2</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88a8b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88a8b-107">DESCRIPTION</span></span>
<span data-ttu-id="88a8b-108">Das Cmdlet **Add-AzureRmHDInsightConfigValues** fügt eine Anpassung des Hadoop-Konfigurationswerts, wie core-site.xml oder hive-site.xml, und/oder eine Anpassung der freigegebenen Struktur Bibliothek an das vom New-AzureRmHDInsightClusterConfig-Cmdlet erstellte HDInsight-Konfigurationsobjekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="88a8b-108">The **Add-AzureRmHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="88a8b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88a8b-109">EXAMPLES</span></span>

### <span data-ttu-id="88a8b-110">Beispiel 1: Hinzufügen eines benutzerdefinierten Konfigurationswerts zum Cluster-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="88a8b-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightConfigValues `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="88a8b-111">Dieser Befehl fügt dem Cluster mit dem Namen "Your-Hadoop-001" einen Hadoop-Konfigurationswert hinzu.</span><span class="sxs-lookup"><span data-stu-id="88a8b-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="88a8b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="88a8b-112">PARAMETERS</span></span>

### <span data-ttu-id="88a8b-113">-Config</span><span class="sxs-lookup"><span data-stu-id="88a8b-113">-Config</span></span>
<span data-ttu-id="88a8b-114">Gibt das HDInsight-Cluster Konfigurationsobjekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="88a8b-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="88a8b-115">Dieses Objekt wird vom New-AzureRmHDInsightClusterConfig-Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="88a8b-115">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-116">-Core</span><span class="sxs-lookup"><span data-stu-id="88a8b-116">-Core</span></span>
<span data-ttu-id="88a8b-117">Gibt die grundlegenden Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88a8b-118">-DefaultProfile</span></span>
<span data-ttu-id="88a8b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="88a8b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88a8b-120">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="88a8b-120">-HBaseEnv</span></span>
<span data-ttu-id="88a8b-121">Gibt die HBAs-env-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-121">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-122">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="88a8b-122">-HBaseSite</span></span>
<span data-ttu-id="88a8b-123">Gibt die HBAs-Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-123">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-124">-HDFS</span><span class="sxs-lookup"><span data-stu-id="88a8b-124">-Hdfs</span></span>
<span data-ttu-id="88a8b-125">Gibt die HDFS-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-125">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-126">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="88a8b-126">-HiveEnv</span></span>
<span data-ttu-id="88a8b-127">Gibt die Struktur env-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-127">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-128">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="88a8b-128">-HiveSite</span></span>
<span data-ttu-id="88a8b-129">Gibt die Struktur Website-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-129">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-130">-MapRed</span><span class="sxs-lookup"><span data-stu-id="88a8b-130">-MapRed</span></span>
<span data-ttu-id="88a8b-131">Gibt die MapRed-Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-131">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-132">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="88a8b-132">-OozieEnv</span></span>
<span data-ttu-id="88a8b-133">Gibt die Oozie env-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-133">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-134">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="88a8b-134">-OozieSite</span></span>
<span data-ttu-id="88a8b-135">Gibt die Oozie-Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-135">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-136">-RServer</span><span class="sxs-lookup"><span data-stu-id="88a8b-136">-RServer</span></span>
<span data-ttu-id="88a8b-137">Gibt die RServer-Konfigurationen an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-137">Specifies the RServer configurations.</span></span> <span data-ttu-id="88a8b-138">Nur für RServer-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="88a8b-138">Valid only for RServer clusters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-139">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="88a8b-139">-Spark2Defaults</span></span>
<span data-ttu-id="88a8b-140">Gibt die Spark2-Standardkonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-140">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-141">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="88a8b-141">-Spark2ThriftConf</span></span>
<span data-ttu-id="88a8b-142">Gibt die Spark2 Thrift SparkConf-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-142">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-143">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="88a8b-143">-SparkDefaults</span></span>
<span data-ttu-id="88a8b-144">Gibt die Standardkonfigurationen für Sparks dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-144">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-145">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="88a8b-145">-SparkThriftConf</span></span>
<span data-ttu-id="88a8b-146">Gibt die Spark Thrift SparkConf-Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-146">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-147">-Storm</span><span class="sxs-lookup"><span data-stu-id="88a8b-147">-Storm</span></span>
<span data-ttu-id="88a8b-148">Gibt die Sturm Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-148">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-149">-TEZ</span><span class="sxs-lookup"><span data-stu-id="88a8b-149">-Tez</span></span>
<span data-ttu-id="88a8b-150">Gibt die TEZ-Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-150">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-151">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="88a8b-151">-WebHCat</span></span>
<span data-ttu-id="88a8b-152">Gibt die WebHCat-Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-152">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-153">-Garn</span><span class="sxs-lookup"><span data-stu-id="88a8b-153">-Yarn</span></span>
<span data-ttu-id="88a8b-154">Gibt die Garn Websitekonfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="88a8b-154">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a8b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88a8b-155">CommonParameters</span></span>
<span data-ttu-id="88a8b-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88a8b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88a8b-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88a8b-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88a8b-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="88a8b-158">INPUTS</span></span>

### <span data-ttu-id="88a8b-159">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="88a8b-159">AzureHDInsightConfig</span></span>
<span data-ttu-id="88a8b-160">Der Parameter "config" akzeptiert den Wert vom Typ "AzureHDInsightConfig" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="88a8b-160">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="88a8b-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88a8b-161">OUTPUTS</span></span>

### <span data-ttu-id="88a8b-162">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="88a8b-162">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="88a8b-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="88a8b-163">NOTES</span></span>

## <span data-ttu-id="88a8b-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88a8b-164">RELATED LINKS</span></span>

[<span data-ttu-id="88a8b-165">Neu – AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="88a8b-165">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


