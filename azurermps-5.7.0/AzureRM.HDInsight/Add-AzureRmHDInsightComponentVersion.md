---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightcomponentversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightComponentVersion.md
ms.openlocfilehash: ed0d91ff7b5013a586e983844eb74b0c9d6917ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482938"
---
# <span data-ttu-id="207f0-101">Add-AzureRmHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="207f0-101">Add-AzureRmHDInsightComponentVersion</span></span>

## <span data-ttu-id="207f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="207f0-102">SYNOPSIS</span></span>
<span data-ttu-id="207f0-103">Fügt eine Version für einen in einem Cluster ausgeführten Dienst zu einem Cluster Konfigurationsobjekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="207f0-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="207f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="207f0-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="207f0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="207f0-105">DESCRIPTION</span></span>
<span data-ttu-id="207f0-106">Das Add-AzureRmHDInsightComponentVersion-Cmdlet fügt dem Azure HDInsight-Konfigurationsobjekt, das vom New-AzureRmHDInsightClusterConfig-Cmdlet erstellt wird, eine Version für einen in einem Cluster ausgeführten Dienst hinzu.</span><span class="sxs-lookup"><span data-stu-id="207f0-106">The Add-AzureRmHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="207f0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="207f0-107">EXAMPLES</span></span>

### <span data-ttu-id="207f0-108">--------------------------Beispiel 1: Hinzufügen einer Version für Spark zum Cluster-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="207f0-108">--------------------------  Example 1: Add a version for Spark to the cluster configuration object.</span></span>  --------------------------
```
PS C:\> # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzureStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container001"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-spark-001"
        $clusterCreds = Get-Credential
        $sshClusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightComponentVersion `
                -ComponentName "Spark" `
                -ComponentVersion "2.0" `
            | New-AzureRmHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer `
                -SshCredential $sshCredentials `
                -Version "3.5"
```

<span data-ttu-id="207f0-109">Dieser Befehl fügt die Spark-Version zum HDInsight-Cluster mit dem Namen "Your-Spark-001" hinzu.</span><span class="sxs-lookup"><span data-stu-id="207f0-109">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="207f0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="207f0-110">PARAMETERS</span></span>

### <span data-ttu-id="207f0-111">-Komponentenname</span><span class="sxs-lookup"><span data-stu-id="207f0-111">-ComponentName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="207f0-112">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="207f0-112">-ComponentVersion</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="207f0-113">-Config</span><span class="sxs-lookup"><span data-stu-id="207f0-113">-Config</span></span>
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

### <span data-ttu-id="207f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="207f0-114">-DefaultProfile</span></span>
<span data-ttu-id="207f0-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="207f0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="207f0-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="207f0-116">-Confirm</span></span>
<span data-ttu-id="207f0-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="207f0-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="207f0-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="207f0-118">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="207f0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="207f0-119">CommonParameters</span></span>
<span data-ttu-id="207f0-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="207f0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="207f0-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="207f0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="207f0-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="207f0-122">INPUTS</span></span>

### <span data-ttu-id="207f0-123">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="207f0-123">AzureHDInsightConfig</span></span>
<span data-ttu-id="207f0-124">Der Parameter "config" akzeptiert den Wert vom Typ "AzureHDInsightConfig" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="207f0-124">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="207f0-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="207f0-125">OUTPUTS</span></span>

### <span data-ttu-id="207f0-126">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="207f0-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="207f0-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="207f0-127">NOTES</span></span>

## <span data-ttu-id="207f0-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="207f0-128">RELATED LINKS</span></span>

