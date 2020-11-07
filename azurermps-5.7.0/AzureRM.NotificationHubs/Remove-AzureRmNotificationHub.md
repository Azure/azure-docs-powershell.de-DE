---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
ms.openlocfilehash: 2a5ec9ee9c24ed0612f43ffc03f80d5dfe9df464
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664619"
---
# <span data-ttu-id="33616-101">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="33616-101">Remove-AzureRmNotificationHub</span></span>

## <span data-ttu-id="33616-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="33616-102">SYNOPSIS</span></span>
<span data-ttu-id="33616-103">Entfernt einen vorhandenen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="33616-103">Removes an existing notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33616-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="33616-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33616-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33616-105">DESCRIPTION</span></span>
<span data-ttu-id="33616-106">Mit dem Cmdlet **Remove-AzureRmNotificationHub** wird ein vorhandener Benachrichtigungs-Hub entfernt.</span><span class="sxs-lookup"><span data-stu-id="33616-106">The **Remove-AzureRmNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="33616-107">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="33616-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="33616-108">Zu den Plattformen gehören: IOS, Android, Windows Phone 8 und Windows Store.</span><span class="sxs-lookup"><span data-stu-id="33616-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="33616-109">Benachrichtigungshubs entsprechen in etwa den einzelnen apps: jede Ihrer Apps verfügt in der Regel über einen eigenen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="33616-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="33616-110">Sie können einen vorhandenen Benachrichtigungs-Hub mithilfe des Cmdlets **Remove-AzureRmNotificationHub** entfernen.</span><span class="sxs-lookup"><span data-stu-id="33616-110">You can remove an existing notification hub by using the **Remove-AzureRmNotificationHub** cmdlet.</span></span>
<span data-ttu-id="33616-111">Nachdem ein Hub entfernt wurde, können Sie diesen Hub nicht mehr verwenden, um Push-Benachrichtigungen an Benutzer zu senden.</span><span class="sxs-lookup"><span data-stu-id="33616-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="33616-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33616-112">EXAMPLES</span></span>

### <span data-ttu-id="33616-113">Beispiel 1: Entfernen eines benachrichtigungshubs</span><span class="sxs-lookup"><span data-stu-id="33616-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="33616-114">Dieser Befehl entfernt den Benachrichtigungs-Hub mit dem Namen ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="33616-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="33616-115">Um den Hub zu entfernen, müssen Sie den Namespace angeben, in dem sich der Hub befindet, sowie die Ressourcengruppe, der der Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="33616-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="33616-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="33616-116">PARAMETERS</span></span>

### <span data-ttu-id="33616-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33616-117">-DefaultProfile</span></span>
<span data-ttu-id="33616-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="33616-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33616-119">-Force</span><span class="sxs-lookup"><span data-stu-id="33616-119">-Force</span></span>
<span data-ttu-id="33616-120">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="33616-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="33616-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="33616-121">-Namespace</span></span>
<span data-ttu-id="33616-122">Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="33616-122">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="33616-123">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="33616-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="33616-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="33616-124">-NotificationHub</span></span>
<span data-ttu-id="33616-125">Gibt den Benachrichtigungs-Hub an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="33616-125">Specifies the notification hub to be removed.</span></span>

<span data-ttu-id="33616-126">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="33616-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33616-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="33616-127">-ResourceGroup</span></span>
<span data-ttu-id="33616-128">Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="33616-128">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="33616-129">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="33616-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="33616-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="33616-130">-Confirm</span></span>
<span data-ttu-id="33616-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="33616-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33616-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33616-132">-WhatIf</span></span>
<span data-ttu-id="33616-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="33616-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33616-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="33616-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33616-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33616-135">CommonParameters</span></span>
<span data-ttu-id="33616-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33616-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33616-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33616-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33616-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="33616-138">INPUTS</span></span>

### <span data-ttu-id="33616-139">Keine</span><span class="sxs-lookup"><span data-stu-id="33616-139">None</span></span>
<span data-ttu-id="33616-140">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="33616-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33616-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="33616-141">OUTPUTS</span></span>

## <span data-ttu-id="33616-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="33616-142">NOTES</span></span>

## <span data-ttu-id="33616-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="33616-143">RELATED LINKS</span></span>

[<span data-ttu-id="33616-144">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="33616-144">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="33616-145">Neu – AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="33616-145">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="33616-146">Satz-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="33616-146">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


