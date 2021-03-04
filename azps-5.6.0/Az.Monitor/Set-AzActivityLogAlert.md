---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/powershell/module/az.monitor/set-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
ms.openlocfilehash: d01399eeedf3b27bbf74e969876e24180ed571b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924792"
---
# <span data-ttu-id="0b518-101">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0b518-101">Set-AzActivityLogAlert</span></span>

## <span data-ttu-id="0b518-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b518-102">SYNOPSIS</span></span>
<span data-ttu-id="0b518-103">Erstellt eine neue oder legt eine vorhandene Aktivitätsprotokollbenachrichtigung fest.</span><span class="sxs-lookup"><span data-stu-id="0b518-103">Creates a new or sets an existing activity log alert.</span></span>

## <span data-ttu-id="0b518-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b518-104">SYNTAX</span></span>

### <span data-ttu-id="0b518-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0b518-105">SetByNameAndResourceGroup</span></span>
```
Set-AzActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b518-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0b518-106">SetByResourceId</span></span>
```
Set-AzActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b518-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="0b518-107">SetByInputObject</span></span>
```
Set-AzActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b518-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b518-108">DESCRIPTION</span></span>
<span data-ttu-id="0b518-109">Das **Cmdlet Set-AzActivityLogAlert** erstellt ein neues oder legt eine vorhandene Aktivitätsprotokollbenachrichtigung fest.</span><span class="sxs-lookup"><span data-stu-id="0b518-109">The **Set-AzActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="0b518-110">Für Tags, Bedingungen und Aktionen müssen die Objekte im Voraus erstellt und als Parameter in diesem Aufruf als durch Komma getrennte Übergeben werden (siehe beispiel unten).</span><span class="sxs-lookup"><span data-stu-id="0b518-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="0b518-111">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h. es kann eine Bestätigung vom Benutzer anfordern, bevor die Ressource tatsächlich erstellt/geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0b518-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="0b518-112">**HINWEIS:** Dieses Cmdlet und die zugehörigen cmdlet ersetzen das veraltete (November 2017) **Add-AzLogAlertRule**.</span><span class="sxs-lookup"><span data-stu-id="0b518-112">**NOTE**: This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzLogAlertRule**.</span></span>

## <span data-ttu-id="0b518-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b518-113">EXAMPLES</span></span>

### <span data-ttu-id="0b518-114">Beispiel 1: Erstellen einer Aktivitätsprotokollbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="0b518-114">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equal 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equal 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="0b518-115">Die ersten vier Befehle erstellen Blattbedingung und Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0b518-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="0b518-116">Der letzte Befehl erstellt eine Aktivitätsprotokollbenachrichtigung mit der Bedingung und der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0b518-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="0b518-117">Beispiel 2: Erstellen einer Aktivitätsprotokollbenachrichtigung deaktiviert</span><span class="sxs-lookup"><span data-stu-id="0b518-117">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equal 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equal 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="0b518-118">Die ersten vier Befehle erstellen Blattbedingung und Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0b518-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="0b518-119">Mit dem letzten Befehl wird eine Aktivitätsprotokollbenachrichtigung mit der Bedingung und der Aktionsgruppe erstellt, die Benachrichtigung wird jedoch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0b518-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="0b518-120">Beispiel 3: Festlegen einer Aktivitätsprotokollbenachrichtigung basierend auf einem Wert aus der Pipe oder dem Parameter InputObject</span><span class="sxs-lookup"><span data-stu-id="0b518-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzActivityLogAlert
PS C:\>$alert = Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzActivityLogAlert -InputObject $alert
```

<span data-ttu-id="0b518-121">Der erste Befehl ähnelt einem Nop. Er legt die Benachrichtigung mit den gleichen Werten fest, die bereits enthalten sind Die restlichen Befehle rufen die Warnungsregel ab, ändern die Beschreibung und deaktivieren sie, und verwenden Sie dann den Parameter InputObject, um diese Änderungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0b518-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="0b518-122">Beispiel 4: Festlegen einer Aktivitätsprotokollbenachrichtigung basierend auf dem ResourceId-Wert aus der Pipe</span><span class="sxs-lookup"><span data-stu-id="0b518-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Set-AzActivityLogAlert -DisableAlert
```

<span data-ttu-id="0b518-123">Wenn die angegebene Protokollbenachrichtigungsregel vorhanden ist, wird sie mit diesem Befehl deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0b518-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="0b518-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0b518-124">PARAMETERS</span></span>

### <span data-ttu-id="0b518-125">-Aktion</span><span class="sxs-lookup"><span data-stu-id="0b518-125">-Action</span></span>
<span data-ttu-id="0b518-126">Die Liste der Aktionsgruppen für die Aktivitätsprotokollbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="0b518-126">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b518-127">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="0b518-127">-Condition</span></span>
<span data-ttu-id="0b518-128">Die Liste der Bedingungen für die Aktivitätsprotokollbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="0b518-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="0b518-129">**HINWEIS:** In der Liste der Bedingungen muss mindestens eine mit dem Feld gleich "Kategorie" vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="0b518-129">**NOTE**: In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="0b518-130">Das Back-End antwortet mit 400 (BadRequest), wenn diese Bedingung nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0b518-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b518-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b518-131">-DefaultProfile</span></span>
<span data-ttu-id="0b518-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0b518-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b518-133">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b518-133">-Description</span></span>
<span data-ttu-id="0b518-134">Die Beschreibung der Warnungsressource.</span><span class="sxs-lookup"><span data-stu-id="0b518-134">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b518-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="0b518-135">-DisableAlert</span></span>
<span data-ttu-id="0b518-136">Ermöglicht dem Benutzer das Erstellen eines deaktivierten Aktivitätsprotokolls.</span><span class="sxs-lookup"><span data-stu-id="0b518-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="0b518-137">Wenn sie nicht angegeben werden, werden die Benachrichtigungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0b518-137">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b518-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b518-138">-InputObject</span></span>
<span data-ttu-id="0b518-139">Legt die InputObject-Tags-Eigenschaft des Aufrufs fest, um den erforderlichen Namen und die Eigenschaften des Ressourcengruppennamens zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="0b518-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b518-140">-Location</span><span class="sxs-lookup"><span data-stu-id="0b518-140">-Location</span></span>
<span data-ttu-id="0b518-141">Der Speicherort, an dem die Aktivitätsprotokollbenachrichtigung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0b518-141">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b518-142">-Name</span><span class="sxs-lookup"><span data-stu-id="0b518-142">-Name</span></span>
<span data-ttu-id="0b518-143">Der Name der Aktivitätsprotokollbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="0b518-143">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b518-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b518-144">-ResourceGroupName</span></span>
<span data-ttu-id="0b518-145">Der Name der Ressourcengruppe, in der die Warnungsressource vorhanden sein soll.</span><span class="sxs-lookup"><span data-stu-id="0b518-145">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b518-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b518-146">-ResourceId</span></span>
<span data-ttu-id="0b518-147">Legt die ResourceId-Tags-Eigenschaft des Aufrufs fest, um den erforderlichen Namen, die Eigenschaften des Ressourcengruppennamens zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="0b518-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b518-148">-Scope</span><span class="sxs-lookup"><span data-stu-id="0b518-148">-Scope</span></span>
<span data-ttu-id="0b518-149">Die Liste der Bereiche für die Aktivitätsprotokollbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="0b518-149">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b518-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b518-150">-Tag</span></span>
<span data-ttu-id="0b518-151">Legt die Tags-Eigenschaft der Aktivitätsprotokollbenachrichtigungsressource fest.</span><span class="sxs-lookup"><span data-stu-id="0b518-151">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b518-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b518-152">-Confirm</span></span>
<span data-ttu-id="0b518-153">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b518-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b518-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b518-154">-WhatIf</span></span>
<span data-ttu-id="0b518-155">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b518-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b518-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b518-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b518-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b518-157">CommonParameters</span></span>
<span data-ttu-id="0b518-158">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b518-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b518-159">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b518-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b518-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b518-160">INPUTS</span></span>

### <span data-ttu-id="0b518-161">System.String</span><span class="sxs-lookup"><span data-stu-id="0b518-161">System.String</span></span>

### <span data-ttu-id="0b518-162">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0b518-162">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0b518-163">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="0b518-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0b518-164">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="0b518-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0b518-165">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0b518-165">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0b518-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="0b518-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="0b518-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b518-167">OUTPUTS</span></span>

### <span data-ttu-id="0b518-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="0b518-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="0b518-169">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0b518-169">NOTES</span></span>

## <span data-ttu-id="0b518-170">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0b518-170">RELATED LINKS</span></span>

[<span data-ttu-id="0b518-171">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0b518-171">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="0b518-172">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0b518-172">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="0b518-173">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0b518-173">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="0b518-174">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0b518-174">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="0b518-175">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="0b518-175">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="0b518-176">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="0b518-176">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
