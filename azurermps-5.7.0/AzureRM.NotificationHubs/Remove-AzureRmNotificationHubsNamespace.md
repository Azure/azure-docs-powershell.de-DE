---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 2a728cdae95c117e73f38b16cdea5407c1f4954e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481078"
---
# <span data-ttu-id="979aa-101">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="979aa-101">Remove-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="979aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="979aa-102">SYNOPSIS</span></span>
<span data-ttu-id="979aa-103">Entfernt einen Benachrichtigungs-Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="979aa-103">Removes a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="979aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="979aa-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="979aa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="979aa-105">DESCRIPTION</span></span>
<span data-ttu-id="979aa-106">Das Cmdlet **Remove-AzureRmNotificationHubsNamespace** entfernt einen Benachrichtigungs-Hub-Namespace aus Ihrer Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="979aa-106">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>

<span data-ttu-id="979aa-107">Namespaces sind logische Container, die Ihnen beim organisieren und Verwalten Ihrer benachrichtigungshubs helfen.</span><span class="sxs-lookup"><span data-stu-id="979aa-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="979aa-108">Das Cmdlet **Remove-AzureRmNotificationHubsNamespace** entfernt einen Benachrichtigungs-Hub-Namespace aus Ihrer Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="979aa-108">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="979aa-109">Wenn Sie dieses Cmdlet ausführen, wird der angegebene Namespace zusammen mit allen benachrichtigungshubs gelöscht, die diesem Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="979aa-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="979aa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="979aa-110">EXAMPLES</span></span>

### <span data-ttu-id="979aa-111">Beispiel 1: Entfernen eines Notification Hub-Namespace</span><span class="sxs-lookup"><span data-stu-id="979aa-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="979aa-112">Dieser Befehl entfernt den Namespace mit dem Namen ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="979aa-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="979aa-113">Sie müssen die Ressourcengruppe angeben, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="979aa-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="979aa-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="979aa-114">PARAMETERS</span></span>

### <span data-ttu-id="979aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="979aa-115">-DefaultProfile</span></span>
<span data-ttu-id="979aa-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="979aa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="979aa-117">-Force</span><span class="sxs-lookup"><span data-stu-id="979aa-117">-Force</span></span>
<span data-ttu-id="979aa-118">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="979aa-118">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979aa-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="979aa-119">-Namespace</span></span>
<span data-ttu-id="979aa-120">Gibt den Namespace an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="979aa-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="979aa-121">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="979aa-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="979aa-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="979aa-122">-ResourceGroup</span></span>
<span data-ttu-id="979aa-123">Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="979aa-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="979aa-124">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="979aa-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="979aa-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="979aa-125">-Confirm</span></span>
<span data-ttu-id="979aa-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="979aa-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979aa-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="979aa-127">-WhatIf</span></span>
<span data-ttu-id="979aa-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="979aa-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="979aa-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="979aa-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979aa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="979aa-130">CommonParameters</span></span>
<span data-ttu-id="979aa-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="979aa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="979aa-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="979aa-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="979aa-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="979aa-133">INPUTS</span></span>

### <span data-ttu-id="979aa-134">Keine</span><span class="sxs-lookup"><span data-stu-id="979aa-134">None</span></span>
<span data-ttu-id="979aa-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="979aa-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="979aa-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="979aa-136">OUTPUTS</span></span>

## <span data-ttu-id="979aa-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="979aa-137">NOTES</span></span>

## <span data-ttu-id="979aa-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="979aa-138">RELATED LINKS</span></span>

[<span data-ttu-id="979aa-139">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="979aa-139">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="979aa-140">Neu – AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="979aa-140">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="979aa-141">Satz-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="979aa-141">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


