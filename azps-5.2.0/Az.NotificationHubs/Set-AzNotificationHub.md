---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 7083c6872981cefaa12dc01612f3eb27cc7676ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295822"
---
# <span data-ttu-id="4f840-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4f840-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="4f840-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f840-102">SYNOPSIS</span></span>
<span data-ttu-id="4f840-103">Legt Eigenschaftswerte für einen Benachrichtigungshub fest.</span><span class="sxs-lookup"><span data-stu-id="4f840-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="4f840-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f840-104">SYNTAX</span></span>

### <span data-ttu-id="4f840-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f840-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f840-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f840-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f840-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f840-107">DESCRIPTION</span></span>
<span data-ttu-id="4f840-108">Das **Cmdlet Set-AzNotificationHub** ändert die Eigenschaftswerte eines Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="4f840-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="4f840-109">Sie können den Wert einer Benachrichtigungshubeigenschaft auf zwei Arten ändern.</span><span class="sxs-lookup"><span data-stu-id="4f840-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="4f840-110">Sie können beispielsweise eine Instanz des **NotificationHubAttributes-Objekts** erstellen und dieses Objekt dann mit den Eigenschaftswerten konfigurieren, die der neue Hub besitzen soll.</span><span class="sxs-lookup"><span data-stu-id="4f840-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="4f840-111">Dies kann über .NET Framework geschehen.</span><span class="sxs-lookup"><span data-stu-id="4f840-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="4f840-112">Anschließend können Sie diese Eigenschaftswerte über den Parameter *NotificationHubObj* in Ihren Hub kopieren.</span><span class="sxs-lookup"><span data-stu-id="4f840-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="4f840-113">Alternativ können Sie eine JSON(JavaScript Object Notation)-Datei erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann über den *Parameter InputFile* anwenden.</span><span class="sxs-lookup"><span data-stu-id="4f840-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="4f840-114">Eine #A0 ist eine Textdatei, in der die folgende Syntax verwendet wird: {</span><span class="sxs-lookup"><span data-stu-id="4f840-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="4f840-115">"Name": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="4f840-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="4f840-116">"Location": "West US",</span><span class="sxs-lookup"><span data-stu-id="4f840-116">"Location": "West US",</span></span>  
<span data-ttu-id="4f840-117">} Bei Verwendung in Verbindung mit dem **Cmdlet "Set-AzNotificationHub"** wird im vorherigen Beispiel für JSON der Standortwert eines Benachrichtigungshubs mit dem Namen "ContosoNotificationHub" auf "USA, Westen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4f840-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="4f840-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f840-118">EXAMPLES</span></span>

### <span data-ttu-id="4f840-119">Beispiel 1: Ändern der Eigenschaftswerte für einen Benachrichtigungshub</span><span class="sxs-lookup"><span data-stu-id="4f840-119">Example 1: Modify the property values for a notification hub</span></span>
```powershell
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="4f840-120">Dieser Befehl ändert die Eigenschaftswerte für einen Benachrichtigungshub im ContosoNamespace-Namespace und hat ihn der Ressourcengruppe "ContosoNotificationsGroup" zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="4f840-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="4f840-121">Die Eigenschaftswerte sowie der Name des zu ändernde Hubs werden im Befehl nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="4f840-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="4f840-122">Stattdessen sind diese Informationen in der Eingabedatei enthalten, auf C:\Configuration\Hubs.jsist.</span><span class="sxs-lookup"><span data-stu-id="4f840-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

### <span data-ttu-id="4f840-123">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4f840-123">Example 2</span></span>

<span data-ttu-id="4f840-124">Legt Eigenschaftswerte für einen Benachrichtigungshub fest.</span><span class="sxs-lookup"><span data-stu-id="4f840-124">Sets property values for a notification hub.</span></span> <span data-ttu-id="4f840-125">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="4f840-125">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHubObj <NotificationHubAttributes> -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="4f840-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f840-126">PARAMETERS</span></span>

### <span data-ttu-id="4f840-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f840-127">-DefaultProfile</span></span>
<span data-ttu-id="4f840-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4f840-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f840-129">-Force</span><span class="sxs-lookup"><span data-stu-id="4f840-129">-Force</span></span>
<span data-ttu-id="4f840-130">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="4f840-130">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4f840-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="4f840-131">-InputFile</span></span>
<span data-ttu-id="4f840-132">Gibt den Pfad zu einer JSON-Datei an, die Konfigurationsinformationen für den Benachrichtigungshub enthält.</span><span class="sxs-lookup"><span data-stu-id="4f840-132">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f840-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4f840-133">-Namespace</span></span>
<span data-ttu-id="4f840-134">Gibt den Namespace an, dem der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4f840-134">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="4f840-135">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="4f840-135">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="4f840-136">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="4f840-136">-NotificationHubObj</span></span>
<span data-ttu-id="4f840-137">Gibt das **NotificationHubAttributes-Objekt** an, das Konfigurationsinformationen für den Hub enthält, den dieses Cmdlet ändert.</span><span class="sxs-lookup"><span data-stu-id="4f840-137">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f840-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4f840-138">-ResourceGroup</span></span>
<span data-ttu-id="4f840-139">Gibt die Ressourcengruppe an, der der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4f840-139">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="4f840-140">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach die Bestandsverwaltung und die Verwaltung von Azure unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4f840-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="4f840-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f840-141">-Confirm</span></span>
<span data-ttu-id="4f840-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f840-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f840-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4f840-143">-WhatIf</span></span>
<span data-ttu-id="4f840-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f840-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f840-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f840-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f840-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f840-146">CommonParameters</span></span>
<span data-ttu-id="4f840-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f840-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f840-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f840-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f840-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f840-149">INPUTS</span></span>

### <span data-ttu-id="4f840-150">System.String</span><span class="sxs-lookup"><span data-stu-id="4f840-150">System.String</span></span>

## <span data-ttu-id="4f840-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f840-151">OUTPUTS</span></span>

### <span data-ttu-id="4f840-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="4f840-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="4f840-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4f840-153">NOTES</span></span>

## <span data-ttu-id="4f840-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4f840-154">RELATED LINKS</span></span>

[<span data-ttu-id="4f840-155">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4f840-155">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="4f840-156">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4f840-156">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="4f840-157">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4f840-157">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


