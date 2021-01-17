---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 207a07186cd7284059e0824da1f86afbc22873f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307936"
---
# <span data-ttu-id="2a827-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2a827-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="2a827-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a827-102">SYNOPSIS</span></span>
<span data-ttu-id="2a827-103">Entfernt eine Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2a827-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="2a827-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a827-104">SYNTAX</span></span>

### <span data-ttu-id="2a827-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2a827-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a827-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a827-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a827-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a827-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a827-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a827-108">DESCRIPTION</span></span>
<span data-ttu-id="2a827-109">Das **Cmdlet "Remove-AzServiceEndpointPolicy"** entfernt eine Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2a827-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="2a827-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2a827-110">EXAMPLES</span></span>

### <span data-ttu-id="2a827-111">Beispiel 1: Entfernt eine Dienstendpunktrichtlinie unter Verwendung des Namens</span><span class="sxs-lookup"><span data-stu-id="2a827-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="2a827-112">Mit diesem Befehl wird eine Dienstendpunktrichtlinie mit dem Namen "Richtlinie1" entfernt, die zu einer Ressourcengruppe mit dem Namen "resourcegroup1" gehört.</span><span class="sxs-lookup"><span data-stu-id="2a827-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="2a827-113">Beispiel 2: Entfernen einer Dienstendpunktrichtlinie mithilfe eines Eingabeobjekts</span><span class="sxs-lookup"><span data-stu-id="2a827-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="2a827-114">Mit diesem Befehl wird ein Dienstendpunktrichtlinienobjekt "Policy1" entfernt, das zu einer Ressourcengruppe mit dem Namen "resourcegroup1" gehört.</span><span class="sxs-lookup"><span data-stu-id="2a827-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="2a827-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a827-115">PARAMETERS</span></span>

### <span data-ttu-id="2a827-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a827-116">-DefaultProfile</span></span>
<span data-ttu-id="2a827-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a827-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a827-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2a827-118">-Force</span></span>
<span data-ttu-id="2a827-119">Bestätigen Sie sie nicht, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="2a827-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2a827-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a827-120">-InputObject</span></span>
<span data-ttu-id="2a827-121">Das Richtlinienobjekt für den Dienstendpunkt.</span><span class="sxs-lookup"><span data-stu-id="2a827-121">The service endpoint policy object.</span></span>

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

### <span data-ttu-id="2a827-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2a827-122">-Name</span></span>
<span data-ttu-id="2a827-123">Der Name der Dienstendpunktrichtlinie</span><span class="sxs-lookup"><span data-stu-id="2a827-123">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="2a827-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a827-124">-PassThru</span></span>
<span data-ttu-id="2a827-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2a827-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="2a827-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a827-126">-ResourceGroupName</span></span>
<span data-ttu-id="2a827-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2a827-127">The resource group name.</span></span>

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

### <span data-ttu-id="2a827-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a827-128">-ResourceId</span></span>
<span data-ttu-id="2a827-129">Die ID der Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2a827-129">The ID of service endpoint policy.</span></span>

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

### <span data-ttu-id="2a827-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a827-130">-Confirm</span></span>
<span data-ttu-id="2a827-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a827-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a827-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2a827-132">-WhatIf</span></span>
<span data-ttu-id="2a827-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a827-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a827-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a827-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a827-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a827-135">CommonParameters</span></span>
<span data-ttu-id="2a827-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a827-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a827-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a827-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a827-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2a827-138">INPUTS</span></span>

### <span data-ttu-id="2a827-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2a827-139">System.String</span></span>

### <span data-ttu-id="2a827-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2a827-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="2a827-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2a827-141">OUTPUTS</span></span>

### <span data-ttu-id="2a827-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a827-142">System.Boolean</span></span>

## <span data-ttu-id="2a827-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2a827-143">NOTES</span></span>

## <span data-ttu-id="2a827-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2a827-144">RELATED LINKS</span></span>

[<span data-ttu-id="2a827-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2a827-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="2a827-146">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2a827-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="2a827-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2a827-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
