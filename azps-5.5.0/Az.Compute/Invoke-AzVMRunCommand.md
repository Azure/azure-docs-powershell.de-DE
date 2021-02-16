---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 77ac953e1b67ea896f15b13a2695505aabc05bbb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162260"
---
# <span data-ttu-id="08f11-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="08f11-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="08f11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08f11-102">SYNOPSIS</span></span>
<span data-ttu-id="08f11-103">Führen Sie einen Befehl auf der VM aus.</span><span class="sxs-lookup"><span data-stu-id="08f11-103">Run a command on the VM.</span></span>

## <span data-ttu-id="08f11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08f11-104">SYNTAX</span></span>

### <span data-ttu-id="08f11-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="08f11-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08f11-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="08f11-106">ResourceIdParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08f11-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="08f11-107">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08f11-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08f11-108">DESCRIPTION</span></span>
<span data-ttu-id="08f11-109">Rufen Sie einen Ausführungsbefehl auf der VM auf.</span><span class="sxs-lookup"><span data-stu-id="08f11-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="08f11-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="08f11-110">EXAMPLES</span></span>

### <span data-ttu-id="08f11-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="08f11-111">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -VMName 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{param1 = "var1"; param2 = "var2"}
```

<span data-ttu-id="08f11-112">Rufen Sie einen Ausführungsbefehl von RunPowerShellScript auf, wobei das Skript "sample.ps1" und die Parameter auf der VM von "vmname" in der Ressourcengruppe "rgname" überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="08f11-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="08f11-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08f11-113">PARAMETERS</span></span>

### <span data-ttu-id="08f11-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08f11-114">-AsJob</span></span>
<span data-ttu-id="08f11-115">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie ein Auftragsobjekt zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="08f11-115">Run cmdlet in the background and return a job object to track progress.</span></span>

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

### <span data-ttu-id="08f11-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="08f11-116">-CommandId</span></span>
<span data-ttu-id="08f11-117">Die Befehls-ID "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="08f11-117">The run command ID.</span></span>

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

### <span data-ttu-id="08f11-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08f11-118">-DefaultProfile</span></span>
<span data-ttu-id="08f11-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08f11-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08f11-120">-Parameter</span><span class="sxs-lookup"><span data-stu-id="08f11-120">-Parameter</span></span>
<span data-ttu-id="08f11-121">Die Parameter des Befehls "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="08f11-121">The run command parameters.</span></span>

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

### <span data-ttu-id="08f11-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08f11-122">-ResourceGroupName</span></span>
<span data-ttu-id="08f11-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="08f11-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08f11-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08f11-124">-ResourceId</span></span>
<span data-ttu-id="08f11-125">Die Ressourcen-ID für die VM.</span><span class="sxs-lookup"><span data-stu-id="08f11-125">The resource ID for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08f11-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="08f11-126">-ScriptPath</span></span>
<span data-ttu-id="08f11-127">Pfad des auszuführende Skripts.</span><span class="sxs-lookup"><span data-stu-id="08f11-127">Path of the script to be executed.</span></span>  <span data-ttu-id="08f11-128">Wenn dieser Wert angegeben wird, überschreibt das angegebene Skript das Standardskript des Befehls.</span><span class="sxs-lookup"><span data-stu-id="08f11-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="08f11-129">-VM</span><span class="sxs-lookup"><span data-stu-id="08f11-129">-VM</span></span>
<span data-ttu-id="08f11-130">Das Ps-Objekt für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="08f11-130">The PS virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08f11-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="08f11-131">-VMName</span></span>
<span data-ttu-id="08f11-132">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="08f11-132">The name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08f11-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08f11-133">-Confirm</span></span>
<span data-ttu-id="08f11-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08f11-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08f11-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="08f11-135">-WhatIf</span></span>
<span data-ttu-id="08f11-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08f11-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08f11-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08f11-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08f11-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08f11-138">CommonParameters</span></span>
<span data-ttu-id="08f11-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08f11-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08f11-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08f11-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08f11-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="08f11-141">INPUTS</span></span>

### <span data-ttu-id="08f11-142">System.String</span><span class="sxs-lookup"><span data-stu-id="08f11-142">System.String</span></span>

### <span data-ttu-id="08f11-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="08f11-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="08f11-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="08f11-144">OUTPUTS</span></span>

### <span data-ttu-id="08f11-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="08f11-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="08f11-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="08f11-146">NOTES</span></span>

## <span data-ttu-id="08f11-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="08f11-147">RELATED LINKS</span></span>
