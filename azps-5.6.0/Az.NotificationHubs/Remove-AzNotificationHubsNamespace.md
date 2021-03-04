---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: a1e5a8b33ab9df4e48495d00b6a27e105088f4fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918184"
---
# <span data-ttu-id="20cf1-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="20cf1-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="20cf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="20cf1-103">Entfernt einen Benachrichtigungshubnamespace.</span><span class="sxs-lookup"><span data-stu-id="20cf1-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="20cf1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20cf1-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20cf1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20cf1-105">DESCRIPTION</span></span>
<span data-ttu-id="20cf1-106">Das **Cmdlet Remove-AzNotificationHubsNamespace** entfernt einen Benachrichtigungshubnamespace aus Ihrer Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="20cf1-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="20cf1-107">Namespaces sind logische Container, mit deren Hilfe Sie Ihre Benachrichtigungshubs organisieren und verwalten können.</span><span class="sxs-lookup"><span data-stu-id="20cf1-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="20cf1-108">Das **Cmdlet Remove-AzNotificationHubsNamespace** entfernt einen Benachrichtigungshubnamespace aus Ihrer Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="20cf1-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="20cf1-109">Wenn Sie dieses Cmdlet ausführen, wird der angegebene Namespace zusammen mit allen Benachrichtigungshubs gelöscht, die diesem Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="20cf1-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="20cf1-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="20cf1-110">EXAMPLES</span></span>

### <span data-ttu-id="20cf1-111">Beispiel 1: Entfernen eines Benachrichtigungshubnamespaces</span><span class="sxs-lookup"><span data-stu-id="20cf1-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="20cf1-112">Mit diesem Befehl wird der Namespace contosoNamespace entfernt.</span><span class="sxs-lookup"><span data-stu-id="20cf1-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="20cf1-113">Sie müssen die Ressourcengruppe angeben, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="20cf1-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="20cf1-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="20cf1-114">PARAMETERS</span></span>

### <span data-ttu-id="20cf1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20cf1-115">-DefaultProfile</span></span>
<span data-ttu-id="20cf1-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="20cf1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20cf1-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="20cf1-117">-Force</span></span>
<span data-ttu-id="20cf1-118">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="20cf1-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="20cf1-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="20cf1-119">-Namespace</span></span>
<span data-ttu-id="20cf1-120">Gibt den Namespace an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="20cf1-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="20cf1-121">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="20cf1-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="20cf1-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="20cf1-122">-ResourceGroup</span></span>
<span data-ttu-id="20cf1-123">Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="20cf1-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="20cf1-124">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die einfach die Bestandsverwaltung und die Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="20cf1-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="20cf1-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="20cf1-125">-Confirm</span></span>
<span data-ttu-id="20cf1-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="20cf1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20cf1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20cf1-127">-WhatIf</span></span>
<span data-ttu-id="20cf1-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20cf1-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20cf1-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20cf1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20cf1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20cf1-130">CommonParameters</span></span>
<span data-ttu-id="20cf1-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20cf1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20cf1-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20cf1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20cf1-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="20cf1-133">INPUTS</span></span>

### <span data-ttu-id="20cf1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="20cf1-134">System.String</span></span>

## <span data-ttu-id="20cf1-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="20cf1-135">OUTPUTS</span></span>

### <span data-ttu-id="20cf1-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="20cf1-136">System.Void</span></span>

## <span data-ttu-id="20cf1-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="20cf1-137">NOTES</span></span>

## <span data-ttu-id="20cf1-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="20cf1-138">RELATED LINKS</span></span>

[<span data-ttu-id="20cf1-139">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="20cf1-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="20cf1-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="20cf1-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="20cf1-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="20cf1-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


