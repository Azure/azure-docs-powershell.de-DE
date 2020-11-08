---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: d270e3020e03a02461d9c54e19458af10401ee79
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174513"
---
# <span data-ttu-id="16891-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="16891-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="16891-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16891-102">SYNOPSIS</span></span>
<span data-ttu-id="16891-103">Ruft Informationen zu ihren benachrichtigungshubs ab.</span><span class="sxs-lookup"><span data-stu-id="16891-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="16891-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16891-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16891-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16891-105">DESCRIPTION</span></span>
<span data-ttu-id="16891-106">Das Cmdlet " **Get-AzNotificationHub** " Ruft Informationen zu den benachrichtigungshubs in einem angegebenen Namespace ab, die einer angegebenen Ressourcengruppe zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="16891-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="16891-107">So können Sie beispielsweise Informationen zu allen benachrichtigungshubs im Namespace ContosoNamespace abrufen und der ContosoNotificationsGroup-Ressourcengruppe zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="16891-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="16891-108">Alternativ können Sie den *NotificationHub* -Parameter verwenden, um die zurückgegebenen Daten auf Informationen zu einem bestimmten Benachrichtigungs-Hub zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="16891-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="16891-109">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients unabhängig von der Plattform zu senden, wie beispielsweise IOS, Android, Windows Phone 8 und Windows Store, die von diesen Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16891-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="16891-110">Diese Hubs sind in etwa mit einzelnen apps vergleichbar, und jede Ihrer Apps verfügt in der Regel über einen eigenen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="16891-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="16891-111">Dieses Cmdlet ruft nur Informationen über den Hub selbst ab.</span><span class="sxs-lookup"><span data-stu-id="16891-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="16891-112">Andere Cmdlets, wie "Get-AzNotificationHubAuthorizationRules", "Get-AzNotificationHubListKeys" und "Get-AzNotificationHubPNSCredentials", sind erforderlich, um Informationen zu den Autorisierungsregeln eines Hubs, Verbindungszeichenfolgen und Anmeldeinformationen für den Platt Form Benachrichtigungsdienst abzurufen.</span><span class="sxs-lookup"><span data-stu-id="16891-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="16891-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16891-113">EXAMPLES</span></span>

### <span data-ttu-id="16891-114">Beispiel 1: Abrufen von Informationen für alle benachrichtigungshubs in einem bestimmten Namespace</span><span class="sxs-lookup"><span data-stu-id="16891-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="16891-115">Dieser Befehl ruft Informationen für alle benachrichtigungshubs im Namespace mit dem Namen ContosoNamespace ab, die der Ressourcengruppe ContosoNotificationsGroup zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="16891-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="16891-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="16891-116">PARAMETERS</span></span>

### <span data-ttu-id="16891-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16891-117">-DefaultProfile</span></span>
<span data-ttu-id="16891-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="16891-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16891-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="16891-119">-Namespace</span></span>
<span data-ttu-id="16891-120">Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="16891-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="16891-121">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="16891-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="16891-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="16891-122">-NotificationHub</span></span>
<span data-ttu-id="16891-123">Gibt den Namen des benachrichtigungshubs an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="16891-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="16891-124">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="16891-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16891-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="16891-125">-ResourceGroup</span></span>
<span data-ttu-id="16891-126">Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="16891-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="16891-127">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="16891-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="16891-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16891-128">CommonParameters</span></span>
<span data-ttu-id="16891-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16891-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16891-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16891-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16891-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16891-131">INPUTS</span></span>

### <span data-ttu-id="16891-132">System. String</span><span class="sxs-lookup"><span data-stu-id="16891-132">System.String</span></span>

## <span data-ttu-id="16891-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16891-133">OUTPUTS</span></span>

### <span data-ttu-id="16891-134">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="16891-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="16891-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="16891-135">NOTES</span></span>

## <span data-ttu-id="16891-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16891-136">RELATED LINKS</span></span>

[<span data-ttu-id="16891-137">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="16891-137">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="16891-138">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="16891-138">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="16891-139">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="16891-139">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="16891-140">Neu – AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="16891-140">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="16891-141">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="16891-141">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="16891-142">Satz-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="16891-142">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


