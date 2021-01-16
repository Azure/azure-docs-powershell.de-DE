---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
ms.openlocfilehash: 5dd91db9a8141bf9992da9eb364b00301036a898
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294178"
---
# <span data-ttu-id="77886-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="77886-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="77886-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77886-102">SYNOPSIS</span></span>
<span data-ttu-id="77886-103">Erstellen oder Aktualisieren einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="77886-103">Create or update a private cloud</span></span>

## <span data-ttu-id="77886-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77886-104">SYNTAX</span></span>

```
New-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="77886-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="77886-105">DESCRIPTION</span></span>
<span data-ttu-id="77886-106">Erstellen oder Aktualisieren einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="77886-106">Create or update a private cloud</span></span>

## <span data-ttu-id="77886-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="77886-107">EXAMPLES</span></span>

### <span data-ttu-id="77886-108">Beispiel 1: Erstellen einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="77886-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="77886-109">Erstellen einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="77886-109">Create private cloud</span></span>

## <span data-ttu-id="77886-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77886-110">PARAMETERS</span></span>

### <span data-ttu-id="77886-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77886-111">-AsJob</span></span>
<span data-ttu-id="77886-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="77886-112">Run the command as a job</span></span>

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

### <span data-ttu-id="77886-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77886-113">-DefaultProfile</span></span>
<span data-ttu-id="77886-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="77886-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77886-115">-Internet</span><span class="sxs-lookup"><span data-stu-id="77886-115">-Internet</span></span>
<span data-ttu-id="77886-116">Die Internetverbindung ist aktiviert oder deaktiviert</span><span class="sxs-lookup"><span data-stu-id="77886-116">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77886-117">-Location</span><span class="sxs-lookup"><span data-stu-id="77886-117">-Location</span></span>
<span data-ttu-id="77886-118">Ressourcenspeicherort</span><span class="sxs-lookup"><span data-stu-id="77886-118">Resource location</span></span>

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

### <span data-ttu-id="77886-119">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="77886-119">-ManagementClusterSize</span></span>
<span data-ttu-id="77886-120">Clustergröße</span><span class="sxs-lookup"><span data-stu-id="77886-120">The cluster size</span></span>

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

### <span data-ttu-id="77886-121">-Name</span><span class="sxs-lookup"><span data-stu-id="77886-121">-Name</span></span>
<span data-ttu-id="77886-122">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="77886-122">Name of the private cloud</span></span>

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

### <span data-ttu-id="77886-123">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="77886-123">-NetworkBlock</span></span>
<span data-ttu-id="77886-124">Der Adressblock sollte VNet in Ihrem Abonnement und lokal eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="77886-124">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="77886-125">Stellen Sie sicher, dass das #A0 (A.B.C.D/X) entspricht, wobei A, B, C, D zwischen 0 und 255 liegt und X zwischen 0 und 22</span><span class="sxs-lookup"><span data-stu-id="77886-125">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="77886-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="77886-126">-NoWait</span></span>
<span data-ttu-id="77886-127">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="77886-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="77886-128">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="77886-128">-NsxtPassword</span></span>
<span data-ttu-id="77886-129">Optional können Sie das Kennwort für NSX-T Manager festlegen, wenn die private Cloud erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="77886-129">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="77886-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77886-130">-ResourceGroupName</span></span>
<span data-ttu-id="77886-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="77886-131">The name of the resource group.</span></span>
<span data-ttu-id="77886-132">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="77886-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="77886-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="77886-133">-Sku</span></span>
<span data-ttu-id="77886-134">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="77886-134">The name of the SKU.</span></span>

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

### <span data-ttu-id="77886-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="77886-135">-SubscriptionId</span></span>
<span data-ttu-id="77886-136">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="77886-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="77886-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="77886-137">-Tag</span></span>
<span data-ttu-id="77886-138">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="77886-138">Resource tags</span></span>

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

### <span data-ttu-id="77886-139">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="77886-139">-VcenterPassword</span></span>
<span data-ttu-id="77886-140">Optional können Sie das vCenter-Administratorkennwort festlegen, wenn die private Cloud erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="77886-140">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="77886-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77886-141">-Confirm</span></span>
<span data-ttu-id="77886-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="77886-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77886-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="77886-143">-WhatIf</span></span>
<span data-ttu-id="77886-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77886-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77886-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77886-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77886-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77886-146">CommonParameters</span></span>
<span data-ttu-id="77886-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77886-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77886-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77886-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77886-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="77886-149">INPUTS</span></span>

## <span data-ttu-id="77886-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="77886-150">OUTPUTS</span></span>

### <span data-ttu-id="77886-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="77886-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="77886-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="77886-152">NOTES</span></span>

<span data-ttu-id="77886-153">ALIASE</span><span class="sxs-lookup"><span data-stu-id="77886-153">ALIASES</span></span>

## <span data-ttu-id="77886-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="77886-154">RELATED LINKS</span></span>

