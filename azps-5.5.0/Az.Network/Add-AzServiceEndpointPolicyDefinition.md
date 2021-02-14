---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: eaab1bdf26fb1cb99bfa7e947a4b7140971fda53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157196"
---
# <span data-ttu-id="23b0e-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23b0e-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="23b0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="23b0e-103">Fügt einer angegebenen Richtlinie eine Richtlinie für den Dienstendpunkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="23b0e-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="23b0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23b0e-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23b0e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23b0e-105">DESCRIPTION</span></span>
<span data-ttu-id="23b0e-106">Das **Cmdlet "Add-AzServiceEndpointPolicyDefinition"** fügt der Richtlinie eine Richtlinie für den Dienstendpunkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="23b0e-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="23b0e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="23b0e-107">EXAMPLES</span></span>

### <span data-ttu-id="23b0e-108">Beispiel 1: Aktualisiert die Definition einer Dienstendpunktrichtlinie in einer Dienstendpunktrichtlinie</span><span class="sxs-lookup"><span data-stu-id="23b0e-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="23b0e-109">Mit diesem Befehl wurde die Richtliniendefinition für den Dienstendpunkt mit dem Namen "ServiceEndpointPolicyDefinition1", dem Dienst "Microsoft.Storage", den Dienstressourcenabonnements/sub1 und der Beschreibung "Neue Definition" aktualisiert, die zur Ressourcengruppe "ResourceGroup01" gehört, und diese in der Variablen "$policydef" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="23b0e-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="23b0e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23b0e-110">PARAMETERS</span></span>

### <span data-ttu-id="23b0e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23b0e-111">-DefaultProfile</span></span>
<span data-ttu-id="23b0e-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23b0e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23b0e-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23b0e-113">-Description</span></span>
<span data-ttu-id="23b0e-114">Beschreibung der Definition</span><span class="sxs-lookup"><span data-stu-id="23b0e-114">The description of the definition</span></span>

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

### <span data-ttu-id="23b0e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="23b0e-115">-Name</span></span>
<span data-ttu-id="23b0e-116">Der Name der Richtliniendefinition für den Dienstendpunkt</span><span class="sxs-lookup"><span data-stu-id="23b0e-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="23b0e-117">-Service</span><span class="sxs-lookup"><span data-stu-id="23b0e-117">-Service</span></span>
<span data-ttu-id="23b0e-118">Name des Diensts</span><span class="sxs-lookup"><span data-stu-id="23b0e-118">Name of the service</span></span>

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

### <span data-ttu-id="23b0e-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="23b0e-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="23b0e-120">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="23b0e-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="23b0e-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="23b0e-121">-ServiceResource</span></span>
<span data-ttu-id="23b0e-122">Liste der Dienstressourcen</span><span class="sxs-lookup"><span data-stu-id="23b0e-122">List of service resources</span></span>

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

### <span data-ttu-id="23b0e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23b0e-123">-Confirm</span></span>
<span data-ttu-id="23b0e-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23b0e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23b0e-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="23b0e-125">-WhatIf</span></span>
<span data-ttu-id="23b0e-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23b0e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23b0e-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23b0e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23b0e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b0e-128">CommonParameters</span></span>
<span data-ttu-id="23b0e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23b0e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23b0e-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23b0e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b0e-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="23b0e-131">INPUTS</span></span>

### <span data-ttu-id="23b0e-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="23b0e-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="23b0e-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="23b0e-133">OUTPUTS</span></span>

### <span data-ttu-id="23b0e-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="23b0e-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="23b0e-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="23b0e-135">NOTES</span></span>

## <span data-ttu-id="23b0e-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="23b0e-136">RELATED LINKS</span></span>

[<span data-ttu-id="23b0e-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23b0e-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="23b0e-138">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23b0e-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="23b0e-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23b0e-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="23b0e-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23b0e-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
