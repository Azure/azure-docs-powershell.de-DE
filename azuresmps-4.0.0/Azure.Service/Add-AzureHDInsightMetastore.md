---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EB196CF5-3E2C-4F38-A983-3365A379672A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 637fc6f65c7168db9ba7e45cea7268208b334c99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005929"
---
# <span data-ttu-id="4bd3f-101">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="4bd3f-101">Add-AzureHDInsightMetastore</span></span>

## <span data-ttu-id="4bd3f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4bd3f-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd3f-103">Fügt ein SQL Server-Daten Bank Konto zu einer HDInsight-Cluster Konfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-103">Adds a SQL Server database account to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="4bd3f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bd3f-104">SYNTAX</span></span>

```
Add-AzureHDInsightMetastore -Config <AzureHDInsightConfig> -Credential <PSCredential> -DatabaseName <String>
 -MetastoreType <AzureHDInsightMetastoreType> -SqlAzureServerName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4bd3f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bd3f-105">DESCRIPTION</span></span>
<span data-ttu-id="4bd3f-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="4bd3f-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="4bd3f-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="4bd3f-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="4bd3f-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="4bd3f-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="4bd3f-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="4bd3f-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4bd3f-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="4bd3f-112">Das Cmdlet **Add-AzureHDInsightMetastore** fügt eine Microsoft SQL Server-Datenbank zu einer Azure HDInsight-Konfiguration hinzu, die vom Cmdlet **New-AzureHDInsightClusterConfig** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-112">The **Add-AzureHDInsightMetastore** cmdlet adds a Microsoft SQL Server database to an Azure HDInsight configuration that is created by the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>
<span data-ttu-id="4bd3f-113">Die Datenbank wird zum Speichern von Metadaten für Hive-oder Oozie oder beides verwendet.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-113">The database is used to store metadata for Hive or Oozie, or both.</span></span>

## <span data-ttu-id="4bd3f-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4bd3f-114">EXAMPLES</span></span>

### <span data-ttu-id="4bd3f-115">Beispiel 1: Hinzufügen eines metastores</span><span class="sxs-lookup"><span data-stu-id="4bd3f-115">Example 1: Add a metastore</span></span>
```
PS C:\>$Metaconfig = Add-AzureHDInsightMetastore -Config $Config -SqlAzureServerName "ContosoSQLServer" -DatabaseName "DBname" -Credential (Get-Credential) -MetastoreType HiveMetaStore
```

<span data-ttu-id="4bd3f-116">Dieser Befehl fügt eine SQL Server-Datenbank mit dem Namen ContosoSQLServer hinzu, die als Hive-metastore für einen HDInsight-Cluster fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-116">This command adds a SQL Server database named ContosoSQLServer to serve as a Hive metastore for an HDInsight cluster.</span></span>

### <span data-ttu-id="4bd3f-117">Beispiel 2: Konfigurieren des Speichers und Hinzufügen von metastores</span><span class="sxs-lookup"><span data-stu-id="4bd3f-117">Example 2: Configure storage and add metastores</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer"
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="4bd3f-118">Der erste Befehl verwendet das Cmdlet " **Get-AzureSubscription** ", um die aktuelle Abonnement-ID abzurufen, und speichert Sie dann in der $SubId-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="4bd3f-119">Der zweite und der dritte Befehl verwenden das Cmdlet " **Get-AzureStorageKey** ", um die primären Speicherschlüssel für MyBlobStorage und MySecondBlobStorage abzurufen, und speichern Sie dann die Schlüssel in den Variablen $Key 1 und $Key 2.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="4bd3f-120">Der vierte, fünfte und sechste Befehl verwenden Sie das Cmdlet **Get-Credential** , um Anmeldeinformationen für das aktuelle Abonnement sowie für Oozie und Hive abzurufen, und speichern Sie dann die Anmeldeinformationen in Variablen.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="4bd3f-121">Der endgültige Befehl führt eine Abfolge von Vorgängen mithilfe dieser Cmdlets aus:</span><span class="sxs-lookup"><span data-stu-id="4bd3f-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="4bd3f-122">**New-AzureHDInsightClusterConfig** zum Erstellen einer HDInsight-Cluster Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="4bd3f-123">**Legen Sie AzureHDInsightDefaultStorage** , um das Standardspeicher Konto für die Konfiguration auf MyBlobStorage.BLOB.Core.Windows.net zu legen.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="4bd3f-124">**Add-AzureHDInsightStorage** , um der Konfiguration ein zweites Speicherkonto mit dem Namen MySecondBlobStorage.BLOB.Core.Windows.net hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="4bd3f-125">**Add-AzureHDInsightMetastore** , um der Konfiguration einen metastore für Oozie und einen metastore für Hive hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="4bd3f-126">**New-AzureHDInsightCluster** zum Erstellen eines HDInsight-Clusters mit der neuen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="4bd3f-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bd3f-127">PARAMETERS</span></span>

### <span data-ttu-id="4bd3f-128">-Config</span><span class="sxs-lookup"><span data-stu-id="4bd3f-128">-Config</span></span>
<span data-ttu-id="4bd3f-129">Gibt ein Configuration-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-129">Specifies a configuration object.</span></span>
<span data-ttu-id="4bd3f-130">Dieses Cmdlet fügt dem Configuration-Objekt metastore-Informationen hinzu, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-130">This cmdlet adds metastore information to the configuration object that this parameter specifies.</span></span>

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

### <span data-ttu-id="4bd3f-131">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="4bd3f-131">-Credential</span></span>
<span data-ttu-id="4bd3f-132">Gibt die Anmeldeinformationen an, die für den Zugriff auf eine SQL Server-Datenbank verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-132">Specifies the credentials that are used to access a SQL Server database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd3f-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4bd3f-133">-DatabaseName</span></span>
<span data-ttu-id="4bd3f-134">Gibt den Namen der Datenbank an, in der die Hive-oder Oozie-Metadaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-134">Specifies the name of the database to store Hive or Oozie metadata.</span></span>

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

### <span data-ttu-id="4bd3f-135">-Metastoretype</span><span class="sxs-lookup"><span data-stu-id="4bd3f-135">-MetastoreType</span></span>
<span data-ttu-id="4bd3f-136">Gibt den metastore-Typ an.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-136">Specifies the metastore type.</span></span>
<span data-ttu-id="4bd3f-137">Die zulässigen Werte für diesen Parameter sind: HiveMetaStore oder OozieMetaStore.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-137">The acceptable values for this parameter are: HiveMetaStore or OozieMetaStore.</span></span>

```yaml
Type: AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd3f-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="4bd3f-138">-Profile</span></span>
<span data-ttu-id="4bd3f-139">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4bd3f-140">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4bd3f-141">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="4bd3f-141">-SqlAzureServerName</span></span>
<span data-ttu-id="4bd3f-142">Gibt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des SQL Server an, der die Datenbank zum Speichern von Metadaten enthält.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-142">Specifies the fully qualified domain name (FQDN) of the SQL Server that contains the database to store metadata.</span></span>

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

### <span data-ttu-id="4bd3f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd3f-143">CommonParameters</span></span>
<span data-ttu-id="4bd3f-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bd3f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd3f-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd3f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd3f-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4bd3f-146">INPUTS</span></span>

## <span data-ttu-id="4bd3f-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4bd3f-147">OUTPUTS</span></span>

## <span data-ttu-id="4bd3f-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="4bd3f-148">NOTES</span></span>

## <span data-ttu-id="4bd3f-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4bd3f-149">RELATED LINKS</span></span>

[<span data-ttu-id="4bd3f-150">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="4bd3f-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="4bd3f-151">Neu – AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4bd3f-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="4bd3f-152">Neu – AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4bd3f-152">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="4bd3f-153">Satz-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="4bd3f-153">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
