---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: c532633de593294c6b5dbe0e09b9615a1d5355a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305587"
---
# <span data-ttu-id="affaf-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="affaf-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="affaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="affaf-102">SYNOPSIS</span></span>
<span data-ttu-id="affaf-103">Ändert eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="affaf-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="affaf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="affaf-104">SYNTAX</span></span>

### <span data-ttu-id="affaf-105">BySpecifiedScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="affaf-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="affaf-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="affaf-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="affaf-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="affaf-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="affaf-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="affaf-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="affaf-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="affaf-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="affaf-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="affaf-110">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="affaf-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="affaf-111">DESCRIPTION</span></span>
<span data-ttu-id="affaf-112">Das **Cmdlet "Set-AzResourceLock"** ändert eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="affaf-112">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="affaf-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="affaf-113">EXAMPLES</span></span>

### <span data-ttu-id="affaf-114">Beispiel 1: Aktualisieren von Notizen für eine Sperre</span><span class="sxs-lookup"><span data-stu-id="affaf-114">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="affaf-115">Mit diesem Befehl wird die Notiz für eine Sperre namens "ContosoSiteLock" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="affaf-115">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="affaf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="affaf-116">PARAMETERS</span></span>

### <span data-ttu-id="affaf-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="affaf-117">-ApiVersion</span></span>
<span data-ttu-id="affaf-118">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="affaf-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="affaf-119">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="affaf-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affaf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="affaf-120">-DefaultProfile</span></span>
<span data-ttu-id="affaf-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="affaf-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="affaf-122">-Force</span><span class="sxs-lookup"><span data-stu-id="affaf-122">-Force</span></span>
<span data-ttu-id="affaf-123">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="affaf-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="affaf-124">-LockId</span><span class="sxs-lookup"><span data-stu-id="affaf-124">-LockId</span></span>
<span data-ttu-id="affaf-125">Gibt die ID der Sperre an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="affaf-125">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affaf-126">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="affaf-126">-LockLevel</span></span>
<span data-ttu-id="affaf-127">Gibt die Ebene für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="affaf-127">Specifies the level for the lock.</span></span>
<span data-ttu-id="affaf-128">Derzeit ist der einzige gültige Wert "CanNotDelete".</span><span class="sxs-lookup"><span data-stu-id="affaf-128">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affaf-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="affaf-129">-LockName</span></span>
<span data-ttu-id="affaf-130">Gibt den Namen der Sperre an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="affaf-130">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affaf-131">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="affaf-131">-LockNotes</span></span>
<span data-ttu-id="affaf-132">Gibt die Notizen für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="affaf-132">Specifies the notes for the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affaf-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="affaf-133">-Pre</span></span>
<span data-ttu-id="affaf-134">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="affaf-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="affaf-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="affaf-135">-ResourceGroupName</span></span>
<span data-ttu-id="affaf-136">Gibt den Namen der Ressourcengruppe an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="affaf-136">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affaf-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="affaf-137">-ResourceName</span></span>
<span data-ttu-id="affaf-138">Gibt den Namen der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="affaf-138">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="affaf-139">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende `/` Format: Serverdatenbank</span><span class="sxs-lookup"><span data-stu-id="affaf-139">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affaf-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="affaf-140">-ResourceType</span></span>
<span data-ttu-id="affaf-141">Gibt den Ressourcentyp an, für den die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="affaf-141">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affaf-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="affaf-142">-Scope</span></span>
<span data-ttu-id="affaf-143">Gibt den Bereich an, auf den die Sperre angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="affaf-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="affaf-144">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: Name der Name der Abonnement-ID-Ressourcengruppe, Name des Servernamens, Um eine Ressourcengruppe anzugeben, verwenden Sie das folgende Format: Name der `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` `/databases/` `/subscriptions/` Abonnement-ID-Ressourcengruppe. `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="affaf-144">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affaf-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="affaf-145">-Confirm</span></span>
<span data-ttu-id="affaf-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="affaf-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affaf-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="affaf-147">-WhatIf</span></span>
<span data-ttu-id="affaf-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="affaf-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="affaf-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="affaf-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affaf-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="affaf-150">CommonParameters</span></span>
<span data-ttu-id="affaf-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="affaf-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="affaf-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="affaf-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="affaf-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="affaf-153">INPUTS</span></span>

### <span data-ttu-id="affaf-154">System.String</span><span class="sxs-lookup"><span data-stu-id="affaf-154">System.String</span></span>

### <span data-ttu-id="affaf-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span><span class="sxs-lookup"><span data-stu-id="affaf-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="affaf-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="affaf-156">OUTPUTS</span></span>

### <span data-ttu-id="affaf-157">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="affaf-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="affaf-158">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="affaf-158">NOTES</span></span>

## <span data-ttu-id="affaf-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="affaf-159">RELATED LINKS</span></span>

[<span data-ttu-id="affaf-160">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="affaf-160">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="affaf-161">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="affaf-161">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="affaf-162">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="affaf-162">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


