---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: 85dd5d73d2f0f4ce15dcffb2733f803cf6e67c0a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406280"
---
# <span data-ttu-id="1dbdd-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1dbdd-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="1dbdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dbdd-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbdd-103">Ruft Informationen zu Ihren Benachrichtigungshubs ab.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="1dbdd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dbdd-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dbdd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1dbdd-105">DESCRIPTION</span></span>
<span data-ttu-id="1dbdd-106">Das **Get-AzNotificationHub-Cmdlet** ruft Informationen zu den Benachrichtigungshubs in einem angegebenen Namespace ab und wird einer bestimmten Ressourcengruppe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="1dbdd-107">Sie können beispielsweise Informationen zu allen Benachrichtigungshubs im Namespace "ContosoNamespace" erhalten und der Ressourcengruppe "ContosoNotificationsGroup" zugewiesen sein.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="1dbdd-108">Alternativ können Sie den Parameter *NotificationHub verwenden,* um die zurückgegebenen Daten auf Informationen zu einem bestimmten Benachrichtigungshub zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="1dbdd-109">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen an mehrere Clients zu senden, unabhängig von der von diesen Clients verwendeten Plattform, z. B. iOS, Android, Windows Phone 8 und Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="1dbdd-110">Diese Hubs entsprechen in etwa einzelnen Apps, und jede Ihrer Apps hat in der Regel einen eigenen Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="1dbdd-111">Dieses Cmdlet ruft nur Informationen über den Hub selbst ab.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="1dbdd-112">Andere Cmdlets wie "Get-AzNotificationHubAuthorizationRules", "Get-AzNotificationHubListKeys" und "Get-AzNotificationHubPNSCredentials" sind erforderlich, um Informationen zu den Autorisierungsregeln, Verbindungszeichenfolgen und Anmeldeinformationen des Plattformbenachrichtigungsdiensts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="1dbdd-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1dbdd-113">EXAMPLES</span></span>

### <span data-ttu-id="1dbdd-114">Beispiel 1: Informationen für alle Benachrichtigungshubs in einem bestimmten Namespace</span><span class="sxs-lookup"><span data-stu-id="1dbdd-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="1dbdd-115">Dieser Befehl ruft Informationen für alle Benachrichtigungshubs im Namespace "ContosoNamespace" ab, die der Ressourcengruppe "ContosoNotificationsGroup" zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="1dbdd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dbdd-116">PARAMETERS</span></span>

### <span data-ttu-id="1dbdd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbdd-117">-DefaultProfile</span></span>
<span data-ttu-id="1dbdd-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1dbdd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dbdd-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1dbdd-119">-Namespace</span></span>
<span data-ttu-id="1dbdd-120">Gibt den Namespace an, dem der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="1dbdd-121">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="1dbdd-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="1dbdd-122">-NotificationHub</span></span>
<span data-ttu-id="1dbdd-123">Gibt den Namen des Benachrichtigungshubs an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="1dbdd-124">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen unabhängig von der von diesen Clients verwendeten Plattform an mehrere Clients zu senden.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="1dbdd-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1dbdd-125">-ResourceGroup</span></span>
<span data-ttu-id="1dbdd-126">Gibt die Ressourcengruppe an, der der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="1dbdd-127">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach die Bestandsverwaltung und die Verwaltung von Azure unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="1dbdd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbdd-128">CommonParameters</span></span>
<span data-ttu-id="1dbdd-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbdd-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dbdd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbdd-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1dbdd-131">INPUTS</span></span>

### <span data-ttu-id="1dbdd-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1dbdd-132">System.String</span></span>

## <span data-ttu-id="1dbdd-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1dbdd-133">OUTPUTS</span></span>

### <span data-ttu-id="1dbdd-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="1dbdd-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="1dbdd-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1dbdd-135">NOTES</span></span>

## <span data-ttu-id="1dbdd-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1dbdd-136">RELATED LINKS</span></span>




[<span data-ttu-id="1dbdd-137">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1dbdd-137">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="1dbdd-138">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1dbdd-138">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="1dbdd-139">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1dbdd-139">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


