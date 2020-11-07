---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 7d3c27ad8dacb288aeb0d15235aacc48405b8a6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664678"
---
# <span data-ttu-id="5f746-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="5f746-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="5f746-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f746-102">SYNOPSIS</span></span>
<span data-ttu-id="5f746-103">Befehl "ausführen" auf dem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="5f746-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f746-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f746-104">SYNTAX</span></span>

### <span data-ttu-id="5f746-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f746-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f746-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="5f746-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f746-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f746-107">DESCRIPTION</span></span>
<span data-ttu-id="5f746-108">Rufen Sie einen Befehl ausführen auf dem virtuellen Computer auf.</span><span class="sxs-lookup"><span data-stu-id="5f746-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="5f746-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f746-109">EXAMPLES</span></span>

### <span data-ttu-id="5f746-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5f746-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="5f746-111">Rufen Sie einen Ausführungsbefehl von RunPowerShellScript auf, indem Sie das Skript "sample.ps1" und die Parameter auf dem VM von "VMName" in der Ressourcengruppe "rgname" überschreiben.</span><span class="sxs-lookup"><span data-stu-id="5f746-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="5f746-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f746-112">PARAMETERS</span></span>

### <span data-ttu-id="5f746-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f746-113">-AsJob</span></span>
<span data-ttu-id="5f746-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="5f746-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f746-115">-CommandId</span><span class="sxs-lookup"><span data-stu-id="5f746-115">-CommandId</span></span>
<span data-ttu-id="5f746-116">Die Befehls-ID ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f746-116">The run command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f746-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f746-117">-DefaultProfile</span></span>
<span data-ttu-id="5f746-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f746-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f746-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="5f746-119">-Parameter</span></span>
<span data-ttu-id="5f746-120">Die Parameter des Befehls ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f746-120">The run command parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f746-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f746-121">-ResourceGroupName</span></span>
<span data-ttu-id="5f746-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5f746-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f746-123">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="5f746-123">-ScriptPath</span></span>
<span data-ttu-id="5f746-124">Der Pfad des Skripts, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f746-124">Path of the script to be executed.</span></span>  <span data-ttu-id="5f746-125">Wenn dieser Wert angegeben wird, wird das Standardskript des Befehls vom angegebenen Skript überschrieben.</span><span class="sxs-lookup"><span data-stu-id="5f746-125">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f746-126">-VM</span><span class="sxs-lookup"><span data-stu-id="5f746-126">-VM</span></span>
<span data-ttu-id="5f746-127">Das Objekt der virtuellen PS-Maschine.</span><span class="sxs-lookup"><span data-stu-id="5f746-127">The PS virtual Machine Object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f746-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="5f746-128">-VMName</span></span>
<span data-ttu-id="5f746-129">Der Name der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="5f746-129">The name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f746-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5f746-130">-Confirm</span></span>
<span data-ttu-id="5f746-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f746-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f746-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f746-132">-WhatIf</span></span>
<span data-ttu-id="5f746-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f746-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f746-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f746-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f746-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f746-135">CommonParameters</span></span>
<span data-ttu-id="5f746-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f746-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f746-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f746-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f746-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f746-138">INPUTS</span></span>

### <span data-ttu-id="5f746-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5f746-139">System.String</span></span>
<span data-ttu-id="5f746-140">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5f746-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5f746-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f746-141">OUTPUTS</span></span>

### <span data-ttu-id="5f746-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="5f746-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="5f746-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f746-143">NOTES</span></span>

## <span data-ttu-id="5f746-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f746-144">RELATED LINKS</span></span>
