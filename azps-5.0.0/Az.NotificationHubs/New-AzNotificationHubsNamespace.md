---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301353"
---
# <span data-ttu-id="d17da-101">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d17da-101">New-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="d17da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d17da-102">SYNOPSIS</span></span>
<span data-ttu-id="d17da-103">Erstellt einen Benachrichtigungs-Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="d17da-103">Creates a notification hub namespace.</span></span>

## <span data-ttu-id="d17da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d17da-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d17da-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d17da-105">DESCRIPTION</span></span>
<span data-ttu-id="d17da-106">Das Cmdlet **New-AzNotificationHubsNamespace** erstellt einen Benachrichtigungs-Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="d17da-106">The **New-AzNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>
<span data-ttu-id="d17da-107">Namespaces sind logische Container, die Ihnen beim organisieren und Verwalten Ihrer benachrichtigungshubs helfen.</span><span class="sxs-lookup"><span data-stu-id="d17da-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="d17da-108">Sie müssen über mindestens einen Benachrichtigungs-Hub-Namespace verfügen.</span><span class="sxs-lookup"><span data-stu-id="d17da-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="d17da-109">Ein einzelner Namespace kann mehrere Hubs beherbergen.</span><span class="sxs-lookup"><span data-stu-id="d17da-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="d17da-110">Sie können mehrere Namespaces haben, um Ihre Hubs zu organisieren oder bestimmten Personen die Berechtigung zum Verwalten einer ausgewählten Teilmenge ihrer Hubs zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="d17da-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>
<span data-ttu-id="d17da-111">Wenn Sie einen Namespace erstellen möchten, stellen Sie sicher, dass Sie einen eindeutigen Namen für den Namespace angeben. Geben Sie das Rechenzentrum an, in dem sich der Namespace befinden soll. und geben Sie die Ressourcengruppe an, der der Namespace zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d17da-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="d17da-112">Nachdem der Namespace erstellt wurde, können Sie das New-AzNotificationHubsNamespaceAuthorizationRules-Cmdlet verwenden, um diesem Namespace Autorisierungsregeln zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="d17da-112">After the namespace has been created you can use the New-AzNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="d17da-113">Autorisierungsregeln werden verwendet, um Berechtigungen für den Namespace zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="d17da-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="d17da-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d17da-114">EXAMPLES</span></span>

### <span data-ttu-id="d17da-115">Beispiel 1: Erstellen eines benachrichtigungshubs</span><span class="sxs-lookup"><span data-stu-id="d17da-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="d17da-116">Dieser Befehl erstellt einen Benachrichtigungs-Hub mit dem Namen ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="d17da-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="d17da-117">Der Namespace befindet sich im West-US-Rechenzentrum und wird der ContosoNotificationsGroup-Ressourcengruppe zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d17da-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="d17da-118">Beispiel 2: Erstellen eines benachrichtigungshubs mit Tags</span><span class="sxs-lookup"><span data-stu-id="d17da-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="d17da-119">Dieser Befehl erstellt einen Benachrichtigungs-Hub mit dem Namen ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="d17da-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="d17da-120">Der Namespace befindet sich im West-US-Rechenzentrum und wird der ContosoNotificationsGroup-Ressourcengruppe zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d17da-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="d17da-121">Darüber hinaus erstellt dieser Befehl ein Tag mit dem Namen Audience und dem Wert PartnerOrganizations und wird dem Namespace zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d17da-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="d17da-122">Dadurch wird sichergestellt, dass der Namespace jedes Mal angezeigt wird, wenn Sie nach Elementen filtern, deren Audience-Tag auf PartnerOrganizations festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="d17da-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="d17da-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="d17da-123">PARAMETERS</span></span>

### <span data-ttu-id="d17da-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d17da-124">-DefaultProfile</span></span>
<span data-ttu-id="d17da-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d17da-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d17da-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="d17da-126">-Location</span></span>
<span data-ttu-id="d17da-127">Gibt den Anzeigenamen des Rechenzentrums an, das den Namespace hosten soll.</span><span class="sxs-lookup"><span data-stu-id="d17da-127">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="d17da-128">Obwohl Sie diesen Parameter an einen beliebigen gültigen Speicherort setzen können, empfiehlt es sich, für optimale Leistung ein Rechenzentrum in der Nähe der meisten Benutzer zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d17da-128">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

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

### <span data-ttu-id="d17da-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d17da-129">-Namespace</span></span>
<span data-ttu-id="d17da-130">Gibt den Namen des neuen Namespaces an.</span><span class="sxs-lookup"><span data-stu-id="d17da-130">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="d17da-131">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="d17da-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="d17da-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d17da-132">-ResourceGroup</span></span>
<span data-ttu-id="d17da-133">Gibt die Ressourcengruppe an, der der Namespace zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="d17da-133">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="d17da-134">Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d17da-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="d17da-135">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d17da-135">-SkuTier</span></span>
<span data-ttu-id="d17da-136">SKU-Ebene des Namespaces</span><span class="sxs-lookup"><span data-stu-id="d17da-136">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="d17da-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="d17da-137">-Tag</span></span>
<span data-ttu-id="d17da-138">Gibt Namen-Wert-Paare an, die zum Kategorisieren und organisieren von Azure-Elementen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="d17da-138">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="d17da-139">Tags funktionieren ähnlich wie Schlüsselwörter und funktionieren in einer Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="d17da-139">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="d17da-140">Wenn Sie beispielsweise nach allen Elementen mit der Tag-Abteilung suchen, gibt die Suche alle Azure-Elemente zurück, die diese Kategorie aufweisen, und zwar unabhängig von Elementen wie Elementtyp, Speicherort oder Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d17da-140">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="d17da-141">Ein einzelnes Tag besteht aus zwei Teilen: dem *Namen* und optional dem *Wert*.</span><span class="sxs-lookup"><span data-stu-id="d17da-141">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="d17da-142">Beispielsweise ist in Department: IT der Tag-Name Department, und der Tag-Wert ist dieser.</span><span class="sxs-lookup"><span data-stu-id="d17da-142">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="d17da-143">Verwenden Sie zum Hinzufügen einer Kategorie die Hashtabellen Syntax ähnlich dieser, wodurch das Tag CalendarYear: 2016 erstellt wird:</span><span class="sxs-lookup"><span data-stu-id="d17da-143">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d17da-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d17da-144">-Confirm</span></span>
<span data-ttu-id="d17da-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d17da-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d17da-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d17da-146">-WhatIf</span></span>
<span data-ttu-id="d17da-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d17da-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d17da-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d17da-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d17da-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d17da-149">CommonParameters</span></span>
<span data-ttu-id="d17da-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d17da-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d17da-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d17da-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d17da-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d17da-152">INPUTS</span></span>

### <span data-ttu-id="d17da-153">System. String</span><span class="sxs-lookup"><span data-stu-id="d17da-153">System.String</span></span>

### <span data-ttu-id="d17da-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d17da-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d17da-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d17da-155">OUTPUTS</span></span>

### <span data-ttu-id="d17da-156">Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d17da-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="d17da-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="d17da-157">NOTES</span></span>

## <span data-ttu-id="d17da-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d17da-158">RELATED LINKS</span></span>

[<span data-ttu-id="d17da-159">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d17da-159">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="d17da-160">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d17da-160">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="d17da-161">Satz-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d17da-161">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


