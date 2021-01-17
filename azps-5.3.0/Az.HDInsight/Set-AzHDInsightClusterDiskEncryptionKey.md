---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: b3421fa4382912d11a3e3a28b81acffb7be123a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467739"
---
# <span data-ttu-id="b0f82-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b0f82-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="b0f82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0f82-102">SYNOPSIS</span></span>
<span data-ttu-id="b0f82-103">Dreht den Datenträgerverschlüsselungsschlüssel des angegebenen HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="b0f82-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="b0f82-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0f82-104">SYNTAX</span></span>

### <span data-ttu-id="b0f82-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b0f82-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0f82-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0f82-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0f82-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0f82-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0f82-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0f82-108">DESCRIPTION</span></span>
<span data-ttu-id="b0f82-109">Drehen Sie den Datenträgerverschlüsselungsschlüssel des angegebenen HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="b0f82-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="b0f82-110">Für diesen Vorgang muss der Cluster Zugriff auf den aktuellen und den vorgesehenen neuen Schlüssel haben. Andernfalls kann der Drehschlüsselvorgang fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="b0f82-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="b0f82-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b0f82-111">EXAMPLES</span></span>

### <span data-ttu-id="b0f82-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b0f82-112">Example 1</span></span>
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

### <span data-ttu-id="b0f82-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b0f82-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="b0f82-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0f82-114">PARAMETERS</span></span>

### <span data-ttu-id="b0f82-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0f82-115">-DefaultProfile</span></span>
<span data-ttu-id="b0f82-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0f82-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0f82-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="b0f82-117">-EncryptionKeyName</span></span>
<span data-ttu-id="b0f82-118">Ruft den Namen des Verschlüsselungsschlüssels ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="b0f82-118">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="b0f82-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="b0f82-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="b0f82-120">Ruft die Verschlüsselungsschlüsselversion ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="b0f82-120">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="b0f82-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="b0f82-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="b0f82-122">Ruft den Verschlüsselungstresor-URI ab oder legt den URI fest.</span><span class="sxs-lookup"><span data-stu-id="b0f82-122">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="b0f82-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0f82-123">-InputObject</span></span>
<span data-ttu-id="b0f82-124">Ruft das Eingabeobjekt ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="b0f82-124">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="b0f82-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b0f82-125">-Name</span></span>
<span data-ttu-id="b0f82-126">Ruft den Namen des Cluster ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="b0f82-126">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="b0f82-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0f82-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0f82-128">Ruft den Namen der Ressourcengruppe ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="b0f82-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="b0f82-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0f82-129">-ResourceId</span></span>
<span data-ttu-id="b0f82-130">Ruft die Ressourcen-ID ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="b0f82-130">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="b0f82-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0f82-131">-Confirm</span></span>
<span data-ttu-id="b0f82-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b0f82-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0f82-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b0f82-133">-WhatIf</span></span>
<span data-ttu-id="b0f82-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b0f82-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0f82-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0f82-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0f82-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0f82-136">CommonParameters</span></span>
<span data-ttu-id="b0f82-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0f82-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0f82-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0f82-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0f82-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b0f82-139">INPUTS</span></span>

### <span data-ttu-id="b0f82-140">Keine</span><span class="sxs-lookup"><span data-stu-id="b0f82-140">None</span></span>

## <span data-ttu-id="b0f82-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b0f82-141">OUTPUTS</span></span>

### <span data-ttu-id="b0f82-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="b0f82-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="b0f82-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b0f82-143">NOTES</span></span>

## <span data-ttu-id="b0f82-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b0f82-144">RELATED LINKS</span></span>

[<span data-ttu-id="b0f82-145">Vom Kunden verwaltete Datenträgerverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="b0f82-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/en-us/azure/hdinsight/disk-encryption)
