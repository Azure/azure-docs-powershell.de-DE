---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 7a7c70dc9cf106aebc44df4733c4f8f9abaa78a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147916"
---
# <span data-ttu-id="eb925-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="eb925-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="eb925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb925-102">SYNOPSIS</span></span>
<span data-ttu-id="eb925-103">Erstellt eine neue Autorisierungsregel für Ereignishubs für Namespace oder Eventhub.</span><span class="sxs-lookup"><span data-stu-id="eb925-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="eb925-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb925-104">SYNTAX</span></span>

### <span data-ttu-id="eb925-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="eb925-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb925-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb925-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb925-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb925-107">DESCRIPTION</span></span>
<span data-ttu-id="eb925-108">Das New-AzEventHubAuthorizationRule erstellt eine neue Autorisierungsregel für Ereignishubs.</span><span class="sxs-lookup"><span data-stu-id="eb925-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="eb925-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eb925-109">EXAMPLES</span></span>

### <span data-ttu-id="eb925-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eb925-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="eb925-111">Erstellt eine Autorisierungsregel \` "MyAuthRuleName", die Listen- und Sendeberechtigungen für den Namespace "MyNamespaceName" mit der Ressourcengruppe \` \` \` \` "MyResourceGroupName" \` gewährt.</span><span class="sxs-lookup"><span data-stu-id="eb925-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="eb925-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="eb925-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="eb925-113">Erstellt eine Autorisierungsregel "MyAuthRuleName", die Listen- und Sendeberechtigungen für den Ereignishub \` \` \` "MyEventHubName" im Namespace "MyNamespaceName" mit der Ressourcengruppe \` \` \` \` "MyResourceGroupName" \` gewährt.</span><span class="sxs-lookup"><span data-stu-id="eb925-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="eb925-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb925-114">PARAMETERS</span></span>

### <span data-ttu-id="eb925-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb925-115">-DefaultProfile</span></span>
<span data-ttu-id="eb925-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb925-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb925-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="eb925-117">-EventHub</span></span>
<span data-ttu-id="eb925-118">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="eb925-118">EventHub Name</span></span>

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

### <span data-ttu-id="eb925-119">-Name</span><span class="sxs-lookup"><span data-stu-id="eb925-119">-Name</span></span>
<span data-ttu-id="eb925-120">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="eb925-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="eb925-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="eb925-121">-Namespace</span></span>
<span data-ttu-id="eb925-122">Namespacename</span><span class="sxs-lookup"><span data-stu-id="eb925-122">Namespace Name</span></span>

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

### <span data-ttu-id="eb925-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb925-123">-ResourceGroupName</span></span>
<span data-ttu-id="eb925-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="eb925-124">Resource Group Name</span></span>

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

### <span data-ttu-id="eb925-125">-Rights</span><span class="sxs-lookup"><span data-stu-id="eb925-125">-Rights</span></span>
<span data-ttu-id="eb925-126">Rechte, z. B. "Zuhören";"Senden";"Verwalten"</span><span class="sxs-lookup"><span data-stu-id="eb925-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="eb925-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb925-127">-Confirm</span></span>
<span data-ttu-id="eb925-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb925-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb925-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="eb925-129">-WhatIf</span></span>
<span data-ttu-id="eb925-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb925-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb925-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb925-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb925-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb925-132">CommonParameters</span></span>
<span data-ttu-id="eb925-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb925-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb925-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb925-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb925-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eb925-135">INPUTS</span></span>

### <span data-ttu-id="eb925-136">System.String</span><span class="sxs-lookup"><span data-stu-id="eb925-136">System.String</span></span>

### <span data-ttu-id="eb925-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="eb925-137">System.String[]</span></span>

## <span data-ttu-id="eb925-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eb925-138">OUTPUTS</span></span>

### <span data-ttu-id="eb925-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="eb925-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="eb925-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="eb925-140">NOTES</span></span>

## <span data-ttu-id="eb925-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="eb925-141">RELATED LINKS</span></span>
