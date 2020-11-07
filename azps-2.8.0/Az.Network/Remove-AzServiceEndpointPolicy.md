---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: fbe09b0ce6ad997ee914bf515aeb78f3fcee7971
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822827"
---
# <span data-ttu-id="e88ca-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e88ca-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="e88ca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e88ca-102">SYNOPSIS</span></span>
<span data-ttu-id="e88ca-103">Entfernt eine Dienstendpunkt Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="e88ca-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="e88ca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e88ca-104">SYNTAX</span></span>

### <span data-ttu-id="e88ca-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e88ca-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e88ca-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e88ca-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e88ca-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e88ca-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e88ca-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e88ca-108">DESCRIPTION</span></span>
<span data-ttu-id="e88ca-109">Das Cmdlet **Remove-AzServiceEndpointPolicy** entfernt eine Dienstendpunkt Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="e88ca-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="e88ca-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e88ca-110">EXAMPLES</span></span>

### <span data-ttu-id="e88ca-111">Beispiel 1: entfernt eine Dienstendpunkt-Richtlinie mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="e88ca-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="e88ca-112">Mit diesem Befehl wird eine Dienstendpunkt-Richtlinie mit dem Namen Fischereipolitik1, der zu ResourceGroup gehört, mit dem Namen "resourcegroup1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="e88ca-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="e88ca-113">Beispiel 2: Entfernen einer Dienstendpunkt Richtlinie mithilfe des Eingabeobjekts</span><span class="sxs-lookup"><span data-stu-id="e88ca-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="e88ca-114">Dieser Befehl entfernt ein Dienstendpunkt-Richtlinienobjekt Fischereipolitik1, das zu ResourceGroup gehört, mit dem Namen "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="e88ca-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="e88ca-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e88ca-115">PARAMETERS</span></span>

### <span data-ttu-id="e88ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88ca-116">-DefaultProfile</span></span>
<span data-ttu-id="e88ca-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e88ca-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e88ca-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e88ca-118">-Force</span></span>
<span data-ttu-id="e88ca-119">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="e88ca-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88ca-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e88ca-120">-InputObject</span></span>
<span data-ttu-id="e88ca-121">Das Dienstendpunkt-Richtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="e88ca-121">The service endpoint policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e88ca-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e88ca-122">-Name</span></span>
<span data-ttu-id="e88ca-123">Der Name der Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="e88ca-123">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e88ca-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e88ca-124">-PassThru</span></span>
<span data-ttu-id="e88ca-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e88ca-125">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88ca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e88ca-126">-ResourceGroupName</span></span>
<span data-ttu-id="e88ca-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e88ca-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e88ca-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e88ca-128">-ResourceId</span></span>
<span data-ttu-id="e88ca-129">Die ID der Dienstendpunkt Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="e88ca-129">The ID of service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e88ca-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e88ca-130">-Confirm</span></span>
<span data-ttu-id="e88ca-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e88ca-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e88ca-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e88ca-132">-WhatIf</span></span>
<span data-ttu-id="e88ca-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e88ca-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e88ca-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e88ca-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e88ca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88ca-135">CommonParameters</span></span>
<span data-ttu-id="e88ca-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e88ca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88ca-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e88ca-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88ca-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e88ca-138">INPUTS</span></span>

### <span data-ttu-id="e88ca-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e88ca-139">System.String</span></span>

### <span data-ttu-id="e88ca-140">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e88ca-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="e88ca-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e88ca-141">OUTPUTS</span></span>

### <span data-ttu-id="e88ca-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e88ca-142">System.Boolean</span></span>

## <span data-ttu-id="e88ca-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="e88ca-143">NOTES</span></span>

## <span data-ttu-id="e88ca-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e88ca-144">RELATED LINKS</span></span>

[<span data-ttu-id="e88ca-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e88ca-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="e88ca-146">Neu – AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e88ca-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="e88ca-147">Satz-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e88ca-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
