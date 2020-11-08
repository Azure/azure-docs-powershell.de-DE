---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 1B6AC121-1AA0-4D28-B1EA-C96147FDD168
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02435c28ca17666a3b19389fde039353f3d779a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005922"
---
# <span data-ttu-id="e5697-101">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="e5697-101">Add-AzureHDInsightStorage</span></span>

## <span data-ttu-id="e5697-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5697-102">SYNOPSIS</span></span>
<span data-ttu-id="e5697-103">Fügt einen BLOB-Speicherkonto Eintrag zu einer HDInsight-Konfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="e5697-103">Adds a blob storage account entry to an HDInsight configuration.</span></span>

## <span data-ttu-id="e5697-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5697-104">SYNTAX</span></span>

```
Add-AzureHDInsightStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e5697-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5697-105">DESCRIPTION</span></span>
<span data-ttu-id="e5697-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="e5697-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="e5697-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="e5697-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="e5697-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e5697-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="e5697-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="e5697-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="e5697-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="e5697-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="e5697-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e5697-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="e5697-112">Mit dem Cmdlet **Add-AzureHDInsightStorage** wird eine Azure HDInsight-Konfiguration ein BLOB-Speicherkonto Eintrag hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e5697-112">The **Add-AzureHDInsightStorage** cmdlet adds a blob storage account entry to an Azure HDInsight configuration.</span></span>

## <span data-ttu-id="e5697-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5697-113">EXAMPLES</span></span>

### <span data-ttu-id="e5697-114">Beispiel 1: Hinzufügen eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="e5697-114">Example 1: Add a storage account</span></span>
```
PS C:\>$StoreConfig = Add-AzureHDInsightStorage -Config $Config -StorageAccountName "MyStorage" -StorageAccountKey "Key"
```

<span data-ttu-id="e5697-115">Dieser Befehl fügt dem in $config gespeicherten Konfigurationsobjekt ein Speicherkonto mit dem Namen mystorage hinzu und speichert dann die Konfiguration in der $StoreConfig Variablen.</span><span class="sxs-lookup"><span data-stu-id="e5697-115">This command adds a storage account named MyStorage to the configuration object stored in $Config, and then stores the configuration in the $StoreConfig variable.</span></span>

### <span data-ttu-id="e5697-116">Beispiel 2: Konfigurieren mehrerer Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="e5697-116">Example 2: Configure multiple storage accounts</span></span>
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="e5697-117">Der erste Befehl verwendet das Cmdlet " **Get-AzureSubscription** ", um die aktuelle Abonnement-ID abzurufen, und speichert Sie dann in der $SubId-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e5697-117">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="e5697-118">Der zweite und der dritte Befehl verwenden das Cmdlet " **Get-AzureStorageKey** ", um die primären Speicherschlüssel für MyBlobStorage und MySecondBlobStorage abzurufen, und speichern Sie dann die Schlüssel in den Variablen $Key 1 und $Key 2.</span><span class="sxs-lookup"><span data-stu-id="e5697-118">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="e5697-119">Der vierte, fünfte und sechste Befehl erhält die Anmeldeinformationen für das aktuelle Abonnement sowie für Oozie und Hive und speichert die Anmeldeinformationen dann in Variablen.</span><span class="sxs-lookup"><span data-stu-id="e5697-119">The fourth, fifth, and sixth commands get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="e5697-120">Der endgültige Befehl führt eine Abfolge von Vorgängen mithilfe dieser Cmdlets aus:</span><span class="sxs-lookup"><span data-stu-id="e5697-120">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="e5697-121">**New-AzureHDInsightClusterConfig** zum Erstellen einer HDInsight-Cluster Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e5697-121">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration</span></span>
- <span data-ttu-id="e5697-122">**Festlegen von AzureHDInsightDefaultStorage** zum Festlegen des Standardspeicher Kontos für die Konfiguration auf MyBlobStorage.BLOB.Core.Windows.net</span><span class="sxs-lookup"><span data-stu-id="e5697-122">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net</span></span>
- <span data-ttu-id="e5697-123">**Add-AzureHDInsightStorage** zum Hinzufügen eines zweiten speicherkontos mit dem Namen MySecondBlobStorage.BLOB.Core.Windows.net zur Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e5697-123">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration</span></span>
- <span data-ttu-id="e5697-124">**Add-AzureHDInsightStorage** , um der Konfiguration einen metastore für Oozie und einen metastore für Hive hinzuzufügen</span><span class="sxs-lookup"><span data-stu-id="e5697-124">**Add-AzureHDInsightStorage** to add a metastore for Oozie and a metastore for Hive to the configuration</span></span>
- <span data-ttu-id="e5697-125">**New-AzureHDInsightCluster** zum Erstellen eines HDInsight-Clusters mit der neuen Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e5697-125">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration</span></span>

## <span data-ttu-id="e5697-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5697-126">PARAMETERS</span></span>

### <span data-ttu-id="e5697-127">-Config</span><span class="sxs-lookup"><span data-stu-id="e5697-127">-Config</span></span>
<span data-ttu-id="e5697-128">Gibt ein Configuration-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e5697-128">Specifies a configuration object.</span></span>
<span data-ttu-id="e5697-129">Dieses Cmdlet fügt dem Objekt, das dieser Parameter angibt, Speicherkonto Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="e5697-129">This cmdlet adds storage account information to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="e5697-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="e5697-130">-Profile</span></span>
<span data-ttu-id="e5697-131">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e5697-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e5697-132">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e5697-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e5697-133">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e5697-133">-StorageAccountKey</span></span>
<span data-ttu-id="e5697-134">Gibt den speicherkontoschlüssel an, der für den Zugriff auf ein Speicherkonto verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e5697-134">Specifies the storage account key that is used to access a storage account.</span></span>

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

### <span data-ttu-id="e5697-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e5697-135">-StorageAccountName</span></span>
<span data-ttu-id="e5697-136">Gibt den Namen des Azure-speicherkontos an, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5697-136">Specifies the name of the Azure storage account to add.</span></span>

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

### <span data-ttu-id="e5697-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5697-137">CommonParameters</span></span>
<span data-ttu-id="e5697-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5697-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5697-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5697-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5697-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5697-140">INPUTS</span></span>

## <span data-ttu-id="e5697-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5697-141">OUTPUTS</span></span>

## <span data-ttu-id="e5697-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5697-142">NOTES</span></span>

## <span data-ttu-id="e5697-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5697-143">RELATED LINKS</span></span>

[<span data-ttu-id="e5697-144">Neu – AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e5697-144">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="e5697-145">Neu – AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e5697-145">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="e5697-146">Satz-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="e5697-146">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


