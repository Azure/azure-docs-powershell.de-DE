---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: d5e8b16fec390c4b4d900760d3efb60abfb7da0e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467847"
---
# <span data-ttu-id="e36d6-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="e36d6-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="e36d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e36d6-102">SYNOPSIS</span></span>
<span data-ttu-id="e36d6-103">Legt die Richtlinie für die zulässige Größe virtueller Computer für eine Übungseinheit in DevTest Labs fest.</span><span class="sxs-lookup"><span data-stu-id="e36d6-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="e36d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e36d6-104">SYNTAX</span></span>

### <span data-ttu-id="e36d6-105">Aktivieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="e36d6-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e36d6-106">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="e36d6-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e36d6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e36d6-107">DESCRIPTION</span></span>
<span data-ttu-id="e36d6-108">Das **Cmdlet "Set-AzDtlAllowedVMSizesPolicy"** legt die Richtlinie für zulässige Größen für virtuelle Computer fest, die eine Liste der in einem Labor zulässigen Größen virtueller Computer angibt.</span><span class="sxs-lookup"><span data-stu-id="e36d6-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="e36d6-109">Das Cmdlet verwendet die angegebene Ressourcengruppe und den Namen der Übungseinheit zum Festlegen der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="e36d6-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="e36d6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e36d6-110">EXAMPLES</span></span>

## <span data-ttu-id="e36d6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e36d6-111">PARAMETERS</span></span>

### <span data-ttu-id="e36d6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e36d6-112">-DefaultProfile</span></span>
<span data-ttu-id="e36d6-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e36d6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e36d6-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="e36d6-114">-Disable</span></span>
<span data-ttu-id="e36d6-115">Gibt an, dass die Richtlinie mit diesem Cmdlet deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="e36d6-115">Indicates that this cmdlet disables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36d6-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="e36d6-116">-Enable</span></span>
<span data-ttu-id="e36d6-117">Gibt an, dass die Richtlinie mit diesem Cmdlet aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="e36d6-117">Indicates that this cmdlet enables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36d6-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="e36d6-118">-LabName</span></span>
<span data-ttu-id="e36d6-119">Gibt den Namen der Übung an, für die dieses Cmdlet die Größenrichtlinie für virtuelle Computer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e36d6-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="e36d6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e36d6-120">-ResourceGroupName</span></span>
<span data-ttu-id="e36d6-121">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="e36d6-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="e36d6-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="e36d6-122">-VmSizes</span></span>
<span data-ttu-id="e36d6-123">Gibt als Zeichenfolgenarray die Liste der in der Übung zulässigen Größen virtueller Computer an.</span><span class="sxs-lookup"><span data-stu-id="e36d6-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36d6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e36d6-124">-Confirm</span></span>
<span data-ttu-id="e36d6-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e36d6-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36d6-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e36d6-126">-WhatIf</span></span>
<span data-ttu-id="e36d6-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e36d6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e36d6-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e36d6-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36d6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36d6-129">CommonParameters</span></span>
<span data-ttu-id="e36d6-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e36d6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36d6-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e36d6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36d6-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e36d6-132">INPUTS</span></span>

### <span data-ttu-id="e36d6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e36d6-133">System.String</span></span>

## <span data-ttu-id="e36d6-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e36d6-134">OUTPUTS</span></span>

### <span data-ttu-id="e36d6-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="e36d6-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="e36d6-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e36d6-136">NOTES</span></span>

## <span data-ttu-id="e36d6-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e36d6-137">RELATED LINKS</span></span>

[<span data-ttu-id="e36d6-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="e36d6-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)


