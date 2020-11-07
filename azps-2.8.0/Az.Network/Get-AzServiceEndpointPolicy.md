---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: fdff53931891ce62b2182f2c8c78d54312141f5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822271"
---
# <span data-ttu-id="eeeec-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="eeeec-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="eeeec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eeeec-102">SYNOPSIS</span></span>
<span data-ttu-id="eeeec-103">Ruft eine Dienstendpunkt Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="eeeec-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="eeeec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eeeec-104">SYNTAX</span></span>

### <span data-ttu-id="eeeec-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="eeeec-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeeec-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eeeec-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeeec-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eeeec-107">DESCRIPTION</span></span>
<span data-ttu-id="eeeec-108">Das Cmdlet " **Get-AzServiceEndpointPolicy** " Ruft eine Dienstendpunkt Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="eeeec-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="eeeec-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eeeec-109">EXAMPLES</span></span>

### <span data-ttu-id="eeeec-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eeeec-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="eeeec-111">Dieser Befehl ruft die Dienstendpunkt Richtlinie mit dem Namen ServiceEndpointPolicy1 ab, die zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert Sie in der $Policy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="eeeec-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="eeeec-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="eeeec-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="eeeec-113">Dieser Befehl ruft eine Liste aller Dienstendpunkt Richtlinien in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert Sie in der $policyList-Variablen.</span><span class="sxs-lookup"><span data-stu-id="eeeec-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="eeeec-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="eeeec-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="eeeec-115">Dieser Befehl ruft eine Liste aller Dienstendpunkt Richtlinien ab, die mit "ServiceEndpointPolicy" beginnen.</span><span class="sxs-lookup"><span data-stu-id="eeeec-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="eeeec-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="eeeec-116">PARAMETERS</span></span>

### <span data-ttu-id="eeeec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeeec-117">-DefaultProfile</span></span>
<span data-ttu-id="eeeec-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eeeec-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eeeec-119">-Name</span><span class="sxs-lookup"><span data-stu-id="eeeec-119">-Name</span></span>
<span data-ttu-id="eeeec-120">Der Name der Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="eeeec-120">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="eeeec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeeec-121">-ResourceGroupName</span></span>
<span data-ttu-id="eeeec-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eeeec-122">The resource group name.</span></span>

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

### <span data-ttu-id="eeeec-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="eeeec-123">-ResourceId</span></span>
<span data-ttu-id="eeeec-124">Die ID der Dienstendpunkt Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="eeeec-124">The ID of the service endpoint policy.</span></span>

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

### <span data-ttu-id="eeeec-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eeeec-125">-Confirm</span></span>
<span data-ttu-id="eeeec-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eeeec-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeeec-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeeec-127">-WhatIf</span></span>
<span data-ttu-id="eeeec-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eeeec-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eeeec-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eeeec-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeeec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeeec-130">CommonParameters</span></span>
<span data-ttu-id="eeeec-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeeec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeeec-132">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eeeec-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeeec-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eeeec-133">INPUTS</span></span>

### <span data-ttu-id="eeeec-134">System. String</span><span class="sxs-lookup"><span data-stu-id="eeeec-134">System.String</span></span>

## <span data-ttu-id="eeeec-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eeeec-135">OUTPUTS</span></span>

### <span data-ttu-id="eeeec-136">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="eeeec-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="eeeec-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="eeeec-137">NOTES</span></span>

## <span data-ttu-id="eeeec-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eeeec-138">RELATED LINKS</span></span>

[<span data-ttu-id="eeeec-139">Neu – AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="eeeec-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="eeeec-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="eeeec-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="eeeec-141">Satz-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="eeeec-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
