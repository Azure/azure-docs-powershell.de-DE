---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubpnscredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubPNSCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubPNSCredentials.md
ms.openlocfilehash: 8f0136a69e18da206975e42ffaf505460daccc97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662991"
---
# <span data-ttu-id="80be9-101">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="80be9-101">Get-AzureRmNotificationHubPNSCredentials</span></span>

## <span data-ttu-id="80be9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80be9-102">SYNOPSIS</span></span>
<span data-ttu-id="80be9-103">Ruft die PNS-Anmeldeinformationen für einen Benachrichtigungs-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="80be9-103">Gets the PNS credentials for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80be9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80be9-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubPNSCredentials [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80be9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80be9-105">DESCRIPTION</span></span>
<span data-ttu-id="80be9-106">Das Cmdlet " **Get-AzureRmNotificationHubPNSCredentials** " Ruft die PNS-Anmeldeinformationen (Platform Notification Service) für einen Benachrichtigungs-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="80be9-106">The **Get-AzureRmNotificationHubPNSCredentials** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="80be9-107">Jeder Benachrichtigungs-Hub verfügt über einen einzigen Satz von PNS-Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="80be9-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="80be9-108">Diese Anmeldeinformationen werden für einzelne Push-Benachrichtigungsdienste wie, aber nicht ausschließlich, verwendet. der IOS-Push-Benachrichtigungsdienst, der Android-Push-Benachrichtigungsdienst und Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="80be9-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="80be9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80be9-109">EXAMPLES</span></span>

### <span data-ttu-id="80be9-110">Beispiel 1: Abrufen von PNS-Anmeldeinformationen für einen bestimmten Benachrichtigungs-Hub</span><span class="sxs-lookup"><span data-stu-id="80be9-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubPNSCredentials -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="80be9-111">Dieser Befehl ruft die PNS-Anmeldeinformationen für den Benachrichtigungs-Hub mit dem Namen ContosoInternalHub ab, der zur Ressourcengruppe mit dem Namen ContosoNotificationsGroup gehört.</span><span class="sxs-lookup"><span data-stu-id="80be9-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="80be9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="80be9-112">PARAMETERS</span></span>

### <span data-ttu-id="80be9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80be9-113">-DefaultProfile</span></span>
<span data-ttu-id="80be9-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="80be9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80be9-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="80be9-115">-Namespace</span></span>
<span data-ttu-id="80be9-116">Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="80be9-116">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="80be9-117">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="80be9-117">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="80be9-118">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="80be9-118">-NotificationHub</span></span>
<span data-ttu-id="80be9-119">Gibt den Benachrichtigungs-Hub an, dem die PNS-Anmeldeinformationen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="80be9-119">Specifies the notification hub that the PNS credentials are assigned to.</span></span>
<span data-ttu-id="80be9-120">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="80be9-120">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="80be9-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="80be9-121">-ResourceGroup</span></span>
<span data-ttu-id="80be9-122">Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="80be9-122">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="80be9-123">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="80be9-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="80be9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80be9-124">CommonParameters</span></span>
<span data-ttu-id="80be9-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80be9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80be9-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80be9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80be9-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80be9-127">INPUTS</span></span>

### <span data-ttu-id="80be9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="80be9-128">System.String</span></span>

## <span data-ttu-id="80be9-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80be9-129">OUTPUTS</span></span>

### <span data-ttu-id="80be9-130">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="80be9-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="80be9-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="80be9-131">NOTES</span></span>

## <span data-ttu-id="80be9-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80be9-132">RELATED LINKS</span></span>

[<span data-ttu-id="80be9-133">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="80be9-133">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)


