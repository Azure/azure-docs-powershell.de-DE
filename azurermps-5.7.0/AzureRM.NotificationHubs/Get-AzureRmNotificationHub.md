---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
ms.openlocfilehash: cfe24ac2900e46a031980886f80bf39b9eee28e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504514"
---
# <span data-ttu-id="884e7-101">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="884e7-101">Get-AzureRmNotificationHub</span></span>

## <span data-ttu-id="884e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="884e7-102">SYNOPSIS</span></span>
<span data-ttu-id="884e7-103">Ruft Informationen zu ihren benachrichtigungshubs ab.</span><span class="sxs-lookup"><span data-stu-id="884e7-103">Gets information about your notification hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="884e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="884e7-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="884e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="884e7-105">DESCRIPTION</span></span>
<span data-ttu-id="884e7-106">Das Cmdlet " **Get-AzureRmNotificationHub** " Ruft Informationen zu den benachrichtigungshubs in einem angegebenen Namespace ab, die einer angegebenen Ressourcengruppe zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="884e7-106">The **Get-AzureRmNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="884e7-107">So können Sie beispielsweise Informationen zu allen benachrichtigungshubs im Namespace ContosoNamespace abrufen und der ContosoNotificationsGroup-Ressourcengruppe zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="884e7-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>

<span data-ttu-id="884e7-108">Alternativ können Sie den *NotificationHub* -Parameter verwenden, um die zurückgegebenen Daten auf Informationen zu einem bestimmten Benachrichtigungs-Hub zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="884e7-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>

<span data-ttu-id="884e7-109">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients unabhängig von der Plattform zu senden, wie beispielsweise IOS, Android, Windows Phone 8 und Windows Store, die von diesen Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="884e7-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="884e7-110">Diese Hubs sind in etwa mit einzelnen apps vergleichbar, und jede Ihrer Apps verfügt in der Regel über einen eigenen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="884e7-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="884e7-111">Dieses Cmdlet ruft nur Informationen über den Hub selbst ab.</span><span class="sxs-lookup"><span data-stu-id="884e7-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="884e7-112">Andere Cmdlets, wie "Get-AzureRmNotificationHubAuthorizationRules", "Get-AzureRmNotificationHubListKeys" und "Get-AzureRmNotificationHubPNSCredentials", sind erforderlich, um Informationen zu den Autorisierungsregeln eines Hubs, Verbindungszeichenfolgen und Anmeldeinformationen für den Platt Form Benachrichtigungsdienst abzurufen.</span><span class="sxs-lookup"><span data-stu-id="884e7-112">Other cmdlets, such as Get-AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys, and Get-AzureRmNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="884e7-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="884e7-113">EXAMPLES</span></span>

### <span data-ttu-id="884e7-114">Beispiel 1: Abrufen von Informationen für alle benachrichtigungshubs in einem bestimmten Namespace</span><span class="sxs-lookup"><span data-stu-id="884e7-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="884e7-115">Dieser Befehl ruft Informationen für alle benachrichtigungshubs im Namespace mit dem Namen ContosoNamespace ab, die der Ressourcengruppe ContosoNotificationsGroup zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="884e7-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="884e7-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="884e7-116">PARAMETERS</span></span>

### <span data-ttu-id="884e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="884e7-117">-DefaultProfile</span></span>
<span data-ttu-id="884e7-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="884e7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="884e7-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="884e7-119">-Namespace</span></span>
<span data-ttu-id="884e7-120">Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="884e7-120">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="884e7-121">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="884e7-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="884e7-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="884e7-122">-NotificationHub</span></span>
<span data-ttu-id="884e7-123">Gibt den Namen des benachrichtigungshubs an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="884e7-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>

<span data-ttu-id="884e7-124">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="884e7-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="884e7-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="884e7-125">-ResourceGroup</span></span>
<span data-ttu-id="884e7-126">Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="884e7-126">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="884e7-127">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="884e7-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="884e7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="884e7-128">CommonParameters</span></span>
<span data-ttu-id="884e7-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="884e7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="884e7-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="884e7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="884e7-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="884e7-131">INPUTS</span></span>

### <span data-ttu-id="884e7-132">Keine</span><span class="sxs-lookup"><span data-stu-id="884e7-132">None</span></span>
<span data-ttu-id="884e7-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="884e7-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="884e7-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="884e7-134">OUTPUTS</span></span>

### <span data-ttu-id="884e7-135">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes]</span><span class="sxs-lookup"><span data-stu-id="884e7-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes]</span></span>

## <span data-ttu-id="884e7-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="884e7-136">NOTES</span></span>

## <span data-ttu-id="884e7-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="884e7-137">RELATED LINKS</span></span>

[<span data-ttu-id="884e7-138">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="884e7-138">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="884e7-139">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="884e7-139">Get-AzureRmNotificationHubListKeys</span></span>](./Get-AzureRmNotificationHubListKeys.md)

[<span data-ttu-id="884e7-140">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="884e7-140">Get-AzureRmNotificationHubPNSCredentials</span></span>](./Get-AzureRmNotificationHubPNSCredentials.md)

[<span data-ttu-id="884e7-141">Neu – AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="884e7-141">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="884e7-142">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="884e7-142">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="884e7-143">Satz-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="884e7-143">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


