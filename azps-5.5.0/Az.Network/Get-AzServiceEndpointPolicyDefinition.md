---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 164fc5edb4bac3b90debde0aaf6205c719f5c95c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160964"
---
# <span data-ttu-id="6bbc2-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6bbc2-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="6bbc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bbc2-102">SYNOPSIS</span></span>
<span data-ttu-id="6bbc2-103">Ruft eine Richtliniendefinition für den Dienstendpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="6bbc2-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="6bbc2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6bbc2-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bbc2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6bbc2-105">DESCRIPTION</span></span>
<span data-ttu-id="6bbc2-106">Das **Cmdlet "Get-AzServiceEndpointPolicyDefinition"** ruft eine Richtliniendefinition für den Dienstendpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="6bbc2-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="6bbc2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6bbc2-107">EXAMPLES</span></span>

### <span data-ttu-id="6bbc2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6bbc2-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="6bbc2-109">Dieser Befehl ruft die Richtlinie für den Dienstendpunkt namens "ServiceEndpointPolicyDefinition1" in ServiceEndpointPolicy $Policy speichert sie in der $policydef Variable.</span><span class="sxs-lookup"><span data-stu-id="6bbc2-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="6bbc2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bbc2-110">PARAMETERS</span></span>

### <span data-ttu-id="6bbc2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bbc2-111">-DefaultProfile</span></span>
<span data-ttu-id="6bbc2-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6bbc2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bbc2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6bbc2-113">-Name</span></span>
<span data-ttu-id="6bbc2-114">Der Name der Richtliniendefinition für den Dienstendpunkt</span><span class="sxs-lookup"><span data-stu-id="6bbc2-114">The name of the service endpoint policy definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bbc2-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="6bbc2-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="6bbc2-116">Die Dienstendpunktrichtlinie</span><span class="sxs-lookup"><span data-stu-id="6bbc2-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="6bbc2-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bbc2-117">-Confirm</span></span>
<span data-ttu-id="6bbc2-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6bbc2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bbc2-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6bbc2-119">-WhatIf</span></span>
<span data-ttu-id="6bbc2-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6bbc2-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bbc2-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6bbc2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bbc2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bbc2-122">CommonParameters</span></span>
<span data-ttu-id="6bbc2-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bbc2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bbc2-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bbc2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bbc2-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6bbc2-125">INPUTS</span></span>

### <span data-ttu-id="6bbc2-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="6bbc2-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="6bbc2-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6bbc2-127">OUTPUTS</span></span>

### <span data-ttu-id="6bbc2-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6bbc2-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="6bbc2-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6bbc2-129">NOTES</span></span>

## <span data-ttu-id="6bbc2-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6bbc2-130">RELATED LINKS</span></span>

[<span data-ttu-id="6bbc2-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6bbc2-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="6bbc2-132">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6bbc2-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="6bbc2-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6bbc2-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="6bbc2-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6bbc2-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
