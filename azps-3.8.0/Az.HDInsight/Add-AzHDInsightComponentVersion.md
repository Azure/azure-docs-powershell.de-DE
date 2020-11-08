---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightcomponentversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
ms.openlocfilehash: 868ab69420cac66e911d772f4362e70ec2c03a1d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003002"
---
# <span data-ttu-id="d195a-101">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="d195a-101">Add-AzHDInsightComponentVersion</span></span>

## <span data-ttu-id="d195a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d195a-102">SYNOPSIS</span></span>
<span data-ttu-id="d195a-103">Fügt eine Version für einen in einem Cluster ausgeführten Dienst zu einem Cluster Konfigurationsobjekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="d195a-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

## <span data-ttu-id="d195a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d195a-104">SYNTAX</span></span>

```
Add-AzHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d195a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d195a-105">DESCRIPTION</span></span>
<span data-ttu-id="d195a-106">Das Add-AzHDInsightComponentVersion-Cmdlet fügt dem Azure HDInsight-Konfigurationsobjekt, das vom New-AzHDInsightClusterConfig-Cmdlet erstellt wird, eine Version für einen in einem Cluster ausgeführten Dienst hinzu.</span><span class="sxs-lookup"><span data-stu-id="d195a-106">The Add-AzHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="d195a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d195a-107">EXAMPLES</span></span>

### <span data-ttu-id="d195a-108">Beispiel 1: Hinzufügen einer Version für Spark zum Cluster-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="d195a-108">Example 1: Add a version for Spark to the cluster configuration object.</span></span>
```
PS C:\> # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
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
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightClusterConfig `
            | Add-AzHDInsightComponentVersion `
                -ComponentName "Spark" `
                -ComponentVersion "2.0" `
            | New-AzHDInsightCluster `
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

<span data-ttu-id="d195a-109">Dieser Befehl fügt die Spark-Version zum HDInsight-Cluster mit dem Namen "Your-Spark-001" hinzu.</span><span class="sxs-lookup"><span data-stu-id="d195a-109">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="d195a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d195a-110">PARAMETERS</span></span>

### <span data-ttu-id="d195a-111">-Komponentenname</span><span class="sxs-lookup"><span data-stu-id="d195a-111">-ComponentName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d195a-112">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="d195a-112">-ComponentVersion</span></span>
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

### <span data-ttu-id="d195a-113">-Config</span><span class="sxs-lookup"><span data-stu-id="d195a-113">-Config</span></span>
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

### <span data-ttu-id="d195a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d195a-114">-DefaultProfile</span></span>
<span data-ttu-id="d195a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d195a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d195a-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d195a-116">-Confirm</span></span>
<span data-ttu-id="d195a-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d195a-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d195a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d195a-118">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d195a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d195a-119">CommonParameters</span></span>
<span data-ttu-id="d195a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d195a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d195a-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d195a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d195a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d195a-122">INPUTS</span></span>

### <span data-ttu-id="d195a-123">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d195a-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="d195a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d195a-124">OUTPUTS</span></span>

### <span data-ttu-id="d195a-125">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d195a-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="d195a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="d195a-126">NOTES</span></span>

## <span data-ttu-id="d195a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d195a-127">RELATED LINKS</span></span>
