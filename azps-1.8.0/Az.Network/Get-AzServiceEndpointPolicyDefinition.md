---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: a0e4f0c877d43ffa49737e3c3a180783a385c795
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660704"
---
# <span data-ttu-id="30075-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="30075-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="30075-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="30075-102">SYNOPSIS</span></span>
<span data-ttu-id="30075-103">Ruft eine Dienstendpunkt-Richtliniendefinition ab.</span><span class="sxs-lookup"><span data-stu-id="30075-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="30075-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="30075-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30075-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30075-105">DESCRIPTION</span></span>
<span data-ttu-id="30075-106">Das Cmdlet " **Get-AzServiceEndpointPolicyDefinition** " Ruft eine Dienstendpunkt-Richtliniendefinition ab.</span><span class="sxs-lookup"><span data-stu-id="30075-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="30075-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30075-107">EXAMPLES</span></span>

### <span data-ttu-id="30075-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="30075-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="30075-109">Dieser Befehl ruft die Dienstendpunkt-Richtliniendefinition mit dem Namen ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy ab $Policy speichert Sie in der $policydef-Variablen.</span><span class="sxs-lookup"><span data-stu-id="30075-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="30075-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="30075-110">PARAMETERS</span></span>

### <span data-ttu-id="30075-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30075-111">-DefaultProfile</span></span>
<span data-ttu-id="30075-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="30075-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30075-113">-Name</span><span class="sxs-lookup"><span data-stu-id="30075-113">-Name</span></span>
<span data-ttu-id="30075-114">Der Name der Dienstendpunkt-Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="30075-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="30075-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="30075-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="30075-116">Die Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="30075-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="30075-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="30075-117">-Confirm</span></span>
<span data-ttu-id="30075-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="30075-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30075-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30075-119">-WhatIf</span></span>
<span data-ttu-id="30075-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="30075-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30075-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30075-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30075-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30075-122">CommonParameters</span></span>
<span data-ttu-id="30075-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30075-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30075-124">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30075-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30075-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="30075-125">INPUTS</span></span>

### <span data-ttu-id="30075-126">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="30075-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="30075-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="30075-127">OUTPUTS</span></span>

### <span data-ttu-id="30075-128">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="30075-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="30075-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="30075-129">NOTES</span></span>

## <span data-ttu-id="30075-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="30075-130">RELATED LINKS</span></span>

[<span data-ttu-id="30075-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="30075-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="30075-132">Neu – AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="30075-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="30075-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="30075-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="30075-134">Satz-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="30075-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
