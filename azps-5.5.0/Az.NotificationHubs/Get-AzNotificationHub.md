---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: 944805a4883edce9354cfa372bfd30db145fc4ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160497"
---
# <span data-ttu-id="dcbd9-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="dcbd9-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="dcbd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcbd9-102">SYNOPSIS</span></span>
<span data-ttu-id="dcbd9-103">Ruft Informationen zu Ihren Benachrichtigungshubs ab.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="dcbd9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dcbd9-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcbd9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dcbd9-105">DESCRIPTION</span></span>
<span data-ttu-id="dcbd9-106">Das **Get-AzNotificationHub-Cmdlet** ruft Informationen zu den Benachrichtigungshubs in einem angegebenen Namespace ab und wird einer bestimmten Ressourcengruppe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="dcbd9-107">Sie können z. B. Informationen zu allen Benachrichtigungshubs im Namespace "ContosoNamespace" erhalten und der Ressourcengruppe "ContosoNotificationsGroup" zugewiesen sein.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="dcbd9-108">Alternativ können Sie den Parameter *NotificationHub verwenden,* um die zurückgegebenen Daten auf Informationen zu einem bestimmten Benachrichtigungshub zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="dcbd9-109">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen an mehrere Clients zu senden, unabhängig von der von diesen Clients verwendeten Plattform, z. B. iOS, Android, Windows Phone 8 und Windows Store.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="dcbd9-110">Diese Hubs entsprechen in etwa einzelnen Apps, und jede Ihrer Apps hat in der Regel einen eigenen Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="dcbd9-111">Dieses Cmdlet ruft nur Informationen über den Hub selbst ab.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="dcbd9-112">Andere Cmdlets wie "Get-AzNotificationHubAuthorizationRules", "Get-AzNotificationHubListKeys" und "Get-AzNotificationHubPNSCredentials" sind erforderlich, um Informationen zu den Autorisierungsregeln, Verbindungszeichenfolgen und Anmeldeinformationen des Plattformbenachrichtigungsdiensts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="dcbd9-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dcbd9-113">EXAMPLES</span></span>

### <span data-ttu-id="dcbd9-114">Beispiel 1: Informationen für alle Benachrichtigungshubs in einem bestimmten Namespace</span><span class="sxs-lookup"><span data-stu-id="dcbd9-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```powershell
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="dcbd9-115">Dieser Befehl ruft Informationen für alle Benachrichtigungshubs im Namespace "ContosoNamespace" ab, die der Ressourcengruppe "ContosoNotificationsGroup" zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

### <span data-ttu-id="dcbd9-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dcbd9-116">Example 2</span></span>

<span data-ttu-id="dcbd9-117">Ruft Informationen zu Ihren Benachrichtigungshubs ab.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-117">Gets information about your notification hubs.</span></span> <span data-ttu-id="dcbd9-118">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="dcbd9-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHub 'ContosoInternalHub' -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="dcbd9-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcbd9-119">PARAMETERS</span></span>

### <span data-ttu-id="dcbd9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcbd9-120">-DefaultProfile</span></span>
<span data-ttu-id="dcbd9-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="dcbd9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcbd9-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dcbd9-122">-Namespace</span></span>
<span data-ttu-id="dcbd9-123">Gibt den Namespace an, dem der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-123">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="dcbd9-124">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-124">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="dcbd9-125">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="dcbd9-125">-NotificationHub</span></span>
<span data-ttu-id="dcbd9-126">Gibt den Namen des Benachrichtigungshubs an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-126">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="dcbd9-127">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen unabhängig von der von diesen Clients verwendeten Plattform an mehrere Clients zu senden.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-127">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="dcbd9-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dcbd9-128">-ResourceGroup</span></span>
<span data-ttu-id="dcbd9-129">Gibt die Ressourcengruppe an, der der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-129">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="dcbd9-130">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach die Bestandsverwaltung und die Verwaltung von Azure unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-130">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="dcbd9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcbd9-131">CommonParameters</span></span>
<span data-ttu-id="dcbd9-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcbd9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcbd9-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcbd9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcbd9-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dcbd9-134">INPUTS</span></span>

### <span data-ttu-id="dcbd9-135">System.String</span><span class="sxs-lookup"><span data-stu-id="dcbd9-135">System.String</span></span>

## <span data-ttu-id="dcbd9-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dcbd9-136">OUTPUTS</span></span>

### <span data-ttu-id="dcbd9-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="dcbd9-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="dcbd9-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dcbd9-138">NOTES</span></span>

## <span data-ttu-id="dcbd9-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dcbd9-139">RELATED LINKS</span></span>

[<span data-ttu-id="dcbd9-140">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dcbd9-140">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="dcbd9-141">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="dcbd9-141">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="dcbd9-142">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="dcbd9-142">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="dcbd9-143">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="dcbd9-143">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="dcbd9-144">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="dcbd9-144">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="dcbd9-145">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="dcbd9-145">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


