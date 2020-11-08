---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 27124aa859fc9c97a74a3ed401c67de328d93884
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003453"
---
# <span data-ttu-id="82909-101">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="82909-101">New-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="82909-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="82909-102">SYNOPSIS</span></span>
<span data-ttu-id="82909-103">Erstellt eine Dienstendpunkt-Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="82909-103">Creates a service endpoint policy definition.</span></span>

## <span data-ttu-id="82909-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="82909-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicyDefinition -Name <String> [-Description <String>] [-ServiceResource <String[]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82909-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="82909-105">DESCRIPTION</span></span>
<span data-ttu-id="82909-106">Mit dem Cmdlet **New-AzServiceEndpointPolicyDefinition** erstellen Sie eine Definition für Dienstendpunkt Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="82909-106">The **New-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="82909-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="82909-107">EXAMPLES</span></span>

### <span data-ttu-id="82909-108">Beispiel 1: Erstellen einer Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="82909-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="82909-109">Mit diesem Befehl wird die Definition der Dienstendpunkt Richtlinie mit dem Namen ServiceEndpointPolicyDefinition1, dem Dienst Microsoft. Storage, den Dienst Ressourcen Abonnements/-Sub1 und der Beschreibung "neue Definition" erstellt, die zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und in der $policydef-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="82909-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="82909-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="82909-110">PARAMETERS</span></span>

### <span data-ttu-id="82909-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82909-111">-DefaultProfile</span></span>
<span data-ttu-id="82909-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="82909-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82909-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="82909-113">-Description</span></span>
<span data-ttu-id="82909-114">Die Beschreibung der Definition</span><span class="sxs-lookup"><span data-stu-id="82909-114">The description of the definition</span></span>

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

### <span data-ttu-id="82909-115">-Name</span><span class="sxs-lookup"><span data-stu-id="82909-115">-Name</span></span>
<span data-ttu-id="82909-116">Der Name der Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="82909-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="82909-117">-Service</span><span class="sxs-lookup"><span data-stu-id="82909-117">-Service</span></span>
<span data-ttu-id="82909-118">Name des Diensts</span><span class="sxs-lookup"><span data-stu-id="82909-118">Name of the service</span></span>

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

### <span data-ttu-id="82909-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="82909-119">-ServiceResource</span></span>
<span data-ttu-id="82909-120">Liste der Dienst Ressourcen</span><span class="sxs-lookup"><span data-stu-id="82909-120">List of service resources</span></span>

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

### <span data-ttu-id="82909-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="82909-121">-Confirm</span></span>
<span data-ttu-id="82909-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="82909-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82909-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82909-123">-WhatIf</span></span>
<span data-ttu-id="82909-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82909-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82909-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82909-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82909-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82909-126">CommonParameters</span></span>
<span data-ttu-id="82909-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82909-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82909-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82909-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82909-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="82909-129">INPUTS</span></span>

### <span data-ttu-id="82909-130">Keine</span><span class="sxs-lookup"><span data-stu-id="82909-130">None</span></span>

## <span data-ttu-id="82909-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="82909-131">OUTPUTS</span></span>

### <span data-ttu-id="82909-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="82909-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="82909-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="82909-133">NOTES</span></span>

## <span data-ttu-id="82909-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="82909-134">RELATED LINKS</span></span>

[<span data-ttu-id="82909-135">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="82909-135">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="82909-136">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="82909-136">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="82909-137">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="82909-137">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="82909-138">Satz-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="82909-138">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
