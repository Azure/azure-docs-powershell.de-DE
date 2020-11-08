---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
ms.openlocfilehash: f2ed1813859f92624696eef7fa4f881f3eba1628
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167166"
---
# <span data-ttu-id="5e825-101">New-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="5e825-101">New-AzVMWareCluster</span></span>

## <span data-ttu-id="5e825-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e825-102">SYNOPSIS</span></span>
<span data-ttu-id="5e825-103">Erstellen oder Aktualisieren eines Clusters in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="5e825-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="5e825-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e825-104">SYNTAX</span></span>

```
New-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -ClusterSize <Int32>
 -SkuName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5e825-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e825-105">DESCRIPTION</span></span>
<span data-ttu-id="5e825-106">Erstellen oder Aktualisieren eines Clusters in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="5e825-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="5e825-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e825-107">EXAMPLES</span></span>

### <span data-ttu-id="5e825-108">Beispiel 1: Erstellen eines Clusters</span><span class="sxs-lookup"><span data-stu-id="5e825-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="5e825-109">Erstellen eines Clusters</span><span class="sxs-lookup"><span data-stu-id="5e825-109">Create cluster</span></span>

## <span data-ttu-id="5e825-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e825-110">PARAMETERS</span></span>

### <span data-ttu-id="5e825-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e825-111">-AsJob</span></span>
<span data-ttu-id="5e825-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="5e825-112">Run the command as a job</span></span>

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

### <span data-ttu-id="5e825-113">-Clusterisieren</span><span class="sxs-lookup"><span data-stu-id="5e825-113">-ClusterSize</span></span>
<span data-ttu-id="5e825-114">Die Clustergröße</span><span class="sxs-lookup"><span data-stu-id="5e825-114">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e825-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e825-115">-DefaultProfile</span></span>
<span data-ttu-id="5e825-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e825-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e825-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5e825-117">-Name</span></span>
<span data-ttu-id="5e825-118">Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="5e825-118">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="5e825-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5e825-119">-NoWait</span></span>
<span data-ttu-id="5e825-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="5e825-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5e825-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="5e825-121">-PrivateCloudName</span></span>
<span data-ttu-id="5e825-122">Der Name der privaten Cloud.</span><span class="sxs-lookup"><span data-stu-id="5e825-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="5e825-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e825-123">-ResourceGroupName</span></span>
<span data-ttu-id="5e825-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e825-124">The name of the resource group.</span></span>
<span data-ttu-id="5e825-125">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="5e825-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5e825-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5e825-126">-SkuName</span></span>
<span data-ttu-id="5e825-127">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="5e825-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="5e825-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5e825-128">-SubscriptionId</span></span>
<span data-ttu-id="5e825-129">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="5e825-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5e825-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e825-130">-Confirm</span></span>
<span data-ttu-id="5e825-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e825-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e825-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e825-132">-WhatIf</span></span>
<span data-ttu-id="5e825-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e825-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e825-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e825-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e825-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e825-135">CommonParameters</span></span>
<span data-ttu-id="5e825-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e825-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e825-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e825-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e825-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e825-138">INPUTS</span></span>

## <span data-ttu-id="5e825-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e825-139">OUTPUTS</span></span>

### <span data-ttu-id="5e825-140">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="5e825-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="5e825-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e825-141">NOTES</span></span>

<span data-ttu-id="5e825-142">Aliase</span><span class="sxs-lookup"><span data-stu-id="5e825-142">ALIASES</span></span>

## <span data-ttu-id="5e825-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e825-143">RELATED LINKS</span></span>

