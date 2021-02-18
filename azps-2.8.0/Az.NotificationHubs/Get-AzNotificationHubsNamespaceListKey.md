---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 88e43b182694b50169738e0b775d9202aac15ffa
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410462"
---
# <span data-ttu-id="21c1f-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="21c1f-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="21c1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="21c1f-103">Ruft die primären und sekundären Verbindungszeichenfolgen ab, die einer Autorisierungsregel für den Benachrichtigungshubnamespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="21c1f-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="21c1f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21c1f-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21c1f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21c1f-105">DESCRIPTION</span></span>
<span data-ttu-id="21c1f-106">Das **Cmdlet "Get-AzNotificationHubsNamespaceListKey"** gibt die primären und sekundären Verbindungszeichenfolgen für eine SAS (Shared Access Signature)-Autorisierungsregel zurück, die einem Benachrichtigungshub-Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="21c1f-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="21c1f-107">Autorisierungsregeln verwalten Benutzerrechte für einen Benachrichtigungshub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="21c1f-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="21c1f-108">Jede Regel enthält eine primäre und eine sekundäre Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="21c1f-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="21c1f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="21c1f-109">EXAMPLES</span></span>

### <span data-ttu-id="21c1f-110">Beispiel 1: Erhalten der primären und sekundären Verbindungszeichenfolgen für eine Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="21c1f-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="21c1f-111">Dieser Befehl gibt die primären und sekundären Verbindungszeichenfolgen für die Autorisierungsregel "ListenRule" zurück, die dem Namespace "ContosoNamespace" zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="21c1f-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="21c1f-112">Wenn Sie diesen Befehl ausführen, müssen Sie den Namen der Ressourcengruppe eingeben, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="21c1f-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="21c1f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21c1f-113">PARAMETERS</span></span>

### <span data-ttu-id="21c1f-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="21c1f-114">-AuthorizationRule</span></span>
<span data-ttu-id="21c1f-115">Gibt den Namen einer SAS-Authentifizierungsregel an.</span><span class="sxs-lookup"><span data-stu-id="21c1f-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="21c1f-116">Diese Regeln bestimmen den Typ des Zugriffs, den Benutzer auf den Benachrichtigungshub haben.</span><span class="sxs-lookup"><span data-stu-id="21c1f-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="21c1f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c1f-117">-DefaultProfile</span></span>
<span data-ttu-id="21c1f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="21c1f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21c1f-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="21c1f-119">-Namespace</span></span>
<span data-ttu-id="21c1f-120">Gibt den Namespace an, der die Verbindungszeichenfolgen enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="21c1f-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="21c1f-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="21c1f-121">-ResourceGroup</span></span>
<span data-ttu-id="21c1f-122">Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="21c1f-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="21c1f-123">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach die Bestandsverwaltung und die Verwaltung von Azure unterstützen.</span><span class="sxs-lookup"><span data-stu-id="21c1f-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="21c1f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c1f-124">CommonParameters</span></span>
<span data-ttu-id="21c1f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21c1f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c1f-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21c1f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c1f-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="21c1f-127">INPUTS</span></span>

### <span data-ttu-id="21c1f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="21c1f-128">System.String</span></span>

## <span data-ttu-id="21c1f-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="21c1f-129">OUTPUTS</span></span>

### <span data-ttu-id="21c1f-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="21c1f-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="21c1f-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="21c1f-131">NOTES</span></span>

## <span data-ttu-id="21c1f-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="21c1f-132">RELATED LINKS</span></span>

[<span data-ttu-id="21c1f-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="21c1f-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)



