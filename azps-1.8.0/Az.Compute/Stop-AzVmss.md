---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: d00a51a722fa03742c56387ee27faa4f6228ded7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661415"
---
# <span data-ttu-id="5b40c-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5b40c-101">Stop-AzVmss</span></span>

## <span data-ttu-id="5b40c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b40c-102">SYNOPSIS</span></span>
<span data-ttu-id="5b40c-103">Beendet die VMSS oder einen Satz virtueller Computer innerhalb des VMSS.</span><span class="sxs-lookup"><span data-stu-id="5b40c-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="5b40c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b40c-104">SYNTAX</span></span>

### <span data-ttu-id="5b40c-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b40c-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b40c-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="5b40c-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b40c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b40c-107">DESCRIPTION</span></span>
<span data-ttu-id="5b40c-108">Das Cmdlet **Stop-AzVmss** beendet alle virtuellen Maschinen innerhalb des Scale-Sets (Virtual Machine Scale) (VMSS) oder einer Gruppe virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="5b40c-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="5b40c-109">Sie können den *InstanceId* -Parameter verwenden, um einen Satz virtueller Computer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="5b40c-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="5b40c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b40c-110">EXAMPLES</span></span>

### <span data-ttu-id="5b40c-111">Beispiel 1: Beenden aller virtuellen Computer innerhalb des VMSS</span><span class="sxs-lookup"><span data-stu-id="5b40c-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="5b40c-112">Dieser Befehl beendet alle virtuellen Computer, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="5b40c-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="5b40c-113">Beispiel 2: Beenden einer bestimmten Gruppe von virtuellen Computern innerhalb des VMSS</span><span class="sxs-lookup"><span data-stu-id="5b40c-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="5b40c-114">Mit diesem Befehl wird eine bestimmte Gruppe von virtuellen Computern beendet, die durch das Array der Instanz-ID-Zeichenfolge angegeben werden, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="5b40c-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="5b40c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b40c-115">PARAMETERS</span></span>

### <span data-ttu-id="5b40c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b40c-116">-AsJob</span></span>
<span data-ttu-id="5b40c-117">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="5b40c-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5b40c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b40c-118">-DefaultProfile</span></span>
<span data-ttu-id="5b40c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b40c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b40c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5b40c-120">-Force</span></span>
<span data-ttu-id="5b40c-121">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="5b40c-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5b40c-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="5b40c-122">-InstanceId</span></span>
<span data-ttu-id="5b40c-123">Gibt als Zeichenfolgenarray die ID oder IDs der Instanzen des virtuellen Computers an, die von diesem Cmdlet angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="5b40c-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="5b40c-124">Beispiel: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="5b40c-124">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b40c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b40c-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b40c-126">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="5b40c-126">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b40c-127">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="5b40c-127">-StayProvisioned</span></span>
<span data-ttu-id="5b40c-128">Wenn angegeben, wird der virtuelle Computer in den Zustand beendet gesetzt.</span><span class="sxs-lookup"><span data-stu-id="5b40c-128">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="5b40c-129">Wenn keine Angabe erfolgt, gibt der virtuelle Computer den Status "Stopped-dereserviert" ein.</span><span class="sxs-lookup"><span data-stu-id="5b40c-129">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="5b40c-130">Der Benutzer wird weiterhin für VMS im Zustand "beendet", jedoch nicht für VMS im Status "nicht mehr zugewiesen" berechnet.</span><span class="sxs-lookup"><span data-stu-id="5b40c-130">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b40c-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5b40c-131">-VMScaleSetName</span></span>
<span data-ttu-id="5b40c-132">Gibt den Namen der VMSS an, für die dieses Cmdlet die virtuellen Computer beendet.</span><span class="sxs-lookup"><span data-stu-id="5b40c-132">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b40c-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5b40c-133">-Confirm</span></span>
<span data-ttu-id="5b40c-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b40c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b40c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b40c-135">-WhatIf</span></span>
<span data-ttu-id="5b40c-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b40c-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b40c-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b40c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b40c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b40c-138">CommonParameters</span></span>
<span data-ttu-id="5b40c-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b40c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b40c-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b40c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b40c-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b40c-141">INPUTS</span></span>

### <span data-ttu-id="5b40c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5b40c-142">System.String</span></span>

### <span data-ttu-id="5b40c-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="5b40c-143">System.String[]</span></span>

## <span data-ttu-id="5b40c-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b40c-144">OUTPUTS</span></span>

### <span data-ttu-id="5b40c-145">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="5b40c-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="5b40c-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b40c-146">NOTES</span></span>

## <span data-ttu-id="5b40c-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b40c-147">RELATED LINKS</span></span>

[<span data-ttu-id="5b40c-148">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5b40c-148">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="5b40c-149">Neu – AzVmss</span><span class="sxs-lookup"><span data-stu-id="5b40c-149">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="5b40c-150">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5b40c-150">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="5b40c-151">Neustart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5b40c-151">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="5b40c-152">Satz-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5b40c-152">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="5b40c-153">Anfang-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5b40c-153">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="5b40c-154">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5b40c-154">Update-AzVmss</span></span>](./Update-AzVmss.md)


