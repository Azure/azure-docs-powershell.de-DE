---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: ff315c7f3634c0a8a4afd5c4b54926c0a260ed75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481769"
---
# <span data-ttu-id="21bd8-101">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="21bd8-101">Remove-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="21bd8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="21bd8-103">Entfernt einen Benachrichtigungs-Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="21bd8-103">Removes a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21bd8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21bd8-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21bd8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21bd8-105">DESCRIPTION</span></span>
<span data-ttu-id="21bd8-106">Das Cmdlet **Remove-AzureRmNotificationHubsNamespace** entfernt einen Benachrichtigungs-Hub-Namespace aus Ihrer Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="21bd8-106">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>

<span data-ttu-id="21bd8-107">Namespaces sind logische Container, die Ihnen beim organisieren und Verwalten Ihrer benachrichtigungshubs helfen.</span><span class="sxs-lookup"><span data-stu-id="21bd8-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="21bd8-108">Das Cmdlet **Remove-AzureRmNotificationHubsNamespace** entfernt einen Benachrichtigungs-Hub-Namespace aus Ihrer Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="21bd8-108">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="21bd8-109">Wenn Sie dieses Cmdlet ausführen, wird der angegebene Namespace zusammen mit allen benachrichtigungshubs gelöscht, die diesem Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="21bd8-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="21bd8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21bd8-110">EXAMPLES</span></span>

### <span data-ttu-id="21bd8-111">Beispiel 1: Entfernen eines Notification Hub-Namespace</span><span class="sxs-lookup"><span data-stu-id="21bd8-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="21bd8-112">Dieser Befehl entfernt den Namespace mit dem Namen ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="21bd8-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="21bd8-113">Sie müssen die Ressourcengruppe angeben, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="21bd8-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="21bd8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="21bd8-114">PARAMETERS</span></span>

### <span data-ttu-id="21bd8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="21bd8-115">-Force</span></span>
<span data-ttu-id="21bd8-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="21bd8-116">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21bd8-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="21bd8-117">-Namespace</span></span>
<span data-ttu-id="21bd8-118">Gibt den Namespace an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="21bd8-118">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="21bd8-119">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="21bd8-119">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="21bd8-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="21bd8-120">-ResourceGroup</span></span>
<span data-ttu-id="21bd8-121">Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="21bd8-121">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="21bd8-122">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21bd8-122">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="21bd8-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="21bd8-123">-Confirm</span></span>
<span data-ttu-id="21bd8-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21bd8-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21bd8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21bd8-125">-WhatIf</span></span>
<span data-ttu-id="21bd8-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21bd8-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21bd8-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21bd8-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21bd8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21bd8-128">-DefaultProfile</span></span>
<span data-ttu-id="21bd8-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="21bd8-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21bd8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21bd8-130">CommonParameters</span></span>
<span data-ttu-id="21bd8-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21bd8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21bd8-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21bd8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21bd8-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21bd8-133">INPUTS</span></span>

## <span data-ttu-id="21bd8-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21bd8-134">OUTPUTS</span></span>

## <span data-ttu-id="21bd8-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="21bd8-135">NOTES</span></span>

## <span data-ttu-id="21bd8-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21bd8-136">RELATED LINKS</span></span>

[<span data-ttu-id="21bd8-137">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="21bd8-137">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="21bd8-138">Neu – AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="21bd8-138">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="21bd8-139">Satz-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="21bd8-139">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


