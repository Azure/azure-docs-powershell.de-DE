---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: f7965e43c7a294d50d6f0774f76504a90c9d7148
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844332"
---
# <span data-ttu-id="31165-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="31165-101">Restart-AzVM</span></span>

## <span data-ttu-id="31165-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31165-102">SYNOPSIS</span></span>
<span data-ttu-id="31165-103">Startet einen virtuellen Azure-Computer neu.</span><span class="sxs-lookup"><span data-stu-id="31165-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="31165-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31165-104">SYNTAX</span></span>

### <span data-ttu-id="31165-105">RestartResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="31165-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31165-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="31165-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31165-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="31165-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31165-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="31165-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31165-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31165-109">DESCRIPTION</span></span>
<span data-ttu-id="31165-110">Mit dem Cmdlet " **Restart-AzVM** " wird ein Azure Virtual Machine neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="31165-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="31165-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31165-111">EXAMPLES</span></span>

### <span data-ttu-id="31165-112">Beispiel 1: Erneutes Starten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="31165-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="31165-113">Mit diesem Befehl wird der virtuelle Computer mit dem Namen VirtualMachine07 in ResourceGroup11 neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="31165-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="31165-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="31165-114">PARAMETERS</span></span>

### <span data-ttu-id="31165-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31165-115">-AsJob</span></span>
<span data-ttu-id="31165-116">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="31165-116">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31165-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31165-117">-DefaultProfile</span></span>
<span data-ttu-id="31165-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="31165-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31165-119">-ID</span><span class="sxs-lookup"><span data-stu-id="31165-119">-Id</span></span>
<span data-ttu-id="31165-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="31165-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31165-121">-Name</span><span class="sxs-lookup"><span data-stu-id="31165-121">-Name</span></span>
<span data-ttu-id="31165-122">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="31165-122">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31165-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="31165-123">-PerformMaintenance</span></span>
<span data-ttu-id="31165-124">So führen Sie die Wartung der virtuellen Maschine durch</span><span class="sxs-lookup"><span data-stu-id="31165-124">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31165-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31165-125">-ResourceGroupName</span></span>
<span data-ttu-id="31165-126">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="31165-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31165-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="31165-127">-Confirm</span></span>
<span data-ttu-id="31165-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="31165-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31165-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31165-129">-WhatIf</span></span>
<span data-ttu-id="31165-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="31165-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31165-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31165-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31165-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31165-132">CommonParameters</span></span>
<span data-ttu-id="31165-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31165-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31165-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31165-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31165-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31165-135">INPUTS</span></span>

### <span data-ttu-id="31165-136">Keine</span><span class="sxs-lookup"><span data-stu-id="31165-136">None</span></span>
<span data-ttu-id="31165-137">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="31165-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31165-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31165-138">OUTPUTS</span></span>

### <span data-ttu-id="31165-139">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="31165-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="31165-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="31165-140">NOTES</span></span>

## <span data-ttu-id="31165-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31165-141">RELATED LINKS</span></span>

[<span data-ttu-id="31165-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="31165-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="31165-143">Neu – AzVM</span><span class="sxs-lookup"><span data-stu-id="31165-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="31165-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="31165-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="31165-145">Anfang-AzVM</span><span class="sxs-lookup"><span data-stu-id="31165-145">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="31165-146">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="31165-146">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="31165-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="31165-147">Update-AzVM</span></span>](./Update-AzVM.md)


