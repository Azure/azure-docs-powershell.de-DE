---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 2ff37cec23499afb0a0bb14069dc4e694f4440f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928331"
---
# <span data-ttu-id="22656-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="22656-101">Start-AzVmss</span></span>

## <span data-ttu-id="22656-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22656-102">SYNOPSIS</span></span>
<span data-ttu-id="22656-103">Startet den VMSS oder eine Gruppe virtueller Computer innerhalb des VMSS.</span><span class="sxs-lookup"><span data-stu-id="22656-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="22656-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22656-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22656-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22656-105">DESCRIPTION</span></span>
<span data-ttu-id="22656-106">Das **Cmdlet Start-AzVmss** startet alle virtuellen Computer im VmSS (Virtual Machine Scale Set) oder einer Reihe virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="22656-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="22656-107">Sie können den *Parameter InstanzId* verwenden, um eine Gruppe virtueller Computer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="22656-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="22656-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="22656-108">EXAMPLES</span></span>

### <span data-ttu-id="22656-109">Beispiel 1: Starten einer bestimmten Gruppe virtueller Computer im VMSS</span><span class="sxs-lookup"><span data-stu-id="22656-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="22656-110">Mit diesem Befehl wird eine bestimmte Gruppe virtueller Computer gestartet, die vom Array der Instanz-ID-Zeichenfolge angegeben werden, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="22656-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="22656-111">Beispiel 2: Starten aller virtuellen Computer innerhalb des VMSS</span><span class="sxs-lookup"><span data-stu-id="22656-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="22656-112">Mit diesem Befehl werden alle virtuellen Computer gestartet, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="22656-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="22656-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="22656-113">PARAMETERS</span></span>

### <span data-ttu-id="22656-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22656-114">-AsJob</span></span>
<span data-ttu-id="22656-115">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="22656-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="22656-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22656-116">-DefaultProfile</span></span>
<span data-ttu-id="22656-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22656-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22656-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="22656-118">-InstanceId</span></span>
<span data-ttu-id="22656-119">Gibt als Zeichenfolgenarray die ID oder IDs der Instanzen an, die das Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="22656-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="22656-120">Zum Beispiel: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="22656-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="22656-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22656-121">-ResourceGroupName</span></span>
<span data-ttu-id="22656-122">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="22656-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="22656-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="22656-123">-VMScaleSetName</span></span>
<span data-ttu-id="22656-124">Gibt den Namen des VMSS an, mit dem dieses Cmdlet die virtuellen Computer startet.</span><span class="sxs-lookup"><span data-stu-id="22656-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="22656-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="22656-125">-Confirm</span></span>
<span data-ttu-id="22656-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="22656-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22656-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22656-127">-WhatIf</span></span>
<span data-ttu-id="22656-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22656-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22656-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22656-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22656-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22656-130">CommonParameters</span></span>
<span data-ttu-id="22656-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22656-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22656-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22656-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22656-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="22656-133">INPUTS</span></span>

### <span data-ttu-id="22656-134">System.String</span><span class="sxs-lookup"><span data-stu-id="22656-134">System.String</span></span>

### <span data-ttu-id="22656-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="22656-135">System.String[]</span></span>

## <span data-ttu-id="22656-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="22656-136">OUTPUTS</span></span>

### <span data-ttu-id="22656-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="22656-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="22656-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="22656-138">NOTES</span></span>

## <span data-ttu-id="22656-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="22656-139">RELATED LINKS</span></span>

[<span data-ttu-id="22656-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="22656-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="22656-141">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="22656-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="22656-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="22656-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="22656-143">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="22656-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="22656-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="22656-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="22656-145">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="22656-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="22656-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="22656-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


