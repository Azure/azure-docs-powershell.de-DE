---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 207a07186cd7284059e0824da1f86afbc22873f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473442"
---
# <span data-ttu-id="57579-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="57579-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="57579-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57579-102">SYNOPSIS</span></span>
<span data-ttu-id="57579-103">Entfernt eine Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="57579-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="57579-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57579-104">SYNTAX</span></span>

### <span data-ttu-id="57579-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="57579-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57579-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57579-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57579-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57579-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57579-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57579-108">DESCRIPTION</span></span>
<span data-ttu-id="57579-109">Das **Cmdlet "Remove-AzServiceEndpointPolicy"** entfernt eine Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="57579-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="57579-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="57579-110">EXAMPLES</span></span>

### <span data-ttu-id="57579-111">Beispiel 1: Entfernt eine Dienstendpunktrichtlinie unter Verwendung des Namens</span><span class="sxs-lookup"><span data-stu-id="57579-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="57579-112">Mit diesem Befehl wird eine Dienstendpunktrichtlinie mit dem Namen "Richtlinie1" entfernt, die zu einer Ressourcengruppe mit dem Namen "resourcegroup1" gehört.</span><span class="sxs-lookup"><span data-stu-id="57579-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="57579-113">Beispiel 2: Entfernen einer Dienstendpunktrichtlinie mithilfe eines Eingabeobjekts</span><span class="sxs-lookup"><span data-stu-id="57579-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="57579-114">Mit diesem Befehl wird ein Dienstendpunktrichtlinienobjekt "Policy1" entfernt, das zu einer Ressourcengruppe mit dem Namen "resourcegroup1" gehört.</span><span class="sxs-lookup"><span data-stu-id="57579-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="57579-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57579-115">PARAMETERS</span></span>

### <span data-ttu-id="57579-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57579-116">-DefaultProfile</span></span>
<span data-ttu-id="57579-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57579-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57579-118">-Force</span><span class="sxs-lookup"><span data-stu-id="57579-118">-Force</span></span>
<span data-ttu-id="57579-119">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="57579-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="57579-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57579-120">-InputObject</span></span>
<span data-ttu-id="57579-121">Das Richtlinienobjekt für den Dienstendpunkt.</span><span class="sxs-lookup"><span data-stu-id="57579-121">The service endpoint policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57579-122">-Name</span><span class="sxs-lookup"><span data-stu-id="57579-122">-Name</span></span>
<span data-ttu-id="57579-123">Der Name der Dienstendpunktrichtlinie</span><span class="sxs-lookup"><span data-stu-id="57579-123">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57579-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57579-124">-PassThru</span></span>
<span data-ttu-id="57579-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="57579-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="57579-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57579-126">-ResourceGroupName</span></span>
<span data-ttu-id="57579-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="57579-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57579-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57579-128">-ResourceId</span></span>
<span data-ttu-id="57579-129">Die ID der Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="57579-129">The ID of service endpoint policy.</span></span>

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

### <span data-ttu-id="57579-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57579-130">-Confirm</span></span>
<span data-ttu-id="57579-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="57579-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57579-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="57579-132">-WhatIf</span></span>
<span data-ttu-id="57579-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="57579-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57579-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="57579-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57579-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57579-135">CommonParameters</span></span>
<span data-ttu-id="57579-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57579-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57579-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57579-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57579-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="57579-138">INPUTS</span></span>

### <span data-ttu-id="57579-139">System.String</span><span class="sxs-lookup"><span data-stu-id="57579-139">System.String</span></span>

### <span data-ttu-id="57579-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="57579-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="57579-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="57579-141">OUTPUTS</span></span>

### <span data-ttu-id="57579-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57579-142">System.Boolean</span></span>

## <span data-ttu-id="57579-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="57579-143">NOTES</span></span>

## <span data-ttu-id="57579-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="57579-144">RELATED LINKS</span></span>

[<span data-ttu-id="57579-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="57579-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="57579-146">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="57579-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="57579-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="57579-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
