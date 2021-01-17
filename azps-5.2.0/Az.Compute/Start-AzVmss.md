---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 1845e7f1e76f4b05624c9c79500389b2839d25dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362324"
---
# <span data-ttu-id="3cb23-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3cb23-101">Start-AzVmss</span></span>

## <span data-ttu-id="3cb23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cb23-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb23-103">Startet den VMSS oder eine Reihe virtueller Computer innerhalb der VMSS.</span><span class="sxs-lookup"><span data-stu-id="3cb23-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="3cb23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3cb23-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cb23-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3cb23-105">DESCRIPTION</span></span>
<span data-ttu-id="3cb23-106">Das **Cmdlet "Start-AzVmss"** startet alle virtuellen Computer innerhalb des Virtual Machine Scale Set (VMSS) oder einer Reihe virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="3cb23-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="3cb23-107">Sie können den Parameter *"InstanceId"* verwenden, um eine Reihe virtueller Computer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="3cb23-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="3cb23-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3cb23-108">EXAMPLES</span></span>

### <span data-ttu-id="3cb23-109">Beispiel 1: Starten einer bestimmten Gruppe virtueller Computer innerhalb der VMSS</span><span class="sxs-lookup"><span data-stu-id="3cb23-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="3cb23-110">Dieser Befehl startet eine bestimmte Gruppe virtueller Computer, die durch das Zeichenfolgenarray der Instanz-ID angegeben werden und zu der VMSS namens ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="3cb23-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="3cb23-111">Beispiel 2: Starten aller virtuellen Computer innerhalb der VMSS</span><span class="sxs-lookup"><span data-stu-id="3cb23-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="3cb23-112">Dieser Befehl startet alle virtuellen Computer, die der VMSS namens ContosoVMSS angehören.</span><span class="sxs-lookup"><span data-stu-id="3cb23-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="3cb23-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cb23-113">PARAMETERS</span></span>

### <span data-ttu-id="3cb23-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cb23-114">-AsJob</span></span>
<span data-ttu-id="3cb23-115">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="3cb23-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3cb23-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb23-116">-DefaultProfile</span></span>
<span data-ttu-id="3cb23-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3cb23-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cb23-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="3cb23-118">-InstanceId</span></span>
<span data-ttu-id="3cb23-119">Gibt als Zeichenfolgenarray die ID oder IDs der Instanzen an, mit denen das Cmdlet gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3cb23-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="3cb23-120">Zum Beispiel: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="3cb23-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="3cb23-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cb23-121">-ResourceGroupName</span></span>
<span data-ttu-id="3cb23-122">Gibt den Namen der Ressourcengruppe der VMSS an.</span><span class="sxs-lookup"><span data-stu-id="3cb23-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="3cb23-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3cb23-123">-VMScaleSetName</span></span>
<span data-ttu-id="3cb23-124">Gibt den Namen der VMSS an, mit dem dieses Cmdlet die virtuellen Computer startet.</span><span class="sxs-lookup"><span data-stu-id="3cb23-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="3cb23-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cb23-125">-Confirm</span></span>
<span data-ttu-id="3cb23-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3cb23-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cb23-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3cb23-127">-WhatIf</span></span>
<span data-ttu-id="3cb23-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3cb23-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cb23-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3cb23-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cb23-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb23-130">CommonParameters</span></span>
<span data-ttu-id="3cb23-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cb23-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb23-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cb23-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb23-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3cb23-133">INPUTS</span></span>

### <span data-ttu-id="3cb23-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3cb23-134">System.String</span></span>

### <span data-ttu-id="3cb23-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3cb23-135">System.String[]</span></span>

## <span data-ttu-id="3cb23-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3cb23-136">OUTPUTS</span></span>

### <span data-ttu-id="3cb23-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3cb23-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3cb23-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3cb23-138">NOTES</span></span>

## <span data-ttu-id="3cb23-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3cb23-139">RELATED LINKS</span></span>

[<span data-ttu-id="3cb23-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3cb23-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="3cb23-141">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3cb23-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="3cb23-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3cb23-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="3cb23-143">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3cb23-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="3cb23-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3cb23-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="3cb23-145">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3cb23-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="3cb23-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3cb23-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


