---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: eac0d67e2c9ffc77d9387eeb599ad624ac01fbbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945941"
---
# <span data-ttu-id="fd2a3-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fd2a3-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="fd2a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd2a3-102">SYNOPSIS</span></span>
<span data-ttu-id="fd2a3-103">Ruft eine Dienstendpunktrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="fd2a3-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="fd2a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd2a3-104">SYNTAX</span></span>

### <span data-ttu-id="fd2a3-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd2a3-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd2a3-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd2a3-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd2a3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd2a3-107">DESCRIPTION</span></span>
<span data-ttu-id="fd2a3-108">Das **Get-AzServiceEndpointPolicy-Cmdlet** ruft eine Dienstendpunktrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="fd2a3-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="fd2a3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fd2a3-109">EXAMPLES</span></span>

### <span data-ttu-id="fd2a3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fd2a3-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fd2a3-111">Dieser Befehl ruft die Dienstendpunktrichtlinie mit dem Namen ServiceEndpointPolicy1 ab, die zur Ressourcengruppe "ResourceGroup01" gehört und sie in der $policy speichert.</span><span class="sxs-lookup"><span data-stu-id="fd2a3-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="fd2a3-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fd2a3-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fd2a3-113">Dieser Befehl ruft eine Liste aller Dienstendpunktrichtlinien in der Ressourcengruppe "ResourceGroup01" ab und speichert sie in der $policyList Variablen.</span><span class="sxs-lookup"><span data-stu-id="fd2a3-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="fd2a3-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fd2a3-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="fd2a3-115">Dieser Befehl ruft eine Liste aller Dienstendpunktrichtlinien ab, die mit "ServiceEndpointPolicy" beginnen.</span><span class="sxs-lookup"><span data-stu-id="fd2a3-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="fd2a3-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fd2a3-116">PARAMETERS</span></span>

### <span data-ttu-id="fd2a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd2a3-117">-DefaultProfile</span></span>
<span data-ttu-id="fd2a3-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd2a3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd2a3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fd2a3-119">-Name</span></span>
<span data-ttu-id="fd2a3-120">Der Name der Dienstendpunktrichtlinie</span><span class="sxs-lookup"><span data-stu-id="fd2a3-120">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="fd2a3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd2a3-121">-ResourceGroupName</span></span>
<span data-ttu-id="fd2a3-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fd2a3-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="fd2a3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd2a3-123">-ResourceId</span></span>
<span data-ttu-id="fd2a3-124">Die ID der Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="fd2a3-124">The ID of the service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd2a3-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fd2a3-125">-Confirm</span></span>
<span data-ttu-id="fd2a3-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd2a3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd2a3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd2a3-127">-WhatIf</span></span>
<span data-ttu-id="fd2a3-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd2a3-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd2a3-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd2a3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd2a3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd2a3-130">CommonParameters</span></span>
<span data-ttu-id="fd2a3-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd2a3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd2a3-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd2a3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd2a3-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fd2a3-133">INPUTS</span></span>

### <span data-ttu-id="fd2a3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fd2a3-134">System.String</span></span>

## <span data-ttu-id="fd2a3-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fd2a3-135">OUTPUTS</span></span>

### <span data-ttu-id="fd2a3-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fd2a3-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="fd2a3-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fd2a3-137">NOTES</span></span>

## <span data-ttu-id="fd2a3-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fd2a3-138">RELATED LINKS</span></span>

[<span data-ttu-id="fd2a3-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fd2a3-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="fd2a3-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fd2a3-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="fd2a3-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fd2a3-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
