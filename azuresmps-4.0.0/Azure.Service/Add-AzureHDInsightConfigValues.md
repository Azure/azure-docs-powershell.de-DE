---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6F89C297-4D3D-4DAD-A63A-FCC51A86BF43
online version: ''
schema: 2.0.0
ms.openlocfilehash: 542b2fb83b69fe5eb63ac6b8b979df6cc8051ed2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005934"
---
# <span data-ttu-id="42402-101">Add-AzureHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="42402-101">Add-AzureHDInsightConfigValues</span></span>

## <span data-ttu-id="42402-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42402-102">SYNOPSIS</span></span>
<span data-ttu-id="42402-103">Fügt einer HDInsight-Cluster Konfiguration eine Anpassung des Hadoop-Konfigurationswerts oder eine freigegebene Hive-Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="42402-103">Adds a Hadoop configuration value customization or a Hive shared library customization to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="42402-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42402-104">SYNTAX</span></span>

```
Add-AzureHDInsightConfigValues -Config <AzureHDInsightConfig> [-Core <Hashtable>] [-Yarn <Hashtable>]
 [-Hdfs <Hashtable>] [-Hive <AzureHDInsightHiveConfiguration>]
 [-MapReduce <AzureHDInsightMapReduceConfiguration>] [-Oozie <AzureHDInsightOozieConfiguration>]
 [-Storm <Hashtable>] [-Spark <Hashtable>] [-HBase <AzureHDInsightHBaseConfiguration>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="42402-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42402-105">DESCRIPTION</span></span>
<span data-ttu-id="42402-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="42402-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="42402-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="42402-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="42402-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="42402-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="42402-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span><span class="sxs-lookup"><span data-stu-id="42402-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="42402-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span><span class="sxs-lookup"><span data-stu-id="42402-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="42402-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span><span class="sxs-lookup"><span data-stu-id="42402-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="42402-112">Das **Add-AzureHDInsightConfigValues-** Cmdlet fügt eine Anpassung des Hadoop-Konfigurationswerts wie Core-site.xml oder Hive-site.xml oder eine freigegebene Bibliothek für eine Hive-Konfiguration zu einer Azure HDInsight-Cluster Konfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="42402-112">The **Add-AzureHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as Core-site.xml or Hive-site.xml, or a Hive shared library customization to an Azure HDInsight cluster configuration.</span></span>

<span data-ttu-id="42402-113">Das Cmdlet fügt einem angegebenen Konfigurationsobjekt benutzerdefinierte Konfigurationswerte hinzu.</span><span class="sxs-lookup"><span data-stu-id="42402-113">The cmdlet adds custom configuration values to a specified configuration object.</span></span>
<span data-ttu-id="42402-114">Die benutzerdefinierten Einstellungen werden den Konfigurationsdateien der relevanten Hadoop-Dienste hinzugefügt, wenn der Cluster bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="42402-114">The custom settings are added to the configuration files of the relevant Hadoop services when the cluster is deployed.</span></span>

## <span data-ttu-id="42402-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42402-115">EXAMPLES</span></span>

### <span data-ttu-id="42402-116">Beispiel 1: Konfigurieren eines Clusters</span><span class="sxs-lookup"><span data-stu-id="42402-116">Example 1: Configure a cluster</span></span>
```
PS C:\>$HiveConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightHiveConfiguration'
PS C:\> $HiveConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $HiveConfigValues.AdditionalLibraries = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightDefaultStorageAccount'
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountName = "MyStorageAccount.blob.core.windows.net"
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountKey = (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageContainerName = "MySharedLibContainer"
PS C:\> $OozieConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightOozieConfiguration'
PS C:\> $OozieConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $MapredConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightMapReduceConfiguration'
PS C:\> $MapredConfigValues.Configuration = @{ mapred.map.max.attempts = 2 }
PS C:\> $MapredConfigValues.CapacitySchedulerConfiguration = @{ mapred.capacity-scheduler.init-poll-interval = 1000 }
PS C:\> $Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyStorageAccount.blob.core.windows.net -StorageAccountKey (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary -StorageContainerName "MyStorageContainer"
    | Add-AzureHDInsightConfigValues -Core @{ io.file.buffer.size = 300000 } -MapReduce $MapredConfigValues -Hive $HiveConfigValues -Oozie $OozieConfigValues
PS C:\> $Config | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds -Name "MyCluster" -Location "North Europe"
```

<span data-ttu-id="42402-117">Der erste Befehl erstellt ein neues **AzureHDInsightHiveConfiguration** -Objekt und speichert es dann in der $HiveConfigValues-Variablen.</span><span class="sxs-lookup"><span data-stu-id="42402-117">The first command creates a new **AzureHDInsightHiveConfiguration** object, and then stores it in the $HiveConfigValues variable.</span></span>

<span data-ttu-id="42402-118">Die nächsten fünf Befehle erstellen Konfigurationswerte für Hive und speichern diese Werte als Mitglieder von $HiveConfigValues.</span><span class="sxs-lookup"><span data-stu-id="42402-118">The next five commands create configuration values for Hive and store those values as members of $HiveConfigValues.</span></span>

<span data-ttu-id="42402-119">Der siebte Befehl erstellt ein **AzureHDInsightOozieConfiguration** -Objekt und speichert es dann in der $OozieConfigValues-Variablen.</span><span class="sxs-lookup"><span data-stu-id="42402-119">The seventh command creates an **AzureHDInsightOozieConfiguration** object, and then stores it in the $OozieConfigValues variable.</span></span>
<span data-ttu-id="42402-120">Der achte Befehl erstellt einen Konfigurationswert für Oozie und speichert diese Werte dann als Mitglied von $OozieConfigValues.</span><span class="sxs-lookup"><span data-stu-id="42402-120">The eighth command creates a configuration value for Oozie, and then stores that values as a member of $OozieConfigValues.</span></span>

<span data-ttu-id="42402-121">Der neunte Befehl erstellt ein **AzureHDInsightMapReduceConfiguration** -Objekt und speichert es dann in der $MapredConfigValues-Variablen.</span><span class="sxs-lookup"><span data-stu-id="42402-121">The ninth command creates an **AzureHDInsightMapReduceConfiguration** object, and then stores it in the $MapredConfigValues variable.</span></span>
<span data-ttu-id="42402-122">Die nächsten beiden Befehle erstellen Konfigurationswerte für MapReduce und speichern diese Werte als Mitglieder von $MapredConfigValues.</span><span class="sxs-lookup"><span data-stu-id="42402-122">The next two commands create configuration values for MapReduce and store those values as members of $MapredConfigValues.</span></span>

<span data-ttu-id="42402-123">Der zwölfte Befehl verwendet das Cmdlet **New-AzureHDInsightClusterConfig** , um eine HDInsight-Cluster Konfiguration zu erstellen, und speichert Sie dann in der $config-Variablen.</span><span class="sxs-lookup"><span data-stu-id="42402-123">The twelfth command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>
<span data-ttu-id="42402-124">Der Befehl übergibt $config an das Cmdlet " **AzureHDInsightDefaultStorage** ", um die Standardspeichereinstellung und das Cmdlet " **Add-AzureHDInsightConfigValues** " zu aktualisieren, um die neuen Konfigurationswerte zur Cluster Konfiguration hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="42402-124">The command uses the pipeline operator to pass $Config to the **Set-AzureHDInsightDefaultStorage** cmdlet to update the default storage setting and to the **Add-AzureHDInsightConfigValues** cmdlet to add the new configuration values to the cluster configuration.</span></span>

<span data-ttu-id="42402-125">Der endgültige Befehl verwendet den Pipelineoperator, um $config an das Cmdlet **New-AzureHDInsightCluster** zu übergeben, um einen neuen HDInsight-Cluster mit den angepassten Einstellungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="42402-125">The final command uses the pipeline operator to pass $Config to the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster with the customized settings.</span></span>

## <span data-ttu-id="42402-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="42402-126">PARAMETERS</span></span>

### <span data-ttu-id="42402-127">-Config</span><span class="sxs-lookup"><span data-stu-id="42402-127">-Config</span></span>
<span data-ttu-id="42402-128">Gibt das Configuration-Objekt an, dem eine Hadoop-Konfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="42402-128">Specifies the configuration object to which to add a Hadoop configuration.</span></span>

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

### <span data-ttu-id="42402-129">-Core</span><span class="sxs-lookup"><span data-stu-id="42402-129">-Core</span></span>
<span data-ttu-id="42402-130">Gibt einen Satz von Hadoop-Konfigurationswerten für Core-site.xml an.</span><span class="sxs-lookup"><span data-stu-id="42402-130">Specifies a set of Hadoop configuration values for Core-site.xml.</span></span>

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

### <span data-ttu-id="42402-131">-HBAs</span><span class="sxs-lookup"><span data-stu-id="42402-131">-HBase</span></span>
<span data-ttu-id="42402-132">Gibt einen Satz von HBAs-Konfigurationswerten für Hbase-site.xml an.</span><span class="sxs-lookup"><span data-stu-id="42402-132">Specifies a set of HBase configuration values for Hbase-site.xml.</span></span>

```yaml
Type: AzureHDInsightHBaseConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42402-133">-HDFS</span><span class="sxs-lookup"><span data-stu-id="42402-133">-Hdfs</span></span>
<span data-ttu-id="42402-134">Gibt einen Satz von Hadoop-Konfigurationswerten für Hdfs-site.xml an.</span><span class="sxs-lookup"><span data-stu-id="42402-134">Specifies a set of Hadoop configuration values for Hdfs-site.xml.</span></span>

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

### <span data-ttu-id="42402-135">-Hive</span><span class="sxs-lookup"><span data-stu-id="42402-135">-Hive</span></span>
<span data-ttu-id="42402-136">Gibt ein Anpassungs Objekt für den Hadoop-hivedienst an, einschließlich einer Reihe von Hadoop-Konfigurationswerten für Hive-site.xml-und Hive-freigegebene Bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="42402-136">Specifies a customization object for Hadoop Hive service, including a set of Hadoop configuration values for Hive-site.xml and Hive shared libraries.</span></span>

```yaml
Type: AzureHDInsightHiveConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42402-137">-MapReduce</span><span class="sxs-lookup"><span data-stu-id="42402-137">-MapReduce</span></span>
<span data-ttu-id="42402-138">Gibt ein Anpassungs Objekt für MapReduce und den Kapazitätsplaner an.</span><span class="sxs-lookup"><span data-stu-id="42402-138">Specifies a customization object for MapReduce and the capacity scheduler.</span></span>

```yaml
Type: AzureHDInsightMapReduceConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42402-139">-Oozie</span><span class="sxs-lookup"><span data-stu-id="42402-139">-Oozie</span></span>
<span data-ttu-id="42402-140">Gibt ein Anpassungs Objekt für den Hadoop-Oozie-Dienst an, einschließlich einer Reihe von Hadoop-Konfigurationswerten für Oozie-site.xml.</span><span class="sxs-lookup"><span data-stu-id="42402-140">Specifies a customization object for Hadoop Oozie service, including a set of Hadoop configuration values for Oozie-site.xml.</span></span>

```yaml
Type: AzureHDInsightOozieConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42402-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="42402-141">-Profile</span></span>
<span data-ttu-id="42402-142">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="42402-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="42402-143">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="42402-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="42402-144">-Funken</span><span class="sxs-lookup"><span data-stu-id="42402-144">-Spark</span></span>
<span data-ttu-id="42402-145">Gibt ein Anpassungs Objekt für Apache Spark an.</span><span class="sxs-lookup"><span data-stu-id="42402-145">Specifies a customization object for Apache Spark.</span></span>

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

### <span data-ttu-id="42402-146">-Storm</span><span class="sxs-lookup"><span data-stu-id="42402-146">-Storm</span></span>
<span data-ttu-id="42402-147">Gibt ein Anpassungs Objekt für Apache Storm an.</span><span class="sxs-lookup"><span data-stu-id="42402-147">Specifies a customization object for Apache Storm.</span></span>

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

### <span data-ttu-id="42402-148">-Garn</span><span class="sxs-lookup"><span data-stu-id="42402-148">-Yarn</span></span>
<span data-ttu-id="42402-149">Gibt ein Anpassungs Objekt für Hadoop-Garn an und gibt einen Satz angepasster Garn Konfigurationswerte für Yarn-site.xml an.</span><span class="sxs-lookup"><span data-stu-id="42402-149">Specifies a customization object for Hadoop YARN, specifying a set of customized YARN configuration values for Yarn-site.xml.</span></span>

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

### <span data-ttu-id="42402-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42402-150">CommonParameters</span></span>
<span data-ttu-id="42402-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42402-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42402-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42402-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42402-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42402-153">INPUTS</span></span>

## <span data-ttu-id="42402-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42402-154">OUTPUTS</span></span>

## <span data-ttu-id="42402-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="42402-155">NOTES</span></span>

## <span data-ttu-id="42402-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42402-156">RELATED LINKS</span></span>

[<span data-ttu-id="42402-157">Neu – AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="42402-157">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="42402-158">Neu – AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="42402-158">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="42402-159">Satz-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="42402-159">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
