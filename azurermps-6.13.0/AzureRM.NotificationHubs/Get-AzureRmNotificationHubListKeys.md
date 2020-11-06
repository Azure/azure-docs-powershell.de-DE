---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhublistkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
ms.openlocfilehash: 05c6ce89577e3c24368ddf47a0dec0abfeb2a388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498241"
---
# <span data-ttu-id="9ad7b-101">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="9ad7b-101">Get-AzureRmNotificationHubListKeys</span></span>

## <span data-ttu-id="9ad7b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ad7b-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad7b-103">Ruft die primären und sekundären Verbindungszeichenfolgen ab, die einer Benachrichtigungs-Hub-Autorisierungsregel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9ad7b-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ad7b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ad7b-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubListKeys [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ad7b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ad7b-105">DESCRIPTION</span></span>
<span data-ttu-id="9ad7b-106">Das Cmdlet " **Get-AzureRmNotificationHubListKeys** " gibt die primären und sekundären Verbindungszeichenfolgen einer Benachrichtigungs-Hub-Autorisierungsregel (Shared Access Signature, SAS) zurück.</span><span class="sxs-lookup"><span data-stu-id="9ad7b-106">The **Get-AzureRmNotificationHubListKeys** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="9ad7b-107">Autorisierungsregeln verwalten Benutzerrechte für den Hub.</span><span class="sxs-lookup"><span data-stu-id="9ad7b-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="9ad7b-108">Jede Regel umfasst eine primäre und eine sekundäre Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9ad7b-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="9ad7b-109">Diese Verbindungszeichenfolgen (URIs) führen die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="9ad7b-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="9ad7b-110">Verweisen von Benutzern auf eine Ressource</span><span class="sxs-lookup"><span data-stu-id="9ad7b-110">Point users to a resource.</span></span>
- <span data-ttu-id="9ad7b-111">Fügen Sie ein Token mit Abfrageparametern ein.</span><span class="sxs-lookup"><span data-stu-id="9ad7b-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="9ad7b-112">Einer dieser Parameter, die Signatur, wird verwendet, um den Benutzer zu authentifizieren und die angegebene Zugriffsebene bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9ad7b-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="9ad7b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ad7b-113">EXAMPLES</span></span>

### <span data-ttu-id="9ad7b-114">Beispiel 1: Abrufen der primären und sekundären Verbindungszeichenfolgen für eine Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="9ad7b-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubListKeys -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="9ad7b-115">Dieser Befehl ruft die primären und sekundären Verbindungszeichenfolgen für die Autorisierungsregel ListenRule ab, eine Regel, die dem ContosoInternalHub-Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9ad7b-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="9ad7b-116">Der Befehl muss den Hub-Namespace und die Ressourcengruppe enthalten.</span><span class="sxs-lookup"><span data-stu-id="9ad7b-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="9ad7b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ad7b-117">PARAMETERS</span></span>

### <span data-ttu-id="9ad7b-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9ad7b-118">-AuthorizationRule</span></span>
<span data-ttu-id="9ad7b-119">Gibt den Namen einer Authentifizierungsregel für eine gemeinsame zugriffssignatur (SAS) an.</span><span class="sxs-lookup"><span data-stu-id="9ad7b-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="9ad7b-120">Diese Regeln bestimmen die Art des Zugriffs, den Benutzer für den Benachrichtigungs-Hub haben.</span><span class="sxs-lookup"><span data-stu-id="9ad7b-120">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="9ad7b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad7b-121">-DefaultProfile</span></span>
<span data-ttu-id="9ad7b-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9ad7b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ad7b-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9ad7b-123">-Namespace</span></span>
<span data-ttu-id="9ad7b-124">Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9ad7b-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="9ad7b-125">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="9ad7b-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="9ad7b-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="9ad7b-126">-NotificationHub</span></span>
<span data-ttu-id="9ad7b-127">Gibt den Benachrichtigungs-Hub an, dem dieses Cmdlet eine Autorisierungsregel zuweist.</span><span class="sxs-lookup"><span data-stu-id="9ad7b-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="9ad7b-128">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9ad7b-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="9ad7b-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9ad7b-129">-ResourceGroup</span></span>
<span data-ttu-id="9ad7b-130">Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9ad7b-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="9ad7b-131">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ad7b-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="9ad7b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad7b-132">CommonParameters</span></span>
<span data-ttu-id="9ad7b-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ad7b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad7b-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ad7b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad7b-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ad7b-135">INPUTS</span></span>

### <span data-ttu-id="9ad7b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9ad7b-136">System.String</span></span>

## <span data-ttu-id="9ad7b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ad7b-137">OUTPUTS</span></span>

### <span data-ttu-id="9ad7b-138">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="9ad7b-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="9ad7b-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ad7b-139">NOTES</span></span>

## <span data-ttu-id="9ad7b-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ad7b-140">RELATED LINKS</span></span>

[<span data-ttu-id="9ad7b-141">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9ad7b-141">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)


