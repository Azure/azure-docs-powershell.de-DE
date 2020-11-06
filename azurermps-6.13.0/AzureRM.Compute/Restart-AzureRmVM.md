---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVM.md
ms.openlocfilehash: f8451f4164b58c2d6599778ab86dfca4e5ff79dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480430"
---
# <span data-ttu-id="7ecf7-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7ecf7-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="7ecf7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ecf7-102">SYNOPSIS</span></span>
<span data-ttu-id="7ecf7-103">Startet einen virtuellen Azure-Computer neu.</span><span class="sxs-lookup"><span data-stu-id="7ecf7-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ecf7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ecf7-104">SYNTAX</span></span>

### <span data-ttu-id="7ecf7-105">RestartResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ecf7-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ecf7-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7ecf7-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ecf7-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7ecf7-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ecf7-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7ecf7-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ecf7-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ecf7-109">DESCRIPTION</span></span>
<span data-ttu-id="7ecf7-110">Mit dem Cmdlet " **Restart-AzureRmVM** " wird ein Azure Virtual Machine neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="7ecf7-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="7ecf7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ecf7-111">EXAMPLES</span></span>

### <span data-ttu-id="7ecf7-112">Beispiel 1: Erneutes Starten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="7ecf7-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="7ecf7-113">Mit diesem Befehl wird der virtuelle Computer mit dem Namen VirtualMachine07 in ResourceGroup11 neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="7ecf7-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="7ecf7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ecf7-114">PARAMETERS</span></span>

### <span data-ttu-id="7ecf7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ecf7-115">-AsJob</span></span>
<span data-ttu-id="7ecf7-116">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="7ecf7-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7ecf7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ecf7-117">-DefaultProfile</span></span>
<span data-ttu-id="7ecf7-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7ecf7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ecf7-119">-ID</span><span class="sxs-lookup"><span data-stu-id="7ecf7-119">-Id</span></span>
<span data-ttu-id="7ecf7-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7ecf7-120">The resource group name.</span></span>

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

### <span data-ttu-id="7ecf7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7ecf7-121">-Name</span></span>
<span data-ttu-id="7ecf7-122">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="7ecf7-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="7ecf7-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="7ecf7-123">-PerformMaintenance</span></span>
<span data-ttu-id="7ecf7-124">So führen Sie die Wartung der virtuellen Maschine durch</span><span class="sxs-lookup"><span data-stu-id="7ecf7-124">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="7ecf7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ecf7-125">-ResourceGroupName</span></span>
<span data-ttu-id="7ecf7-126">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="7ecf7-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7ecf7-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7ecf7-127">-Confirm</span></span>
<span data-ttu-id="7ecf7-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ecf7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ecf7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ecf7-129">-WhatIf</span></span>
<span data-ttu-id="7ecf7-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ecf7-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ecf7-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ecf7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ecf7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ecf7-132">CommonParameters</span></span>
<span data-ttu-id="7ecf7-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ecf7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ecf7-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ecf7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ecf7-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ecf7-135">INPUTS</span></span>

### <span data-ttu-id="7ecf7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7ecf7-136">System.String</span></span>

### <span data-ttu-id="7ecf7-137">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="7ecf7-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7ecf7-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ecf7-138">OUTPUTS</span></span>

### <span data-ttu-id="7ecf7-139">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="7ecf7-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="7ecf7-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ecf7-140">NOTES</span></span>

## <span data-ttu-id="7ecf7-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ecf7-141">RELATED LINKS</span></span>

[<span data-ttu-id="7ecf7-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7ecf7-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="7ecf7-143">Neu – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7ecf7-143">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="7ecf7-144">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7ecf7-144">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="7ecf7-145">Anfang-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7ecf7-145">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="7ecf7-146">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7ecf7-146">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="7ecf7-147">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7ecf7-147">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


