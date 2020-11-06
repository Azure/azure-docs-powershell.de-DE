---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 2402591c6c388dbe7c1c6b24a1beb2b298012d4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505633"
---
# <span data-ttu-id="9f502-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="9f502-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="9f502-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9f502-102">SYNOPSIS</span></span>
<span data-ttu-id="9f502-103">Befehl "ausführen" auf dem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="9f502-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f502-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f502-104">SYNTAX</span></span>

### <span data-ttu-id="9f502-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="9f502-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f502-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="9f502-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f502-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f502-107">DESCRIPTION</span></span>
<span data-ttu-id="9f502-108">Rufen Sie einen Befehl ausführen auf dem virtuellen Computer auf.</span><span class="sxs-lookup"><span data-stu-id="9f502-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="9f502-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f502-109">EXAMPLES</span></span>

### <span data-ttu-id="9f502-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9f502-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="9f502-111">Rufen Sie einen Ausführungsbefehl von RunPowerShellScript auf, indem Sie das Skript "sample.ps1" und die Parameter auf dem VM von "VMName" in der Ressourcengruppe "rgname" überschreiben.</span><span class="sxs-lookup"><span data-stu-id="9f502-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="9f502-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f502-112">PARAMETERS</span></span>

### <span data-ttu-id="9f502-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="9f502-113">-CommandId</span></span>
<span data-ttu-id="9f502-114">Die Befehls-ID ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f502-114">The run command id.</span></span>

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

### <span data-ttu-id="9f502-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f502-115">-DefaultProfile</span></span>
<span data-ttu-id="9f502-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9f502-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f502-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="9f502-117">-Parameter</span></span>
<span data-ttu-id="9f502-118">Die Parameter des Befehls ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f502-118">The run command parameters.</span></span>

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

### <span data-ttu-id="9f502-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f502-119">-ResourceGroupName</span></span>
<span data-ttu-id="9f502-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9f502-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f502-121">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="9f502-121">-ScriptPath</span></span>
<span data-ttu-id="9f502-122">Der Pfad des Skripts, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f502-122">Path of the script to be executed.</span></span>  <span data-ttu-id="9f502-123">Wenn dieser Wert angegeben wird, wird das Standardskript des Befehls vom angegebenen Skript überschrieben.</span><span class="sxs-lookup"><span data-stu-id="9f502-123">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="9f502-124">-VM</span><span class="sxs-lookup"><span data-stu-id="9f502-124">-VM</span></span>
<span data-ttu-id="9f502-125">Das Objekt der virtuellen PS-Maschine.</span><span class="sxs-lookup"><span data-stu-id="9f502-125">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="9f502-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="9f502-126">-VMName</span></span>
<span data-ttu-id="9f502-127">Der Name der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="9f502-127">The name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f502-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9f502-128">-Confirm</span></span>
<span data-ttu-id="9f502-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f502-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f502-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f502-130">-WhatIf</span></span>
<span data-ttu-id="9f502-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f502-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f502-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f502-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f502-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f502-133">CommonParameters</span></span>
<span data-ttu-id="9f502-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f502-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f502-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f502-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f502-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9f502-136">INPUTS</span></span>

### <span data-ttu-id="9f502-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9f502-137">System.String</span></span>
<span data-ttu-id="9f502-138">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9f502-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9f502-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9f502-139">OUTPUTS</span></span>

### <span data-ttu-id="9f502-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="9f502-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="9f502-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f502-141">NOTES</span></span>

## <span data-ttu-id="9f502-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9f502-142">RELATED LINKS</span></span>

