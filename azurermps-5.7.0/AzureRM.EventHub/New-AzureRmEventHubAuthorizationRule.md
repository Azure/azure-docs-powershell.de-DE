---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: ae7fe44bf0fd3eccb157cefd6f57dade203d4fb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664231"
---
# <span data-ttu-id="39a3e-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="39a3e-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="39a3e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="39a3e-103">Erstellt eine neue Autorisierungsregel für Ereignis Hubs für Namespace oder eventhub.</span><span class="sxs-lookup"><span data-stu-id="39a3e-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39a3e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39a3e-104">SYNTAX</span></span>

### <span data-ttu-id="39a3e-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="39a3e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39a3e-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="39a3e-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39a3e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39a3e-107">DESCRIPTION</span></span>
<span data-ttu-id="39a3e-108">Das New-AzureRmEventHubAuthorizationRule-Cmdlet erstellt eine neue Autorisierungsregel für Ereignis Hubs.</span><span class="sxs-lookup"><span data-stu-id="39a3e-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="39a3e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39a3e-109">EXAMPLES</span></span>

### <span data-ttu-id="39a3e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39a3e-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="39a3e-111">Erstellt eine Autorisierungsregel \` MyAuthRuleName \` Gewährung von Listen-und sende Rechten an den Namespace \` mynamespacename \` mit Ressourcengruppen- \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="39a3e-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="39a3e-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="39a3e-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="39a3e-113">Erstellt eine Autorisierungsregel \` MyAuthRuleName \` Erteilen von Listen-und sende rechten für den Ereignis-Hub \` MyEventHubName \` im Namespace \` mynamespacename \` mit der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="39a3e-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="39a3e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="39a3e-114">PARAMETERS</span></span>

### <span data-ttu-id="39a3e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39a3e-115">-DefaultProfile</span></span>
<span data-ttu-id="39a3e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39a3e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39a3e-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="39a3e-117">-EventHub</span></span>
<span data-ttu-id="39a3e-118">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="39a3e-118">EventHub Name</span></span>

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

### <span data-ttu-id="39a3e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="39a3e-119">-Name</span></span>
<span data-ttu-id="39a3e-120">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="39a3e-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="39a3e-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="39a3e-121">-Namespace</span></span>
<span data-ttu-id="39a3e-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="39a3e-122">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39a3e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39a3e-123">-ResourceGroupName</span></span>
<span data-ttu-id="39a3e-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="39a3e-124">Resource Group Name</span></span>

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

### <span data-ttu-id="39a3e-125">-Rechte</span><span class="sxs-lookup"><span data-stu-id="39a3e-125">-Rights</span></span>
<span data-ttu-id="39a3e-126">Rechte wie "Abhören", "Senden", "verwalten"</span><span class="sxs-lookup"><span data-stu-id="39a3e-126">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39a3e-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="39a3e-127">-Confirm</span></span>
<span data-ttu-id="39a3e-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39a3e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39a3e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39a3e-129">-WhatIf</span></span>
<span data-ttu-id="39a3e-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39a3e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39a3e-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39a3e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39a3e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39a3e-132">CommonParameters</span></span>
<span data-ttu-id="39a3e-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39a3e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="39a3e-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39a3e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39a3e-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39a3e-135">INPUTS</span></span>

### <span data-ttu-id="39a3e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="39a3e-136">System.String</span></span>
<span data-ttu-id="39a3e-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="39a3e-137">System.String[]</span></span>


## <span data-ttu-id="39a3e-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39a3e-138">OUTPUTS</span></span>

### <span data-ttu-id="39a3e-139">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="39a3e-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="39a3e-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="39a3e-140">NOTES</span></span>

## <span data-ttu-id="39a3e-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39a3e-141">RELATED LINKS</span></span>
