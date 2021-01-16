---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 062d16155d4e1644e09f914a1114741e7bc5365f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295877"
---
# <span data-ttu-id="4e0fc-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="4e0fc-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="4e0fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e0fc-102">SYNOPSIS</span></span>
<span data-ttu-id="4e0fc-103">Ruft die primären und sekundären Verbindungszeichenfolgen ab, die einer Benachrichtigungshubautorisierungsregel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="4e0fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e0fc-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e0fc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e0fc-105">DESCRIPTION</span></span>
<span data-ttu-id="4e0fc-106">Das **Cmdlet "Get-AzNotificationHubListKey"** gibt die primären und sekundären Verbindungszeichenfolgen einer SAS (Shared Access Signature)-Autorisierungsregel (Notification Hub Shared Access Signature) zurück.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="4e0fc-107">Autorisierungsregeln verwalten Benutzerrechte für den Hub.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="4e0fc-108">Jede Regel enthält eine primäre und eine sekundäre Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="4e0fc-109">Diese Verbindungszeichenfolgen (URIs) führen Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="4e0fc-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="4e0fc-110">Zeigen Sie die Benutzer auf eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-110">Point users to a resource.</span></span>
- <span data-ttu-id="4e0fc-111">Fügen Sie ein Token mit Abfrageparametern ein.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="4e0fc-112">Einer dieser Parameter, die Signatur, wird verwendet, um den Benutzer zu authentifizieren und die angegebene Zugriffsebene zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="4e0fc-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4e0fc-113">EXAMPLES</span></span>

### <span data-ttu-id="4e0fc-114">Beispiel 1: Erhalten der primären und sekundären Verbindungszeichenfolgen für eine Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="4e0fc-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="4e0fc-115">Dieser Befehl ruft die primären und sekundären Verbindungszeichenfolgen für die Autorisierungsregel "ListenRule" ab, eine Regel, die dem ContosoInternalHub-Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="4e0fc-116">Der Befehl muss den Hubnamespace und die Ressourcengruppe enthalten.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="4e0fc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e0fc-117">PARAMETERS</span></span>

### <span data-ttu-id="4e0fc-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4e0fc-118">-AuthorizationRule</span></span>
<span data-ttu-id="4e0fc-119">Gibt den Namen einer SAS (Shared Access Signature)-Authentifizierungsregel an.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="4e0fc-120">Diese Regeln bestimmen den Typ des Zugriffs, den Benutzer auf den Benachrichtigungshub haben.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-120">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="4e0fc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e0fc-121">-DefaultProfile</span></span>
<span data-ttu-id="4e0fc-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4e0fc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e0fc-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4e0fc-123">-Namespace</span></span>
<span data-ttu-id="4e0fc-124">Gibt den Namespace an, dem der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="4e0fc-125">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="4e0fc-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="4e0fc-126">-NotificationHub</span></span>
<span data-ttu-id="4e0fc-127">Gibt den Benachrichtigungshub an, dem dieses Cmdlet eine Autorisierungsregel zugibt.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="4e0fc-128">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen unabhängig von der von diesen Clients verwendeten Plattform an mehrere Clients zu senden.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="4e0fc-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4e0fc-129">-ResourceGroup</span></span>
<span data-ttu-id="4e0fc-130">Gibt die Ressourcengruppe an, der der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="4e0fc-131">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach die Bestandsverwaltung und die Verwaltung von Azure unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="4e0fc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e0fc-132">CommonParameters</span></span>
<span data-ttu-id="4e0fc-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e0fc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e0fc-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e0fc-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e0fc-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4e0fc-135">INPUTS</span></span>

### <span data-ttu-id="4e0fc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4e0fc-136">System.String</span></span>

## <span data-ttu-id="4e0fc-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4e0fc-137">OUTPUTS</span></span>

### <span data-ttu-id="4e0fc-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="4e0fc-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="4e0fc-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4e0fc-139">NOTES</span></span>

## <span data-ttu-id="4e0fc-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4e0fc-140">RELATED LINKS</span></span>

[<span data-ttu-id="4e0fc-141">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4e0fc-141">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)


