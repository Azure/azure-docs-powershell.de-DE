---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: f1a4fbf1e921ed7b6c2205e92ff3c5b868f5ad66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820591"
---
# <span data-ttu-id="1d16d-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1d16d-101">Remove-AzVmss</span></span>

## <span data-ttu-id="1d16d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1d16d-102">SYNOPSIS</span></span>
<span data-ttu-id="1d16d-103">Entfernt das VMSS oder einen virtuellen Computer, der sich innerhalb des VMSS befindet.</span><span class="sxs-lookup"><span data-stu-id="1d16d-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="1d16d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d16d-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d16d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d16d-105">DESCRIPTION</span></span>
<span data-ttu-id="1d16d-106">Das Cmdlet **Remove-AzVmss** entfernt den virtuellen Computer-Skalierungs Satz (VMSS) aus Azure.</span><span class="sxs-lookup"><span data-stu-id="1d16d-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="1d16d-107">Dieses Cmdlet kann auch verwendet werden, um einen bestimmten virtuellen Computer innerhalb des VMSS zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="1d16d-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="1d16d-108">Sie können den *InstanceId* -Parameter verwenden, um einen bestimmten virtuellen Computer innerhalb des VMSS zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="1d16d-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="1d16d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d16d-109">EXAMPLES</span></span>

### <span data-ttu-id="1d16d-110">Beispiel 1: Entfernen eines VMSS</span><span class="sxs-lookup"><span data-stu-id="1d16d-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="1d16d-111">Mit diesem Befehl wird der VMSS mit dem Namen VMScaleSet001 entfernt, der zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="1d16d-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="1d16d-112">Beispiel 2: Entfernen eines virtuellen Computers in einem VMSS</span><span class="sxs-lookup"><span data-stu-id="1d16d-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="1d16d-113">Dieser Befehl entfernt den virtuellen Computer mit Instanz-ID 3 aus dem VMSS mit dem Namen VMScaleSet002, der zur Ressourcengruppe mit dem Namen Group002 gehört.</span><span class="sxs-lookup"><span data-stu-id="1d16d-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="1d16d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d16d-114">PARAMETERS</span></span>

### <span data-ttu-id="1d16d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d16d-115">-AsJob</span></span>
<span data-ttu-id="1d16d-116">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="1d16d-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1d16d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d16d-117">-DefaultProfile</span></span>
<span data-ttu-id="1d16d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1d16d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d16d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1d16d-119">-Force</span></span>
<span data-ttu-id="1d16d-120">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="1d16d-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1d16d-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="1d16d-121">-InstanceId</span></span>
<span data-ttu-id="1d16d-122">Gibt als Zeichenfolgenarray die ID der Instanzen an, die gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1d16d-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="1d16d-123">Zum Beispiel: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="1d16d-123">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="1d16d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d16d-124">-ResourceGroupName</span></span>
<span data-ttu-id="1d16d-125">Gibt den Namen der Ressourcengruppe an, zu der der VMSS gehört.</span><span class="sxs-lookup"><span data-stu-id="1d16d-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="1d16d-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1d16d-126">-VMScaleSetName</span></span>
<span data-ttu-id="1d16d-127">Art der Name des VMSS, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="1d16d-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="1d16d-128">Wenn Sie den *InstanceId* -Parameter angeben, entfernt das Cmdlet den angegebenen virtuellen Computer aus dem VMSS, der durch diesen Parameter benannt wird.</span><span class="sxs-lookup"><span data-stu-id="1d16d-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="1d16d-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1d16d-129">-Confirm</span></span>
<span data-ttu-id="1d16d-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d16d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d16d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d16d-131">-WhatIf</span></span>
<span data-ttu-id="1d16d-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d16d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d16d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d16d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d16d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d16d-134">CommonParameters</span></span>
<span data-ttu-id="1d16d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d16d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d16d-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d16d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d16d-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1d16d-137">INPUTS</span></span>

### <span data-ttu-id="1d16d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1d16d-138">System.String</span></span>

### <span data-ttu-id="1d16d-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="1d16d-139">System.String[]</span></span>

## <span data-ttu-id="1d16d-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1d16d-140">OUTPUTS</span></span>

### <span data-ttu-id="1d16d-141">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="1d16d-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="1d16d-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="1d16d-142">NOTES</span></span>

## <span data-ttu-id="1d16d-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1d16d-143">RELATED LINKS</span></span>

[<span data-ttu-id="1d16d-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1d16d-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="1d16d-145">Neu – AzVmss</span><span class="sxs-lookup"><span data-stu-id="1d16d-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="1d16d-146">Neustart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1d16d-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="1d16d-147">Satz-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1d16d-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="1d16d-148">Anfang-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1d16d-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="1d16d-149">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1d16d-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="1d16d-150">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1d16d-150">Update-AzVmss</span></span>](./Update-AzVmss.md)


