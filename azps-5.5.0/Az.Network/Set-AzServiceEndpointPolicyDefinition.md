---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 46d86b6a910abcd00257277f61bb44dd426ab945
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172428"
---
# <span data-ttu-id="357fc-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="357fc-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="357fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="357fc-102">SYNOPSIS</span></span>
<span data-ttu-id="357fc-103">Aktualisiert die Richtliniendefinition für den Dienstendpunkt.</span><span class="sxs-lookup"><span data-stu-id="357fc-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="357fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="357fc-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="357fc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="357fc-105">DESCRIPTION</span></span>
<span data-ttu-id="357fc-106">Das **Cmdlet "Set-AzServiceEndpointPolicyDefinition"** erstellt eine Richtlinie für den Dienstendpunkt.</span><span class="sxs-lookup"><span data-stu-id="357fc-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="357fc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="357fc-107">EXAMPLES</span></span>

### <span data-ttu-id="357fc-108">Beispiel 1: Aktualisiert die Definition einer Dienstendpunktrichtlinie in einer Dienstendpunktrichtlinie</span><span class="sxs-lookup"><span data-stu-id="357fc-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="357fc-109">Mit diesem Befehl wird eine Richtlinie für den Dienstendpunkt namens "Policydef1" in der vom Objektobjektobjekt definierten Dienstendpunktrichtlinie $ServiceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="357fc-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="357fc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="357fc-110">PARAMETERS</span></span>

### <span data-ttu-id="357fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="357fc-111">-DefaultProfile</span></span>
<span data-ttu-id="357fc-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="357fc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="357fc-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="357fc-113">-Description</span></span>
<span data-ttu-id="357fc-114">Beschreibung der Definition</span><span class="sxs-lookup"><span data-stu-id="357fc-114">The description of the definition</span></span>

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

### <span data-ttu-id="357fc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="357fc-115">-Name</span></span>
<span data-ttu-id="357fc-116">Der Name der Regel</span><span class="sxs-lookup"><span data-stu-id="357fc-116">The name of the rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="357fc-117">-Service</span><span class="sxs-lookup"><span data-stu-id="357fc-117">-Service</span></span>
<span data-ttu-id="357fc-118">Name des Diensts</span><span class="sxs-lookup"><span data-stu-id="357fc-118">Name of the service</span></span>

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

### <span data-ttu-id="357fc-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="357fc-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="357fc-120">The NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="357fc-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="357fc-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="357fc-121">-ServiceResource</span></span>
<span data-ttu-id="357fc-122">Liste der Dienstressourcen</span><span class="sxs-lookup"><span data-stu-id="357fc-122">List of service resources</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="357fc-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="357fc-123">-Confirm</span></span>
<span data-ttu-id="357fc-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="357fc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="357fc-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="357fc-125">-WhatIf</span></span>
<span data-ttu-id="357fc-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="357fc-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="357fc-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="357fc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="357fc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="357fc-128">CommonParameters</span></span>
<span data-ttu-id="357fc-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="357fc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="357fc-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="357fc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="357fc-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="357fc-131">INPUTS</span></span>

### <span data-ttu-id="357fc-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="357fc-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="357fc-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="357fc-133">OUTPUTS</span></span>

### <span data-ttu-id="357fc-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="357fc-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="357fc-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="357fc-135">NOTES</span></span>

## <span data-ttu-id="357fc-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="357fc-136">RELATED LINKS</span></span>

[<span data-ttu-id="357fc-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="357fc-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="357fc-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="357fc-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="357fc-139">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="357fc-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="357fc-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="357fc-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
