---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
ms.openlocfilehash: 12b9b3870b5239746a8524bad9aad0f44161acd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849760"
---
# <span data-ttu-id="b1e0f-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="b1e0f-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="b1e0f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="b1e0f-103">Befehl "ausführen" auf dem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="b1e0f-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1e0f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1e0f-104">SYNTAX</span></span>

### <span data-ttu-id="b1e0f-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1e0f-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1e0f-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="b1e0f-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1e0f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1e0f-107">DESCRIPTION</span></span>
<span data-ttu-id="b1e0f-108">Rufen Sie einen Befehl ausführen auf dem virtuellen Computer auf.</span><span class="sxs-lookup"><span data-stu-id="b1e0f-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="b1e0f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1e0f-109">EXAMPLES</span></span>

### <span data-ttu-id="b1e0f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b1e0f-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="b1e0f-111">Rufen Sie einen Ausführungsbefehl von RunPowerShellScript auf, indem Sie das Skript "sample.ps1" und die Parameter auf dem VM von "VMName" in der Ressourcengruppe "rgname" überschreiben.</span><span class="sxs-lookup"><span data-stu-id="b1e0f-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="b1e0f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1e0f-112">PARAMETERS</span></span>

### <span data-ttu-id="b1e0f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1e0f-113">-AsJob</span></span>
<span data-ttu-id="b1e0f-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="b1e0f-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b1e0f-115">-CommandId</span><span class="sxs-lookup"><span data-stu-id="b1e0f-115">-CommandId</span></span>
<span data-ttu-id="b1e0f-116">Die Befehls-ID ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1e0f-116">The run command id.</span></span>

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

### <span data-ttu-id="b1e0f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1e0f-117">-DefaultProfile</span></span>
<span data-ttu-id="b1e0f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1e0f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1e0f-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="b1e0f-119">-Parameter</span></span>
<span data-ttu-id="b1e0f-120">Die Parameter des Befehls ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1e0f-120">The run command parameters.</span></span>

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

### <span data-ttu-id="b1e0f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1e0f-121">-ResourceGroupName</span></span>
<span data-ttu-id="b1e0f-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b1e0f-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="b1e0f-123">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="b1e0f-123">-ScriptPath</span></span>
<span data-ttu-id="b1e0f-124">Der Pfad des Skripts, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1e0f-124">Path of the script to be executed.</span></span>  <span data-ttu-id="b1e0f-125">Wenn dieser Wert angegeben wird, wird das Standardskript des Befehls vom angegebenen Skript überschrieben.</span><span class="sxs-lookup"><span data-stu-id="b1e0f-125">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="b1e0f-126">-VM</span><span class="sxs-lookup"><span data-stu-id="b1e0f-126">-VM</span></span>
<span data-ttu-id="b1e0f-127">Das Objekt der virtuellen PS-Maschine.</span><span class="sxs-lookup"><span data-stu-id="b1e0f-127">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="b1e0f-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="b1e0f-128">-VMName</span></span>
<span data-ttu-id="b1e0f-129">Der Name der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="b1e0f-129">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="b1e0f-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1e0f-130">-Confirm</span></span>
<span data-ttu-id="b1e0f-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1e0f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1e0f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1e0f-132">-WhatIf</span></span>
<span data-ttu-id="b1e0f-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1e0f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1e0f-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1e0f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1e0f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1e0f-135">CommonParameters</span></span>
<span data-ttu-id="b1e0f-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1e0f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1e0f-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1e0f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1e0f-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1e0f-138">INPUTS</span></span>

### <span data-ttu-id="b1e0f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b1e0f-139">System.String</span></span>
<span data-ttu-id="b1e0f-140">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b1e0f-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b1e0f-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1e0f-141">OUTPUTS</span></span>

### <span data-ttu-id="b1e0f-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="b1e0f-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="b1e0f-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1e0f-143">NOTES</span></span>

## <span data-ttu-id="b1e0f-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1e0f-144">RELATED LINKS</span></span>

