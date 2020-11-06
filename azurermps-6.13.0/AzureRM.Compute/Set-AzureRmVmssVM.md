---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: f71e827769015b7abe4d503064d97ec1d3c1228b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502182"
---
# <span data-ttu-id="077a4-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="077a4-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="077a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="077a4-102">SYNOPSIS</span></span>
<span data-ttu-id="077a4-103">Ändert den Zustand einer VMSS-Instanz.</span><span class="sxs-lookup"><span data-stu-id="077a4-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="077a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="077a4-104">SYNTAX</span></span>

### <span data-ttu-id="077a4-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="077a4-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="077a4-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="077a4-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="077a4-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="077a4-107">RedeployMethodParameter</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="077a4-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="077a4-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="077a4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="077a4-109">DESCRIPTION</span></span>
<span data-ttu-id="077a4-110">Das Cmdlet " **Satz-AzureRmVmssVM** " ändert den Zustand einer Virtual Machine Scale Sets (VMSS)-Instanz.</span><span class="sxs-lookup"><span data-stu-id="077a4-110">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="077a4-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="077a4-111">EXAMPLES</span></span>

## <span data-ttu-id="077a4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="077a4-112">PARAMETERS</span></span>

### <span data-ttu-id="077a4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="077a4-113">-AsJob</span></span>
<span data-ttu-id="077a4-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="077a4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="077a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="077a4-115">-DefaultProfile</span></span>
<span data-ttu-id="077a4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="077a4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="077a4-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="077a4-117">-InstanceId</span></span>
<span data-ttu-id="077a4-118">Gibt die ID der VMSS-Instanz an, für die dieses Cmdlet den Zustand geändert hat.</span><span class="sxs-lookup"><span data-stu-id="077a4-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077a4-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="077a4-119">-PerformMaintenance</span></span>
<span data-ttu-id="077a4-120">Gibt an, dass dieses Cmdlet die Wartung auf einem virtuellen Computer im VMSS ausführt.</span><span class="sxs-lookup"><span data-stu-id="077a4-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="077a4-121">– Erneute Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="077a4-121">-Redeploy</span></span>
<span data-ttu-id="077a4-122">Gibt an, dass dieses Cmdlet einen virtuellen Computer im VMSS erneut bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="077a4-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="077a4-123">-Reimage</span><span class="sxs-lookup"><span data-stu-id="077a4-123">-Reimage</span></span>
<span data-ttu-id="077a4-124">Gibt an, dass dieses Cmdlet die VMSS-Instanz erneut abbildet.</span><span class="sxs-lookup"><span data-stu-id="077a4-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="077a4-125">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="077a4-125">-ReimageAll</span></span>
<span data-ttu-id="077a4-126">Gibt an, dass das Cmdlet alle Datenträger in der VMSS-Instanz umbildet.</span><span class="sxs-lookup"><span data-stu-id="077a4-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="077a4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="077a4-127">-ResourceGroupName</span></span>
<span data-ttu-id="077a4-128">Gibt den Namen der Ressourcengruppe an, die die VMSS-Instanz enthält.</span><span class="sxs-lookup"><span data-stu-id="077a4-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="077a4-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="077a4-129">-VMScaleSetName</span></span>
<span data-ttu-id="077a4-130">Gibt den Namen der VMSS-Instanz an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="077a4-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="077a4-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="077a4-131">-Confirm</span></span>
<span data-ttu-id="077a4-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="077a4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="077a4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="077a4-133">-WhatIf</span></span>
<span data-ttu-id="077a4-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="077a4-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="077a4-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="077a4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="077a4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="077a4-136">CommonParameters</span></span>
<span data-ttu-id="077a4-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="077a4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="077a4-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="077a4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="077a4-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="077a4-139">INPUTS</span></span>

### <span data-ttu-id="077a4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="077a4-140">System.String</span></span>

## <span data-ttu-id="077a4-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="077a4-141">OUTPUTS</span></span>

### <span data-ttu-id="077a4-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="077a4-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="077a4-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="077a4-143">NOTES</span></span>

## <span data-ttu-id="077a4-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="077a4-144">RELATED LINKS</span></span>

[<span data-ttu-id="077a4-145">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="077a4-145">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
