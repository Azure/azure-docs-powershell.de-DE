---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 36d86f701bfdeea67869b45512a79eeee45c0457
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938264"
---
# <span data-ttu-id="d0e2e-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0e2e-101">Stop-AzVM</span></span>

## <span data-ttu-id="d0e2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e2e-103">Beendet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="d0e2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0e2e-104">SYNTAX</span></span>

### <span data-ttu-id="d0e2e-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d0e2e-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0e2e-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d0e2e-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0e2e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0e2e-107">DESCRIPTION</span></span>
<span data-ttu-id="d0e2e-108">Das **Cmdlet Stopp-AzVM** beendet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="d0e2e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d0e2e-109">EXAMPLES</span></span>

### <span data-ttu-id="d0e2e-110">Beispiel 1: Beenden eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="d0e2e-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="d0e2e-111">Mit diesem Befehl wird der virtuelle Computer mit dem Namen VirtualMachine07 in ResourceGroup11 beendet.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="d0e2e-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d0e2e-112">PARAMETERS</span></span>

### <span data-ttu-id="d0e2e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0e2e-113">-AsJob</span></span>
<span data-ttu-id="d0e2e-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d0e2e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e2e-115">-DefaultProfile</span></span>
<span data-ttu-id="d0e2e-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0e2e-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="d0e2e-117">-Force</span></span>
<span data-ttu-id="d0e2e-118">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d0e2e-119">-ID</span><span class="sxs-lookup"><span data-stu-id="d0e2e-119">-Id</span></span>
<span data-ttu-id="d0e2e-120">Die ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e2e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d0e2e-121">-Name</span></span>
<span data-ttu-id="d0e2e-122">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e2e-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d0e2e-123">-NoWait</span></span>
<span data-ttu-id="d0e2e-124">Startet den Vorgang und gibt sofort zurück, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="d0e2e-125">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d0e2e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0e2e-126">-ResourceGroupName</span></span>
<span data-ttu-id="d0e2e-127">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-127">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e2e-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="d0e2e-128">-SkipShutdown</span></span>
<span data-ttu-id="d0e2e-129">So fordern Sie ein nicht anmutiges Herunterfahren der VM an, wenn die VM bereitgestellt bleibt.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="d0e2e-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="d0e2e-130">-StayProvisioned</span></span>
<span data-ttu-id="d0e2e-131">Das Cmdlet stoppt alle virtuellen Computer innerhalb des VMSS, verteilt sie aber nicht.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="d0e2e-132">Das Konto wird für die angehaltenen virtuellen Computer in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="d0e2e-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d0e2e-133">-Confirm</span></span>
<span data-ttu-id="d0e2e-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0e2e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0e2e-135">-WhatIf</span></span>
<span data-ttu-id="d0e2e-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0e2e-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0e2e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e2e-138">CommonParameters</span></span>
<span data-ttu-id="d0e2e-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0e2e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e2e-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0e2e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e2e-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d0e2e-141">INPUTS</span></span>

### <span data-ttu-id="d0e2e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d0e2e-142">System.String</span></span>

## <span data-ttu-id="d0e2e-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d0e2e-143">OUTPUTS</span></span>

### <span data-ttu-id="d0e2e-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="d0e2e-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="d0e2e-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d0e2e-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d0e2e-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d0e2e-146">NOTES</span></span>

## <span data-ttu-id="d0e2e-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d0e2e-147">RELATED LINKS</span></span>

[<span data-ttu-id="d0e2e-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0e2e-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d0e2e-149">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0e2e-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="d0e2e-150">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0e2e-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="d0e2e-151">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0e2e-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="d0e2e-152">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0e2e-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="d0e2e-153">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0e2e-153">Update-AzVM</span></span>](./Update-AzVM.md)


