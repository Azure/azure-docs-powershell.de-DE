---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: d5e8b16fec390c4b4d900760d3efb60abfb7da0e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296926"
---
# <span data-ttu-id="f95cb-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="f95cb-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="f95cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f95cb-102">SYNOPSIS</span></span>
<span data-ttu-id="f95cb-103">Legt die Richtlinie für die zulässige Größe virtueller Computer für eine Übungseinheit in DevTest Labs fest.</span><span class="sxs-lookup"><span data-stu-id="f95cb-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="f95cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f95cb-104">SYNTAX</span></span>

### <span data-ttu-id="f95cb-105">Aktivieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="f95cb-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f95cb-106">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="f95cb-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f95cb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f95cb-107">DESCRIPTION</span></span>
<span data-ttu-id="f95cb-108">Das **Cmdlet "Set-AzDtlAllowedVMSizesPolicy"** legt die Richtlinie für zulässige Größen für virtuelle Computer fest, die eine Liste der in einem Labor zulässigen Größen virtueller Computer angibt.</span><span class="sxs-lookup"><span data-stu-id="f95cb-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="f95cb-109">Das Cmdlet verwendet die angegebene Ressourcengruppe und den Namen der Übungseinheit zum Festlegen der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="f95cb-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="f95cb-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f95cb-110">EXAMPLES</span></span>

## <span data-ttu-id="f95cb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f95cb-111">PARAMETERS</span></span>

### <span data-ttu-id="f95cb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95cb-112">-DefaultProfile</span></span>
<span data-ttu-id="f95cb-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f95cb-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f95cb-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="f95cb-114">-Disable</span></span>
<span data-ttu-id="f95cb-115">Gibt an, dass die Richtlinie mit diesem Cmdlet deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="f95cb-115">Indicates that this cmdlet disables the policy.</span></span>

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

### <span data-ttu-id="f95cb-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="f95cb-116">-Enable</span></span>
<span data-ttu-id="f95cb-117">Gibt an, dass die Richtlinie mit diesem Cmdlet aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="f95cb-117">Indicates that this cmdlet enables the policy.</span></span>

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

### <span data-ttu-id="f95cb-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="f95cb-118">-LabName</span></span>
<span data-ttu-id="f95cb-119">Gibt den Namen der Übung an, für die dieses Cmdlet die Größenrichtlinie für virtuelle Computer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f95cb-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="f95cb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f95cb-120">-ResourceGroupName</span></span>
<span data-ttu-id="f95cb-121">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="f95cb-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="f95cb-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="f95cb-122">-VmSizes</span></span>
<span data-ttu-id="f95cb-123">Gibt als Zeichenfolgenarray die Liste der in der Übung zulässigen Größen virtueller Computer an.</span><span class="sxs-lookup"><span data-stu-id="f95cb-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

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

### <span data-ttu-id="f95cb-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f95cb-124">-Confirm</span></span>
<span data-ttu-id="f95cb-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f95cb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f95cb-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f95cb-126">-WhatIf</span></span>
<span data-ttu-id="f95cb-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f95cb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f95cb-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f95cb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f95cb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95cb-129">CommonParameters</span></span>
<span data-ttu-id="f95cb-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f95cb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95cb-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f95cb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95cb-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f95cb-132">INPUTS</span></span>

### <span data-ttu-id="f95cb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f95cb-133">System.String</span></span>

## <span data-ttu-id="f95cb-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f95cb-134">OUTPUTS</span></span>

### <span data-ttu-id="f95cb-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="f95cb-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="f95cb-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f95cb-136">NOTES</span></span>

## <span data-ttu-id="f95cb-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f95cb-137">RELATED LINKS</span></span>

[<span data-ttu-id="f95cb-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="f95cb-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)


