---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: db2b3357b7db90b5d5b310c43afb3f29ca596878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498245"
---
# <span data-ttu-id="6ffc7-101">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6ffc7-101">Get-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="6ffc7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6ffc7-102">SYNOPSIS</span></span>
<span data-ttu-id="6ffc7-103">Ruft Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungs-Hub zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-103">Gets information about the authorization rules associated with a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ffc7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ffc7-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ffc7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ffc7-105">DESCRIPTION</span></span>
<span data-ttu-id="6ffc7-106">Das Cmdlet " **Get-AzureRmNotificationHubAuthorizationRules** " Ruft Informationen zu den SAS-Autorisierungsregeln (Shared Access Signature) ab, die einem Benachrichtigungs-Hub zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-106">The **Get-AzureRmNotificationHubAuthorizationRules** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="6ffc7-107">Das Cmdlet gibt Informationen zu allen Regeln zurück, die einem Hub zugeordnet sind, oder ruft durch Einschließen des *AuthorizationRule* -Parameters Informationen zu einer bestimmten Regel ab.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>
<span data-ttu-id="6ffc7-108">Autorisierungsregeln verwalten den Zugriff auf Ihre benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="6ffc7-109">Eine Autorisierungsregel erstellt Links als URI, die auf unterschiedlichen Berechtigungsstufen basieren.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="6ffc7-110">Clients werden basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="6ffc7-111">Beispielsweise wird ein Client mit der Berechtigung "anhören" an den URI für diese Berechtigung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="6ffc7-112">Das Cmdlet " **Get-AzureRmNotificationHubAuthorizationRules** " ruft nur Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungs-Hub zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-112">The **Get-AzureRmNotificationHubAuthorizationRules** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="6ffc7-113">Wenn Sie Informationen zum Hub selbst abrufen möchten, verwenden Sie Get-AzureRmNotificationHub.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-113">To get information about the hub itself, use Get-AzureRmNotificationHub.</span></span>

## <span data-ttu-id="6ffc7-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ffc7-114">EXAMPLES</span></span>

### <span data-ttu-id="6ffc7-115">Beispiel 1: Abrufen von Informationen zu allen Autorisierungsregeln, die einem Benachrichtigungs-Hub zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="6ffc7-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="6ffc7-116">Dieser Befehl ruft Informationen für alle Autorisierungsregeln ab, die dem Benachrichtigungs-Hub mit dem Namen ContosoInternalHub im Namespace ContosoNamespace zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="6ffc7-117">Sie müssen den Namespace angeben, in dem sich der Hub befindet, sowie die Ressourcengruppe, der der Hub zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="6ffc7-118">Beispiel 2: Abrufen von Informationen zu Autorisierungsregeln, die einem Benachrichtigungs-Hub zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="6ffc7-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="6ffc7-119">Dieser Befehl ruft Informationen für alle Autorisierungsregeln ab, die dem Benachrichtigungs-Hub mit dem Namen ContosoInternalHub im Namespace ContosoNamespace zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="6ffc7-120">Der Befehl verwendet den *AuthorizationRule* -Parameter, um die zurückgegebenen Daten auf eine einzelne Autorisierungsregel mit dem Namen ListenRule zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="6ffc7-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ffc7-121">PARAMETERS</span></span>

### <span data-ttu-id="6ffc7-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6ffc7-122">-AuthorizationRule</span></span>
<span data-ttu-id="6ffc7-123">Gibt den Namen einer SAS-Authentifizierungsregel an.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="6ffc7-124">Diese Regeln bestimmen die Art des Zugriffs, den Benutzer für den Benachrichtigungs-Hub haben.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-124">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ffc7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ffc7-125">-DefaultProfile</span></span>
<span data-ttu-id="6ffc7-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6ffc7-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ffc7-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6ffc7-127">-Namespace</span></span>
<span data-ttu-id="6ffc7-128">Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="6ffc7-129">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ffc7-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="6ffc7-130">-NotificationHub</span></span>
<span data-ttu-id="6ffc7-131">Gibt den Benachrichtigungs-Hub an, dem dieses Cmdlet Autorisierungsregeln zuweist.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="6ffc7-132">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ffc7-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6ffc7-133">-ResourceGroup</span></span>
<span data-ttu-id="6ffc7-134">Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="6ffc7-135">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die zur Vereinfachung der Bestandsverwaltung und der Azure-Verwaltung beizutragen.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="6ffc7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ffc7-136">CommonParameters</span></span>
<span data-ttu-id="6ffc7-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ffc7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ffc7-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ffc7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ffc7-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6ffc7-139">INPUTS</span></span>

### <span data-ttu-id="6ffc7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6ffc7-140">System.String</span></span>

## <span data-ttu-id="6ffc7-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6ffc7-141">OUTPUTS</span></span>

### <span data-ttu-id="6ffc7-142">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="6ffc7-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="6ffc7-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="6ffc7-143">NOTES</span></span>

## <span data-ttu-id="6ffc7-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6ffc7-144">RELATED LINKS</span></span>

[<span data-ttu-id="6ffc7-145">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6ffc7-145">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="6ffc7-146">Neu – AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6ffc7-146">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="6ffc7-147">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6ffc7-147">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="6ffc7-148">Satz-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6ffc7-148">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


