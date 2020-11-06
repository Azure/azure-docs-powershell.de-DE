---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssRollingUpgradePolicy.md
ms.openlocfilehash: f77e018f464ffe7329d8b89cb74b8c44359d8a3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476918"
---
# <span data-ttu-id="f9ec8-101">Set-AzureRmVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="f9ec8-101">Set-AzureRmVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="f9ec8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9ec8-102">SYNOPSIS</span></span>
<span data-ttu-id="f9ec8-103">Legt die VMSS-Eigenschaften für Rolling Upgrade-Richtlinien fest.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-103">Sets the VMSS rolling upgrade policy properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9ec8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9ec8-104">SYNTAX</span></span>

```
Set-AzureRmVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9ec8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9ec8-105">DESCRIPTION</span></span>
<span data-ttu-id="f9ec8-106">Legt die VMSS-Eigenschaften für Rolling Upgrade-Richtlinien fest.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="f9ec8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9ec8-107">EXAMPLES</span></span>

### <span data-ttu-id="f9ec8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f9ec8-108">Example 1</span></span>
```
PS C:\> Set-AzureRmVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="f9ec8-109">Dieser Befehl legt 40 Prozent für MaxBatchInstance, 35 Prozent für MaxUnhealthyInstance, 30 Prozent für MaxUnhealthyUpgradedInstance und 30 Sekunden Pausenzeit zwischen den Batches für VMSS lokales Objekt $VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="f9ec8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9ec8-110">PARAMETERS</span></span>

### <span data-ttu-id="f9ec8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9ec8-111">-DefaultProfile</span></span>
<span data-ttu-id="f9ec8-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9ec8-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="f9ec8-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="f9ec8-114">Der maximale Prozentsatz der virtuellen Computer Instanzen, die vom parallelen Upgrade in einem Batch gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="f9ec8-115">Da dies ein Maximum ist, können ungesunde Instanzen in früheren oder zukünftigen Batches dazu führen, dass der Prozentsatz der Instanzen in einem Batch verringert wird, um eine höhere Zuverlässigkeit zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="f9ec8-116">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-116">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9ec8-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="f9ec8-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="f9ec8-118">Der maximale Prozentsatz der gesamten virtuellen Computer Instanzen im Skalierungs Satz, die gleichzeitig fehlerhaft sein können, entweder als Ergebnis eines Upgrades oder durch die Integritätsprüfung des virtuellen Computers in einem ungesunden Zustand, bevor das parallele Upgrade abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="f9ec8-119">Diese Einschränkung wird vor dem Starten eines Batches überprüft.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="f9ec8-120">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-120">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9ec8-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="f9ec8-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="f9ec8-122">Der maximale Prozentsatz der aktualisierten virtuellen Computer Instanzen, die sich in einem fehlerhaften Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="f9ec8-123">Diese Überprüfung erfolgt, nachdem jeder Batch aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="f9ec8-124">Wenn dieser Prozentsatz jemals überschritten wird, wird das Rolling-Update abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="f9ec8-125">Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-125">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9ec8-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="f9ec8-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="f9ec8-127">Die Wartezeit zwischen dem Abschließen des Updates für alle virtuellen Computer in einem Batch und dem Starten des nächsten Batches.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="f9ec8-128">Die Zeitdauer sollte im ISO 8601-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="f9ec8-129">Der Standardwert ist 0 Sekunden (PT0S).</span><span class="sxs-lookup"><span data-stu-id="f9ec8-129">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9ec8-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f9ec8-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f9ec8-131">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="f9ec8-132">Sie können das New-AzureRmVmssConfig-Cmdlet verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-132">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9ec8-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f9ec8-133">-Confirm</span></span>
<span data-ttu-id="f9ec8-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9ec8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9ec8-135">-WhatIf</span></span>
<span data-ttu-id="f9ec8-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9ec8-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9ec8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9ec8-138">CommonParameters</span></span>
<span data-ttu-id="f9ec8-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9ec8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9ec8-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9ec8-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9ec8-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9ec8-141">INPUTS</span></span>

### <span data-ttu-id="f9ec8-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f9ec8-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="f9ec8-143">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="f9ec8-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="f9ec8-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9ec8-144">OUTPUTS</span></span>

### <span data-ttu-id="f9ec8-145">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f9ec8-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f9ec8-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9ec8-146">NOTES</span></span>

## <span data-ttu-id="f9ec8-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9ec8-147">RELATED LINKS</span></span>
