---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e6e3fb3c1998a009b10599c3ea059a147ab7f9ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165566"
---
# <span data-ttu-id="750fc-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="750fc-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="750fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="750fc-102">SYNOPSIS</span></span>
<span data-ttu-id="750fc-103">Entfernt die Autorisierungsregel für einen ServiceBus-Namespace oder eine Warteschlange oder ein Thema aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="750fc-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="750fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="750fc-104">SYNTAX</span></span>

### <span data-ttu-id="750fc-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="750fc-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="750fc-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="750fc-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="750fc-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="750fc-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="750fc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="750fc-108">DESCRIPTION</span></span>
<span data-ttu-id="750fc-109">Das Cmdlet **Remove-AzServiceBusAuthorizationRule** entfernt die Autorisierungsregel für einen ServiceBus-Namespace oder eine Warteschlange oder ein Thema für die angegebene Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="750fc-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="750fc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="750fc-110">EXAMPLES</span></span>

### <span data-ttu-id="750fc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="750fc-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="750fc-112">Entfernt die Autorisierungsregel `SBAuthoRule1` für Namespace `SB-Example1` aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="750fc-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="750fc-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="750fc-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="750fc-114">Entfernt die Autorisierungsregel `SBAuthoRule1` der Warteschlange `SBQueue` aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="750fc-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="750fc-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="750fc-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="750fc-116">Entfernt die Autorisierungsregel `SBAuthoRule1` des Themas `SBTopic` aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="750fc-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="750fc-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="750fc-117">PARAMETERS</span></span>

### <span data-ttu-id="750fc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="750fc-118">-DefaultProfile</span></span>
<span data-ttu-id="750fc-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="750fc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="750fc-120">-Force</span><span class="sxs-lookup"><span data-stu-id="750fc-120">-Force</span></span>
<span data-ttu-id="750fc-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="750fc-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="750fc-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="750fc-122">-InputObject</span></span>
<span data-ttu-id="750fc-123">ServiceBus-AuthorizationRule-Objekt</span><span class="sxs-lookup"><span data-stu-id="750fc-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="750fc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="750fc-124">-Name</span></span>
<span data-ttu-id="750fc-125">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="750fc-125">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="750fc-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="750fc-126">-Namespace</span></span>
<span data-ttu-id="750fc-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="750fc-127">Namespace Name</span></span>

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

### <span data-ttu-id="750fc-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="750fc-128">-PassThru</span></span>
<span data-ttu-id="750fc-129">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="750fc-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="750fc-130">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="750fc-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="750fc-131">-Queue</span><span class="sxs-lookup"><span data-stu-id="750fc-131">-Queue</span></span>
<span data-ttu-id="750fc-132">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="750fc-132">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="750fc-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="750fc-133">-ResourceGroupName</span></span>
<span data-ttu-id="750fc-134">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="750fc-134">Resource Group Name</span></span>

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

### <span data-ttu-id="750fc-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="750fc-135">-Topic</span></span>
<span data-ttu-id="750fc-136">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="750fc-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="750fc-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="750fc-137">-Confirm</span></span>
<span data-ttu-id="750fc-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="750fc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="750fc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="750fc-139">-WhatIf</span></span>
<span data-ttu-id="750fc-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="750fc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="750fc-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="750fc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="750fc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="750fc-142">CommonParameters</span></span>
<span data-ttu-id="750fc-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="750fc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="750fc-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="750fc-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="750fc-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="750fc-145">INPUTS</span></span>

### <span data-ttu-id="750fc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="750fc-146">System.String</span></span>

### <span data-ttu-id="750fc-147">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="750fc-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="750fc-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="750fc-148">OUTPUTS</span></span>

### <span data-ttu-id="750fc-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="750fc-149">System.Boolean</span></span>

## <span data-ttu-id="750fc-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="750fc-150">NOTES</span></span>

## <span data-ttu-id="750fc-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="750fc-151">RELATED LINKS</span></span>
