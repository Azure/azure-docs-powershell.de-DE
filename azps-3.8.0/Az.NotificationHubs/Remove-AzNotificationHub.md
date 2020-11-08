---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: 66f3dae7d92b9db18db418bf9de62671f084b7c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002982"
---
# <span data-ttu-id="4ac4b-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4ac4b-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="4ac4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ac4b-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac4b-103">Entfernt einen vorhandenen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="4ac4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ac4b-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ac4b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ac4b-105">DESCRIPTION</span></span>
<span data-ttu-id="4ac4b-106">Mit dem Cmdlet **Remove-AzNotificationHub** wird ein vorhandener Benachrichtigungs-Hub entfernt.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="4ac4b-107">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="4ac4b-108">Zu den Plattformen gehören: IOS, Android, Windows Phone 8 und Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="4ac4b-109">Benachrichtigungshubs entsprechen in etwa den einzelnen apps: jede Ihrer Apps verfügt in der Regel über einen eigenen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="4ac4b-110">Sie können einen vorhandenen Benachrichtigungs-Hub mithilfe des Cmdlets **Remove-AzNotificationHub** entfernen.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="4ac4b-111">Nachdem ein Hub entfernt wurde, können Sie diesen Hub nicht mehr verwenden, um Push-Benachrichtigungen an Benutzer zu senden.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="4ac4b-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ac4b-112">EXAMPLES</span></span>

### <span data-ttu-id="4ac4b-113">Beispiel 1: Entfernen eines benachrichtigungshubs</span><span class="sxs-lookup"><span data-stu-id="4ac4b-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="4ac4b-114">Dieser Befehl entfernt den Benachrichtigungs-Hub mit dem Namen ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="4ac4b-115">Um den Hub zu entfernen, müssen Sie den Namespace angeben, in dem sich der Hub befindet, sowie die Ressourcengruppe, der der Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="4ac4b-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ac4b-116">PARAMETERS</span></span>

### <span data-ttu-id="4ac4b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac4b-117">-DefaultProfile</span></span>
<span data-ttu-id="4ac4b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4ac4b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ac4b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4ac4b-119">-Force</span></span>
<span data-ttu-id="4ac4b-120">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4ac4b-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4ac4b-121">-Namespace</span></span>
<span data-ttu-id="4ac4b-122">Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="4ac4b-123">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="4ac4b-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="4ac4b-124">-NotificationHub</span></span>
<span data-ttu-id="4ac4b-125">Gibt den Benachrichtigungs-Hub an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="4ac4b-126">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="4ac4b-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4ac4b-127">-ResourceGroup</span></span>
<span data-ttu-id="4ac4b-128">Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="4ac4b-129">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="4ac4b-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4ac4b-130">-Confirm</span></span>
<span data-ttu-id="4ac4b-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ac4b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ac4b-132">-WhatIf</span></span>
<span data-ttu-id="4ac4b-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ac4b-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ac4b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac4b-135">CommonParameters</span></span>
<span data-ttu-id="4ac4b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac4b-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ac4b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac4b-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ac4b-138">INPUTS</span></span>

### <span data-ttu-id="4ac4b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4ac4b-139">System.String</span></span>

## <span data-ttu-id="4ac4b-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ac4b-140">OUTPUTS</span></span>

### <span data-ttu-id="4ac4b-141">System. void</span><span class="sxs-lookup"><span data-stu-id="4ac4b-141">System.Void</span></span>

## <span data-ttu-id="4ac4b-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ac4b-142">NOTES</span></span>

## <span data-ttu-id="4ac4b-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ac4b-143">RELATED LINKS</span></span>

[<span data-ttu-id="4ac4b-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4ac4b-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="4ac4b-145">Neu – AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4ac4b-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="4ac4b-146">Satz-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4ac4b-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


