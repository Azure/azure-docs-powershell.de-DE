---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: a74edbec0051e3a77ab3ac10595f787dd45a2dfc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364411"
---
# <span data-ttu-id="94a99-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="94a99-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="94a99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94a99-102">SYNOPSIS</span></span>
<span data-ttu-id="94a99-103">Ruft eine Dienstendpunktrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="94a99-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="94a99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94a99-104">SYNTAX</span></span>

### <span data-ttu-id="94a99-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="94a99-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94a99-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94a99-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94a99-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94a99-107">DESCRIPTION</span></span>
<span data-ttu-id="94a99-108">Das **Cmdlet "Get-AzServiceEndpointPolicy"** ruft eine Richtlinie für den Dienstendpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="94a99-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="94a99-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="94a99-109">EXAMPLES</span></span>

### <span data-ttu-id="94a99-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="94a99-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="94a99-111">Dieser Befehl ruft die Dienstendpunktrichtlinie namens "ServiceEndpointPolicy1" ab, die zur Ressourcengruppe "ResourceGroup01" gehört, und speichert sie in der $policy Variable.</span><span class="sxs-lookup"><span data-stu-id="94a99-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="94a99-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="94a99-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="94a99-113">Dieser Befehl ruft eine Liste aller Dienstendpunktrichtlinien in der Ressourcengruppe mit dem Namen "ResourceGroup01" ab und speichert sie in der $policyList Variable.</span><span class="sxs-lookup"><span data-stu-id="94a99-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="94a99-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="94a99-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="94a99-115">Dieser Befehl ruft eine Liste aller Dienstendpunktrichtlinien ab, die mit "ServiceEndpointPolicy" beginnen.</span><span class="sxs-lookup"><span data-stu-id="94a99-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="94a99-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94a99-116">PARAMETERS</span></span>

### <span data-ttu-id="94a99-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a99-117">-DefaultProfile</span></span>
<span data-ttu-id="94a99-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94a99-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94a99-119">-Name</span><span class="sxs-lookup"><span data-stu-id="94a99-119">-Name</span></span>
<span data-ttu-id="94a99-120">Der Name der Dienstendpunktrichtlinie</span><span class="sxs-lookup"><span data-stu-id="94a99-120">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="94a99-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94a99-121">-ResourceGroupName</span></span>
<span data-ttu-id="94a99-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="94a99-122">The resource group name.</span></span>

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

### <span data-ttu-id="94a99-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94a99-123">-ResourceId</span></span>
<span data-ttu-id="94a99-124">Die ID der Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="94a99-124">The ID of the service endpoint policy.</span></span>

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

### <span data-ttu-id="94a99-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94a99-125">-Confirm</span></span>
<span data-ttu-id="94a99-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="94a99-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94a99-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="94a99-127">-WhatIf</span></span>
<span data-ttu-id="94a99-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94a99-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94a99-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94a99-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94a99-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a99-130">CommonParameters</span></span>
<span data-ttu-id="94a99-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94a99-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a99-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94a99-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a99-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="94a99-133">INPUTS</span></span>

### <span data-ttu-id="94a99-134">System.String</span><span class="sxs-lookup"><span data-stu-id="94a99-134">System.String</span></span>

## <span data-ttu-id="94a99-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="94a99-135">OUTPUTS</span></span>

### <span data-ttu-id="94a99-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="94a99-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="94a99-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="94a99-137">NOTES</span></span>

## <span data-ttu-id="94a99-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="94a99-138">RELATED LINKS</span></span>

[<span data-ttu-id="94a99-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="94a99-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="94a99-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="94a99-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="94a99-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="94a99-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
