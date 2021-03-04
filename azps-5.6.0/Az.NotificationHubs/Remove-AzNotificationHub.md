---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: b7932eb4f5d68986033243bc3e5e5161861a0bb8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918192"
---
# <span data-ttu-id="7b4f9-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7b4f9-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="7b4f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b4f9-102">SYNOPSIS</span></span>
<span data-ttu-id="7b4f9-103">Entfernt einen vorhandenen Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="7b4f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b4f9-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b4f9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7b4f9-105">DESCRIPTION</span></span>
<span data-ttu-id="7b4f9-106">Das **Cmdlet Remove-AzNotificationHub** entfernt einen vorhandenen Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="7b4f9-107">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="7b4f9-108">Plattformen umfassen, sind aber nicht beschränkt auf: iOS, Android, Windows Phone 8 und Windows Store.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="7b4f9-109">Benachrichtigungshubs entsprechen in etwa einzelnen Apps: Jede Ihrer Apps hat in der Regel einen eigenen Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="7b4f9-110">Sie können einen vorhandenen Benachrichtigungshub mithilfe des **Cmdlets Remove-AzNotificationHub** entfernen.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="7b4f9-111">Nachdem ein Hub entfernt wurde, können Sie diesen Hub nicht mehr verwenden, um Pushbenachrichtigungen an Benutzer zu senden.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="7b4f9-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7b4f9-112">EXAMPLES</span></span>

### <span data-ttu-id="7b4f9-113">Beispiel 1: Entfernen eines Benachrichtigungshubs</span><span class="sxs-lookup"><span data-stu-id="7b4f9-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="7b4f9-114">Mit diesem Befehl wird der Benachrichtigungshub namens ContosoInternalHub entfernt.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="7b4f9-115">Zum Entfernen des Hubs müssen Sie den Namespace angeben, in dem sich der Hub befindet, sowie die Ressourcengruppe, der der Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="7b4f9-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7b4f9-116">PARAMETERS</span></span>

### <span data-ttu-id="7b4f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b4f9-117">-DefaultProfile</span></span>
<span data-ttu-id="7b4f9-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7b4f9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b4f9-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="7b4f9-119">-Force</span></span>
<span data-ttu-id="7b4f9-120">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7b4f9-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7b4f9-121">-Namespace</span></span>
<span data-ttu-id="7b4f9-122">Gibt den Namespace an, dem der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="7b4f9-123">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="7b4f9-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="7b4f9-124">-NotificationHub</span></span>
<span data-ttu-id="7b4f9-125">Gibt den zu entfernenden Benachrichtigungshub an.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="7b4f9-126">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="7b4f9-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7b4f9-127">-ResourceGroup</span></span>
<span data-ttu-id="7b4f9-128">Gibt die Ressourcengruppe an, der der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="7b4f9-129">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die einfach die Bestandsverwaltung und die Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="7b4f9-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7b4f9-130">-Confirm</span></span>
<span data-ttu-id="7b4f9-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b4f9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b4f9-132">-WhatIf</span></span>
<span data-ttu-id="7b4f9-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b4f9-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b4f9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b4f9-135">CommonParameters</span></span>
<span data-ttu-id="7b4f9-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b4f9-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b4f9-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b4f9-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7b4f9-138">INPUTS</span></span>

### <span data-ttu-id="7b4f9-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7b4f9-139">System.String</span></span>

## <span data-ttu-id="7b4f9-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7b4f9-140">OUTPUTS</span></span>

### <span data-ttu-id="7b4f9-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="7b4f9-141">System.Void</span></span>

## <span data-ttu-id="7b4f9-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7b4f9-142">NOTES</span></span>

## <span data-ttu-id="7b4f9-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7b4f9-143">RELATED LINKS</span></span>

[<span data-ttu-id="7b4f9-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7b4f9-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="7b4f9-145">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7b4f9-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="7b4f9-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7b4f9-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


