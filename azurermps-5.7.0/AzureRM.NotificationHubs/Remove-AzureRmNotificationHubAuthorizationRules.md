---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 9ae94e039d91f8f21015fb28b726ef5bacfb4ae4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481081"
---
# <span data-ttu-id="c625a-101">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="c625a-101">Remove-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="c625a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c625a-102">SYNOPSIS</span></span>
<span data-ttu-id="c625a-103">Entfernt eine Autorisierungsregel aus einem Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="c625a-103">Removes an authorization rule from a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c625a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c625a-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c625a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c625a-105">DESCRIPTION</span></span>
<span data-ttu-id="c625a-106">Das Cmdlet " **Remove-AzureRmNotificationHubAuthorizationRules** " entfernt eine Autorisierungsregel für eine freigegebene zugriffssignatur (SAS) von einem Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="c625a-106">The **Remove-AzureRmNotificationHubAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>

<span data-ttu-id="c625a-107">Autorisierungsregeln verwalten den Zugriff auf Ihre benachrichtigungshubs durch das Erstellen von Links als URIs basierend auf unterschiedlichen Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="c625a-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="c625a-108">Berechtigungsstufen können eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="c625a-108">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="c625a-109">Hören</span><span class="sxs-lookup"><span data-stu-id="c625a-109">Listen</span></span>
- <span data-ttu-id="c625a-110">Senden</span><span class="sxs-lookup"><span data-stu-id="c625a-110">Send</span></span>
- <span data-ttu-id="c625a-111">Verwalten</span><span class="sxs-lookup"><span data-stu-id="c625a-111">Manage</span></span>

<span data-ttu-id="c625a-112">Clients werden basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="c625a-112">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="c625a-113">Beispielsweise wird ein Client, der die Berechtigung "anhören" erhält, an den URI für diese Berechtigung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="c625a-113">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="c625a-114">Wenn Sie eine Autorisierungsregel entfernen, wird auch die entsprechende Benutzerberechtigung entfernt.</span><span class="sxs-lookup"><span data-stu-id="c625a-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="c625a-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c625a-115">EXAMPLES</span></span>

### <span data-ttu-id="c625a-116">Beispiel 1: Entfernen einer Autorisierungsregel von einem Benachrichtigungs-Hub</span><span class="sxs-lookup"><span data-stu-id="c625a-116">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="c625a-117">Dieser Befehl entfernt die Autorisierungsregel namens ListenRule aus dem Benachrichtigungs-Hub mit dem Namen ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="c625a-117">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="c625a-118">Wenn Sie diesen Befehl ausführen, müssen Sie sowohl den Namespace als auch die Ressourcengruppe angeben, der der Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c625a-118">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="c625a-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="c625a-119">PARAMETERS</span></span>

### <span data-ttu-id="c625a-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c625a-120">-AuthorizationRule</span></span>
<span data-ttu-id="c625a-121">Gibt den Namen der SAS-Authentifizierungsregel an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c625a-121">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c625a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c625a-122">-DefaultProfile</span></span>
<span data-ttu-id="c625a-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c625a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c625a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c625a-124">-Force</span></span>
<span data-ttu-id="c625a-125">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="c625a-125">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c625a-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c625a-126">-Namespace</span></span>
<span data-ttu-id="c625a-127">Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c625a-127">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="c625a-128">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="c625a-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c625a-129">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="c625a-129">-NotificationHub</span></span>
<span data-ttu-id="c625a-130">Gibt den Benachrichtigungs-Hub an, dem die Autorisierungsregeln zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="c625a-130">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="c625a-131">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients unabhängig von der Plattform zu senden.</span><span class="sxs-lookup"><span data-stu-id="c625a-131">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c625a-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c625a-132">-ResourceGroup</span></span>
<span data-ttu-id="c625a-133">Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c625a-133">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="c625a-134">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c625a-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="c625a-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c625a-135">-Confirm</span></span>
<span data-ttu-id="c625a-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c625a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c625a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c625a-137">-WhatIf</span></span>
<span data-ttu-id="c625a-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c625a-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c625a-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c625a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c625a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c625a-140">CommonParameters</span></span>
<span data-ttu-id="c625a-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c625a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c625a-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c625a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c625a-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c625a-143">INPUTS</span></span>

### <span data-ttu-id="c625a-144">Keine</span><span class="sxs-lookup"><span data-stu-id="c625a-144">None</span></span>
<span data-ttu-id="c625a-145">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c625a-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c625a-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c625a-146">OUTPUTS</span></span>

## <span data-ttu-id="c625a-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="c625a-147">NOTES</span></span>

## <span data-ttu-id="c625a-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c625a-148">RELATED LINKS</span></span>

[<span data-ttu-id="c625a-149">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="c625a-149">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="c625a-150">Neu – AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="c625a-150">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="c625a-151">Satz-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="c625a-151">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


