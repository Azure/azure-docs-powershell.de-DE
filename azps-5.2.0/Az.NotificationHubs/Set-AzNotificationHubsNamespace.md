---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295810"
---
# <span data-ttu-id="67abd-101">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="67abd-101">Set-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="67abd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67abd-102">SYNOPSIS</span></span>
<span data-ttu-id="67abd-103">Legt Eigenschaftswerte für einen Benachrichtigungshub-Namespace fest.</span><span class="sxs-lookup"><span data-stu-id="67abd-103">Sets property values for a notification hub namespace.</span></span>

## <span data-ttu-id="67abd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67abd-104">SYNTAX</span></span>

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67abd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67abd-105">DESCRIPTION</span></span>
<span data-ttu-id="67abd-106">Das **Cmdlet Set-AzNotificationHubsNamespace** legt die Eigenschaftswerte eines vorhandenen Benachrichtigungshub-Namespaces fest.</span><span class="sxs-lookup"><span data-stu-id="67abd-106">The **Set-AzNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>
<span data-ttu-id="67abd-107">Namespaces sind logische Container, mit deren Hilfe Sie Ihre Benachrichtigungshubs organisieren und verwalten können.</span><span class="sxs-lookup"><span data-stu-id="67abd-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="67abd-108">Sie müssen über mindestens einen Benachrichtigungshub-Namespace verfügen.</span><span class="sxs-lookup"><span data-stu-id="67abd-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="67abd-109">Darüber hinaus müssen alle Benachrichtigungshubs über einen zugewiesenen Namespace verfügen.</span><span class="sxs-lookup"><span data-stu-id="67abd-109">Additionally, all notification hubs must have an assigned namespace.</span></span>
<span data-ttu-id="67abd-110">Dieses Cmdlet wird in erster Linie zum Aktivieren und Deaktivieren eines Namespaces verwendet.</span><span class="sxs-lookup"><span data-stu-id="67abd-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="67abd-111">Wenn ein Namespace deaktiviert ist, können Benutzer keine Verbindung mit einem der Benachrichtigungshubs im Namespace herstellen, und Administratoren können diese Hubs auch nicht zum Senden von Pushbenachrichtigungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="67abd-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="67abd-112">Um einen deaktivierten Namespace erneut zu aktivieren, verwenden Sie dieses Cmdlet, um die **"State"-Eigenschaft** des Namespaces auf "Active" zu setzen.</span><span class="sxs-lookup"><span data-stu-id="67abd-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>
<span data-ttu-id="67abd-113">Sie können dieses Cmdlet auch verwenden, um einen Namespace als kritisch zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="67abd-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="67abd-114">Dadurch wird verhindert, dass der Namespace gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="67abd-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="67abd-115">Um einen kritischen Namespace zu entfernen, müssen Sie zuerst das "Critical"-Tag entfernen.</span><span class="sxs-lookup"><span data-stu-id="67abd-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="67abd-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="67abd-116">EXAMPLES</span></span>

### <span data-ttu-id="67abd-117">Beispiel 1: Deaktivieren eines Namespaces</span><span class="sxs-lookup"><span data-stu-id="67abd-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="67abd-118">Mit diesem Befehl wird der Namespace "ContosoPartners" deaktiviert, der sich im Rechenzentrum "USA, Westen" befindet und der Ressourcengruppe "ContosoNotificationsGroup" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="67abd-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="67abd-119">Beispiel 2: Aktivieren eines Namespaces</span><span class="sxs-lookup"><span data-stu-id="67abd-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="67abd-120">Dieser Befehl aktiviert den Namespace "ContosoPartners", der sich im Rechenzentrum "USA, Westen" befindet und der Ressourcengruppe "ContosoNotificationsGroup" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="67abd-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="67abd-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67abd-121">PARAMETERS</span></span>

### <span data-ttu-id="67abd-122">-Kritisch</span><span class="sxs-lookup"><span data-stu-id="67abd-122">-Critical</span></span>
<span data-ttu-id="67abd-123">Gibt an, ob der Namespace ein kritischer Namespace ist.</span><span class="sxs-lookup"><span data-stu-id="67abd-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="67abd-124">Wichtige Namespaces können nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="67abd-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="67abd-125">Um einen kritischen Namespace zu löschen, müssen Sie den Wert dieser Eigenschaft auf "False" festlegen, um den Namespace als nicht kritisch zu markieren.</span><span class="sxs-lookup"><span data-stu-id="67abd-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67abd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67abd-126">-DefaultProfile</span></span>
<span data-ttu-id="67abd-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="67abd-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67abd-128">-Force</span><span class="sxs-lookup"><span data-stu-id="67abd-128">-Force</span></span>
<span data-ttu-id="67abd-129">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="67abd-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="67abd-130">-Location</span><span class="sxs-lookup"><span data-stu-id="67abd-130">-Location</span></span>
<span data-ttu-id="67abd-131">Gibt den Anzeigenamen des Rechenzentrums an, das den Namespace hostet.</span><span class="sxs-lookup"><span data-stu-id="67abd-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="67abd-132">Obwohl Sie diesen Parameter auf einen beliebigen gültigen Azure-Standort festlegen können, sollten Sie für optimale Leistung ein Rechenzentrum verwenden, das sich in der Nähe der Meisten Ihrer Benutzer befindet.</span><span class="sxs-lookup"><span data-stu-id="67abd-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>
<span data-ttu-id="67abd-133">Führen Sie den folgenden Befehl aus, um eine aktuelle Liste der Azure-Speicherorte zu erhalten: `Get-AzLocation | Select-Object DisplayName`</span><span class="sxs-lookup"><span data-stu-id="67abd-133">To get an up-to-date list of Azure locations run the following command: `Get-AzLocation | Select-Object DisplayName`</span></span>

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

### <span data-ttu-id="67abd-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="67abd-134">-Namespace</span></span>
<span data-ttu-id="67abd-135">Gibt den Namespace an, den dieses Cmdlet ändert.</span><span class="sxs-lookup"><span data-stu-id="67abd-135">Specifies the namespace that this cmdlet modifies.</span></span>
<span data-ttu-id="67abd-136">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="67abd-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="67abd-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="67abd-137">-ResourceGroup</span></span>
<span data-ttu-id="67abd-138">Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="67abd-138">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="67abd-139">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach die Bestandsverwaltung und die Verwaltung von Azure unterstützen.</span><span class="sxs-lookup"><span data-stu-id="67abd-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="67abd-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="67abd-140">-SkuTier</span></span>
<span data-ttu-id="67abd-141">SKU-Ebene des Namespaces</span><span class="sxs-lookup"><span data-stu-id="67abd-141">Sku tier of the namespace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67abd-142">-State</span><span class="sxs-lookup"><span data-stu-id="67abd-142">-State</span></span>
<span data-ttu-id="67abd-143">Gibt den aktuellen Zustand des Namespace an.</span><span class="sxs-lookup"><span data-stu-id="67abd-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="67abd-144">Die zulässigen Werte für diesen Parameter sind: "Aktiv" und "Deaktiviert".</span><span class="sxs-lookup"><span data-stu-id="67abd-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67abd-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="67abd-145">-Tag</span></span>
<span data-ttu-id="67abd-146">Gibt Name-Wert-Paare an, die zum Kategorisieren und Organisieren von Azure-Elementen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="67abd-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="67abd-147">Tags funktionieren ähnlich wie Schlüsselwörter und funktionieren in einer gesamten Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="67abd-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="67abd-148">Wenn Sie z. B. nach allen Elementen mit der Markierung "Department:IT" suchen, gibt die Suche alle Azure-Elemente zurück, die dieses Tag enthalten, unabhängig von Elementtyp, Speicherort oder Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="67abd-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="67abd-149">Ein einzelnes Tag besteht aus zwei Teilen: dem *Namen* und (optional) dem *Wert.*</span><span class="sxs-lookup"><span data-stu-id="67abd-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="67abd-150">In "Department:IT" ist der Tagname beispielsweise "Department" (Abteilung) und der Tagwert "IT".</span><span class="sxs-lookup"><span data-stu-id="67abd-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="67abd-151">Verwenden Sie zum Hinzufügen eines Tags eine ähnliche Syntax für Hashtabellen, die das Tag "CalendarYear:2016: -Tags @{Name="CalendarYear" erstellt. Value="2016"} Um mehrere Tags in demselben Befehl hinzuzufügen, trennen Sie die einzelnen Tags durch Kommas: -Tag @{Name="CalendarYear"; Value="2016"}, @{Name="FiscalYear"; Value="2017"}</span><span class="sxs-lookup"><span data-stu-id="67abd-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016: -Tags @{Name="CalendarYear";Value="2016"} To add multiple tags in the same command, separate the individual tags by using commas: -Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67abd-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67abd-152">-Confirm</span></span>
<span data-ttu-id="67abd-153">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="67abd-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67abd-154">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="67abd-154">-WhatIf</span></span>
<span data-ttu-id="67abd-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67abd-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67abd-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67abd-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67abd-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67abd-157">CommonParameters</span></span>
<span data-ttu-id="67abd-158">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67abd-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67abd-159">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67abd-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67abd-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="67abd-160">INPUTS</span></span>

### <span data-ttu-id="67abd-161">System.String</span><span class="sxs-lookup"><span data-stu-id="67abd-161">System.String</span></span>

### <span data-ttu-id="67abd-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span><span class="sxs-lookup"><span data-stu-id="67abd-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span></span>

### <span data-ttu-id="67abd-163">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="67abd-163">System.Boolean</span></span>

### <span data-ttu-id="67abd-164">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="67abd-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="67abd-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="67abd-165">OUTPUTS</span></span>

### <span data-ttu-id="67abd-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="67abd-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="67abd-167">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="67abd-167">NOTES</span></span>

## <span data-ttu-id="67abd-168">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="67abd-168">RELATED LINKS</span></span>

[<span data-ttu-id="67abd-169">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="67abd-169">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="67abd-170">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="67abd-170">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="67abd-171">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="67abd-171">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)


