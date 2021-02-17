---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158745"
---
# <span data-ttu-id="e0aa1-101">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e0aa1-101">New-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="e0aa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="e0aa1-103">Erstellt einen Benachrichtigungshub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-103">Creates a notification hub namespace.</span></span>

## <span data-ttu-id="e0aa1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0aa1-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0aa1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0aa1-105">DESCRIPTION</span></span>
<span data-ttu-id="e0aa1-106">Das **Cmdlet "New-AzNotificationHubsNamespace"** erstellt einen Benachrichtigungshub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-106">The **New-AzNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>
<span data-ttu-id="e0aa1-107">Namespaces sind logische Container, mit deren Hilfe Sie Ihre Benachrichtigungshubs organisieren und verwalten können.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="e0aa1-108">Sie müssen über mindestens einen Benachrichtigungshub-Namespace verfügen.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="e0aa1-109">Ein einzelner Namespace kann mehrere Hubs haben.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="e0aa1-110">Sie können über mehrere Namespaces verfügen, um Ihre Hubs zu organisieren oder bestimmten Personen die Berechtigung zum Verwalten einer ausgewählten Teilmenge Ihrer Hubs zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>
<span data-ttu-id="e0aa1-111">Um einen Namespace zu erstellen, stellen Sie sicher, dass Sie einen eindeutigen Namen für den Namespace angeben. geben Sie das Rechenzentrum an, in dem sich der Namespace befinden soll; und geben Sie die Ressourcengruppe an, der der Namespace zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="e0aa1-112">Nachdem der Namespace erstellt wurde, können Sie das cmdlet New-AzNotificationHubsNamespaceAuthorizationRules verwenden, um diesem Namespace Autorisierungsregeln zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-112">After the namespace has been created you can use the New-AzNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="e0aa1-113">Autorisierungsregeln werden verwendet, um Berechtigungen für den Namespace zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="e0aa1-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e0aa1-114">EXAMPLES</span></span>

### <span data-ttu-id="e0aa1-115">Beispiel 1: Erstellen eines Benachrichtigungshubs</span><span class="sxs-lookup"><span data-stu-id="e0aa1-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="e0aa1-116">Mit diesem Befehl wird ein Benachrichtigungshub namens "ContosoPartners" erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="e0aa1-117">Der Namespace befindet sich im Rechenzentrum "USA, Westen" und wird der Ressourcengruppe "ContosoNotificationsGroup" zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="e0aa1-118">Beispiel 2: Erstellen eines Benachrichtigungshubs mit Tags</span><span class="sxs-lookup"><span data-stu-id="e0aa1-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="e0aa1-119">Mit diesem Befehl wird ein Benachrichtigungshub namens "ContosoPartners" erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="e0aa1-120">Der Namespace befindet sich im Rechenzentrum "USA, Westen" und wird der Ressourcengruppe "ContosoNotificationsGroup" zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="e0aa1-121">Darüber hinaus erstellt dieser Befehl ein Tag mit dem Namen "Audience" und dem Wert "PartnerOrganizations" und wird dem Namespace zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="e0aa1-122">Dadurch wird sichergestellt, dass der Namespace immer angezeigt wird, wenn Sie nach Elementen filtern, für die das Tag "Audience" auf "PartnerOrganizations" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="e0aa1-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0aa1-123">PARAMETERS</span></span>

### <span data-ttu-id="e0aa1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0aa1-124">-DefaultProfile</span></span>
<span data-ttu-id="e0aa1-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e0aa1-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0aa1-126">-Location</span><span class="sxs-lookup"><span data-stu-id="e0aa1-126">-Location</span></span>
<span data-ttu-id="e0aa1-127">Gibt den Anzeigenamen des Rechenzentrums an, das den Namespace hosten soll.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-127">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="e0aa1-128">Obwohl Sie diesen Parameter auf einen beliebigen gültigen Speicherort festlegen können, können Sie zur optimalen Leistung ein Rechenzentrum verwenden, das sich in der Nähe der Mehrzahl der Benutzer befindet.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-128">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

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

### <span data-ttu-id="e0aa1-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e0aa1-129">-Namespace</span></span>
<span data-ttu-id="e0aa1-130">Gibt den Namen des neuen Namespace an.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-130">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="e0aa1-131">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="e0aa1-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e0aa1-132">-ResourceGroup</span></span>
<span data-ttu-id="e0aa1-133">Gibt die Ressourcengruppe an, der der Namespace zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-133">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="e0aa1-134">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach zur Bestandsverwaltung und Verwaltung beitragen.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="e0aa1-135">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e0aa1-135">-SkuTier</span></span>
<span data-ttu-id="e0aa1-136">SKU-Ebene des Namespaces</span><span class="sxs-lookup"><span data-stu-id="e0aa1-136">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="e0aa1-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0aa1-137">-Tag</span></span>
<span data-ttu-id="e0aa1-138">Gibt Name-Wert-Paare an, die zum Kategorisieren und Organisieren von Azure-Elementen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-138">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="e0aa1-139">Tags funktionieren ähnlich wie Schlüsselwörter und funktionieren in einer gesamten Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-139">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="e0aa1-140">Wenn Sie z. B. nach allen Elementen mit dem Tag "Department:IT" suchen, gibt die Suche alle Azure-Elemente zurück, die dieses Tag enthalten, unabhängig von Elementtyp, Speicherort oder Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-140">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="e0aa1-141">Ein einzelnes Tag besteht aus zwei Teilen: dem *Namen* und optional dem *Wert.*</span><span class="sxs-lookup"><span data-stu-id="e0aa1-141">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="e0aa1-142">In "Department:IT" ist der Tagname beispielsweise "Department" (Abteilung) und der Tagwert "IT".</span><span class="sxs-lookup"><span data-stu-id="e0aa1-142">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="e0aa1-143">Verwenden Sie zum Hinzufügen eines Tags eine ähnliche Hashtabellensyntax wie die folgende, wodurch das Tag "CalendarYear:2016" erstellt wird:</span><span class="sxs-lookup"><span data-stu-id="e0aa1-143">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

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

### <span data-ttu-id="e0aa1-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0aa1-144">-Confirm</span></span>
<span data-ttu-id="e0aa1-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0aa1-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e0aa1-146">-WhatIf</span></span>
<span data-ttu-id="e0aa1-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0aa1-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0aa1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0aa1-149">CommonParameters</span></span>
<span data-ttu-id="e0aa1-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0aa1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0aa1-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0aa1-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0aa1-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e0aa1-152">INPUTS</span></span>

### <span data-ttu-id="e0aa1-153">System.String</span><span class="sxs-lookup"><span data-stu-id="e0aa1-153">System.String</span></span>

### <span data-ttu-id="e0aa1-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e0aa1-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e0aa1-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e0aa1-155">OUTPUTS</span></span>

### <span data-ttu-id="e0aa1-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e0aa1-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="e0aa1-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e0aa1-157">NOTES</span></span>

## <span data-ttu-id="e0aa1-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e0aa1-158">RELATED LINKS</span></span>

[<span data-ttu-id="e0aa1-159">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e0aa1-159">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="e0aa1-160">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e0aa1-160">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="e0aa1-161">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e0aa1-161">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


