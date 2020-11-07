---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 69a9fd259350238175016b3245d22022845a9f51
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823803"
---
# <span data-ttu-id="43c62-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="43c62-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="43c62-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43c62-102">SYNOPSIS</span></span>
<span data-ttu-id="43c62-103">Aktualisiert eine Dienstendpunkt-Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="43c62-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="43c62-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43c62-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43c62-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43c62-105">DESCRIPTION</span></span>
<span data-ttu-id="43c62-106">Das Cmdlet " **Satz-AzServiceEndpointPolicyDefinition** " erstellt eine Dienstendpunkt-Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="43c62-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="43c62-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43c62-107">EXAMPLES</span></span>

### <span data-ttu-id="43c62-108">Beispiel 1: aktualisiert eine Dienstendpunkt-Richtliniendefinition in einer Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="43c62-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="43c62-109">Mit diesem Befehl wird eine Dienstendpunkt-Richtliniendefinition mit dem Namen Policydef1 in der vom Objekt $ServiceEndpointPolicy definierten Dienstendpunkt Richtlinie aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="43c62-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="43c62-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="43c62-110">PARAMETERS</span></span>

### <span data-ttu-id="43c62-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c62-111">-DefaultProfile</span></span>
<span data-ttu-id="43c62-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43c62-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43c62-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43c62-113">-Description</span></span>
<span data-ttu-id="43c62-114">Die Beschreibung der Definition</span><span class="sxs-lookup"><span data-stu-id="43c62-114">The description of the definition</span></span>

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

### <span data-ttu-id="43c62-115">-Name</span><span class="sxs-lookup"><span data-stu-id="43c62-115">-Name</span></span>
<span data-ttu-id="43c62-116">Der Name der Regel</span><span class="sxs-lookup"><span data-stu-id="43c62-116">The name of the rule</span></span>

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

### <span data-ttu-id="43c62-117">-Service</span><span class="sxs-lookup"><span data-stu-id="43c62-117">-Service</span></span>
<span data-ttu-id="43c62-118">Name des Diensts</span><span class="sxs-lookup"><span data-stu-id="43c62-118">Name of the service</span></span>

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

### <span data-ttu-id="43c62-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="43c62-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="43c62-120">Die NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43c62-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="43c62-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="43c62-121">-ServiceResource</span></span>
<span data-ttu-id="43c62-122">Liste der Dienst Ressourcen</span><span class="sxs-lookup"><span data-stu-id="43c62-122">List of service resources</span></span>

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

### <span data-ttu-id="43c62-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="43c62-123">-Confirm</span></span>
<span data-ttu-id="43c62-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="43c62-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43c62-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43c62-125">-WhatIf</span></span>
<span data-ttu-id="43c62-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43c62-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43c62-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43c62-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43c62-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c62-128">CommonParameters</span></span>
<span data-ttu-id="43c62-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43c62-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c62-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43c62-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c62-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43c62-131">INPUTS</span></span>

### <span data-ttu-id="43c62-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="43c62-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="43c62-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43c62-133">OUTPUTS</span></span>

### <span data-ttu-id="43c62-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="43c62-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="43c62-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="43c62-135">NOTES</span></span>

## <span data-ttu-id="43c62-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43c62-136">RELATED LINKS</span></span>

[<span data-ttu-id="43c62-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="43c62-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="43c62-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="43c62-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="43c62-139">Neu – AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="43c62-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="43c62-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="43c62-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
