---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
ms.openlocfilehash: 5ccaccdc5d447ac9ccdc49cf53230c58a5758e4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368848"
---
# <span data-ttu-id="dc9ef-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="dc9ef-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="dc9ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc9ef-102">SYNOPSIS</span></span>
<span data-ttu-id="dc9ef-103">Bewerten sie den Patchstatus eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="dc9ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc9ef-104">SYNTAX</span></span>

### <span data-ttu-id="dc9ef-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc9ef-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc9ef-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc9ef-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc9ef-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc9ef-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc9ef-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc9ef-108">DESCRIPTION</span></span>
<span data-ttu-id="dc9ef-109">Bewertet den Patchstatus einer VM und meldet alle erkannten Patches, die zur Installation verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="dc9ef-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dc9ef-110">EXAMPLES</span></span>

### <span data-ttu-id="dc9ef-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dc9ef-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="dc9ef-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc9ef-112">PARAMETERS</span></span>

### <span data-ttu-id="dc9ef-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc9ef-113">-AsJob</span></span>
<span data-ttu-id="dc9ef-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="dc9ef-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc9ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc9ef-115">-DefaultProfile</span></span>
<span data-ttu-id="dc9ef-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc9ef-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc9ef-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc9ef-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc9ef-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc9ef-119">-ResourceId</span></span>
<span data-ttu-id="dc9ef-120">Ressourcen-ID für Ihren virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-120">Resource ID for your virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc9ef-121">-VM</span><span class="sxs-lookup"><span data-stu-id="dc9ef-121">-VM</span></span>
<span data-ttu-id="dc9ef-122">PowerShell Virtual Machine Object</span><span class="sxs-lookup"><span data-stu-id="dc9ef-122">PowerShell Virtual Machine Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: InputObjectParameterSet
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc9ef-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="dc9ef-123">-VMName</span></span>
<span data-ttu-id="dc9ef-124">Name des virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="dc9ef-124">Virtual Machine name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc9ef-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc9ef-125">-Confirm</span></span>
<span data-ttu-id="dc9ef-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc9ef-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dc9ef-127">-WhatIf</span></span>
<span data-ttu-id="dc9ef-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc9ef-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc9ef-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc9ef-130">CommonParameters</span></span>
<span data-ttu-id="dc9ef-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc9ef-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc9ef-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc9ef-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dc9ef-133">INPUTS</span></span>

### <span data-ttu-id="dc9ef-134">System.String</span><span class="sxs-lookup"><span data-stu-id="dc9ef-134">System.String</span></span>

## <span data-ttu-id="dc9ef-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dc9ef-135">OUTPUTS</span></span>

### <span data-ttu-id="dc9ef-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span><span class="sxs-lookup"><span data-stu-id="dc9ef-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="dc9ef-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dc9ef-137">NOTES</span></span>

## <span data-ttu-id="dc9ef-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dc9ef-138">RELATED LINKS</span></span>
