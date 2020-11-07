---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 5f2c7d4c3a047a4893158e7f1a12b375106d640b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661470"
---
# <span data-ttu-id="5a7b9-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="5a7b9-101">Restart-AzVM</span></span>

## <span data-ttu-id="5a7b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a7b9-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7b9-103">Startet einen virtuellen Azure-Computer neu.</span><span class="sxs-lookup"><span data-stu-id="5a7b9-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="5a7b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a7b9-104">SYNTAX</span></span>

### <span data-ttu-id="5a7b9-105">RestartResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a7b9-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a7b9-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="5a7b9-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a7b9-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="5a7b9-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [[-Name] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a7b9-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="5a7b9-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [[-Name] <String>] [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a7b9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a7b9-109">DESCRIPTION</span></span>
<span data-ttu-id="5a7b9-110">Mit dem Cmdlet " **Restart-AzVM** " wird ein Azure Virtual Machine neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="5a7b9-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="5a7b9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a7b9-111">EXAMPLES</span></span>

### <span data-ttu-id="5a7b9-112">Beispiel 1: Erneutes Starten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="5a7b9-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="5a7b9-113">Mit diesem Befehl wird der virtuelle Computer mit dem Namen VirtualMachine07 in ResourceGroup11 neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="5a7b9-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="5a7b9-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a7b9-114">PARAMETERS</span></span>

### <span data-ttu-id="5a7b9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a7b9-115">-AsJob</span></span>
<span data-ttu-id="5a7b9-116">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="5a7b9-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5a7b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7b9-117">-DefaultProfile</span></span>
<span data-ttu-id="5a7b9-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a7b9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a7b9-119">-ID</span><span class="sxs-lookup"><span data-stu-id="5a7b9-119">-Id</span></span>
<span data-ttu-id="5a7b9-120">Die ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="5a7b9-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="5a7b9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5a7b9-121">-Name</span></span>
<span data-ttu-id="5a7b9-122">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="5a7b9-122">The virtual machine name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7b9-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="5a7b9-123">-PerformMaintenance</span></span>
<span data-ttu-id="5a7b9-124">So führen Sie die Wartung der virtuellen Maschine durch</span><span class="sxs-lookup"><span data-stu-id="5a7b9-124">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="5a7b9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a7b9-125">-ResourceGroupName</span></span>
<span data-ttu-id="5a7b9-126">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="5a7b9-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5a7b9-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5a7b9-127">-Confirm</span></span>
<span data-ttu-id="5a7b9-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a7b9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a7b9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a7b9-129">-WhatIf</span></span>
<span data-ttu-id="5a7b9-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a7b9-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a7b9-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a7b9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a7b9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7b9-132">CommonParameters</span></span>
<span data-ttu-id="5a7b9-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a7b9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7b9-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a7b9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7b9-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a7b9-135">INPUTS</span></span>

### <span data-ttu-id="5a7b9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5a7b9-136">System.String</span></span>

### <span data-ttu-id="5a7b9-137">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="5a7b9-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5a7b9-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a7b9-138">OUTPUTS</span></span>

### <span data-ttu-id="5a7b9-139">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="5a7b9-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="5a7b9-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a7b9-140">NOTES</span></span>

## <span data-ttu-id="5a7b9-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a7b9-141">RELATED LINKS</span></span>

[<span data-ttu-id="5a7b9-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="5a7b9-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="5a7b9-143">Neu – AzVM</span><span class="sxs-lookup"><span data-stu-id="5a7b9-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="5a7b9-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="5a7b9-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="5a7b9-145">Anfang-AzVM</span><span class="sxs-lookup"><span data-stu-id="5a7b9-145">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="5a7b9-146">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="5a7b9-146">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="5a7b9-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="5a7b9-147">Update-AzVM</span></span>](./Update-AzVM.md)


