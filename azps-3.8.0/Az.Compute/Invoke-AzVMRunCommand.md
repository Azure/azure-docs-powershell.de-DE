---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 77ac953e1b67ea896f15b13a2695505aabc05bbb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996184"
---
# <span data-ttu-id="f1b63-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="f1b63-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="f1b63-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1b63-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b63-103">Führen Sie einen Befehl auf dem virtuellen Computer aus.</span><span class="sxs-lookup"><span data-stu-id="f1b63-103">Run a command on the VM.</span></span>

## <span data-ttu-id="f1b63-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1b63-104">SYNTAX</span></span>

### <span data-ttu-id="f1b63-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1b63-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1b63-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="f1b63-106">ResourceIdParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1b63-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="f1b63-107">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1b63-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1b63-108">DESCRIPTION</span></span>
<span data-ttu-id="f1b63-109">Rufen Sie einen Befehl ausführen auf dem virtuellen Computer auf.</span><span class="sxs-lookup"><span data-stu-id="f1b63-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="f1b63-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1b63-110">EXAMPLES</span></span>

### <span data-ttu-id="f1b63-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f1b63-111">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -VMName 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{param1 = "var1"; param2 = "var2"}
```

<span data-ttu-id="f1b63-112">Rufen Sie einen Ausführungsbefehl von RunPowerShellScript auf, indem Sie das Skript "sample.ps1" und die Parameter auf dem VM von "VMName" in der Ressourcengruppe "rgname" überschreiben.</span><span class="sxs-lookup"><span data-stu-id="f1b63-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="f1b63-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1b63-113">PARAMETERS</span></span>

### <span data-ttu-id="f1b63-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1b63-114">-AsJob</span></span>
<span data-ttu-id="f1b63-115">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie ein Auftragsobjekt zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="f1b63-115">Run cmdlet in the background and return a job object to track progress.</span></span>

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

### <span data-ttu-id="f1b63-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="f1b63-116">-CommandId</span></span>
<span data-ttu-id="f1b63-117">Die Befehls-ID ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1b63-117">The run command ID.</span></span>

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

### <span data-ttu-id="f1b63-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b63-118">-DefaultProfile</span></span>
<span data-ttu-id="f1b63-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1b63-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1b63-120">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f1b63-120">-Parameter</span></span>
<span data-ttu-id="f1b63-121">Die Parameter des Befehls ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1b63-121">The run command parameters.</span></span>

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

### <span data-ttu-id="f1b63-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1b63-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1b63-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f1b63-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="f1b63-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f1b63-124">-ResourceId</span></span>
<span data-ttu-id="f1b63-125">Die Ressourcen-ID für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="f1b63-125">The resource ID for the VM.</span></span>

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

### <span data-ttu-id="f1b63-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="f1b63-126">-ScriptPath</span></span>
<span data-ttu-id="f1b63-127">Der Pfad des Skripts, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1b63-127">Path of the script to be executed.</span></span>  <span data-ttu-id="f1b63-128">Wenn dieser Wert angegeben wird, wird das Standardskript des Befehls vom angegebenen Skript überschrieben.</span><span class="sxs-lookup"><span data-stu-id="f1b63-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="f1b63-129">-VM</span><span class="sxs-lookup"><span data-stu-id="f1b63-129">-VM</span></span>
<span data-ttu-id="f1b63-130">Das Objekt der virtuellen PS-Maschine.</span><span class="sxs-lookup"><span data-stu-id="f1b63-130">The PS virtual machine object.</span></span>

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

### <span data-ttu-id="f1b63-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="f1b63-131">-VMName</span></span>
<span data-ttu-id="f1b63-132">Der Name der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="f1b63-132">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="f1b63-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1b63-133">-Confirm</span></span>
<span data-ttu-id="f1b63-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1b63-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1b63-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1b63-135">-WhatIf</span></span>
<span data-ttu-id="f1b63-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1b63-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1b63-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1b63-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1b63-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b63-138">CommonParameters</span></span>
<span data-ttu-id="f1b63-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1b63-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b63-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1b63-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b63-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1b63-141">INPUTS</span></span>

### <span data-ttu-id="f1b63-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f1b63-142">System.String</span></span>

### <span data-ttu-id="f1b63-143">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f1b63-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="f1b63-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1b63-144">OUTPUTS</span></span>

### <span data-ttu-id="f1b63-145">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="f1b63-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="f1b63-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1b63-146">NOTES</span></span>

## <span data-ttu-id="f1b63-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1b63-147">RELATED LINKS</span></span>
