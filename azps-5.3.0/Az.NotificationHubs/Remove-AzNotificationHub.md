---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: 66f3dae7d92b9db18db418bf9de62671f084b7c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385116"
---
# <span data-ttu-id="f5661-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f5661-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="f5661-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5661-102">SYNOPSIS</span></span>
<span data-ttu-id="f5661-103">Entfernt einen vorhandenen Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="f5661-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="f5661-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5661-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5661-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5661-105">DESCRIPTION</span></span>
<span data-ttu-id="f5661-106">Das **Cmdlet "Remove-AzNotificationHub"** entfernt einen vorhandenen Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="f5661-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="f5661-107">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen unabhängig von der von diesen Clients verwendeten Plattform an mehrere Clients zu senden.</span><span class="sxs-lookup"><span data-stu-id="f5661-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="f5661-108">Zu den Plattformen gehören unter anderem: iOS, Android, Windows Phone 8 und Windows Store.</span><span class="sxs-lookup"><span data-stu-id="f5661-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="f5661-109">Benachrichtigungshubs entsprechen in etwa einzelnen Apps: Jede Ihrer Apps hat in der Regel einen eigenen Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="f5661-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="f5661-110">Sie können einen vorhandenen Benachrichtigungshub mithilfe des **Cmdlets "Remove-AzNotificationHub"** entfernen.</span><span class="sxs-lookup"><span data-stu-id="f5661-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="f5661-111">Nachdem ein Hub entfernt wurde, können Sie diesen Hub nicht mehr zum Senden von Pushbenachrichtigungen an Benutzer verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5661-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="f5661-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f5661-112">EXAMPLES</span></span>

### <span data-ttu-id="f5661-113">Beispiel 1: Entfernen eines Benachrichtigungshubs</span><span class="sxs-lookup"><span data-stu-id="f5661-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="f5661-114">Mit diesem Befehl wird der Benachrichtigungshub "ContosoInternalHub" entfernt.</span><span class="sxs-lookup"><span data-stu-id="f5661-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="f5661-115">Um den Hub zu entfernen, müssen Sie den Namespace angeben, in dem sich der Hub befindet, sowie die Ressourcengruppe, der der Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f5661-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="f5661-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5661-116">PARAMETERS</span></span>

### <span data-ttu-id="f5661-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5661-117">-DefaultProfile</span></span>
<span data-ttu-id="f5661-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f5661-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5661-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f5661-119">-Force</span></span>
<span data-ttu-id="f5661-120">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="f5661-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f5661-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f5661-121">-Namespace</span></span>
<span data-ttu-id="f5661-122">Gibt den Namespace an, dem der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f5661-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="f5661-123">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="f5661-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f5661-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="f5661-124">-NotificationHub</span></span>
<span data-ttu-id="f5661-125">Gibt den zu entfernenden Benachrichtigungshub an.</span><span class="sxs-lookup"><span data-stu-id="f5661-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="f5661-126">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen unabhängig von der von diesen Clients verwendeten Plattform an mehrere Clients zu senden.</span><span class="sxs-lookup"><span data-stu-id="f5661-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="f5661-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5661-127">-ResourceGroup</span></span>
<span data-ttu-id="f5661-128">Gibt die Ressourcengruppe an, der der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f5661-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="f5661-129">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach die Bestandsverwaltung und die Verwaltung von Azure unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f5661-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f5661-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5661-130">-Confirm</span></span>
<span data-ttu-id="f5661-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5661-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5661-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f5661-132">-WhatIf</span></span>
<span data-ttu-id="f5661-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5661-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5661-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5661-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5661-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5661-135">CommonParameters</span></span>
<span data-ttu-id="f5661-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5661-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5661-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5661-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5661-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f5661-138">INPUTS</span></span>

### <span data-ttu-id="f5661-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f5661-139">System.String</span></span>

## <span data-ttu-id="f5661-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f5661-140">OUTPUTS</span></span>

### <span data-ttu-id="f5661-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="f5661-141">System.Void</span></span>

## <span data-ttu-id="f5661-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f5661-142">NOTES</span></span>

## <span data-ttu-id="f5661-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f5661-143">RELATED LINKS</span></span>

[<span data-ttu-id="f5661-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f5661-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="f5661-145">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f5661-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="f5661-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f5661-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


