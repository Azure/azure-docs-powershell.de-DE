---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 7a7c70dc9cf106aebc44df4733c4f8f9abaa78a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178886"
---
# <span data-ttu-id="b2e39-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b2e39-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="b2e39-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2e39-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e39-103">Erstellt eine neue Autorisierungsregel für Ereignis Hubs für Namespace oder eventhub.</span><span class="sxs-lookup"><span data-stu-id="b2e39-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="b2e39-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2e39-104">SYNTAX</span></span>

### <span data-ttu-id="b2e39-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2e39-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2e39-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b2e39-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2e39-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2e39-107">DESCRIPTION</span></span>
<span data-ttu-id="b2e39-108">Das New-AzEventHubAuthorizationRule-Cmdlet erstellt eine neue Autorisierungsregel für Ereignis Hubs.</span><span class="sxs-lookup"><span data-stu-id="b2e39-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="b2e39-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2e39-109">EXAMPLES</span></span>

### <span data-ttu-id="b2e39-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b2e39-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="b2e39-111">Erstellt eine Autorisierungsregel \` MyAuthRuleName \` Gewährung von Listen-und sende Rechten an den Namespace \` mynamespacename \` mit Ressourcengruppen- \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b2e39-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b2e39-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b2e39-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="b2e39-113">Erstellt eine Autorisierungsregel \` MyAuthRuleName \` Erteilen von Listen-und sende rechten für den Ereignis-Hub \` MyEventHubName \` im Namespace \` mynamespacename \` mit der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b2e39-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b2e39-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2e39-114">PARAMETERS</span></span>

### <span data-ttu-id="b2e39-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e39-115">-DefaultProfile</span></span>
<span data-ttu-id="b2e39-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b2e39-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2e39-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b2e39-117">-EventHub</span></span>
<span data-ttu-id="b2e39-118">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="b2e39-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e39-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b2e39-119">-Name</span></span>
<span data-ttu-id="b2e39-120">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="b2e39-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="b2e39-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b2e39-121">-Namespace</span></span>
<span data-ttu-id="b2e39-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="b2e39-122">Namespace Name</span></span>

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

### <span data-ttu-id="b2e39-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e39-123">-ResourceGroupName</span></span>
<span data-ttu-id="b2e39-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="b2e39-124">Resource Group Name</span></span>

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

### <span data-ttu-id="b2e39-125">-Rechte</span><span class="sxs-lookup"><span data-stu-id="b2e39-125">-Rights</span></span>
<span data-ttu-id="b2e39-126">Rechte wie "Abhören", "Senden", "verwalten"</span><span class="sxs-lookup"><span data-stu-id="b2e39-126">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e39-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2e39-127">-Confirm</span></span>
<span data-ttu-id="b2e39-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2e39-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2e39-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2e39-129">-WhatIf</span></span>
<span data-ttu-id="b2e39-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2e39-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2e39-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2e39-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2e39-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e39-132">CommonParameters</span></span>
<span data-ttu-id="b2e39-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e39-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e39-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2e39-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e39-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2e39-135">INPUTS</span></span>

### <span data-ttu-id="b2e39-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b2e39-136">System.String</span></span>

### <span data-ttu-id="b2e39-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="b2e39-137">System.String[]</span></span>

## <span data-ttu-id="b2e39-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2e39-138">OUTPUTS</span></span>

### <span data-ttu-id="b2e39-139">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b2e39-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="b2e39-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2e39-140">NOTES</span></span>

## <span data-ttu-id="b2e39-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2e39-141">RELATED LINKS</span></span>
