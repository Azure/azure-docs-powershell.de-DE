---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 2217a0c8aa68e815b650cd3eb564ce7a21733e72
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176259"
---
# <span data-ttu-id="25b4b-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="25b4b-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="25b4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25b4b-102">SYNOPSIS</span></span>
<span data-ttu-id="25b4b-103">Ruft die primären und sekundären Verbindungszeichenfolgen ab, die einer Benachrichtigungs-Hub-Namespace Autorisierungsregel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="25b4b-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="25b4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25b4b-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25b4b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25b4b-105">DESCRIPTION</span></span>
<span data-ttu-id="25b4b-106">Das Cmdlet " **Get-AzNotificationHubsNamespaceListKey** " gibt die primären und sekundären Verbindungszeichenfolgen für eine Berechtigungsregel für eine freigegebene zugriffssignatur (SAS) zurück, die einem Benachrichtigungs-Hub-Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="25b4b-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="25b4b-107">Autorisierungsregeln verwalten Benutzerrechte für einen Benachrichtigungs-Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="25b4b-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="25b4b-108">Jede Regel umfasst eine primäre und eine sekundäre Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="25b4b-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="25b4b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25b4b-109">EXAMPLES</span></span>

### <span data-ttu-id="25b4b-110">Beispiel 1: Abrufen der primären und sekundären Verbindungszeichenfolgen für eine Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="25b4b-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="25b4b-111">Dieser Befehl gibt die primären und sekundären Verbindungszeichenfolgen für die Autorisierungsregel mit dem Namen "ListenRule" zurück, die dem ContosoNamespace-Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="25b4b-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="25b4b-112">Wenn Sie diesen Befehl ausführen, müssen Sie den Namen der Ressourcengruppe angeben, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="25b4b-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="25b4b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="25b4b-113">PARAMETERS</span></span>

### <span data-ttu-id="25b4b-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="25b4b-114">-AuthorizationRule</span></span>
<span data-ttu-id="25b4b-115">Gibt den Namen einer SAS-Authentifizierungsregel an.</span><span class="sxs-lookup"><span data-stu-id="25b4b-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="25b4b-116">Diese Regeln bestimmen die Art des Zugriffs, den Benutzer für den Benachrichtigungs-Hub haben.</span><span class="sxs-lookup"><span data-stu-id="25b4b-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="25b4b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b4b-117">-DefaultProfile</span></span>
<span data-ttu-id="25b4b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="25b4b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25b4b-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="25b4b-119">-Namespace</span></span>
<span data-ttu-id="25b4b-120">Gibt den Namespace an, der die Verbindungszeichenfolgen enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="25b4b-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="25b4b-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="25b4b-121">-ResourceGroup</span></span>
<span data-ttu-id="25b4b-122">Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="25b4b-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="25b4b-123">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="25b4b-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="25b4b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b4b-124">CommonParameters</span></span>
<span data-ttu-id="25b4b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25b4b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b4b-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25b4b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b4b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25b4b-127">INPUTS</span></span>

### <span data-ttu-id="25b4b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="25b4b-128">System.String</span></span>

## <span data-ttu-id="25b4b-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25b4b-129">OUTPUTS</span></span>

### <span data-ttu-id="25b4b-130">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="25b4b-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="25b4b-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="25b4b-131">NOTES</span></span>

## <span data-ttu-id="25b4b-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25b4b-132">RELATED LINKS</span></span>

[<span data-ttu-id="25b4b-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="25b4b-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="25b4b-134">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="25b4b-134">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)


