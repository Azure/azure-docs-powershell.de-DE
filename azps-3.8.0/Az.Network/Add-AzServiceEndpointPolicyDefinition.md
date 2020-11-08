---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: eaab1bdf26fb1cb99bfa7e947a4b7140971fda53
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997242"
---
# <span data-ttu-id="1f771-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1f771-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="1f771-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f771-102">SYNOPSIS</span></span>
<span data-ttu-id="1f771-103">Fügt eine Dienstendpunkt-Richtliniendefinition zu einer angegebenen Richtlinie hinzu.</span><span class="sxs-lookup"><span data-stu-id="1f771-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="1f771-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f771-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f771-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f771-105">DESCRIPTION</span></span>
<span data-ttu-id="1f771-106">Das **Add-AzServiceEndpointPolicyDefinition-** Cmdlet fügt der Richtlinie eine Dienstendpunkt-Richtliniendefinition hinzu.</span><span class="sxs-lookup"><span data-stu-id="1f771-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="1f771-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f771-107">EXAMPLES</span></span>

### <span data-ttu-id="1f771-108">Beispiel 1: aktualisiert eine Dienstendpunkt-Richtliniendefinition in einer Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="1f771-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="1f771-109">Dieser Befehl hat die Definition der Dienstendpunkt Richtlinie mit dem Namen ServiceEndpointPolicyDefinition1, dem Dienst Microsoft. Storage, den Dienst Ressourcen Abonnements/-Sub1 und der Beschreibung "neue Definition" aktualisiert, die zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert Sie in der $policydef Variablen.</span><span class="sxs-lookup"><span data-stu-id="1f771-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="1f771-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f771-110">PARAMETERS</span></span>

### <span data-ttu-id="1f771-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f771-111">-DefaultProfile</span></span>
<span data-ttu-id="1f771-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1f771-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f771-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f771-113">-Description</span></span>
<span data-ttu-id="1f771-114">Die Beschreibung der Definition</span><span class="sxs-lookup"><span data-stu-id="1f771-114">The description of the definition</span></span>

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

### <span data-ttu-id="1f771-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1f771-115">-Name</span></span>
<span data-ttu-id="1f771-116">Der Name der Dienstendpunkt-Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="1f771-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="1f771-117">-Service</span><span class="sxs-lookup"><span data-stu-id="1f771-117">-Service</span></span>
<span data-ttu-id="1f771-118">Name des Diensts</span><span class="sxs-lookup"><span data-stu-id="1f771-118">Name of the service</span></span>

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

### <span data-ttu-id="1f771-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1f771-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="1f771-120">Die ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1f771-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="1f771-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="1f771-121">-ServiceResource</span></span>
<span data-ttu-id="1f771-122">Liste der Dienst Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1f771-122">List of service resources</span></span>

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

### <span data-ttu-id="1f771-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1f771-123">-Confirm</span></span>
<span data-ttu-id="1f771-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f771-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f771-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f771-125">-WhatIf</span></span>
<span data-ttu-id="1f771-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f771-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f771-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f771-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f771-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f771-128">CommonParameters</span></span>
<span data-ttu-id="1f771-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f771-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f771-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f771-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f771-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f771-131">INPUTS</span></span>

### <span data-ttu-id="1f771-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1f771-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="1f771-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f771-133">OUTPUTS</span></span>

### <span data-ttu-id="1f771-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1f771-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="1f771-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f771-135">NOTES</span></span>

## <span data-ttu-id="1f771-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f771-136">RELATED LINKS</span></span>

[<span data-ttu-id="1f771-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1f771-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="1f771-138">Neu – AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1f771-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="1f771-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1f771-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="1f771-140">Satz-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1f771-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
