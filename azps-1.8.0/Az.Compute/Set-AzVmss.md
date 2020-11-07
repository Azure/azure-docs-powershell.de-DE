---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: 99f022f539ff5db9bb99537bb87fce8a8567947c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820524"
---
# <span data-ttu-id="24a05-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="24a05-101">Set-AzVmss</span></span>

## <span data-ttu-id="24a05-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24a05-102">SYNOPSIS</span></span>
<span data-ttu-id="24a05-103">Legt bestimmte Aktionen für einen angegebenen VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="24a05-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="24a05-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24a05-104">SYNTAX</span></span>

### <span data-ttu-id="24a05-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="24a05-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-TempDisk]
 [-Reimage] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24a05-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="24a05-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24a05-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="24a05-107">RedeployMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24a05-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="24a05-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24a05-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24a05-109">DESCRIPTION</span></span>
<span data-ttu-id="24a05-110">Das Cmdlet " **Set-AzVmss** " legt bestimmte Aktionen für den virtuellen Computer-Skalierungs Satz fest (VMSS).</span><span class="sxs-lookup"><span data-stu-id="24a05-110">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="24a05-111">Die einzige Aktion, die dieses Cmdlet unterstützt, ist reimage.</span><span class="sxs-lookup"><span data-stu-id="24a05-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="24a05-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24a05-112">EXAMPLES</span></span>

### <span data-ttu-id="24a05-113">Beispiel 1: umbilden einer VMSS</span><span class="sxs-lookup"><span data-stu-id="24a05-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="24a05-114">Mit diesem Befehl wird der VMSS mit dem Namen ContosoVMSS, der zur Ressourcengruppe mit dem Namen contosogroup gehört, erneut abbildet.</span><span class="sxs-lookup"><span data-stu-id="24a05-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="24a05-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="24a05-115">PARAMETERS</span></span>

### <span data-ttu-id="24a05-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24a05-116">-AsJob</span></span>
<span data-ttu-id="24a05-117">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="24a05-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="24a05-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a05-118">-DefaultProfile</span></span>
<span data-ttu-id="24a05-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24a05-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24a05-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="24a05-120">-InstanceId</span></span>
<span data-ttu-id="24a05-121">Die Instanz-ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="24a05-121">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="24a05-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="24a05-122">-PerformMaintenance</span></span>
<span data-ttu-id="24a05-123">Gibt an, dass dieses Cmdlet die Wartung mindestens einen virtuellen Computer in der VMSS ausführt.</span><span class="sxs-lookup"><span data-stu-id="24a05-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a05-124">– Erneute Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="24a05-124">-Redeploy</span></span>
<span data-ttu-id="24a05-125">Gibt an, dass das Cmdlet einen oder mehrere virtuelle Computer im VMSS erneut bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="24a05-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a05-126">-Reimage</span><span class="sxs-lookup"><span data-stu-id="24a05-126">-Reimage</span></span>
<span data-ttu-id="24a05-127">Gibt an, dass das Cmdlet die VMSS.</span><span class="sxs-lookup"><span data-stu-id="24a05-127">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a05-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="24a05-128">-ReimageAll</span></span>
<span data-ttu-id="24a05-129">Gibt an, dass das Cmdlet alle Datenträger im VMSS umbildet.</span><span class="sxs-lookup"><span data-stu-id="24a05-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="24a05-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a05-130">-ResourceGroupName</span></span>
<span data-ttu-id="24a05-131">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="24a05-131">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="24a05-132">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="24a05-132">-TempDisk</span></span>
<span data-ttu-id="24a05-133">Gibt an, ob der temporäre Datenträger erneut abgespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="24a05-133">Specifies whether to reimage temp disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a05-134">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="24a05-134">-VMScaleSetName</span></span>
<span data-ttu-id="24a05-135">Art der Name des VMSS, für das dieses Cmdlet Aktionen festlegt.</span><span class="sxs-lookup"><span data-stu-id="24a05-135">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="24a05-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="24a05-136">-Confirm</span></span>
<span data-ttu-id="24a05-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="24a05-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24a05-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24a05-138">-WhatIf</span></span>
<span data-ttu-id="24a05-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24a05-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24a05-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24a05-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24a05-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a05-141">CommonParameters</span></span>
<span data-ttu-id="24a05-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24a05-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a05-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24a05-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a05-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24a05-144">INPUTS</span></span>

### <span data-ttu-id="24a05-145">System. String</span><span class="sxs-lookup"><span data-stu-id="24a05-145">System.String</span></span>

### <span data-ttu-id="24a05-146">System. String []</span><span class="sxs-lookup"><span data-stu-id="24a05-146">System.String[]</span></span>

## <span data-ttu-id="24a05-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24a05-147">OUTPUTS</span></span>

### <span data-ttu-id="24a05-148">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="24a05-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="24a05-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="24a05-149">NOTES</span></span>

## <span data-ttu-id="24a05-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24a05-150">RELATED LINKS</span></span>

[<span data-ttu-id="24a05-151">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="24a05-151">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="24a05-152">Neu – AzVmss</span><span class="sxs-lookup"><span data-stu-id="24a05-152">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="24a05-153">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="24a05-153">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="24a05-154">Neustart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="24a05-154">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="24a05-155">Anfang-AzVmss</span><span class="sxs-lookup"><span data-stu-id="24a05-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="24a05-156">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="24a05-156">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="24a05-157">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="24a05-157">Update-AzVmss</span></span>](./Update-AzVmss.md)


