---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 7f0732225389f5174c2097cea57ed38d9ea2be0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918176"
---
# <span data-ttu-id="8aca0-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="8aca0-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="8aca0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aca0-102">SYNOPSIS</span></span>
<span data-ttu-id="8aca0-103">Legt Eigenschaftswerte für einen Benachrichtigungshub fest.</span><span class="sxs-lookup"><span data-stu-id="8aca0-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="8aca0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8aca0-104">SYNTAX</span></span>

### <span data-ttu-id="8aca0-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aca0-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8aca0-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aca0-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8aca0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8aca0-107">DESCRIPTION</span></span>
<span data-ttu-id="8aca0-108">Das **Cmdlet Set-AzNotificationHub** ändert die Eigenschaftswerte eines Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="8aca0-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="8aca0-109">Sie können einen Benachrichtigungshubeigenschaftswert auf zwei Arten ändern.</span><span class="sxs-lookup"><span data-stu-id="8aca0-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="8aca0-110">Zum einen können Sie eine Instanz des **NotificationHubAttributes-Objekts** erstellen und dieses Objekt dann mit den Eigenschaftswerten konfigurieren, die der neue Hub besitzen soll.</span><span class="sxs-lookup"><span data-stu-id="8aca0-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="8aca0-111">Dies kann über die .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="8aca0-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="8aca0-112">Sie können diese Eigenschaftswerte dann über den Parameter *NotificationHubObj* in Ihren Hub kopieren.</span><span class="sxs-lookup"><span data-stu-id="8aca0-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="8aca0-113">Alternativ können Sie eine JSON-Datei (JavaScript Object Notation) erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann über den *Parameter InputFile* anwenden.</span><span class="sxs-lookup"><span data-stu-id="8aca0-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="8aca0-114">Eine #A0 ist eine Textdatei, die eine syntax ähnliche Syntax wie die folgende verwendet: {</span><span class="sxs-lookup"><span data-stu-id="8aca0-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="8aca0-115">"Name": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="8aca0-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="8aca0-116">"Location": "West US",</span><span class="sxs-lookup"><span data-stu-id="8aca0-116">"Location": "West US",</span></span>  
<span data-ttu-id="8aca0-117">} Bei Verwendung in Verbindung mit dem **Set-AzNotificationHub-Cmdlet** legt das vorherige JSON-Beispiel den Standortwert eines Benachrichtigungshubs namens ContosoNotificationHub auf West US fest.</span><span class="sxs-lookup"><span data-stu-id="8aca0-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="8aca0-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8aca0-118">EXAMPLES</span></span>

### <span data-ttu-id="8aca0-119">Beispiel 1: Ändern der Eigenschaftswerte für einen Benachrichtigungshub</span><span class="sxs-lookup"><span data-stu-id="8aca0-119">Example 1: Modify the property values for a notification hub</span></span>
```powershell
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="8aca0-120">Mit diesem Befehl werden die Eigenschaftswerte für einen Benachrichtigungshub geändert, der im ContosoNamespace-Namespace gefunden und der Ressourcengruppe ContosoNotificationsGroup zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="8aca0-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="8aca0-121">Die Eigenschaftswerte sowie der Name des hub, der geändert werden soll, werden im Befehl nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="8aca0-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="8aca0-122">Stattdessen sind diese Informationen in der Eingabedatei enthalten, die C:\Configuration\Hubs.jsist.</span><span class="sxs-lookup"><span data-stu-id="8aca0-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

### <span data-ttu-id="8aca0-123">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8aca0-123">Example 2</span></span>

<span data-ttu-id="8aca0-124">Legt Eigenschaftswerte für einen Benachrichtigungshub fest.</span><span class="sxs-lookup"><span data-stu-id="8aca0-124">Sets property values for a notification hub.</span></span> <span data-ttu-id="8aca0-125">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="8aca0-125">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHubObj <NotificationHubAttributes> -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="8aca0-126">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8aca0-126">PARAMETERS</span></span>

### <span data-ttu-id="8aca0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aca0-127">-DefaultProfile</span></span>
<span data-ttu-id="8aca0-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8aca0-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8aca0-129">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="8aca0-129">-Force</span></span>
<span data-ttu-id="8aca0-130">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="8aca0-130">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8aca0-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="8aca0-131">-InputFile</span></span>
<span data-ttu-id="8aca0-132">Gibt den Pfad zu einer JSON-Datei an, die Konfigurationsinformationen für den Benachrichtigungshub enthält.</span><span class="sxs-lookup"><span data-stu-id="8aca0-132">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="8aca0-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8aca0-133">-Namespace</span></span>
<span data-ttu-id="8aca0-134">Gibt den Namespace an, dem der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="8aca0-134">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="8aca0-135">Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.</span><span class="sxs-lookup"><span data-stu-id="8aca0-135">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="8aca0-136">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="8aca0-136">-NotificationHubObj</span></span>
<span data-ttu-id="8aca0-137">Gibt das **NotificationHubAttributes-Objekt** an, das Konfigurationsinformationen für den Hub enthält, den dieses Cmdlet ändert.</span><span class="sxs-lookup"><span data-stu-id="8aca0-137">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8aca0-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8aca0-138">-ResourceGroup</span></span>
<span data-ttu-id="8aca0-139">Gibt die Ressourcengruppe an, der der Benachrichtigungshub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="8aca0-139">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="8aca0-140">Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die einfach die Bestandsverwaltung und die Azure-Verwaltung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8aca0-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8aca0-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8aca0-141">-Confirm</span></span>
<span data-ttu-id="8aca0-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8aca0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aca0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aca0-143">-WhatIf</span></span>
<span data-ttu-id="8aca0-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8aca0-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8aca0-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8aca0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aca0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aca0-146">CommonParameters</span></span>
<span data-ttu-id="8aca0-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aca0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aca0-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8aca0-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aca0-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8aca0-149">INPUTS</span></span>

### <span data-ttu-id="8aca0-150">System.String</span><span class="sxs-lookup"><span data-stu-id="8aca0-150">System.String</span></span>

## <span data-ttu-id="8aca0-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8aca0-151">OUTPUTS</span></span>

### <span data-ttu-id="8aca0-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="8aca0-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="8aca0-153">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8aca0-153">NOTES</span></span>

## <span data-ttu-id="8aca0-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8aca0-154">RELATED LINKS</span></span>

[<span data-ttu-id="8aca0-155">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="8aca0-155">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="8aca0-156">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="8aca0-156">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="8aca0-157">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="8aca0-157">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


