---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
ms.openlocfilehash: d654b2fa012a793ce48dff2cc5bfb9ade4f99d34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149777"
---
# <span data-ttu-id="56303-101">New-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="56303-101">New-AzVMwareCluster</span></span>

## <span data-ttu-id="56303-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56303-102">SYNOPSIS</span></span>
<span data-ttu-id="56303-103">Erstellen oder Aktualisieren eines Cluster in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="56303-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="56303-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56303-104">SYNTAX</span></span>

```
New-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -SkuName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="56303-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56303-105">DESCRIPTION</span></span>
<span data-ttu-id="56303-106">Erstellen oder Aktualisieren eines Cluster in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="56303-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="56303-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="56303-107">EXAMPLES</span></span>

### <span data-ttu-id="56303-108">Beispiel 1: Erstellen eines Clusters</span><span class="sxs-lookup"><span data-stu-id="56303-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="56303-109">Erstellen eines Clusters</span><span class="sxs-lookup"><span data-stu-id="56303-109">Create cluster</span></span>

## <span data-ttu-id="56303-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56303-110">PARAMETERS</span></span>

### <span data-ttu-id="56303-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56303-111">-AsJob</span></span>
<span data-ttu-id="56303-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="56303-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56303-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="56303-113">-ClusterSize</span></span>
<span data-ttu-id="56303-114">Clustergröße</span><span class="sxs-lookup"><span data-stu-id="56303-114">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56303-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56303-115">-DefaultProfile</span></span>
<span data-ttu-id="56303-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56303-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56303-117">-Name</span><span class="sxs-lookup"><span data-stu-id="56303-117">-Name</span></span>
<span data-ttu-id="56303-118">Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="56303-118">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56303-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="56303-119">-NoWait</span></span>
<span data-ttu-id="56303-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="56303-120">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56303-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="56303-121">-PrivateCloudName</span></span>
<span data-ttu-id="56303-122">Der Name der privaten Cloud.</span><span class="sxs-lookup"><span data-stu-id="56303-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="56303-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56303-123">-ResourceGroupName</span></span>
<span data-ttu-id="56303-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="56303-124">The name of the resource group.</span></span>
<span data-ttu-id="56303-125">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="56303-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="56303-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="56303-126">-SkuName</span></span>
<span data-ttu-id="56303-127">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="56303-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="56303-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56303-128">-SubscriptionId</span></span>
<span data-ttu-id="56303-129">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="56303-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56303-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56303-130">-Confirm</span></span>
<span data-ttu-id="56303-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56303-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56303-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="56303-132">-WhatIf</span></span>
<span data-ttu-id="56303-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56303-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56303-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56303-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56303-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56303-135">CommonParameters</span></span>
<span data-ttu-id="56303-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56303-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56303-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56303-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56303-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="56303-138">INPUTS</span></span>

## <span data-ttu-id="56303-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="56303-139">OUTPUTS</span></span>

### <span data-ttu-id="56303-140">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="56303-140">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="56303-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="56303-141">NOTES</span></span>

<span data-ttu-id="56303-142">ALIASE</span><span class="sxs-lookup"><span data-stu-id="56303-142">ALIASES</span></span>

## <span data-ttu-id="56303-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="56303-143">RELATED LINKS</span></span>

