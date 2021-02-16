---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.VMware/new-azVMwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
ms.openlocfilehash: 3e5e8fa4d098ce68899294a25866b4636c80878e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155961"
---
# <span data-ttu-id="1b3f3-101">New-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="1b3f3-101">New-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="1b3f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="1b3f3-103">Erstellen oder Aktualisieren einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="1b3f3-103">Create or update a private cloud</span></span>

## <span data-ttu-id="1b3f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b3f3-104">SYNTAX</span></span>

```
New-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>] [-AcceptEULA]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1b3f3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b3f3-105">DESCRIPTION</span></span>
<span data-ttu-id="1b3f3-106">Erstellen oder Aktualisieren einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="1b3f3-106">Create or update a private cloud</span></span>

## <span data-ttu-id="1b3f3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1b3f3-107">EXAMPLES</span></span>

### <span data-ttu-id="1b3f3-108">Beispiel 1: Erstellen einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="1b3f3-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMwarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="1b3f3-109">Erstellen einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="1b3f3-109">Create private cloud</span></span>

## <span data-ttu-id="1b3f3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b3f3-110">PARAMETERS</span></span>

### <span data-ttu-id="1b3f3-111">-AcceptEULA</span><span class="sxs-lookup"><span data-stu-id="1b3f3-111">-AcceptEULA</span></span>
<span data-ttu-id="1b3f3-112">Akzeptieren Sie den EULA von AVS, der juristische Ausdruck wird ohne diese Parameter bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="1b3f3-112">Accept EULA of AVS, legal term will pop up without this parameter provided</span></span>

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

### <span data-ttu-id="1b3f3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b3f3-113">-AsJob</span></span>
<span data-ttu-id="1b3f3-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="1b3f3-114">Run the command as a job</span></span>

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

### <span data-ttu-id="1b3f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b3f3-115">-DefaultProfile</span></span>
<span data-ttu-id="1b3f3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b3f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b3f3-117">-Internet</span><span class="sxs-lookup"><span data-stu-id="1b3f3-117">-Internet</span></span>
<span data-ttu-id="1b3f3-118">Die Internetverbindung ist aktiviert oder deaktiviert</span><span class="sxs-lookup"><span data-stu-id="1b3f3-118">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3f3-119">-Location</span><span class="sxs-lookup"><span data-stu-id="1b3f3-119">-Location</span></span>
<span data-ttu-id="1b3f3-120">Ressourcenspeicherort</span><span class="sxs-lookup"><span data-stu-id="1b3f3-120">Resource location</span></span>

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

### <span data-ttu-id="1b3f3-121">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="1b3f3-121">-ManagementClusterSize</span></span>
<span data-ttu-id="1b3f3-122">Clustergröße</span><span class="sxs-lookup"><span data-stu-id="1b3f3-122">The cluster size</span></span>

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

### <span data-ttu-id="1b3f3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1b3f3-123">-Name</span></span>
<span data-ttu-id="1b3f3-124">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="1b3f3-124">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3f3-125">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="1b3f3-125">-NetworkBlock</span></span>
<span data-ttu-id="1b3f3-126">Der Adressblock sollte in VNet in Ihrem Abonnement und lokal eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="1b3f3-126">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="1b3f3-127">Stellen Sie sicher, dass das #A0 (A.B.C.D/X) entspricht, wobei A, B, C, D zwischen 0 und 255 liegt und X zwischen 0 und 22</span><span class="sxs-lookup"><span data-stu-id="1b3f3-127">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="1b3f3-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1b3f3-128">-NoWait</span></span>
<span data-ttu-id="1b3f3-129">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="1b3f3-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1b3f3-130">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="1b3f3-130">-NsxtPassword</span></span>
<span data-ttu-id="1b3f3-131">Optional können Sie das Kennwort für NSX-T Manager festlegen, wenn die private Cloud erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1b3f3-131">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3f3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b3f3-132">-ResourceGroupName</span></span>
<span data-ttu-id="1b3f3-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1b3f3-133">The name of the resource group.</span></span>
<span data-ttu-id="1b3f3-134">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="1b3f3-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1b3f3-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="1b3f3-135">-Sku</span></span>
<span data-ttu-id="1b3f3-136">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="1b3f3-136">The name of the SKU.</span></span>

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

### <span data-ttu-id="1b3f3-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1b3f3-137">-SubscriptionId</span></span>
<span data-ttu-id="1b3f3-138">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="1b3f3-138">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1b3f3-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="1b3f3-139">-Tag</span></span>
<span data-ttu-id="1b3f3-140">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="1b3f3-140">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3f3-141">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="1b3f3-141">-VcenterPassword</span></span>
<span data-ttu-id="1b3f3-142">Optional können Sie das vCenter-Administratorkennwort festlegen, wenn die private Cloud erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1b3f3-142">Optionally, set the vCenter admin password when the private cloud is created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3f3-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b3f3-143">-Confirm</span></span>
<span data-ttu-id="1b3f3-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b3f3-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b3f3-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1b3f3-145">-WhatIf</span></span>
<span data-ttu-id="1b3f3-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b3f3-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b3f3-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b3f3-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b3f3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b3f3-148">CommonParameters</span></span>
<span data-ttu-id="1b3f3-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b3f3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b3f3-150">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b3f3-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b3f3-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1b3f3-151">INPUTS</span></span>

## <span data-ttu-id="1b3f3-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1b3f3-152">OUTPUTS</span></span>

### <span data-ttu-id="1b3f3-153">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="1b3f3-153">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="1b3f3-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1b3f3-154">NOTES</span></span>

<span data-ttu-id="1b3f3-155">ALIASE</span><span class="sxs-lookup"><span data-stu-id="1b3f3-155">ALIASES</span></span>

## <span data-ttu-id="1b3f3-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1b3f3-156">RELATED LINKS</span></span>

