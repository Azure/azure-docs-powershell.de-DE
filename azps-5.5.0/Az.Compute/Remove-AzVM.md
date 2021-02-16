---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 6e733bfecea9a054bbab3794ca61778894c613fe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166441"
---
# <span data-ttu-id="2a187-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="2a187-101">Remove-AzVM</span></span>

## <span data-ttu-id="2a187-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a187-102">SYNOPSIS</span></span>
<span data-ttu-id="2a187-103">Entfernt einen virtuellen Computer aus Azure.</span><span class="sxs-lookup"><span data-stu-id="2a187-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="2a187-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a187-104">SYNTAX</span></span>

### <span data-ttu-id="2a187-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2a187-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a187-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2a187-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a187-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a187-107">DESCRIPTION</span></span>
<span data-ttu-id="2a187-108">Das **Cmdlet "Remove-AzVM"** entfernt einen virtuellen Computer aus Azure.</span><span class="sxs-lookup"><span data-stu-id="2a187-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="2a187-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2a187-109">EXAMPLES</span></span>

### <span data-ttu-id="2a187-110">Beispiel 1: Entfernen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="2a187-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="2a187-111">Mit diesem Befehl wird der virtuelle Computer "VirtualMachine07" in der Ressourcengruppe "ResourceGroup11" entfernt.</span><span class="sxs-lookup"><span data-stu-id="2a187-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="2a187-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a187-112">PARAMETERS</span></span>

### <span data-ttu-id="2a187-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a187-113">-AsJob</span></span>
<span data-ttu-id="2a187-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="2a187-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2a187-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a187-115">-DefaultProfile</span></span>
<span data-ttu-id="2a187-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a187-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a187-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2a187-117">-Force</span></span>
<span data-ttu-id="2a187-118">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="2a187-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a187-119">-ID</span><span class="sxs-lookup"><span data-stu-id="2a187-119">-Id</span></span>
<span data-ttu-id="2a187-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2a187-120">The resource group name.</span></span>

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

### <span data-ttu-id="2a187-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2a187-121">-Name</span></span>
<span data-ttu-id="2a187-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="2a187-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a187-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2a187-123">-NoWait</span></span>
<span data-ttu-id="2a187-124">Der Vorgang wird gestartet und unmittelbar vor Abschluss des Vorgangs beendet.</span><span class="sxs-lookup"><span data-stu-id="2a187-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="2a187-125">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="2a187-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="2a187-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a187-126">-ResourceGroupName</span></span>
<span data-ttu-id="2a187-127">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2a187-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2a187-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a187-128">-Confirm</span></span>
<span data-ttu-id="2a187-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a187-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a187-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2a187-130">-WhatIf</span></span>
<span data-ttu-id="2a187-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a187-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a187-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a187-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a187-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a187-133">CommonParameters</span></span>
<span data-ttu-id="2a187-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a187-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a187-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a187-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a187-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2a187-136">INPUTS</span></span>

### <span data-ttu-id="2a187-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2a187-137">System.String</span></span>

## <span data-ttu-id="2a187-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2a187-138">OUTPUTS</span></span>

### <span data-ttu-id="2a187-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="2a187-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="2a187-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2a187-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2a187-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2a187-141">NOTES</span></span>

## <span data-ttu-id="2a187-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2a187-142">RELATED LINKS</span></span>

[<span data-ttu-id="2a187-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="2a187-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="2a187-144">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2a187-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="2a187-145">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="2a187-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="2a187-146">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="2a187-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="2a187-147">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="2a187-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="2a187-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="2a187-148">Update-AzVM</span></span>](./Update-AzVM.md)


