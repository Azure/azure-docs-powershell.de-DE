---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 146e43ce5f1816994a1d408e215e4b3e27c2bbca
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004193"
---
# <span data-ttu-id="f4eee-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4eee-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="f4eee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4eee-102">SYNOPSIS</span></span>
<span data-ttu-id="f4eee-103">Entfernt eine Dienstendpunkt-Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="f4eee-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="f4eee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4eee-104">SYNTAX</span></span>

### <span data-ttu-id="f4eee-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4eee-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4eee-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4eee-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4eee-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4eee-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4eee-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4eee-108">DESCRIPTION</span></span>
<span data-ttu-id="f4eee-109">Das Cmdlet **Remove-AzServiceEndpointPolicy** entfernt eine Dienstendpunkt Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="f4eee-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="f4eee-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4eee-110">EXAMPLES</span></span>

### <span data-ttu-id="f4eee-111">Beispiel 1: entfernt eine Dienstendpunkt-Richtlinie mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="f4eee-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="f4eee-112">Dieser Befehl entfernt eine Dienstendpunkt Richtlinie mit dem Namen PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="f4eee-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="f4eee-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4eee-113">PARAMETERS</span></span>

### <span data-ttu-id="f4eee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4eee-114">-DefaultProfile</span></span>
<span data-ttu-id="f4eee-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4eee-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4eee-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f4eee-116">-InputObject</span></span>
<span data-ttu-id="f4eee-117">Das Definitionsobjekt für Dienstendpunkt Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="f4eee-117">The service endpoint policy definition object.</span></span>

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

### <span data-ttu-id="f4eee-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f4eee-118">-Name</span></span>
<span data-ttu-id="f4eee-119">Der Name der Dienstendpunkt Definition</span><span class="sxs-lookup"><span data-stu-id="f4eee-119">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="f4eee-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f4eee-120">-ResourceId</span></span>
<span data-ttu-id="f4eee-121">Die ID der Dienstendpunkt Definition.</span><span class="sxs-lookup"><span data-stu-id="f4eee-121">The ID of the service endpoint definition.</span></span>

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

### <span data-ttu-id="f4eee-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f4eee-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="f4eee-123">Die ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f4eee-123">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="f4eee-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f4eee-124">-Confirm</span></span>
<span data-ttu-id="f4eee-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4eee-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4eee-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4eee-126">-WhatIf</span></span>
<span data-ttu-id="f4eee-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4eee-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4eee-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4eee-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4eee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4eee-129">CommonParameters</span></span>
<span data-ttu-id="f4eee-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4eee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4eee-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4eee-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4eee-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4eee-132">INPUTS</span></span>

### <span data-ttu-id="f4eee-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f4eee-133">System.String</span></span>

### <span data-ttu-id="f4eee-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4eee-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="f4eee-135">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f4eee-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f4eee-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4eee-136">OUTPUTS</span></span>

### <span data-ttu-id="f4eee-137">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f4eee-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f4eee-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4eee-138">NOTES</span></span>

## <span data-ttu-id="f4eee-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4eee-139">RELATED LINKS</span></span>

[<span data-ttu-id="f4eee-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4eee-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f4eee-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4eee-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f4eee-142">Neu – AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4eee-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f4eee-143">Satz-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4eee-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
