---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4965fb6047ca31d2c5b70276a777235d2a3cb050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496573"
---
# <span data-ttu-id="caf8e-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="caf8e-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="caf8e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="caf8e-102">SYNOPSIS</span></span>
<span data-ttu-id="caf8e-103">Aktualisiert die angegebene Autorisierungsregel in einem Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="caf8e-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caf8e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="caf8e-104">SYNTAX</span></span>

### <span data-ttu-id="caf8e-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="caf8e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caf8e-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="caf8e-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caf8e-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="caf8e-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caf8e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="caf8e-108">DESCRIPTION</span></span>
<span data-ttu-id="caf8e-109">Das Set-AzureRmEventHubAuthorizationRule-Cmdlet aktualisiert die angegebene Autorisierungsregel für den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="caf8e-109">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="caf8e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="caf8e-110">EXAMPLES</span></span>

### <span data-ttu-id="caf8e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="caf8e-111">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="caf8e-112">Aktualisiert die Autorisierungsregel \` MyAuthRuleName \` so, dass dem Ereignis-Hub \` \` -MyEventHubName, der vom Namespace mynamespacename zugewiesen wird, Verwaltungsrechte gewährt werden \` \` .</span><span class="sxs-lookup"><span data-stu-id="caf8e-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="caf8e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="caf8e-113">PARAMETERS</span></span>

### <span data-ttu-id="caf8e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caf8e-114">-DefaultProfile</span></span>
<span data-ttu-id="caf8e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="caf8e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf8e-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="caf8e-116">-EventHub</span></span>
<span data-ttu-id="caf8e-117">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="caf8e-117">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf8e-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="caf8e-118">-InputObject</span></span>
<span data-ttu-id="caf8e-119">AuthorizationRule-Objekt</span><span class="sxs-lookup"><span data-stu-id="caf8e-119">AuthorizationRule Object</span></span>

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="caf8e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="caf8e-120">-Name</span></span>
<span data-ttu-id="caf8e-121">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="caf8e-121">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf8e-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="caf8e-122">-Namespace</span></span>
<span data-ttu-id="caf8e-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="caf8e-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf8e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caf8e-124">-ResourceGroupName</span></span>
<span data-ttu-id="caf8e-125">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="caf8e-125">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf8e-126">-Rechte</span><span class="sxs-lookup"><span data-stu-id="caf8e-126">-Rights</span></span>
<span data-ttu-id="caf8e-127">Rechte, z.b. @ ("Abhören"; "Senden"; "verwalten")</span><span class="sxs-lookup"><span data-stu-id="caf8e-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf8e-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="caf8e-128">-Confirm</span></span>
<span data-ttu-id="caf8e-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="caf8e-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf8e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caf8e-130">-WhatIf</span></span>
<span data-ttu-id="caf8e-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="caf8e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caf8e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="caf8e-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf8e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf8e-133">CommonParameters</span></span>
<span data-ttu-id="caf8e-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caf8e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="caf8e-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caf8e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf8e-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="caf8e-136">INPUTS</span></span>

### <span data-ttu-id="caf8e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="caf8e-137">System.String</span></span>
<span data-ttu-id="caf8e-138">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes System. String []</span><span class="sxs-lookup"><span data-stu-id="caf8e-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes System.String[]</span></span>


## <span data-ttu-id="caf8e-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="caf8e-139">OUTPUTS</span></span>

### <span data-ttu-id="caf8e-140">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="caf8e-140">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="caf8e-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="caf8e-141">NOTES</span></span>

## <span data-ttu-id="caf8e-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="caf8e-142">RELATED LINKS</span></span>
