---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: addf0e06a3df625bde5b46cc8089fc89ced832dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934952"
---
# <span data-ttu-id="6fba5-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6fba5-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="6fba5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fba5-102">SYNOPSIS</span></span>
<span data-ttu-id="6fba5-103">Dreht den Datenträgerverschlüsselungsschlüssel des angegebenen HDInsight-Clusters.</span><span class="sxs-lookup"><span data-stu-id="6fba5-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="6fba5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fba5-104">SYNTAX</span></span>

### <span data-ttu-id="6fba5-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6fba5-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fba5-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fba5-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fba5-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fba5-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fba5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fba5-108">DESCRIPTION</span></span>
<span data-ttu-id="6fba5-109">Drehen Sie den Datenträgerverschlüsselungsschlüssel des angegebenen HDInsight-Clusters.</span><span class="sxs-lookup"><span data-stu-id="6fba5-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="6fba5-110">Für diesen Vorgang muss der Cluster sowohl auf den aktuellen schlüssel als auch auf den vorgesehenen neuen Schlüssel zugreifen können, da andernfalls der Drehschlüsselvorgang fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="6fba5-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="6fba5-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6fba5-111">EXAMPLES</span></span>

### <span data-ttu-id="6fba5-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6fba5-112">Example 1</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"

Set-AzHDInsightClusterDiskEncryptionKey `
        -ResourceGroupName $clusterResourceGroupName `
        -ClusterName $clusterName `
        -EncryptionKeyName new-key `
        -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
        -EncryptionKeyVersion 00000000000000000000000000000000
```

### <span data-ttu-id="6fba5-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6fba5-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="6fba5-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6fba5-114">PARAMETERS</span></span>

### <span data-ttu-id="6fba5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fba5-115">-DefaultProfile</span></span>
<span data-ttu-id="6fba5-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6fba5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fba5-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="6fba5-117">-EncryptionKeyName</span></span>
<span data-ttu-id="6fba5-118">Ruft den Namen des Verschlüsselungsschlüssels ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="6fba5-118">Gets or sets the encryption key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fba5-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="6fba5-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="6fba5-120">Ruft die Verschlüsselungsschlüsselversion ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="6fba5-120">Gets or sets the encryption key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fba5-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="6fba5-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="6fba5-122">Ruft den Verschlüsselungstresor-URI ab oder legt den -URI fest.</span><span class="sxs-lookup"><span data-stu-id="6fba5-122">Gets or sets the encryption vault uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fba5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fba5-123">-InputObject</span></span>
<span data-ttu-id="6fba5-124">Ruft das Eingabeobjekt ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="6fba5-124">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fba5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6fba5-125">-Name</span></span>
<span data-ttu-id="6fba5-126">Ruft den Namen des Clusters ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="6fba5-126">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fba5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fba5-127">-ResourceGroupName</span></span>
<span data-ttu-id="6fba5-128">Ruft den Namen der Ressourcengruppe ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="6fba5-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fba5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fba5-129">-ResourceId</span></span>
<span data-ttu-id="6fba5-130">Ruft die Ressourcen-ID ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="6fba5-130">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fba5-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6fba5-131">-Confirm</span></span>
<span data-ttu-id="6fba5-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6fba5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fba5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fba5-133">-WhatIf</span></span>
<span data-ttu-id="6fba5-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6fba5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fba5-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6fba5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fba5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fba5-136">CommonParameters</span></span>
<span data-ttu-id="6fba5-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fba5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fba5-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fba5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fba5-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6fba5-139">INPUTS</span></span>

### <span data-ttu-id="6fba5-140">Keine</span><span class="sxs-lookup"><span data-stu-id="6fba5-140">None</span></span>

## <span data-ttu-id="6fba5-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6fba5-141">OUTPUTS</span></span>

### <span data-ttu-id="6fba5-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="6fba5-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="6fba5-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6fba5-143">NOTES</span></span>

## <span data-ttu-id="6fba5-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6fba5-144">RELATED LINKS</span></span>

[<span data-ttu-id="6fba5-145">Vom Kunden verwaltete Schlüsseldatenträgerverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="6fba5-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/azure/hdinsight/disk-encryption)
