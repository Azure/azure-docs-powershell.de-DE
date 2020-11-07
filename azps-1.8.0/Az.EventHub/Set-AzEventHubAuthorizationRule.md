---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 46f640eefcd429a7fec4d06397f394ef31831183
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661020"
---
# <span data-ttu-id="22e60-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="22e60-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="22e60-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22e60-102">SYNOPSIS</span></span>
<span data-ttu-id="22e60-103">Aktualisiert die angegebene Autorisierungsregel in einem Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="22e60-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="22e60-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22e60-104">SYNTAX</span></span>

### <span data-ttu-id="22e60-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="22e60-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22e60-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="22e60-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22e60-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="22e60-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22e60-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22e60-108">DESCRIPTION</span></span>
<span data-ttu-id="22e60-109">Das Set-AzEventHubAuthorizationRule-Cmdlet aktualisiert die angegebene Autorisierungsregel für den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="22e60-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="22e60-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22e60-110">EXAMPLES</span></span>

### <span data-ttu-id="22e60-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="22e60-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="22e60-112">Aktualisiert die Autorisierungsregel \` MyAuthRuleName \` so, dass dem Ereignis-Hub \` \` -MyEventHubName, der vom Namespace mynamespacename zugewiesen wird, Verwaltungsrechte gewährt werden \` \` .</span><span class="sxs-lookup"><span data-stu-id="22e60-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="22e60-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="22e60-113">PARAMETERS</span></span>

### <span data-ttu-id="22e60-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e60-114">-DefaultProfile</span></span>
<span data-ttu-id="22e60-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="22e60-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22e60-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="22e60-116">-EventHub</span></span>
<span data-ttu-id="22e60-117">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="22e60-117">EventHub Name</span></span>

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

### <span data-ttu-id="22e60-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="22e60-118">-InputObject</span></span>
<span data-ttu-id="22e60-119">AuthorizationRule-Objekt</span><span class="sxs-lookup"><span data-stu-id="22e60-119">AuthorizationRule Object</span></span>

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

### <span data-ttu-id="22e60-120">-Name</span><span class="sxs-lookup"><span data-stu-id="22e60-120">-Name</span></span>
<span data-ttu-id="22e60-121">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="22e60-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="22e60-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="22e60-122">-Namespace</span></span>
<span data-ttu-id="22e60-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="22e60-123">Namespace Name</span></span>

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

### <span data-ttu-id="22e60-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22e60-124">-ResourceGroupName</span></span>
<span data-ttu-id="22e60-125">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="22e60-125">Resource Group Name</span></span>

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

### <span data-ttu-id="22e60-126">-Rechte</span><span class="sxs-lookup"><span data-stu-id="22e60-126">-Rights</span></span>
<span data-ttu-id="22e60-127">Rechte, z.b. @ ("Abhören"; "Senden"; "verwalten")</span><span class="sxs-lookup"><span data-stu-id="22e60-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="22e60-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="22e60-128">-Confirm</span></span>
<span data-ttu-id="22e60-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="22e60-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22e60-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22e60-130">-WhatIf</span></span>
<span data-ttu-id="22e60-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22e60-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22e60-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22e60-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22e60-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e60-133">CommonParameters</span></span>
<span data-ttu-id="22e60-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22e60-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e60-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22e60-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e60-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22e60-136">INPUTS</span></span>

### <span data-ttu-id="22e60-137">System. String</span><span class="sxs-lookup"><span data-stu-id="22e60-137">System.String</span></span>

### <span data-ttu-id="22e60-138">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="22e60-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="22e60-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="22e60-139">System.String[]</span></span>

## <span data-ttu-id="22e60-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22e60-140">OUTPUTS</span></span>

### <span data-ttu-id="22e60-141">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="22e60-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="22e60-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="22e60-142">NOTES</span></span>

## <span data-ttu-id="22e60-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22e60-143">RELATED LINKS</span></span>
