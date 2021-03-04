---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
ms.openlocfilehash: 16ea3a8754ef08e933412582f100296d07fcb430
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922056"
---
# <span data-ttu-id="bd396-101">Set-AzVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="bd396-101">Set-AzVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="bd396-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd396-102">SYNOPSIS</span></span>
<span data-ttu-id="bd396-103">Legt die VmSS-Richtlinieneigenschaften für das rollende Upgrade fest.</span><span class="sxs-lookup"><span data-stu-id="bd396-103">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="bd396-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd396-104">SYNTAX</span></span>

```
Set-AzVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd396-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd396-105">DESCRIPTION</span></span>
<span data-ttu-id="bd396-106">Legt die VmSS-Richtlinieneigenschaften für das rollende Upgrade fest.</span><span class="sxs-lookup"><span data-stu-id="bd396-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="bd396-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bd396-107">EXAMPLES</span></span>

### <span data-ttu-id="bd396-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bd396-108">Example 1</span></span>
```
PS C:\> Set-AzVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="bd396-109">Dieser Befehl legt 40 Prozent für MaxBatchInstance, 35 Prozent für MaxUnhealthyInstance, 30 Prozent für MaxUnhealthyUpgradedInstance und 30 Sekunden Pausenzeit zwischen Batches für lokale VMSS-Objekt-$vmss.</span><span class="sxs-lookup"><span data-stu-id="bd396-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="bd396-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bd396-110">PARAMETERS</span></span>

### <span data-ttu-id="bd396-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd396-111">-DefaultProfile</span></span>
<span data-ttu-id="bd396-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd396-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd396-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="bd396-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="bd396-114">Der maximale Prozentwert aller Instanzen virtueller Computer, die durch das fortlaufende Upgrade in einem Batch gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="bd396-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="bd396-115">Da dies eine maximale, fehlerhafte Instanz in vorherigen oder zukünftigen Batches ist, kann der Prozentsatz der Instanzen in einem Batch verringert werden, um eine höhere Zuverlässigkeit sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="bd396-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="bd396-116">Wenn der Wert nicht angegeben ist, ist er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bd396-116">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd396-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="bd396-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="bd396-118">Der maximale Prozentsatz der gesamten Instanzen virtueller Computer im Skalierungssatz, die gleichzeitig fehlerhaft sein können, entweder als Folge eines Upgrades oder durch Die Überprüfung des Zustands des virtuellen Computers in einem fehlerhaften Zustand, bevor das Rollup abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="bd396-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="bd396-119">Diese Einschränkung wird vor dem Starten eines Batches überprüft.</span><span class="sxs-lookup"><span data-stu-id="bd396-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="bd396-120">Wenn der Wert nicht angegeben ist, ist er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bd396-120">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd396-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="bd396-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="bd396-122">Der maximale Prozentsatz der aktualisierten Instanzen virtueller Computer, die sich in einem fehlerhaften Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="bd396-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="bd396-123">Diese Überprüfung wird nach dem Upgrade jedes Batches ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd396-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="bd396-124">Wenn dieser Prozentsatz jemals überschritten wurde, wird das fortlaufende Update abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="bd396-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="bd396-125">Wenn der Wert nicht angegeben ist, ist er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bd396-125">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd396-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="bd396-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="bd396-127">Die Wartezeit zwischen dem Abschließen des Updates für alle virtuellen Computer in einem Batch und dem Starten des nächsten Batches.</span><span class="sxs-lookup"><span data-stu-id="bd396-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="bd396-128">Die Zeitdauer sollte im ISO 8601-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bd396-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="bd396-129">Der Standardwert ist 0 Sekunden (PT0S).</span><span class="sxs-lookup"><span data-stu-id="bd396-129">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd396-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bd396-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="bd396-131">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="bd396-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="bd396-132">Sie können das cmdlet New-AzVmssConfig verwenden, um das -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bd396-132">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd396-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bd396-133">-Confirm</span></span>
<span data-ttu-id="bd396-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd396-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd396-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd396-135">-WhatIf</span></span>
<span data-ttu-id="bd396-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bd396-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd396-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd396-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd396-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd396-138">CommonParameters</span></span>
<span data-ttu-id="bd396-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd396-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd396-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd396-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd396-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bd396-141">INPUTS</span></span>

### <span data-ttu-id="bd396-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bd396-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="bd396-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="bd396-143">System.Int32</span></span>

### <span data-ttu-id="bd396-144">System.String</span><span class="sxs-lookup"><span data-stu-id="bd396-144">System.String</span></span>

## <span data-ttu-id="bd396-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bd396-145">OUTPUTS</span></span>

### <span data-ttu-id="bd396-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bd396-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="bd396-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bd396-147">NOTES</span></span>

## <span data-ttu-id="bd396-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bd396-148">RELATED LINKS</span></span>
