---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: 3fc71bb4e460cb7763fc437f0bc2ac31860dccdf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659376"
---
# <span data-ttu-id="19bcc-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="19bcc-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="19bcc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="19bcc-103">Entfernen eines einzelnen IPrule zum NetworkRuleSet des angegebenen Namespaces</span><span class="sxs-lookup"><span data-stu-id="19bcc-103">Remove a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="19bcc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19bcc-104">SYNTAX</span></span>

### <span data-ttu-id="19bcc-105">IPRulePropertiesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="19bcc-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19bcc-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19bcc-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19bcc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19bcc-107">DESCRIPTION</span></span>
<span data-ttu-id="19bcc-108">Entfernen eines einzelnen IPrule zum NetworkRuleSet des angegebenen Namespaces</span><span class="sxs-lookup"><span data-stu-id="19bcc-108">Remove a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="19bcc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19bcc-109">EXAMPLES</span></span>

### <span data-ttu-id="19bcc-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="19bcc-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="19bcc-111">Entfernt IpMask des NetworkRuleSet des angegebenen Namespaces.</span><span class="sxs-lookup"><span data-stu-id="19bcc-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="19bcc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="19bcc-112">PARAMETERS</span></span>

### <span data-ttu-id="19bcc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19bcc-113">-AsJob</span></span>
<span data-ttu-id="19bcc-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="19bcc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19bcc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19bcc-115">-DefaultProfile</span></span>
<span data-ttu-id="19bcc-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="19bcc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19bcc-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="19bcc-117">-IpMask</span></span>
<span data-ttu-id="19bcc-118">Subnet-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="19bcc-118">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19bcc-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="19bcc-119">-IpRuleObject</span></span>
<span data-ttu-id="19bcc-120">IPRule-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="19bcc-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19bcc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="19bcc-121">-Name</span></span>
<span data-ttu-id="19bcc-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="19bcc-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19bcc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19bcc-123">-PassThru</span></span>
<span data-ttu-id="19bcc-124">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="19bcc-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="19bcc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19bcc-125">-ResourceGroupName</span></span>
<span data-ttu-id="19bcc-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="19bcc-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19bcc-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="19bcc-127">-Confirm</span></span>
<span data-ttu-id="19bcc-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="19bcc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19bcc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19bcc-129">-WhatIf</span></span>
<span data-ttu-id="19bcc-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="19bcc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19bcc-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19bcc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19bcc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19bcc-132">CommonParameters</span></span>
<span data-ttu-id="19bcc-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19bcc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="19bcc-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19bcc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19bcc-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19bcc-135">INPUTS</span></span>

### <span data-ttu-id="19bcc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="19bcc-136">System.String</span></span>

### <span data-ttu-id="19bcc-137">Microsoft. Azure. Commands. ServiceBus. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="19bcc-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="19bcc-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19bcc-138">OUTPUTS</span></span>

### <span data-ttu-id="19bcc-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="19bcc-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="19bcc-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="19bcc-140">NOTES</span></span>

## <span data-ttu-id="19bcc-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19bcc-141">RELATED LINKS</span></span>
