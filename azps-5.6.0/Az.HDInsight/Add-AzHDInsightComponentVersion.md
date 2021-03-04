---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightcomponentversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
ms.openlocfilehash: 9cd0a5def5a05782cce067a97fa85029b8e52ca3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938120"
---
# <span data-ttu-id="32d38-101">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="32d38-101">Add-AzHDInsightComponentVersion</span></span>

## <span data-ttu-id="32d38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32d38-102">SYNOPSIS</span></span>
<span data-ttu-id="32d38-103">Fügt einem Clusterkonfigurationsobjekt eine Version für einen Dienst hinzu, der in einem Cluster ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32d38-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

## <span data-ttu-id="32d38-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32d38-104">SYNTAX</span></span>

```
Add-AzHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32d38-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32d38-105">DESCRIPTION</span></span>
<span data-ttu-id="32d38-106">Das Add-AzHDInsightComponentVersion-Cmdlet fügt dem Azure HDIn New-AzHDInsightClusterConfig sight-Konfigurationsobjekt, das vom cmdlet erstellt wurde, eine Version für einen Dienst hinzu, der in einem Cluster ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32d38-106">The Add-AzHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="32d38-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="32d38-107">EXAMPLES</span></span>

### <span data-ttu-id="32d38-108">Beispiel 1: Hinzufügen einer Version für Spark zum Clusterkonfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="32d38-108">Example 1: Add a version for Spark to the cluster configuration object.</span></span>
```
PS C:\> # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer `
                -SshCredential $sshCredentials `
                -Version "3.5"
```

<span data-ttu-id="32d38-109">Mit diesem Befehl wird die Version von Spark zum HDInsight-Cluster mit dem Namen "your-spark-001" addiert.</span><span class="sxs-lookup"><span data-stu-id="32d38-109">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="32d38-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="32d38-110">PARAMETERS</span></span>

### <span data-ttu-id="32d38-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="32d38-111">-ComponentName</span></span>
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

### <span data-ttu-id="32d38-112">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="32d38-112">-ComponentVersion</span></span>
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

### <span data-ttu-id="32d38-113">-Config</span><span class="sxs-lookup"><span data-stu-id="32d38-113">-Config</span></span>
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

### <span data-ttu-id="32d38-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32d38-114">-DefaultProfile</span></span>
<span data-ttu-id="32d38-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="32d38-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32d38-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="32d38-116">-Confirm</span></span>
<span data-ttu-id="32d38-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="32d38-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32d38-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32d38-118">-WhatIf</span></span>
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

### <span data-ttu-id="32d38-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d38-119">CommonParameters</span></span>
<span data-ttu-id="32d38-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32d38-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d38-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32d38-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d38-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="32d38-122">INPUTS</span></span>

### <span data-ttu-id="32d38-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="32d38-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="32d38-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="32d38-124">OUTPUTS</span></span>

### <span data-ttu-id="32d38-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="32d38-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="32d38-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="32d38-126">NOTES</span></span>

## <span data-ttu-id="32d38-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="32d38-127">RELATED LINKS</span></span>
