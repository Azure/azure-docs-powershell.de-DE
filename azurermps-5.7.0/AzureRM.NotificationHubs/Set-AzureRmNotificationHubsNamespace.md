---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b1fe6ae9085dcfc1d74eaf86af831a1e984a9143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665180"
---
# <span data-ttu-id="ac487-101">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ac487-101">Set-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="ac487-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac487-102">SYNOPSIS</span></span>
<span data-ttu-id="ac487-103">Legt Eigenschaftswerte für einen Notification Hub-Namespace fest.</span><span class="sxs-lookup"><span data-stu-id="ac487-103">Sets property values for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac487-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac487-104">SYNTAX</span></span>

```
Set-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac487-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac487-105">DESCRIPTION</span></span>
<span data-ttu-id="ac487-106">Das Cmdlet " **Set-AzureRmNotificationHubsNamespace** " legt die Eigenschaftswerte eines vorhandenen Benachrichtigungs-Hub-Namespace fest.</span><span class="sxs-lookup"><span data-stu-id="ac487-106">The **Set-AzureRmNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>

<span data-ttu-id="ac487-107">Namespaces sind logische Container, die Ihnen beim organisieren und Verwalten Ihrer benachrichtigungshubs helfen.</span><span class="sxs-lookup"><span data-stu-id="ac487-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="ac487-108">Sie müssen über mindestens einen Benachrichtigungs-Hub-Namespace verfügen.</span><span class="sxs-lookup"><span data-stu-id="ac487-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="ac487-109">Darüber hinaus müssen alle benachrichtigungshubs über einen zugewiesenen Namespace verfügen.</span><span class="sxs-lookup"><span data-stu-id="ac487-109">Additionally, all notification hubs must have an assigned namespace.</span></span>

<span data-ttu-id="ac487-110">Dieses Cmdlet wird in erster Linie verwendet, um einen Namespace zu aktivieren und zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ac487-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="ac487-111">Wenn ein Namespace deaktiviert ist, können Benutzer keine Verbindung mit einem der benachrichtigungshubs im Namespace herstellen, und Administratoren können diese Hubs auch nicht verwenden, um Push-Benachrichtigungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="ac487-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="ac487-112">Wenn Sie einen deaktivierten Namespace erneut aktivieren möchten, verwenden Sie dieses Cmdlet, um die **State** -Eigenschaft des Namespaces auf Active festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ac487-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>

<span data-ttu-id="ac487-113">Sie können dieses Cmdlet auch verwenden, um einen Namespace als kritisch zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="ac487-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="ac487-114">Dadurch wird verhindert, dass der Namespace gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="ac487-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="ac487-115">Um einen kritischen Namespace zu entfernen, müssen Sie zuerst das kritische Tag entfernen.</span><span class="sxs-lookup"><span data-stu-id="ac487-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="ac487-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac487-116">EXAMPLES</span></span>

### <span data-ttu-id="ac487-117">Beispiel 1: Deaktivieren eines Namespaces</span><span class="sxs-lookup"><span data-stu-id="ac487-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="ac487-118">Mit diesem Befehl wird der Namespacenamens ContosoPartners deaktiviert, der sich im Rechenzentrum von West-US befindet und der ContosoNotificationsGroup-Ressourcengruppe zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ac487-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="ac487-119">Beispiel 2: Aktivieren eines Namespaces</span><span class="sxs-lookup"><span data-stu-id="ac487-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="ac487-120">Mit diesem Befehl wird der Namespacenamens ContosoPartners im West US-Rechenzentrum aktiviert und der ContosoNotificationsGroup-Ressourcengruppe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ac487-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="ac487-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac487-121">PARAMETERS</span></span>

### <span data-ttu-id="ac487-122">-Kritisch</span><span class="sxs-lookup"><span data-stu-id="ac487-122">-Critical</span></span>
<span data-ttu-id="ac487-123">Gibt an, ob es sich bei dem Namespace um einen kritischen Namespace handelt.</span><span class="sxs-lookup"><span data-stu-id="ac487-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="ac487-124">Kritische Namespaces können nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="ac487-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="ac487-125">Um einen kritischen Namespace zu löschen, müssen Sie den Wert dieser Eigenschaft auf "false" festlegen, um den Namespace als nicht kritisch zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="ac487-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac487-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac487-126">-DefaultProfile</span></span>
<span data-ttu-id="ac487-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ac487-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac487-128">-Force</span><span class="sxs-lookup"><span data-stu-id="ac487-128">-Force</span></span>
<span data-ttu-id="ac487-129">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="ac487-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ac487-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="ac487-130">-Location</span></span>
<span data-ttu-id="ac487-131">Gibt den Anzeigenamen des Rechenzentrums an, das den Namespace hostet.</span><span class="sxs-lookup"><span data-stu-id="ac487-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="ac487-132">Sie können diesen Parameter zwar auf einen beliebigen gültigen Azure-Speicherort setzen, doch sollten Sie für optimale Leistung ein Rechenzentrum verwenden, das sich in der Nähe der meisten Benutzer befindet.</span><span class="sxs-lookup"><span data-stu-id="ac487-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>

<span data-ttu-id="ac487-133">Führen Sie den folgenden Befehl aus, um eine aktuelle Liste der Azure-Speicherorte abzurufen:</span><span class="sxs-lookup"><span data-stu-id="ac487-133">To get an up-to-date list of Azure locations run the following command:</span></span>

`Get-AzureLocation | Select-Object DisplayName`

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

### <span data-ttu-id="ac487-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ac487-134">-Namespace</span></span>
<span data-ttu-id="ac487-135">Gibt den Namespace an, der vom Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ac487-135">Specifies the namespace that this cmdlet modifies.</span></span>

<span data-ttu-id="ac487-136">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="ac487-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="ac487-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ac487-137">-ResourceGroup</span></span>
<span data-ttu-id="ac487-138">Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ac487-138">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="ac487-139">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ac487-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="ac487-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ac487-140">-SkuTier</span></span>
<span data-ttu-id="ac487-141">SKU-Ebene des Namespaces</span><span class="sxs-lookup"><span data-stu-id="ac487-141">Sku tier of the namespace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac487-142">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="ac487-142">-State</span></span>
<span data-ttu-id="ac487-143">Gibt den aktuellen Zustand des Namespaces an.</span><span class="sxs-lookup"><span data-stu-id="ac487-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="ac487-144">Die zulässigen Werte für diesen Parameter sind: aktiv und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ac487-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac487-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="ac487-145">-Tag</span></span>
<span data-ttu-id="ac487-146">Gibt Namen-Wert-Paare an, die zum Kategorisieren und organisieren von Azure-Elementen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ac487-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="ac487-147">Tags funktionieren ähnlich wie Schlüsselwörter und funktionieren in einer Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="ac487-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="ac487-148">Wenn Sie beispielsweise nach allen Elementen mit der Tag-Abteilung suchen, gibt die Suche alle Azure-Elemente zurück, die diese Kategorie aufweisen, und zwar unabhängig von Elementen wie Elementtyp, Speicherort oder Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ac487-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>

<span data-ttu-id="ac487-149">Ein einzelnes Tag besteht aus zwei Teilen: dem *Namen* und (optional) dem *Wert*.</span><span class="sxs-lookup"><span data-stu-id="ac487-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="ac487-150">In Department: IT lautet der Tag-Name beispielsweise Department, und der Tag-Wert ist er.</span><span class="sxs-lookup"><span data-stu-id="ac487-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="ac487-151">Verwenden Sie zum Hinzufügen einer Kategorie die Hashtabellen Syntax ähnlich dieser, wodurch das Tag CalendarYear: 2016 erstellt wird:</span><span class="sxs-lookup"><span data-stu-id="ac487-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

<span data-ttu-id="ac487-152">-Tags @ {Name = "CalendarYear"; Value = "2016"}</span><span class="sxs-lookup"><span data-stu-id="ac487-152">-Tags @{Name="CalendarYear";Value="2016"}</span></span>

<span data-ttu-id="ac487-153">Wenn Sie mehrere Tags im gleichen Befehl hinzufügen möchten, trennen Sie die einzelnen Tags durch Kommas:</span><span class="sxs-lookup"><span data-stu-id="ac487-153">To add multiple tags in the same command, separate the individual tags by using commas:</span></span>

<span data-ttu-id="ac487-154">-Tag @ {Name = "CalendarYear"; Value = "2016"}, @ {Name = "FiscalYear"; Wert = "2017"}</span><span class="sxs-lookup"><span data-stu-id="ac487-154">-Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac487-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ac487-155">-Confirm</span></span>
<span data-ttu-id="ac487-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac487-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac487-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac487-157">-WhatIf</span></span>
<span data-ttu-id="ac487-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac487-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac487-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac487-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac487-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac487-160">CommonParameters</span></span>
<span data-ttu-id="ac487-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac487-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac487-162">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac487-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac487-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac487-163">INPUTS</span></span>

### <span data-ttu-id="ac487-164">Keine</span><span class="sxs-lookup"><span data-stu-id="ac487-164">None</span></span>
<span data-ttu-id="ac487-165">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ac487-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ac487-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac487-166">OUTPUTS</span></span>

### <span data-ttu-id="ac487-167">Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ac487-167">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="ac487-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac487-168">NOTES</span></span>

## <span data-ttu-id="ac487-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac487-169">RELATED LINKS</span></span>

[<span data-ttu-id="ac487-170">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ac487-170">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="ac487-171">Neu – AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ac487-171">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="ac487-172">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ac487-172">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)


