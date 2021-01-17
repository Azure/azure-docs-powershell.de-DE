---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 862b6f295a997b2027520a3f9c6a9f4f9cfb5ae9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458695"
---
# <span data-ttu-id="902f8-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="902f8-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="902f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="902f8-102">SYNOPSIS</span></span>
<span data-ttu-id="902f8-103">Aktualisiert die angegebene Autorisierungsregel für einen Ereignishub.</span><span class="sxs-lookup"><span data-stu-id="902f8-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="902f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="902f8-104">SYNTAX</span></span>

### <span data-ttu-id="902f8-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="902f8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="902f8-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="902f8-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="902f8-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="902f8-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="902f8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="902f8-108">DESCRIPTION</span></span>
<span data-ttu-id="902f8-109">Das Set-AzEventHubAuthorizationRule aktualisiert die angegebene Autorisierungsregel für den angegebenen Ereignishub.</span><span class="sxs-lookup"><span data-stu-id="902f8-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="902f8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="902f8-110">EXAMPLES</span></span>

### <span data-ttu-id="902f8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="902f8-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="902f8-112">Aktualisiert die Autorisierungsregel "MyAuthRuleName", um dem Ereignishub "MyEventHubName" Die Berechtigung "Verwalten" zu gewähren, die durch den \` \` \` \` Namespace \` "MyNamespaceName" begrenzt \` ist.</span><span class="sxs-lookup"><span data-stu-id="902f8-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="902f8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="902f8-113">PARAMETERS</span></span>

### <span data-ttu-id="902f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="902f8-114">-DefaultProfile</span></span>
<span data-ttu-id="902f8-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="902f8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="902f8-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="902f8-116">-EventHub</span></span>
<span data-ttu-id="902f8-117">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="902f8-117">EventHub Name</span></span>

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

### <span data-ttu-id="902f8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="902f8-118">-InputObject</span></span>
<span data-ttu-id="902f8-119">AuthorizationRule-Objekt</span><span class="sxs-lookup"><span data-stu-id="902f8-119">AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="902f8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="902f8-120">-Name</span></span>
<span data-ttu-id="902f8-121">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="902f8-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="902f8-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="902f8-122">-Namespace</span></span>
<span data-ttu-id="902f8-123">Namespacename</span><span class="sxs-lookup"><span data-stu-id="902f8-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902f8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="902f8-124">-ResourceGroupName</span></span>
<span data-ttu-id="902f8-125">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="902f8-125">Resource Group Name</span></span>

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

### <span data-ttu-id="902f8-126">-Rights</span><span class="sxs-lookup"><span data-stu-id="902f8-126">-Rights</span></span>
<span data-ttu-id="902f8-127">Rechte, z. B. @("Zuhören";"Senden";"Verwalten")</span><span class="sxs-lookup"><span data-stu-id="902f8-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902f8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="902f8-128">-Confirm</span></span>
<span data-ttu-id="902f8-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="902f8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="902f8-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="902f8-130">-WhatIf</span></span>
<span data-ttu-id="902f8-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="902f8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="902f8-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="902f8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="902f8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="902f8-133">CommonParameters</span></span>
<span data-ttu-id="902f8-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="902f8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="902f8-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="902f8-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="902f8-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="902f8-136">INPUTS</span></span>

### <span data-ttu-id="902f8-137">System.String</span><span class="sxs-lookup"><span data-stu-id="902f8-137">System.String</span></span>

### <span data-ttu-id="902f8-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="902f8-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="902f8-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="902f8-139">System.String[]</span></span>

## <span data-ttu-id="902f8-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="902f8-140">OUTPUTS</span></span>

### <span data-ttu-id="902f8-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="902f8-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="902f8-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="902f8-142">NOTES</span></span>

## <span data-ttu-id="902f8-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="902f8-143">RELATED LINKS</span></span>
