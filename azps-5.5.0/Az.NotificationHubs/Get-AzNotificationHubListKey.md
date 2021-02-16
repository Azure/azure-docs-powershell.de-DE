---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 062d16155d4e1644e09f914a1114741e7bc5365f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146532"
---
# <span data-ttu-id="95254-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="95254-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="95254-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95254-102">SYNOPSIS</span></span>
<span data-ttu-id="95254-103">Ruft die primären und sekundären Verbindungszeichenfolgen ab, die einer Benachrichtigungshubautorisierungsregel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="95254-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="95254-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95254-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95254-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95254-105">DESCRIPTION</span></span>
<span data-ttu-id="95254-106">Das **Cmdlet "Get-AzNotificationHubListKey"** gibt die primären und sekundären Verbindungszeichenfolgen einer SAS (Shared Access Signature)-Autorisierungsregel (Notification Hub Shared Access Signature) zurück.</span><span class="sxs-lookup"><span data-stu-id="95254-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="95254-107">Autorisierungsregeln verwalten Benutzerrechte für den Hub.</span><span class="sxs-lookup"><span data-stu-id="95254-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="95254-108">Jede Regel enthält eine primäre und eine sekundäre Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="95254-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="95254-109">Diese Verbindungszeichenfolgen (URIs) führen Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="95254-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="95254-110">Zeigen Sie die Benutzer auf eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="95254-110">Point users to a resource.</span></span>
- <span data-ttu-id="95254-111">Fügen Sie ein Token mit Abfrageparametern ein.</span><span class="sxs-lookup"><span data-stu-id="95254-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="95254-112">Einer dieser Parameter, die Signatur, wird verwendet, um den Benutzer zu authentifizieren und die angegebene Zugriffsebene zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="95254-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="95254-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95254-113">EXAMPLES</span></span>

### <span data-ttu-id="95254-114">Beispiel 1: Erhalten der primären und sekundären Verbindungszeichenfolgen für eine Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="95254-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="95254-115">Dieser Befehl ruft die primären und sekundären Verbindungszeichenfolgen für die Autorisierungsregel "ListenRule" ab, eine Regel, die dem ContosoInternalHub-Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="95254-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="95254-116">Der Befehl muss den Hubnamespace und die Ressourcengruppe enthalten.</span><span class="sxs-lookup"><span data-stu-id="95254-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="95254-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95254-117">PARAMETERS</span></span>

### <span data-ttu-id="95254-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="95254-118">-AuthorizationRule</span></span>
<span data-ttu-id="95254-119">Gibt den Namen einer SAS (Shared Access Signature)-Authentifizierungsregel an.</span><span class="sxs-lookup"><span data-stu-id="95254-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="95254-120">Diese Regeln bestimmen den Typ des Zugriffs, den Benutzer auf den Benachrichtigungshub haben.</span><span class="sxs-lookup"><span data-stu-id="95254-120">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95254-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95254-121">-DefaultProfile</span></span>
<span data-ttu-id="95254-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="95254-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95254-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="95254-123">-Namespace</span></span>
<span data-ttu-id="95254-124">Gibt den Namespace an, dem der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="95254-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="95254-125">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="95254-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="95254-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="95254-126">-NotificationHub</span></span>
<span data-ttu-id="95254-127">Gibt den Benachrichtigungshub an, dem dieses Cmdlet eine Autorisierungsregel zugibt.</span><span class="sxs-lookup"><span data-stu-id="95254-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="95254-128">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen unabhängig von der von diesen Clients verwendeten Plattform an mehrere Clients zu senden.</span><span class="sxs-lookup"><span data-stu-id="95254-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="95254-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="95254-129">-ResourceGroup</span></span>
<span data-ttu-id="95254-130">Gibt die Ressourcengruppe an, der der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="95254-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="95254-131">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach die Bestandsverwaltung und die Verwaltung von Azure unterstützen.</span><span class="sxs-lookup"><span data-stu-id="95254-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="95254-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95254-132">CommonParameters</span></span>
<span data-ttu-id="95254-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95254-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95254-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95254-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95254-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95254-135">INPUTS</span></span>

### <span data-ttu-id="95254-136">System.String</span><span class="sxs-lookup"><span data-stu-id="95254-136">System.String</span></span>

## <span data-ttu-id="95254-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95254-137">OUTPUTS</span></span>

### <span data-ttu-id="95254-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="95254-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="95254-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="95254-139">NOTES</span></span>

## <span data-ttu-id="95254-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="95254-140">RELATED LINKS</span></span>

[<span data-ttu-id="95254-141">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="95254-141">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)


