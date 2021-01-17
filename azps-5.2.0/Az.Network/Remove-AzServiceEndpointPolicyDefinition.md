---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 146e43ce5f1816994a1d408e215e4b3e27c2bbca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361960"
---
# <span data-ttu-id="1d2f2-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1d2f2-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="1d2f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d2f2-102">SYNOPSIS</span></span>
<span data-ttu-id="1d2f2-103">Entfernt eine Richtliniendefinition für den Dienstendpunkt.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="1d2f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d2f2-104">SYNTAX</span></span>

### <span data-ttu-id="1d2f2-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1d2f2-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d2f2-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d2f2-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d2f2-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d2f2-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d2f2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d2f2-108">DESCRIPTION</span></span>
<span data-ttu-id="1d2f2-109">Das **Cmdlet "Remove-AzServiceEndpointPolicy"** entfernt eine Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="1d2f2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1d2f2-110">EXAMPLES</span></span>

### <span data-ttu-id="1d2f2-111">Beispiel 1: Entfernt eine Dienstendpunktrichtlinie unter Verwendung des Namens</span><span class="sxs-lookup"><span data-stu-id="1d2f2-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="1d2f2-112">Mit diesem Befehl wird eine Dienstendpunktrichtlinie mit dem Namen "PolicyDef1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="1d2f2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d2f2-113">PARAMETERS</span></span>

### <span data-ttu-id="1d2f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d2f2-114">-DefaultProfile</span></span>
<span data-ttu-id="1d2f2-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d2f2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d2f2-116">-InputObject</span></span>
<span data-ttu-id="1d2f2-117">Das Richtliniendefinitionsobjekt für den Dienstendpunkt.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-117">The service endpoint policy definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d2f2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1d2f2-118">-Name</span></span>
<span data-ttu-id="1d2f2-119">Der Name der Definition des Dienstendpunkts</span><span class="sxs-lookup"><span data-stu-id="1d2f2-119">The name of the service endpoint definition</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d2f2-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d2f2-120">-ResourceId</span></span>
<span data-ttu-id="1d2f2-121">Die ID der Definition des Dienstendpunkts.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-121">The ID of the service endpoint definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d2f2-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1d2f2-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="1d2f2-123">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1d2f2-123">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d2f2-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d2f2-124">-Confirm</span></span>
<span data-ttu-id="1d2f2-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d2f2-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1d2f2-126">-WhatIf</span></span>
<span data-ttu-id="1d2f2-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d2f2-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d2f2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d2f2-129">CommonParameters</span></span>
<span data-ttu-id="1d2f2-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d2f2-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d2f2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d2f2-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1d2f2-132">INPUTS</span></span>

### <span data-ttu-id="1d2f2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1d2f2-133">System.String</span></span>

### <span data-ttu-id="1d2f2-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1d2f2-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="1d2f2-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1d2f2-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="1d2f2-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1d2f2-136">OUTPUTS</span></span>

### <span data-ttu-id="1d2f2-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1d2f2-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="1d2f2-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1d2f2-138">NOTES</span></span>

## <span data-ttu-id="1d2f2-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1d2f2-139">RELATED LINKS</span></span>

[<span data-ttu-id="1d2f2-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1d2f2-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="1d2f2-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1d2f2-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="1d2f2-142">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1d2f2-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="1d2f2-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1d2f2-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
