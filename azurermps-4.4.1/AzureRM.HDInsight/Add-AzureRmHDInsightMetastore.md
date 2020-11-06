---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightMetastore.md
ms.openlocfilehash: f21108e949ff1d6787488f9f4b6c062d5954a7e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504170"
---
# <span data-ttu-id="55283-101">Add-AzureRmHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="55283-101">Add-AzureRmHDInsightMetastore</span></span>

## <span data-ttu-id="55283-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="55283-102">SYNOPSIS</span></span>
<span data-ttu-id="55283-103">Fügt eine SQL-Datenbank hinzu, die als Hive-oder Oozie-metastore für ein Cluster Konfigurationsobjekt fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="55283-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55283-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="55283-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55283-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55283-105">DESCRIPTION</span></span>
<span data-ttu-id="55283-106">Das Cmdlet **Add-AzureRmHDInsightMetastore** fügt dem HDInsight-Konfigurationsobjekt, das vom New-AzureRmHDInsightClusterConfig-Cmdlet erstellt wird, einen Hive-oder Oozie-metastore hinzu.</span><span class="sxs-lookup"><span data-stu-id="55283-106">The **Add-AzureRmHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="55283-107">Bei einem metastore handelt es sich um eine SQL-Datenbank, die zum Speichern von Metadaten für Hive, Oozie oder beides verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="55283-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="55283-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55283-108">EXAMPLES</span></span>

### <span data-ttu-id="55283-109">Beispiel 1: Hinzufügen eines SQL-Daten Bank metaspeichers zum Cluster-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="55283-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
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

# Hive metastore info
PS C:\> $hiveSqlServer = "your-sqlserver-001"
PS C:\> $hiveDb = "your-sqldb-001"
PS C:\> $hiveCreds = Get-Credential

# Oozie metastore info
PS C:\> $oozieSqlServer = "your-sqlserver-001"
PS C:\> $oozieDb = "your-sqldb-002"
PS C:\> $oozieCreds = Get-Credential

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig  `
            | Add-AzureRmHDInsightMetastore `
                -SqlAzureServerName "$oozieSqlServer.database.contoso.net" `
                -DatabaseName $oozieDb `
                -Credential $oozieCreds `
                -MetastoreType OozieMetastore `
            | Add-AzureRmHDInsightMetastore `
                -SqlAzureServerName "$hiveSqlServer.database.contoso.net" `
                -DatabaseName $hiveDb `
                -Credential $hiveCreds `
                -MetastoreType HiveMetastore `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="55283-110">Dieser Befehl fügt dem Cluster mit dem Namen your-Hadoop-001 einen SQL-Datenbank-metastore hinzu.</span><span class="sxs-lookup"><span data-stu-id="55283-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="55283-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="55283-111">PARAMETERS</span></span>

### <span data-ttu-id="55283-112">-Config</span><span class="sxs-lookup"><span data-stu-id="55283-112">-Config</span></span>
<span data-ttu-id="55283-113">Gibt das HDInsight-Cluster Konfigurationsobjekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="55283-113">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="55283-114">Dieses Objekt wird vom Cmdlet **New-AzureRmHDInsightClusterConfig** erstellt.</span><span class="sxs-lookup"><span data-stu-id="55283-114">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="55283-115">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="55283-115">-Credential</span></span>
<span data-ttu-id="55283-116">Gibt die für die AzureSQL-Server Datenbank zu verwendenden Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="55283-116">Specifies the credentials to use for the AzureSQL Server database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55283-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="55283-117">-DatabaseName</span></span>
<span data-ttu-id="55283-118">Gibt die Datenbank auf der AzureSQL-Server Instanz an, die für diesen metastore verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="55283-118">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55283-119">-Metastoretype</span><span class="sxs-lookup"><span data-stu-id="55283-119">-MetastoreType</span></span>
<span data-ttu-id="55283-120">Gibt den Typ des metastores an.</span><span class="sxs-lookup"><span data-stu-id="55283-120">Specifies the type of metastore.</span></span>
<span data-ttu-id="55283-121">Mögliche Werte sind HiveMetastore oder OozieMetastore.</span><span class="sxs-lookup"><span data-stu-id="55283-121">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases: 
Accepted values: HiveMetastore, OozieMetastore

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55283-122">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="55283-122">-SqlAzureServerName</span></span>
<span data-ttu-id="55283-123">Gibt die AzureSQL-Server Instanz an, die für diesen metastore verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="55283-123">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55283-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55283-124">-DefaultProfile</span></span>
<span data-ttu-id="55283-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="55283-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55283-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55283-126">CommonParameters</span></span>
<span data-ttu-id="55283-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55283-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55283-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55283-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55283-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="55283-129">INPUTS</span></span>

### <span data-ttu-id="55283-130">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="55283-130">AzureHDInsightConfig</span></span>
<span data-ttu-id="55283-131">Der Parameter "config" akzeptiert den Wert vom Typ "AzureHDInsightConfig" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="55283-131">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="55283-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="55283-132">OUTPUTS</span></span>

### <span data-ttu-id="55283-133">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="55283-133">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="55283-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="55283-134">NOTES</span></span>

## <span data-ttu-id="55283-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="55283-135">RELATED LINKS</span></span>

[<span data-ttu-id="55283-136">Neu – AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="55283-136">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


