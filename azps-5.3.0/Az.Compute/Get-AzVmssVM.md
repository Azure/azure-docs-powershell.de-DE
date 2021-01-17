---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 33847b9a86d5fa39511102e964f8f2a63fce6960
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473090"
---
# <span data-ttu-id="c8459-101">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="c8459-101">Get-AzVmssVM</span></span>

## <span data-ttu-id="c8459-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8459-102">SYNOPSIS</span></span>
<span data-ttu-id="c8459-103">Ruft die Eigenschaften eines virtuellen VMSS-Computers ab.</span><span class="sxs-lookup"><span data-stu-id="c8459-103">Gets the properties of a VMSS virtual machine.</span></span>

## <span data-ttu-id="c8459-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8459-104">SYNTAX</span></span>

### <span data-ttu-id="c8459-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="c8459-105">DefaultParameter (Default)</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8459-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="c8459-106">FriendMethod</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8459-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8459-107">DESCRIPTION</span></span>
<span data-ttu-id="c8459-108">Das **Get-AzVmssVM-Cmdlet** ruft die Modellansicht und Instanzansicht eines virtuellen VMSS (Virtual Machine Scale Set) ab.</span><span class="sxs-lookup"><span data-stu-id="c8459-108">The **Get-AzVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="c8459-109">Die Modellansicht ist die vom Benutzer angegebenen Eigenschaften des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="c8459-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="c8459-110">Die Instanzansicht ist der Status der Instanzebene des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="c8459-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="c8459-111">Geben Sie den *Parameter "Status"* an, um nur die Instanzansicht eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c8459-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="c8459-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c8459-112">EXAMPLES</span></span>

### <span data-ttu-id="c8459-113">Beispiel 1: Erhalten der Eigenschaften eines virtuellen VMSS-Computers</span><span class="sxs-lookup"><span data-stu-id="c8459-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="c8459-114">Dieser Befehl ruft die Eigenschaften des virtuellen VMSS-Computers namens VMSS001 ab, der zur Ressourcengruppe "Group001" gehört.</span><span class="sxs-lookup"><span data-stu-id="c8459-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="c8459-115">Da der Befehl den Parameter des *InstanceView-Schalters* nicht anfordert, ruft das Cmdlet die Modellansicht des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="c8459-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="c8459-116">Beispiel 2: Erhalten der Modellansichtseigenschaften eines virtuellen VMSS-Computers</span><span class="sxs-lookup"><span data-stu-id="c8459-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="c8459-117">Dieser Befehl ruft die Eigenschaften des virtuellen VMSS-Computers namens VMSS004 ab, der zur Ressourcengruppe "Group002" gehört.</span><span class="sxs-lookup"><span data-stu-id="c8459-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="c8459-118">Der Befehl ruft die Instanz-ID ab, die in der Variablen gespeichert $ID, für die die Modellansicht angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8459-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="c8459-119">Beispiel 3: Erhalten der Instanzansichtseigenschaften eines virtuellen VMSS-Computers</span><span class="sxs-lookup"><span data-stu-id="c8459-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="c8459-120">Dieser Befehl ruft die Eigenschaften des virtuellen VMSS-Computers namens VMSS004 ab, der zur Ressourcengruppe "Group002" gehört.</span><span class="sxs-lookup"><span data-stu-id="c8459-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="c8459-121">Da der Befehl den *Parameter "InstanceView-Switch"* angibt, ruft das Cmdlet die Instanzansicht des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="c8459-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="c8459-122">Der Befehl ruft die Instanz-ID ab, die in der Variablen gespeichert $ID, für die die Instanzansicht angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8459-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="c8459-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8459-123">PARAMETERS</span></span>

### <span data-ttu-id="c8459-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8459-124">-DefaultProfile</span></span>
<span data-ttu-id="c8459-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8459-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8459-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c8459-126">-InstanceId</span></span>
<span data-ttu-id="c8459-127">Gibt die Instanz-ID an, für die die Modellansicht angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8459-127">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8459-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="c8459-128">-InstanceView</span></span>
<span data-ttu-id="c8459-129">Gibt an, dass dieses Cmdlet nur die Instanzansicht des virtuellen Computers erhält.</span><span class="sxs-lookup"><span data-stu-id="c8459-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="c8459-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8459-130">-ResourceGroupName</span></span>
<span data-ttu-id="c8459-131">Gibt den Namen der Ressourcengruppe der VMSS an.</span><span class="sxs-lookup"><span data-stu-id="c8459-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8459-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c8459-132">-VMScaleSetName</span></span>
<span data-ttu-id="c8459-133">Arten des Namens der VMSS.</span><span class="sxs-lookup"><span data-stu-id="c8459-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8459-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8459-134">CommonParameters</span></span>
<span data-ttu-id="c8459-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8459-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8459-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8459-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8459-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c8459-137">INPUTS</span></span>

### <span data-ttu-id="c8459-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c8459-138">System.String</span></span>

## <span data-ttu-id="c8459-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c8459-139">OUTPUTS</span></span>

### <span data-ttu-id="c8459-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="c8459-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="c8459-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c8459-141">NOTES</span></span>

## <span data-ttu-id="c8459-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c8459-142">RELATED LINKS</span></span>

[<span data-ttu-id="c8459-143">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="c8459-143">Set-AzVmssVM</span></span>](./Set-AzVmssVM.md)

[<span data-ttu-id="c8459-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c8459-144">Get-AzVmss</span></span>](./Get-AzVmss.md)


