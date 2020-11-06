---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: 5fcb99a6e909675b47d245755ffd42e3c058a37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480417"
---
# <span data-ttu-id="f4aab-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f4aab-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="f4aab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4aab-102">SYNOPSIS</span></span>
<span data-ttu-id="f4aab-103">Legt bestimmte Aktionen für einen angegebenen VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="f4aab-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4aab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4aab-104">SYNTAX</span></span>

### <span data-ttu-id="f4aab-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4aab-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4aab-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="f4aab-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4aab-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="f4aab-107">RedeployMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4aab-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="f4aab-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4aab-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4aab-109">DESCRIPTION</span></span>
<span data-ttu-id="f4aab-110">Das Cmdlet " **Set-AzureRmVmss** " legt bestimmte Aktionen für den virtuellen Computer-Skalierungs Satz fest (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f4aab-110">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="f4aab-111">Die einzige Aktion, die dieses Cmdlet unterstützt, ist reimage.</span><span class="sxs-lookup"><span data-stu-id="f4aab-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="f4aab-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4aab-112">EXAMPLES</span></span>

### <span data-ttu-id="f4aab-113">Beispiel 1: umbilden einer VMSS</span><span class="sxs-lookup"><span data-stu-id="f4aab-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="f4aab-114">Mit diesem Befehl wird der VMSS mit dem Namen ContosoVMSS, der zur Ressourcengruppe mit dem Namen contosogroup gehört, erneut abbildet.</span><span class="sxs-lookup"><span data-stu-id="f4aab-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="f4aab-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4aab-115">PARAMETERS</span></span>

### <span data-ttu-id="f4aab-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4aab-116">-AsJob</span></span>
<span data-ttu-id="f4aab-117">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="f4aab-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f4aab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4aab-118">-DefaultProfile</span></span>
<span data-ttu-id="f4aab-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4aab-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4aab-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f4aab-120">-InstanceId</span></span>
<span data-ttu-id="f4aab-121">Die Instanz-ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="f4aab-121">The instance ID of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4aab-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="f4aab-122">-PerformMaintenance</span></span>
<span data-ttu-id="f4aab-123">Gibt an, dass dieses Cmdlet die Wartung mindestens einen virtuellen Computer in der VMSS ausführt.</span><span class="sxs-lookup"><span data-stu-id="f4aab-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="f4aab-124">– Erneute Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="f4aab-124">-Redeploy</span></span>
<span data-ttu-id="f4aab-125">Gibt an, dass das Cmdlet einen oder mehrere virtuelle Computer im VMSS erneut bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f4aab-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="f4aab-126">-Reimage</span><span class="sxs-lookup"><span data-stu-id="f4aab-126">-Reimage</span></span>
<span data-ttu-id="f4aab-127">Gibt an, dass das Cmdlet die VMSS.</span><span class="sxs-lookup"><span data-stu-id="f4aab-127">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="f4aab-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="f4aab-128">-ReimageAll</span></span>
<span data-ttu-id="f4aab-129">Gibt an, dass das Cmdlet alle Datenträger im VMSS umbildet.</span><span class="sxs-lookup"><span data-stu-id="f4aab-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="f4aab-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4aab-130">-ResourceGroupName</span></span>
<span data-ttu-id="f4aab-131">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="f4aab-131">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4aab-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f4aab-132">-VMScaleSetName</span></span>
<span data-ttu-id="f4aab-133">Art der Name des VMSS, für das dieses Cmdlet Aktionen festlegt.</span><span class="sxs-lookup"><span data-stu-id="f4aab-133">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4aab-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f4aab-134">-Confirm</span></span>
<span data-ttu-id="f4aab-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4aab-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4aab-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4aab-136">-WhatIf</span></span>
<span data-ttu-id="f4aab-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4aab-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4aab-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4aab-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4aab-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4aab-139">CommonParameters</span></span>
<span data-ttu-id="f4aab-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4aab-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4aab-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4aab-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4aab-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4aab-142">INPUTS</span></span>

### <span data-ttu-id="f4aab-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f4aab-143">System.String</span></span>

### <span data-ttu-id="f4aab-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="f4aab-144">System.String[]</span></span>

## <span data-ttu-id="f4aab-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4aab-145">OUTPUTS</span></span>

### <span data-ttu-id="f4aab-146">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f4aab-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f4aab-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4aab-147">NOTES</span></span>

## <span data-ttu-id="f4aab-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4aab-148">RELATED LINKS</span></span>

[<span data-ttu-id="f4aab-149">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f4aab-149">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="f4aab-150">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f4aab-150">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="f4aab-151">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f4aab-151">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="f4aab-152">Neustart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f4aab-152">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="f4aab-153">Anfang-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f4aab-153">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="f4aab-154">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f4aab-154">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="f4aab-155">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f4aab-155">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


