---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 634beeaf33515ac5e89011ab47eaea34eccaa581
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822996"
---
# <span data-ttu-id="f1cae-101">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1cae-101">New-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="f1cae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1cae-102">SYNOPSIS</span></span>
<span data-ttu-id="f1cae-103">Erstellt eine Dienstendpunkt-Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="f1cae-103">Creates a service endpoint policy definition.</span></span>

## <span data-ttu-id="f1cae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1cae-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicyDefinition -Name <String> [-Description <String>] [-ServiceResource <String[]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1cae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1cae-105">DESCRIPTION</span></span>
<span data-ttu-id="f1cae-106">Mit dem Cmdlet **New-AzServiceEndpointPolicyDefinition** erstellen Sie eine Definition für Dienstendpunkt Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="f1cae-106">The **New-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="f1cae-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1cae-107">EXAMPLES</span></span>

### <span data-ttu-id="f1cae-108">Beispiel 1: Erstellen einer Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f1cae-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="f1cae-109">Mit diesem Befehl wird die Definition der Dienstendpunkt Richtlinie mit dem Namen ServiceEndpointPolicyDefinition1, dem Dienst Microsoft. Storage, den Dienst Ressourcen Abonnements/-Sub1 und der Beschreibung "neue Definition" erstellt, die zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und in der $policydef-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f1cae-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="f1cae-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1cae-110">PARAMETERS</span></span>

### <span data-ttu-id="f1cae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1cae-111">-DefaultProfile</span></span>
<span data-ttu-id="f1cae-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1cae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1cae-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1cae-113">-Description</span></span>
<span data-ttu-id="f1cae-114">Die Beschreibung der Definition</span><span class="sxs-lookup"><span data-stu-id="f1cae-114">The description of the definition</span></span>

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

### <span data-ttu-id="f1cae-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f1cae-115">-Name</span></span>
<span data-ttu-id="f1cae-116">Der Name der Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f1cae-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="f1cae-117">-Service</span><span class="sxs-lookup"><span data-stu-id="f1cae-117">-Service</span></span>
<span data-ttu-id="f1cae-118">Name des Diensts</span><span class="sxs-lookup"><span data-stu-id="f1cae-118">Name of the service</span></span>

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

### <span data-ttu-id="f1cae-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="f1cae-119">-ServiceResource</span></span>
<span data-ttu-id="f1cae-120">Liste der Dienst Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f1cae-120">List of service resources</span></span>

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

### <span data-ttu-id="f1cae-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1cae-121">-Confirm</span></span>
<span data-ttu-id="f1cae-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1cae-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1cae-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1cae-123">-WhatIf</span></span>
<span data-ttu-id="f1cae-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1cae-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1cae-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1cae-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1cae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1cae-126">CommonParameters</span></span>
<span data-ttu-id="f1cae-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1cae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1cae-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1cae-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1cae-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1cae-129">INPUTS</span></span>

### <span data-ttu-id="f1cae-130">Keine</span><span class="sxs-lookup"><span data-stu-id="f1cae-130">None</span></span>

## <span data-ttu-id="f1cae-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1cae-131">OUTPUTS</span></span>

### <span data-ttu-id="f1cae-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1cae-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="f1cae-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1cae-133">NOTES</span></span>

## <span data-ttu-id="f1cae-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1cae-134">RELATED LINKS</span></span>

[<span data-ttu-id="f1cae-135">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1cae-135">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f1cae-136">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1cae-136">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f1cae-137">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1cae-137">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f1cae-138">Satz-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1cae-138">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
