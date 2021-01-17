---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: a74edbec0051e3a77ab3ac10595f787dd45a2dfc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472595"
---
# <span data-ttu-id="d8ab0-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ab0-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="d8ab0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8ab0-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ab0-103">Ruft eine Dienstendpunktrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="d8ab0-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="d8ab0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8ab0-104">SYNTAX</span></span>

### <span data-ttu-id="d8ab0-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d8ab0-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8ab0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8ab0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8ab0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8ab0-107">DESCRIPTION</span></span>
<span data-ttu-id="d8ab0-108">Das **Cmdlet "Get-AzServiceEndpointPolicy"** ruft eine Richtlinie für den Dienstendpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="d8ab0-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="d8ab0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d8ab0-109">EXAMPLES</span></span>

### <span data-ttu-id="d8ab0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d8ab0-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d8ab0-111">Dieser Befehl ruft die Dienstendpunktrichtlinie namens "ServiceEndpointPolicy1" ab, die zur Ressourcengruppe "ResourceGroup01" gehört, und speichert sie in der $policy Variable.</span><span class="sxs-lookup"><span data-stu-id="d8ab0-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="d8ab0-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d8ab0-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d8ab0-113">Dieser Befehl ruft eine Liste aller Dienstendpunktrichtlinien in der Ressourcengruppe mit dem Namen "ResourceGroup01" ab und speichert sie in der $policyList Variable.</span><span class="sxs-lookup"><span data-stu-id="d8ab0-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="d8ab0-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d8ab0-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="d8ab0-115">Dieser Befehl ruft eine Liste aller Dienstendpunktrichtlinien ab, die mit "ServiceEndpointPolicy" beginnen.</span><span class="sxs-lookup"><span data-stu-id="d8ab0-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="d8ab0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8ab0-116">PARAMETERS</span></span>

### <span data-ttu-id="d8ab0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8ab0-117">-DefaultProfile</span></span>
<span data-ttu-id="d8ab0-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8ab0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8ab0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d8ab0-119">-Name</span></span>
<span data-ttu-id="d8ab0-120">Der Name der Dienstendpunktrichtlinie</span><span class="sxs-lookup"><span data-stu-id="d8ab0-120">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="d8ab0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8ab0-121">-ResourceGroupName</span></span>
<span data-ttu-id="d8ab0-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d8ab0-122">The resource group name.</span></span>

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

### <span data-ttu-id="d8ab0-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8ab0-123">-ResourceId</span></span>
<span data-ttu-id="d8ab0-124">Die ID der Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="d8ab0-124">The ID of the service endpoint policy.</span></span>

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

### <span data-ttu-id="d8ab0-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8ab0-125">-Confirm</span></span>
<span data-ttu-id="d8ab0-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8ab0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8ab0-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d8ab0-127">-WhatIf</span></span>
<span data-ttu-id="d8ab0-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8ab0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8ab0-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8ab0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8ab0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ab0-130">CommonParameters</span></span>
<span data-ttu-id="d8ab0-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8ab0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ab0-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8ab0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ab0-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d8ab0-133">INPUTS</span></span>

### <span data-ttu-id="d8ab0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d8ab0-134">System.String</span></span>

## <span data-ttu-id="d8ab0-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d8ab0-135">OUTPUTS</span></span>

### <span data-ttu-id="d8ab0-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ab0-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="d8ab0-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d8ab0-137">NOTES</span></span>

## <span data-ttu-id="d8ab0-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d8ab0-138">RELATED LINKS</span></span>

[<span data-ttu-id="d8ab0-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ab0-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="d8ab0-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ab0-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="d8ab0-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ab0-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
