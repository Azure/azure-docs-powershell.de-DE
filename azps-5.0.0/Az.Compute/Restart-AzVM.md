---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 358b24c403c4b08b221f97ad99271112ee0852be
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296584"
---
# <span data-ttu-id="8ad39-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="8ad39-101">Restart-AzVM</span></span>

## <span data-ttu-id="8ad39-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ad39-102">SYNOPSIS</span></span>
<span data-ttu-id="8ad39-103">Startet einen virtuellen Azure-Computer neu.</span><span class="sxs-lookup"><span data-stu-id="8ad39-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="8ad39-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ad39-104">SYNTAX</span></span>

### <span data-ttu-id="8ad39-105">RestartResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8ad39-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ad39-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8ad39-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ad39-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8ad39-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ad39-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8ad39-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ad39-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ad39-109">DESCRIPTION</span></span>
<span data-ttu-id="8ad39-110">Mit dem Cmdlet " **Restart-AzVM** " wird ein Azure Virtual Machine neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="8ad39-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="8ad39-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ad39-111">EXAMPLES</span></span>

### <span data-ttu-id="8ad39-112">Beispiel 1: Erneutes Starten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="8ad39-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="8ad39-113">Mit diesem Befehl wird der virtuelle Computer mit dem Namen VirtualMachine07 in ResourceGroup11 neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="8ad39-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="8ad39-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ad39-114">PARAMETERS</span></span>

### <span data-ttu-id="8ad39-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ad39-115">-AsJob</span></span>
<span data-ttu-id="8ad39-116">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="8ad39-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8ad39-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ad39-117">-DefaultProfile</span></span>
<span data-ttu-id="8ad39-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8ad39-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ad39-119">-ID</span><span class="sxs-lookup"><span data-stu-id="8ad39-119">-Id</span></span>
<span data-ttu-id="8ad39-120">Die ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="8ad39-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ad39-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8ad39-121">-Name</span></span>
<span data-ttu-id="8ad39-122">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="8ad39-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ad39-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8ad39-123">-NoWait</span></span>
<span data-ttu-id="8ad39-124">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="8ad39-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="8ad39-125">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="8ad39-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="8ad39-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="8ad39-126">-PerformMaintenance</span></span>
<span data-ttu-id="8ad39-127">So führen Sie die Wartung der virtuellen Maschine durch</span><span class="sxs-lookup"><span data-stu-id="8ad39-127">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ad39-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ad39-128">-ResourceGroupName</span></span>
<span data-ttu-id="8ad39-129">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="8ad39-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ad39-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8ad39-130">-Confirm</span></span>
<span data-ttu-id="8ad39-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8ad39-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ad39-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ad39-132">-WhatIf</span></span>
<span data-ttu-id="8ad39-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ad39-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ad39-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ad39-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ad39-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ad39-135">CommonParameters</span></span>
<span data-ttu-id="8ad39-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ad39-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ad39-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ad39-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ad39-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ad39-138">INPUTS</span></span>

### <span data-ttu-id="8ad39-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8ad39-139">System.String</span></span>

### <span data-ttu-id="8ad39-140">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="8ad39-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8ad39-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ad39-141">OUTPUTS</span></span>

### <span data-ttu-id="8ad39-142">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="8ad39-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="8ad39-143">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8ad39-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8ad39-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ad39-144">NOTES</span></span>

## <span data-ttu-id="8ad39-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ad39-145">RELATED LINKS</span></span>

[<span data-ttu-id="8ad39-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8ad39-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="8ad39-147">Neu – AzVM</span><span class="sxs-lookup"><span data-stu-id="8ad39-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="8ad39-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="8ad39-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="8ad39-149">Anfang-AzVM</span><span class="sxs-lookup"><span data-stu-id="8ad39-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="8ad39-150">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="8ad39-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="8ad39-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8ad39-151">Update-AzVM</span></span>](./Update-AzVM.md)


