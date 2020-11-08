---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
ms.openlocfilehash: 5dd91db9a8141bf9992da9eb364b00301036a898
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173643"
---
# <span data-ttu-id="a69ff-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="a69ff-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="a69ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a69ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a69ff-103">Erstellen oder Aktualisieren einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="a69ff-103">Create or update a private cloud</span></span>

## <span data-ttu-id="a69ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a69ff-104">SYNTAX</span></span>

```
New-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a69ff-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a69ff-105">DESCRIPTION</span></span>
<span data-ttu-id="a69ff-106">Erstellen oder Aktualisieren einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="a69ff-106">Create or update a private cloud</span></span>

## <span data-ttu-id="a69ff-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a69ff-107">EXAMPLES</span></span>

### <span data-ttu-id="a69ff-108">Beispiel 1: Erstellen einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="a69ff-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="a69ff-109">Erstellen einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="a69ff-109">Create private cloud</span></span>

## <span data-ttu-id="a69ff-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a69ff-110">PARAMETERS</span></span>

### <span data-ttu-id="a69ff-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a69ff-111">-AsJob</span></span>
<span data-ttu-id="a69ff-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="a69ff-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a69ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a69ff-113">-DefaultProfile</span></span>
<span data-ttu-id="a69ff-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a69ff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a69ff-115">-Internet</span><span class="sxs-lookup"><span data-stu-id="a69ff-115">-Internet</span></span>
<span data-ttu-id="a69ff-116">Die Verbindung zum Internet ist aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a69ff-116">Connectivity to internet is enabled or disabled</span></span>

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

### <span data-ttu-id="a69ff-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="a69ff-117">-Location</span></span>
<span data-ttu-id="a69ff-118">Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="a69ff-118">Resource location</span></span>

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

### <span data-ttu-id="a69ff-119">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="a69ff-119">-ManagementClusterSize</span></span>
<span data-ttu-id="a69ff-120">Die Clustergröße</span><span class="sxs-lookup"><span data-stu-id="a69ff-120">The cluster size</span></span>

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

### <span data-ttu-id="a69ff-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a69ff-121">-Name</span></span>
<span data-ttu-id="a69ff-122">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="a69ff-122">Name of the private cloud</span></span>

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

### <span data-ttu-id="a69ff-123">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="a69ff-123">-NetworkBlock</span></span>
<span data-ttu-id="a69ff-124">Der Adressblock sollte in VNet sowohl in Ihrem Abonnement als auch lokal eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="a69ff-124">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="a69ff-125">Stellen Sie sicher, dass das CIDR-Format mit (a. b. c. d/X) übereinstimmt, wobei a, b, c, D zwischen 0 und 255 und X zwischen 0 und 22 liegt.</span><span class="sxs-lookup"><span data-stu-id="a69ff-125">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="a69ff-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a69ff-126">-NoWait</span></span>
<span data-ttu-id="a69ff-127">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="a69ff-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a69ff-128">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="a69ff-128">-NsxtPassword</span></span>
<span data-ttu-id="a69ff-129">Optional: Festlegen des NSX-T Manager-Kennworts beim Erstellen der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="a69ff-129">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="a69ff-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a69ff-130">-ResourceGroupName</span></span>
<span data-ttu-id="a69ff-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a69ff-131">The name of the resource group.</span></span>
<span data-ttu-id="a69ff-132">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="a69ff-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a69ff-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="a69ff-133">-Sku</span></span>
<span data-ttu-id="a69ff-134">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="a69ff-134">The name of the SKU.</span></span>

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

### <span data-ttu-id="a69ff-135">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a69ff-135">-SubscriptionId</span></span>
<span data-ttu-id="a69ff-136">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a69ff-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a69ff-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="a69ff-137">-Tag</span></span>
<span data-ttu-id="a69ff-138">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="a69ff-138">Resource tags</span></span>

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

### <span data-ttu-id="a69ff-139">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="a69ff-139">-VcenterPassword</span></span>
<span data-ttu-id="a69ff-140">Optional: Festlegen des vCenter Admin-Kennworts beim Erstellen der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="a69ff-140">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="a69ff-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a69ff-141">-Confirm</span></span>
<span data-ttu-id="a69ff-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a69ff-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a69ff-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a69ff-143">-WhatIf</span></span>
<span data-ttu-id="a69ff-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a69ff-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a69ff-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a69ff-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a69ff-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a69ff-146">CommonParameters</span></span>
<span data-ttu-id="a69ff-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a69ff-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a69ff-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a69ff-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a69ff-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a69ff-149">INPUTS</span></span>

## <span data-ttu-id="a69ff-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a69ff-150">OUTPUTS</span></span>

### <span data-ttu-id="a69ff-151">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="a69ff-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="a69ff-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="a69ff-152">NOTES</span></span>

<span data-ttu-id="a69ff-153">Aliase</span><span class="sxs-lookup"><span data-stu-id="a69ff-153">ALIASES</span></span>

## <span data-ttu-id="a69ff-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a69ff-154">RELATED LINKS</span></span>

