---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubpnscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
ms.openlocfilehash: 282e8092050b5859809c8dad71c4da1ee86c779d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151348"
---
# <span data-ttu-id="36b8e-101">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="36b8e-101">Get-AzNotificationHubPNSCredential</span></span>

## <span data-ttu-id="36b8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36b8e-102">SYNOPSIS</span></span>
<span data-ttu-id="36b8e-103">Ruft die PNS-Anmeldeinformationen für einen Benachrichtigungshub ab.</span><span class="sxs-lookup"><span data-stu-id="36b8e-103">Gets the PNS credentials for a notification hub.</span></span>

## <span data-ttu-id="36b8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36b8e-104">SYNTAX</span></span>

```
Get-AzNotificationHubPNSCredential [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36b8e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36b8e-105">DESCRIPTION</span></span>
<span data-ttu-id="36b8e-106">Das **Cmdlet "Get-AzNotificationHubPNSCredential"** ruft die Anmeldeinformationen des Plattformbenachrichtigungsdiensts (Platform Notification Service, PNS) für einen Benachrichtigungshub ab.</span><span class="sxs-lookup"><span data-stu-id="36b8e-106">The **Get-AzNotificationHubPNSCredential** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="36b8e-107">Jeder Benachrichtigungshub verfügt über einen einzigen Satz von PNS-Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="36b8e-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="36b8e-108">Diese Anmeldeinformationen werden auf einzelne Pushbenachrichtigungsdienste angewendet, z. B. auf: iOS-Pushbenachrichtigungsdienst, Android-Pushbenachrichtigungsdienst und Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="36b8e-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="36b8e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="36b8e-109">EXAMPLES</span></span>

### <span data-ttu-id="36b8e-110">Beispiel 1: Erhalten von PNS-Anmeldeinformationen für einen bestimmten Benachrichtigungshub</span><span class="sxs-lookup"><span data-stu-id="36b8e-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzNotificationHubPNSCredential -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="36b8e-111">Dieser Befehl ruft die PNS-Anmeldeinformationen für den Benachrichtigungshub namens "ContosoInternalHub" ab, der zur Ressourcengruppe "ContosoNotificationsGroup" gehört.</span><span class="sxs-lookup"><span data-stu-id="36b8e-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="36b8e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36b8e-112">PARAMETERS</span></span>

### <span data-ttu-id="36b8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b8e-113">-DefaultProfile</span></span>
<span data-ttu-id="36b8e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="36b8e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36b8e-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="36b8e-115">-Namespace</span></span>
<span data-ttu-id="36b8e-116">Gibt den Namespace an, dem der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="36b8e-116">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="36b8e-117">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="36b8e-117">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="36b8e-118">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="36b8e-118">-NotificationHub</span></span>
<span data-ttu-id="36b8e-119">Gibt den Benachrichtigungshub an, dem die Anmeldeinformationen des PNS zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="36b8e-119">Specifies the notification hub that the PNS credentials are assigned to.</span></span>
<span data-ttu-id="36b8e-120">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen unabhängig von der von diesen Clients verwendeten Plattform an mehrere Clients zu senden.</span><span class="sxs-lookup"><span data-stu-id="36b8e-120">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="36b8e-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="36b8e-121">-ResourceGroup</span></span>
<span data-ttu-id="36b8e-122">Gibt die Ressourcengruppe an, der der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="36b8e-122">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="36b8e-123">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach die Bestandsverwaltung und die Verwaltung von Azure unterstützen.</span><span class="sxs-lookup"><span data-stu-id="36b8e-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="36b8e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b8e-124">CommonParameters</span></span>
<span data-ttu-id="36b8e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36b8e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b8e-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36b8e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b8e-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="36b8e-127">INPUTS</span></span>

### <span data-ttu-id="36b8e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="36b8e-128">System.String</span></span>

## <span data-ttu-id="36b8e-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="36b8e-129">OUTPUTS</span></span>

### <span data-ttu-id="36b8e-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="36b8e-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="36b8e-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="36b8e-131">NOTES</span></span>

## <span data-ttu-id="36b8e-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="36b8e-132">RELATED LINKS</span></span>

[<span data-ttu-id="36b8e-133">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="36b8e-133">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)


