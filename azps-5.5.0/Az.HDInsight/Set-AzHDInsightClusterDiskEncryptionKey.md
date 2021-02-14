---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: b3421fa4382912d11a3e3a28b81acffb7be123a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167425"
---
# <span data-ttu-id="787b7-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="787b7-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="787b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="787b7-102">SYNOPSIS</span></span>
<span data-ttu-id="787b7-103">Dreht den Datenträgerverschlüsselungsschlüssel des angegebenen HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="787b7-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="787b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="787b7-104">SYNTAX</span></span>

### <span data-ttu-id="787b7-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="787b7-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="787b7-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="787b7-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="787b7-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="787b7-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="787b7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="787b7-108">DESCRIPTION</span></span>
<span data-ttu-id="787b7-109">Drehen Sie den Datenträgerverschlüsselungsschlüssel des angegebenen HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="787b7-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="787b7-110">Für diesen Vorgang muss der Cluster Zugriff auf den aktuellen und den vorgesehenen neuen Schlüssel haben, andernfalls kann der Drehschlüsselvorgang fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="787b7-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="787b7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="787b7-111">EXAMPLES</span></span>

### <span data-ttu-id="787b7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="787b7-112">Example 1</span></span>
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

### <span data-ttu-id="787b7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="787b7-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="787b7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="787b7-114">PARAMETERS</span></span>

### <span data-ttu-id="787b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="787b7-115">-DefaultProfile</span></span>
<span data-ttu-id="787b7-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="787b7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="787b7-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="787b7-117">-EncryptionKeyName</span></span>
<span data-ttu-id="787b7-118">Ruft den Namen des Verschlüsselungsschlüssels ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="787b7-118">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="787b7-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="787b7-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="787b7-120">Ruft die Verschlüsselungsschlüsselversion ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="787b7-120">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="787b7-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="787b7-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="787b7-122">Ruft den Verschlüsselungstresor-URI ab oder legt den URI fest.</span><span class="sxs-lookup"><span data-stu-id="787b7-122">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="787b7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="787b7-123">-InputObject</span></span>
<span data-ttu-id="787b7-124">Ruft das Eingabeobjekt ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="787b7-124">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="787b7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="787b7-125">-Name</span></span>
<span data-ttu-id="787b7-126">Ruft den Namen des Cluster ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="787b7-126">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="787b7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="787b7-127">-ResourceGroupName</span></span>
<span data-ttu-id="787b7-128">Ruft den Namen der Ressourcengruppe ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="787b7-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="787b7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="787b7-129">-ResourceId</span></span>
<span data-ttu-id="787b7-130">Ruft die Ressourcen-ID ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="787b7-130">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="787b7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="787b7-131">-Confirm</span></span>
<span data-ttu-id="787b7-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="787b7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="787b7-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="787b7-133">-WhatIf</span></span>
<span data-ttu-id="787b7-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="787b7-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="787b7-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="787b7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="787b7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="787b7-136">CommonParameters</span></span>
<span data-ttu-id="787b7-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="787b7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="787b7-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="787b7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="787b7-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="787b7-139">INPUTS</span></span>

### <span data-ttu-id="787b7-140">Keine</span><span class="sxs-lookup"><span data-stu-id="787b7-140">None</span></span>

## <span data-ttu-id="787b7-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="787b7-141">OUTPUTS</span></span>

### <span data-ttu-id="787b7-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="787b7-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="787b7-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="787b7-143">NOTES</span></span>

## <span data-ttu-id="787b7-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="787b7-144">RELATED LINKS</span></span>

[<span data-ttu-id="787b7-145">Vom Kunden verwaltete Datenträgerverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="787b7-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/en-us/azure/hdinsight/disk-encryption)
