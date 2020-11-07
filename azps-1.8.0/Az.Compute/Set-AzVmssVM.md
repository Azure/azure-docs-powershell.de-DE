---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 8e4226794a147e4c41b94355a0f47cc061cfeb8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820511"
---
# <span data-ttu-id="7a741-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="7a741-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="7a741-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7a741-102">SYNOPSIS</span></span>
<span data-ttu-id="7a741-103">Ändert den Zustand einer VMSS-Instanz.</span><span class="sxs-lookup"><span data-stu-id="7a741-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="7a741-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a741-104">SYNTAX</span></span>

### <span data-ttu-id="7a741-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a741-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a741-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="7a741-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a741-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="7a741-107">RedeployMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a741-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="7a741-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a741-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a741-109">DESCRIPTION</span></span>
<span data-ttu-id="7a741-110">Das Cmdlet " **Satz-AzVmssVM** " ändert den Zustand einer Virtual Machine Scale Sets (VMSS)-Instanz.</span><span class="sxs-lookup"><span data-stu-id="7a741-110">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="7a741-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a741-111">EXAMPLES</span></span>

## <span data-ttu-id="7a741-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a741-112">PARAMETERS</span></span>

### <span data-ttu-id="7a741-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a741-113">-AsJob</span></span>
<span data-ttu-id="7a741-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7a741-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a741-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a741-115">-DefaultProfile</span></span>
<span data-ttu-id="7a741-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7a741-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a741-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="7a741-117">-InstanceId</span></span>
<span data-ttu-id="7a741-118">Gibt die ID der VMSS-Instanz an, für die dieses Cmdlet den Zustand geändert hat.</span><span class="sxs-lookup"><span data-stu-id="7a741-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a741-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="7a741-119">-PerformMaintenance</span></span>
<span data-ttu-id="7a741-120">Gibt an, dass dieses Cmdlet die Wartung auf einem virtuellen Computer im VMSS ausführt.</span><span class="sxs-lookup"><span data-stu-id="7a741-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="7a741-121">– Erneute Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="7a741-121">-Redeploy</span></span>
<span data-ttu-id="7a741-122">Gibt an, dass dieses Cmdlet einen virtuellen Computer im VMSS erneut bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7a741-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="7a741-123">-Reimage</span><span class="sxs-lookup"><span data-stu-id="7a741-123">-Reimage</span></span>
<span data-ttu-id="7a741-124">Gibt an, dass dieses Cmdlet die VMSS-Instanz erneut abbildet.</span><span class="sxs-lookup"><span data-stu-id="7a741-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="7a741-125">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="7a741-125">-ReimageAll</span></span>
<span data-ttu-id="7a741-126">Gibt an, dass das Cmdlet alle Datenträger in der VMSS-Instanz umbildet.</span><span class="sxs-lookup"><span data-stu-id="7a741-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="7a741-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a741-127">-ResourceGroupName</span></span>
<span data-ttu-id="7a741-128">Gibt den Namen der Ressourcengruppe an, die die VMSS-Instanz enthält.</span><span class="sxs-lookup"><span data-stu-id="7a741-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="7a741-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7a741-129">-VMScaleSetName</span></span>
<span data-ttu-id="7a741-130">Gibt den Namen der VMSS-Instanz an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="7a741-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7a741-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7a741-131">-Confirm</span></span>
<span data-ttu-id="7a741-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a741-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a741-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a741-133">-WhatIf</span></span>
<span data-ttu-id="7a741-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a741-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a741-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a741-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a741-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a741-136">CommonParameters</span></span>
<span data-ttu-id="7a741-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a741-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a741-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a741-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a741-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7a741-139">INPUTS</span></span>

### <span data-ttu-id="7a741-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7a741-140">System.String</span></span>

## <span data-ttu-id="7a741-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7a741-141">OUTPUTS</span></span>

### <span data-ttu-id="7a741-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="7a741-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7a741-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="7a741-143">NOTES</span></span>

## <span data-ttu-id="7a741-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7a741-144">RELATED LINKS</span></span>

[<span data-ttu-id="7a741-145">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="7a741-145">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)
