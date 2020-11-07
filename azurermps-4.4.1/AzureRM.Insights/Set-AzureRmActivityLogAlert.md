---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
ms.openlocfilehash: 77d8792bf7499f2634ae525396568a9a21432f6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663574"
---
# <span data-ttu-id="044b4-101">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="044b4-101">Set-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="044b4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="044b4-102">SYNOPSIS</span></span>
<span data-ttu-id="044b4-103">Erstellt ein neues oder legt eine vorhandene Aktivitätsprotokoll Benachrichtigung fest.</span><span class="sxs-lookup"><span data-stu-id="044b4-103">Creates a new or sets an existing activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="044b4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="044b4-104">SYNTAX</span></span>

### <span data-ttu-id="044b4-105">Standardparameter für die Benachrichtigung "Aktivitätsprotokoll festlegen"</span><span class="sxs-lookup"><span data-stu-id="044b4-105">Default parameters for set activity log alert</span></span>
```
Set-AzureRmActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="044b4-106">Parameter zum Festlegen einer Aktivitätsprotokoll Benachrichtigung, wobei der Wert der "einquellen-Nr" aus der Pipe genommen wird</span><span class="sxs-lookup"><span data-stu-id="044b4-106">Parameters to set an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Set-AzureRmActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="044b4-107">Parameter zum Festlegen einer Aktivitätsprotokoll Benachrichtigung, die den Wert aus der Pipe nimmt</span><span class="sxs-lookup"><span data-stu-id="044b4-107">Parameters to set an activity log alerts taking value from the pipe</span></span>
```
Set-AzureRmActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="044b4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="044b4-108">DESCRIPTION</span></span>
<span data-ttu-id="044b4-109">Das Cmdlet " **Set-AzureRmActivityLogAlert** " erstellt ein neues oder legt eine vorhandene Aktivitätsprotokoll Warnung fest.</span><span class="sxs-lookup"><span data-stu-id="044b4-109">The **Set-AzureRmActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="044b4-110">Für Tags, Bedingungen und Aktionen müssen die Objekte im Voraus erstellt und als Parameter in diesem Aufruf als Komma getrennt übergeben werden (siehe Beispiel unten).</span><span class="sxs-lookup"><span data-stu-id="044b4-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="044b4-111">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt/geändert wird.</span><span class="sxs-lookup"><span data-stu-id="044b4-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>

## <span data-ttu-id="044b4-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="044b4-112">EXAMPLES</span></span>

### <span data-ttu-id="044b4-113">Beispiel 1: Erstellen einer Aktivitätsprotokoll Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="044b4-113">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="044b4-114">Die ersten vier Befehle erstellen Blatt Bedingung und Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="044b4-114">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="044b4-115">Der endgültige Befehl erstellt eine Aktivitätsprotokoll Benachrichtigung unter Verwendung der Bedingung und der Gruppe Aktion.</span><span class="sxs-lookup"><span data-stu-id="044b4-115">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="044b4-116">Beispiel 2: Erstellen einer Aktivitätsprotokoll Warnung deaktiviert</span><span class="sxs-lookup"><span data-stu-id="044b4-116">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="044b4-117">Die ersten vier Befehle erstellen Blatt Bedingung und Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="044b4-117">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="044b4-118">Mit dem letzten Befehl wird eine Aktivitätsprotokoll Benachrichtigung mithilfe der Bedingung und der Gruppe "Aktion" erstellt, die Benachrichtigung wird jedoch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="044b4-118">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="044b4-119">Beispiel 3: Einrichten einer Aktivitätsprotokoll Benachrichtigung auf Grundlage eines Werts aus der Pipe oder des Inputobject-Parameters</span><span class="sxs-lookup"><span data-stu-id="044b4-119">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzureRmActivityLogAlert
PS C:\>$alert = Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzureRmActivityLogAlert -InputObject $alert
```

<span data-ttu-id="044b4-120">Der erste Befehl ist mit einem NOP vergleichbar, er legt die Benachrichtigung mit den gleichen Werten fest, die bereits die restlichen Befehle enthalten, die Warnungsregel abzurufen, die Beschreibung zu ändern und zu deaktivieren und dann den Inputobject-Parameter zum Beibehalten dieser Änderungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="044b4-120">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="044b4-121">Beispiel 4: Einrichten einer Aktivitätsprotokoll Benachrichtigung basierend auf dem Wert des Typs "Resourcen" aus der Pipe</span><span class="sxs-lookup"><span data-stu-id="044b4-121">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzureRmActivityLogAlert -DisableAlert
```

<span data-ttu-id="044b4-122">Wenn die angegebene Protokoll Benachrichtigungsregel vorhanden ist, wird Sie von diesem Befehl deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="044b4-122">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="044b4-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="044b4-123">PARAMETERS</span></span>

### <span data-ttu-id="044b4-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="044b4-124">-Location</span></span>
<span data-ttu-id="044b4-125">Der Speicherort, an dem die Aktivitätsprotokoll Benachrichtigung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="044b4-125">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="044b4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="044b4-126">-Name</span></span>
<span data-ttu-id="044b4-127">Der Name der Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="044b4-127">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="044b4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="044b4-128">-ResourceGroupName</span></span>
<span data-ttu-id="044b4-129">Der Name der Ressourcengruppe, in der die Benachrichtigungs Ressource vorhanden sein wird.</span><span class="sxs-lookup"><span data-stu-id="044b4-129">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="044b4-130">-Scope</span><span class="sxs-lookup"><span data-stu-id="044b4-130">-Scope</span></span>
<span data-ttu-id="044b4-131">Die Liste der Bereiche für die Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="044b4-131">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="044b4-132">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="044b4-132">-Condition</span></span>
<span data-ttu-id="044b4-133">Die Liste der Bedingungen für die Benachrichtigung über das Aktivitätsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="044b4-133">The list of conditions for the activity log alert.</span></span>

<span data-ttu-id="044b4-134">**Hinweis** : in der Liste der Bedingungen muss mindestens eine mit dem Feld gleich "Category" vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="044b4-134">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="044b4-135">Das Back-End reagiert mit 400 (BadRequest), wenn diese Bedingung nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="044b4-135">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="044b4-136">– Aktion</span><span class="sxs-lookup"><span data-stu-id="044b4-136">-Action</span></span>
<span data-ttu-id="044b4-137">Die Liste der Aktionsgruppen für die Benachrichtigung zum Aktivitätsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="044b4-137">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="044b4-138">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="044b4-138">-DisableAlert</span></span>
<span data-ttu-id="044b4-139">Ermöglicht es dem Benutzer, eine deaktivierte Aktivitätsprotokoll Benachrichtigung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="044b4-139">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="044b4-140">Wenn diese Option nicht angegeben wurde, werden die Benachrichtigungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="044b4-140">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b4-141">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="044b4-141">-Description</span></span>
<span data-ttu-id="044b4-142">Die Beschreibung der Benachrichtigungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="044b4-142">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="044b4-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="044b4-143">-Tag</span></span>
<span data-ttu-id="044b4-144">Legt die Tags-Eigenschaft der Aktivitätsprotokoll-Warnungs Ressource fest.</span><span class="sxs-lookup"><span data-stu-id="044b4-144">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="044b4-145">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="044b4-145">-InputObject</span></span>
<span data-ttu-id="044b4-146">Legt die Inputobject-Tags-Eigenschaft des Aufrufs fest, um die Eigenschaften erforderlicher Name und Ressourcengruppenname zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="044b4-146">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="044b4-147">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="044b4-147">-ResourceId</span></span>
<span data-ttu-id="044b4-148">Legt die Eigenschaft "resourcetag-Tags" des Aufrufs fest, um den erforderlichen Namen, Eigenschaften von Ressourcengruppenname zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="044b4-148">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="044b4-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="044b4-149">-Confirm</span></span>
<span data-ttu-id="044b4-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="044b4-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="044b4-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="044b4-151">-DefaultProfile</span></span>
<span data-ttu-id="044b4-152">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="044b4-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b4-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="044b4-153">-WhatIf</span></span>
<span data-ttu-id="044b4-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="044b4-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="044b4-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="044b4-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="044b4-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="044b4-156">CommonParameters</span></span>
<span data-ttu-id="044b4-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="044b4-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="044b4-158">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="044b4-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="044b4-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="044b4-159">INPUTS</span></span>

## <span data-ttu-id="044b4-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="044b4-160">OUTPUTS</span></span>

### <span data-ttu-id="044b4-161">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="044b4-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="044b4-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="044b4-162">NOTES</span></span>

## <span data-ttu-id="044b4-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="044b4-163">RELATED LINKS</span></span>

[<span data-ttu-id="044b4-164">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="044b4-164">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="044b4-165">Deaktivieren-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="044b4-165">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="044b4-166">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="044b4-166">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="044b4-167">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="044b4-167">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="044b4-168">Neu – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="044b4-168">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="044b4-169">Neu – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="044b4-169">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
