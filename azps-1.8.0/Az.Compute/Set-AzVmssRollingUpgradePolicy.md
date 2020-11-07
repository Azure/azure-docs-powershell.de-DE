---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
ms.openlocfilehash: c3b43c9a040d915248df6c6082c5b525114664cf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820515"
---
# <span data-ttu-id="6302a-101">Set-AzVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="6302a-101">Set-AzVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="6302a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6302a-102">SYNOPSIS</span></span>
<span data-ttu-id="6302a-103">Legt die VMSS-Eigenschaften für Rolling Upgrade-Richtlinien fest.</span><span class="sxs-lookup"><span data-stu-id="6302a-103">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="6302a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6302a-104">SYNTAX</span></span>

```
Set-AzVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6302a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6302a-105">DESCRIPTION</span></span>
<span data-ttu-id="6302a-106">Legt die VMSS-Eigenschaften für Rolling Upgrade-Richtlinien fest.</span><span class="sxs-lookup"><span data-stu-id="6302a-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="6302a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6302a-107">EXAMPLES</span></span>

### <span data-ttu-id="6302a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6302a-108">Example 1</span></span>
```
PS C:\> Set-AzVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="6302a-109">Dieser Befehl legt 40 Prozent für MaxBatchInstance, 35 Prozent für MaxUnhealthyInstance, 30 Prozent für MaxUnhealthyUpgradedInstance und 30 Sekunden Pausenzeit zwischen den Batches für VMSS lokales Objekt $VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="6302a-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="6302a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6302a-110">PARAMETERS</span></span>

### <span data-ttu-id="6302a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6302a-111">-DefaultProfile</span></span>
<span data-ttu-id="6302a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6302a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6302a-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="6302a-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="6302a-114">Der maximale Prozentsatz der virtuellen Computer Instanzen, die vom parallelen Upgrade in einem Batch gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6302a-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="6302a-115">Da dies ein Maximum ist, können ungesunde Instanzen in früheren oder zukünftigen Batches dazu führen, dass der Prozentsatz der Instanzen in einem Batch verringert wird, um eine höhere Zuverlässigkeit zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="6302a-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="6302a-116">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6302a-116">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="6302a-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="6302a-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="6302a-118">Der maximale Prozentsatz der gesamten virtuellen Computer Instanzen im Skalierungs Satz, die gleichzeitig fehlerhaft sein können, entweder als Ergebnis eines Upgrades oder durch die Integritätsprüfung des virtuellen Computers in einem ungesunden Zustand, bevor das parallele Upgrade abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="6302a-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="6302a-119">Diese Einschränkung wird vor dem Starten eines Batches überprüft.</span><span class="sxs-lookup"><span data-stu-id="6302a-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="6302a-120">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6302a-120">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="6302a-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="6302a-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="6302a-122">Der maximale Prozentsatz der aktualisierten virtuellen Computer Instanzen, die sich in einem fehlerhaften Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="6302a-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="6302a-123">Diese Überprüfung erfolgt, nachdem jeder Batch aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6302a-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="6302a-124">Wenn dieser Prozentsatz jemals überschritten wird, wird das Rolling-Update abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="6302a-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="6302a-125">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6302a-125">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="6302a-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="6302a-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="6302a-127">Die Wartezeit zwischen dem Abschließen des Updates für alle virtuellen Computer in einem Batch und dem Starten des nächsten Batches.</span><span class="sxs-lookup"><span data-stu-id="6302a-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="6302a-128">Die Zeitdauer sollte im ISO 8601-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6302a-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="6302a-129">Der Standardwert ist 0 Sekunden (PT0S).</span><span class="sxs-lookup"><span data-stu-id="6302a-129">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="6302a-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6302a-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6302a-131">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="6302a-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="6302a-132">Sie können das New-AzVmssConfig-Cmdlet verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6302a-132">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="6302a-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6302a-133">-Confirm</span></span>
<span data-ttu-id="6302a-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6302a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6302a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6302a-135">-WhatIf</span></span>
<span data-ttu-id="6302a-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6302a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6302a-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6302a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6302a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6302a-138">CommonParameters</span></span>
<span data-ttu-id="6302a-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6302a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6302a-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6302a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6302a-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6302a-141">INPUTS</span></span>

### <span data-ttu-id="6302a-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6302a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="6302a-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6302a-143">System.Int32</span></span>

### <span data-ttu-id="6302a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6302a-144">System.String</span></span>

## <span data-ttu-id="6302a-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6302a-145">OUTPUTS</span></span>

### <span data-ttu-id="6302a-146">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6302a-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6302a-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="6302a-147">NOTES</span></span>

## <span data-ttu-id="6302a-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6302a-148">RELATED LINKS</span></span>
