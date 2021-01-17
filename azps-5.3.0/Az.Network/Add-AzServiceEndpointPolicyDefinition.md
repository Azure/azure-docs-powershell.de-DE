---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: eaab1bdf26fb1cb99bfa7e947a4b7140971fda53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467439"
---
# <span data-ttu-id="91771-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="91771-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="91771-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91771-102">SYNOPSIS</span></span>
<span data-ttu-id="91771-103">Fügt einer angegebenen Richtlinie eine Richtlinie für den Dienstendpunkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="91771-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="91771-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91771-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91771-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91771-105">DESCRIPTION</span></span>
<span data-ttu-id="91771-106">Das **Cmdlet "Add-AzServiceEndpointPolicyDefinition"** fügt der Richtlinie eine Richtlinie für den Dienstendpunkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="91771-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="91771-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="91771-107">EXAMPLES</span></span>

### <span data-ttu-id="91771-108">Beispiel 1: Aktualisiert die Definition einer Dienstendpunktrichtlinie in einer Dienstendpunktrichtlinie</span><span class="sxs-lookup"><span data-stu-id="91771-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="91771-109">Mit diesem Befehl wurde die Richtliniendefinition für den Dienstendpunkt mit dem Namen "ServiceEndpointPolicyDefinition1", dem Dienst "Microsoft.Storage", "service resources subscriptions/sub1" und der Beschreibung "New Definition" aktualisiert, die zur Ressourcengruppe "ResourceGroup01" gehört und in der Variablen "$policydef" gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="91771-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="91771-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91771-110">PARAMETERS</span></span>

### <span data-ttu-id="91771-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91771-111">-DefaultProfile</span></span>
<span data-ttu-id="91771-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91771-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91771-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91771-113">-Description</span></span>
<span data-ttu-id="91771-114">Beschreibung der Definition</span><span class="sxs-lookup"><span data-stu-id="91771-114">The description of the definition</span></span>

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

### <span data-ttu-id="91771-115">-Name</span><span class="sxs-lookup"><span data-stu-id="91771-115">-Name</span></span>
<span data-ttu-id="91771-116">Der Name der Richtliniendefinition für den Dienstendpunkt</span><span class="sxs-lookup"><span data-stu-id="91771-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="91771-117">-Service</span><span class="sxs-lookup"><span data-stu-id="91771-117">-Service</span></span>
<span data-ttu-id="91771-118">Name des Diensts</span><span class="sxs-lookup"><span data-stu-id="91771-118">Name of the service</span></span>

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

### <span data-ttu-id="91771-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="91771-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="91771-120">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="91771-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="91771-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="91771-121">-ServiceResource</span></span>
<span data-ttu-id="91771-122">Liste der Dienstressourcen</span><span class="sxs-lookup"><span data-stu-id="91771-122">List of service resources</span></span>

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

### <span data-ttu-id="91771-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91771-123">-Confirm</span></span>
<span data-ttu-id="91771-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91771-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91771-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="91771-125">-WhatIf</span></span>
<span data-ttu-id="91771-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91771-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91771-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91771-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91771-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91771-128">CommonParameters</span></span>
<span data-ttu-id="91771-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91771-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91771-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91771-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91771-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="91771-131">INPUTS</span></span>

### <span data-ttu-id="91771-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="91771-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="91771-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="91771-133">OUTPUTS</span></span>

### <span data-ttu-id="91771-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="91771-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="91771-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="91771-135">NOTES</span></span>

## <span data-ttu-id="91771-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="91771-136">RELATED LINKS</span></span>

[<span data-ttu-id="91771-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="91771-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="91771-138">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="91771-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="91771-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="91771-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="91771-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="91771-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
