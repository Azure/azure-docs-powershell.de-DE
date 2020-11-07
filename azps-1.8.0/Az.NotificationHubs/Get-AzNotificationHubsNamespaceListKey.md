---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: c099f3d8419e7298af1a262f824304d50685a420
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660107"
---
# <span data-ttu-id="385b1-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="385b1-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="385b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="385b1-102">SYNOPSIS</span></span>
<span data-ttu-id="385b1-103">Ruft die primären und sekundären Verbindungszeichenfolgen ab, die einer Benachrichtigungs-Hub-Namespace Autorisierungsregel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="385b1-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="385b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="385b1-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="385b1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="385b1-105">DESCRIPTION</span></span>
<span data-ttu-id="385b1-106">Das Cmdlet " **Get-AzNotificationHubsNamespaceListKey** " gibt die primären und sekundären Verbindungszeichenfolgen für eine Berechtigungsregel für eine freigegebene zugriffssignatur (SAS) zurück, die einem Benachrichtigungs-Hub-Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="385b1-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="385b1-107">Autorisierungsregeln verwalten Benutzerrechte für einen Benachrichtigungs-Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="385b1-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="385b1-108">Jede Regel umfasst eine primäre und eine sekundäre Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="385b1-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="385b1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="385b1-109">EXAMPLES</span></span>

### <span data-ttu-id="385b1-110">Beispiel 1: Abrufen der primären und sekundären Verbindungszeichenfolgen für eine Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="385b1-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="385b1-111">Dieser Befehl gibt die primären und sekundären Verbindungszeichenfolgen für die Autorisierungsregel mit dem Namen "ListenRule" zurück, die dem ContosoNamespace-Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="385b1-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="385b1-112">Wenn Sie diesen Befehl ausführen, müssen Sie den Namen der Ressourcengruppe angeben, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="385b1-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="385b1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="385b1-113">PARAMETERS</span></span>

### <span data-ttu-id="385b1-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="385b1-114">-AuthorizationRule</span></span>
<span data-ttu-id="385b1-115">Gibt den Namen einer SAS-Authentifizierungsregel an.</span><span class="sxs-lookup"><span data-stu-id="385b1-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="385b1-116">Diese Regeln bestimmen die Art des Zugriffs, den Benutzer für den Benachrichtigungs-Hub haben.</span><span class="sxs-lookup"><span data-stu-id="385b1-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="385b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385b1-117">-DefaultProfile</span></span>
<span data-ttu-id="385b1-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="385b1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="385b1-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="385b1-119">-Namespace</span></span>
<span data-ttu-id="385b1-120">Gibt den Namespace an, der die Verbindungszeichenfolgen enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="385b1-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="385b1-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="385b1-121">-ResourceGroup</span></span>
<span data-ttu-id="385b1-122">Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="385b1-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="385b1-123">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="385b1-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="385b1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385b1-124">CommonParameters</span></span>
<span data-ttu-id="385b1-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="385b1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385b1-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="385b1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385b1-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="385b1-127">INPUTS</span></span>

### <span data-ttu-id="385b1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="385b1-128">System.String</span></span>

## <span data-ttu-id="385b1-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="385b1-129">OUTPUTS</span></span>

### <span data-ttu-id="385b1-130">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="385b1-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="385b1-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="385b1-131">NOTES</span></span>

## <span data-ttu-id="385b1-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="385b1-132">RELATED LINKS</span></span>

[<span data-ttu-id="385b1-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="385b1-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="385b1-134">Get-AzNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="385b1-134">Get-AzNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRules.md)


