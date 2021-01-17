---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 46e6e29b9a79fb5a8273fb3872d09e2cd290accd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470818"
---
# <span data-ttu-id="44fe7-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="44fe7-101">Stop-AzVM</span></span>

## <span data-ttu-id="44fe7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="44fe7-103">Beendet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="44fe7-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="44fe7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44fe7-104">SYNTAX</span></span>

### <span data-ttu-id="44fe7-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="44fe7-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44fe7-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="44fe7-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44fe7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44fe7-107">DESCRIPTION</span></span>
<span data-ttu-id="44fe7-108">Das **Cmdlet "Stop-AzVM"** beendet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="44fe7-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="44fe7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="44fe7-109">EXAMPLES</span></span>

### <span data-ttu-id="44fe7-110">Beispiel 1: Beenden eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="44fe7-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="44fe7-111">Dieser Befehl stoppt den virtuellen Computer mit dem Namen "VirtualMachine07" in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="44fe7-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="44fe7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44fe7-112">PARAMETERS</span></span>

### <span data-ttu-id="44fe7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44fe7-113">-AsJob</span></span>
<span data-ttu-id="44fe7-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="44fe7-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="44fe7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44fe7-115">-DefaultProfile</span></span>
<span data-ttu-id="44fe7-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44fe7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44fe7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="44fe7-117">-Force</span></span>
<span data-ttu-id="44fe7-118">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="44fe7-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="44fe7-119">-ID</span><span class="sxs-lookup"><span data-stu-id="44fe7-119">-Id</span></span>
<span data-ttu-id="44fe7-120">Die ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="44fe7-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="44fe7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="44fe7-121">-Name</span></span>
<span data-ttu-id="44fe7-122">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="44fe7-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="44fe7-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="44fe7-123">-NoWait</span></span>
<span data-ttu-id="44fe7-124">Startet den Vorgang und kehrt unmittelbar vor Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="44fe7-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="44fe7-125">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="44fe7-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="44fe7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44fe7-126">-ResourceGroupName</span></span>
<span data-ttu-id="44fe7-127">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="44fe7-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="44fe7-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="44fe7-128">-SkipShutdown</span></span>
<span data-ttu-id="44fe7-129">So fordern Sie das Herunterfahren einer nicht kulanzvollen VM an, wenn die VM bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="44fe7-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="44fe7-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="44fe7-130">-StayProvisioned</span></span>
<span data-ttu-id="44fe7-131">Das Cmdlet stoppt alle virtuellen Computer innerhalb der VMSS, verrät diese jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="44fe7-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="44fe7-132">Das Konto wird für die beendeten virtuellen Computer belastet.</span><span class="sxs-lookup"><span data-stu-id="44fe7-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="44fe7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44fe7-133">-Confirm</span></span>
<span data-ttu-id="44fe7-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="44fe7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44fe7-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="44fe7-135">-WhatIf</span></span>
<span data-ttu-id="44fe7-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44fe7-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44fe7-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44fe7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44fe7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44fe7-138">CommonParameters</span></span>
<span data-ttu-id="44fe7-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44fe7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44fe7-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44fe7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44fe7-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="44fe7-141">INPUTS</span></span>

### <span data-ttu-id="44fe7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="44fe7-142">System.String</span></span>

## <span data-ttu-id="44fe7-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="44fe7-143">OUTPUTS</span></span>

### <span data-ttu-id="44fe7-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="44fe7-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="44fe7-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="44fe7-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="44fe7-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="44fe7-146">NOTES</span></span>

## <span data-ttu-id="44fe7-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="44fe7-147">RELATED LINKS</span></span>

[<span data-ttu-id="44fe7-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="44fe7-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="44fe7-149">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="44fe7-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="44fe7-150">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="44fe7-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="44fe7-151">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="44fe7-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="44fe7-152">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="44fe7-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="44fe7-153">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="44fe7-153">Update-AzVM</span></span>](./Update-AzVM.md)


