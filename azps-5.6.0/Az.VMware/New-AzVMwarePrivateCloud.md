---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
ms.openlocfilehash: 8cdc8e49a78c4f2c2bfb88d42fe710ad783df97f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937243"
---
# <span data-ttu-id="5ab9a-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="5ab9a-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="5ab9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ab9a-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab9a-103">Erstellen oder Aktualisieren einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="5ab9a-103">Create or update a private cloud</span></span>

## <span data-ttu-id="5ab9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ab9a-104">SYNTAX</span></span>

```
New-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>] [-AcceptEULA]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5ab9a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ab9a-105">DESCRIPTION</span></span>
<span data-ttu-id="5ab9a-106">Erstellen oder Aktualisieren einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="5ab9a-106">Create or update a private cloud</span></span>

## <span data-ttu-id="5ab9a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5ab9a-107">EXAMPLES</span></span>

### <span data-ttu-id="5ab9a-108">Beispiel 1: Erstellen einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="5ab9a-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="5ab9a-109">Erstellen einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="5ab9a-109">Create private cloud</span></span>

## <span data-ttu-id="5ab9a-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5ab9a-110">PARAMETERS</span></span>

### <span data-ttu-id="5ab9a-111">-AcceptEULA</span><span class="sxs-lookup"><span data-stu-id="5ab9a-111">-AcceptEULA</span></span>
<span data-ttu-id="5ab9a-112">AKZEPTIEREN SIE DIE EULA von AVS, der juristische Ausdruck wird ohne diesen Parameter bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="5ab9a-112">Accept EULA of AVS, legal term will pop up without this parameter provided</span></span>

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

### <span data-ttu-id="5ab9a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ab9a-113">-AsJob</span></span>
<span data-ttu-id="5ab9a-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="5ab9a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="5ab9a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab9a-115">-DefaultProfile</span></span>
<span data-ttu-id="5ab9a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ab9a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ab9a-117">-Internet</span><span class="sxs-lookup"><span data-stu-id="5ab9a-117">-Internet</span></span>
<span data-ttu-id="5ab9a-118">Die Internetverbindung ist aktiviert oder deaktiviert</span><span class="sxs-lookup"><span data-stu-id="5ab9a-118">Connectivity to internet is enabled or disabled</span></span>

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

### <span data-ttu-id="5ab9a-119">-Location</span><span class="sxs-lookup"><span data-stu-id="5ab9a-119">-Location</span></span>
<span data-ttu-id="5ab9a-120">Ressourcenspeicherort</span><span class="sxs-lookup"><span data-stu-id="5ab9a-120">Resource location</span></span>

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

### <span data-ttu-id="5ab9a-121">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="5ab9a-121">-ManagementClusterSize</span></span>
<span data-ttu-id="5ab9a-122">Die Clustergröße</span><span class="sxs-lookup"><span data-stu-id="5ab9a-122">The cluster size</span></span>

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

### <span data-ttu-id="5ab9a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5ab9a-123">-Name</span></span>
<span data-ttu-id="5ab9a-124">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="5ab9a-124">Name of the private cloud</span></span>

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

### <span data-ttu-id="5ab9a-125">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="5ab9a-125">-NetworkBlock</span></span>
<span data-ttu-id="5ab9a-126">Der Adressblock sollte für VNet in Ihrem Abonnement und lokal eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="5ab9a-126">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="5ab9a-127">Stellen Sie sicher, dass das CIDR-Format mit (A.B.C.D/X) konform ist, wobei A,B,C,D zwischen 0 und 255 und X zwischen 0 und 22 liegt.</span><span class="sxs-lookup"><span data-stu-id="5ab9a-127">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="5ab9a-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5ab9a-128">-NoWait</span></span>
<span data-ttu-id="5ab9a-129">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="5ab9a-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5ab9a-130">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="5ab9a-130">-NsxtPassword</span></span>
<span data-ttu-id="5ab9a-131">Legen Sie optional das Kennwort für NSX-T Manager beim Erstellen der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="5ab9a-131">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="5ab9a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab9a-132">-ResourceGroupName</span></span>
<span data-ttu-id="5ab9a-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5ab9a-133">The name of the resource group.</span></span>
<span data-ttu-id="5ab9a-134">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="5ab9a-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5ab9a-135">-Sku</span><span class="sxs-lookup"><span data-stu-id="5ab9a-135">-Sku</span></span>
<span data-ttu-id="5ab9a-136">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="5ab9a-136">The name of the SKU.</span></span>

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

### <span data-ttu-id="5ab9a-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ab9a-137">-SubscriptionId</span></span>
<span data-ttu-id="5ab9a-138">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="5ab9a-138">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5ab9a-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ab9a-139">-Tag</span></span>
<span data-ttu-id="5ab9a-140">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="5ab9a-140">Resource tags</span></span>

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

### <span data-ttu-id="5ab9a-141">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="5ab9a-141">-VcenterPassword</span></span>
<span data-ttu-id="5ab9a-142">Optional können Sie das vCenter-Administratorkennwort festlegen, wenn die private Cloud erstellt wird</span><span class="sxs-lookup"><span data-stu-id="5ab9a-142">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="5ab9a-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5ab9a-143">-Confirm</span></span>
<span data-ttu-id="5ab9a-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5ab9a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ab9a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab9a-145">-WhatIf</span></span>
<span data-ttu-id="5ab9a-146">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5ab9a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ab9a-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5ab9a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ab9a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab9a-148">CommonParameters</span></span>
<span data-ttu-id="5ab9a-149">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ab9a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab9a-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ab9a-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab9a-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5ab9a-151">INPUTS</span></span>

## <span data-ttu-id="5ab9a-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5ab9a-152">OUTPUTS</span></span>

### <span data-ttu-id="5ab9a-153">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="5ab9a-153">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="5ab9a-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5ab9a-154">NOTES</span></span>

<span data-ttu-id="5ab9a-155">ALIASE</span><span class="sxs-lookup"><span data-stu-id="5ab9a-155">ALIASES</span></span>

## <span data-ttu-id="5ab9a-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5ab9a-156">RELATED LINKS</span></span>

