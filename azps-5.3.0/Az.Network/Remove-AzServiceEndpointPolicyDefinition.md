---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 146e43ce5f1816994a1d408e215e4b3e27c2bbca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470132"
---
# <span data-ttu-id="56bea-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="56bea-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="56bea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56bea-102">SYNOPSIS</span></span>
<span data-ttu-id="56bea-103">Entfernt eine Richtliniendefinition für den Dienstendpunkt.</span><span class="sxs-lookup"><span data-stu-id="56bea-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="56bea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56bea-104">SYNTAX</span></span>

### <span data-ttu-id="56bea-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="56bea-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56bea-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56bea-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56bea-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56bea-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56bea-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56bea-108">DESCRIPTION</span></span>
<span data-ttu-id="56bea-109">Das **Cmdlet "Remove-AzServiceEndpointPolicy"** entfernt eine Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="56bea-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="56bea-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="56bea-110">EXAMPLES</span></span>

### <span data-ttu-id="56bea-111">Beispiel 1: Entfernt eine Dienstendpunktrichtlinie unter Verwendung des Namens</span><span class="sxs-lookup"><span data-stu-id="56bea-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="56bea-112">Mit diesem Befehl wird eine Dienstendpunktrichtlinie mit dem Namen "PolicyDef1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="56bea-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="56bea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56bea-113">PARAMETERS</span></span>

### <span data-ttu-id="56bea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56bea-114">-DefaultProfile</span></span>
<span data-ttu-id="56bea-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56bea-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56bea-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56bea-116">-InputObject</span></span>
<span data-ttu-id="56bea-117">Das Richtliniendefinitionsobjekt für den Dienstendpunkt.</span><span class="sxs-lookup"><span data-stu-id="56bea-117">The service endpoint policy definition object.</span></span>

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

### <span data-ttu-id="56bea-118">-Name</span><span class="sxs-lookup"><span data-stu-id="56bea-118">-Name</span></span>
<span data-ttu-id="56bea-119">Der Name der Definition des Dienstendpunkts</span><span class="sxs-lookup"><span data-stu-id="56bea-119">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="56bea-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56bea-120">-ResourceId</span></span>
<span data-ttu-id="56bea-121">Die ID der Definition des Dienstendpunkts.</span><span class="sxs-lookup"><span data-stu-id="56bea-121">The ID of the service endpoint definition.</span></span>

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

### <span data-ttu-id="56bea-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="56bea-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="56bea-123">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="56bea-123">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="56bea-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56bea-124">-Confirm</span></span>
<span data-ttu-id="56bea-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56bea-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56bea-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="56bea-126">-WhatIf</span></span>
<span data-ttu-id="56bea-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56bea-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56bea-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56bea-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56bea-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56bea-129">CommonParameters</span></span>
<span data-ttu-id="56bea-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56bea-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56bea-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56bea-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56bea-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="56bea-132">INPUTS</span></span>

### <span data-ttu-id="56bea-133">System.String</span><span class="sxs-lookup"><span data-stu-id="56bea-133">System.String</span></span>

### <span data-ttu-id="56bea-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="56bea-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="56bea-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="56bea-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="56bea-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="56bea-136">OUTPUTS</span></span>

### <span data-ttu-id="56bea-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="56bea-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="56bea-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="56bea-138">NOTES</span></span>

## <span data-ttu-id="56bea-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="56bea-139">RELATED LINKS</span></span>

[<span data-ttu-id="56bea-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="56bea-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="56bea-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="56bea-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="56bea-142">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="56bea-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="56bea-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="56bea-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
