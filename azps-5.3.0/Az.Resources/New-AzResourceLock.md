---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 7f21704783a9992cc0d1b0fdf3da50cb21656b0e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459296"
---
# <span data-ttu-id="5975a-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5975a-101">New-AzResourceLock</span></span>

## <span data-ttu-id="5975a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5975a-102">SYNOPSIS</span></span>
<span data-ttu-id="5975a-103">Erstellt eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="5975a-103">Creates a resource lock.</span></span>

## <span data-ttu-id="5975a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5975a-104">SYNTAX</span></span>

### <span data-ttu-id="5975a-105">BySpecifiedScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="5975a-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5975a-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5975a-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5975a-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="5975a-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5975a-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="5975a-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5975a-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="5975a-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5975a-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="5975a-110">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5975a-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5975a-111">DESCRIPTION</span></span>
<span data-ttu-id="5975a-112">Das **Cmdlet "New-AzResourceLock"** erstellt eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="5975a-112">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="5975a-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5975a-113">EXAMPLES</span></span>

### <span data-ttu-id="5975a-114">Beispiel 1: Erstellen einer Ressourcensperre auf einer Website</span><span class="sxs-lookup"><span data-stu-id="5975a-114">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="5975a-115">Mit diesem Befehl wird eine Ressourcensperre für eine Website erstellt.</span><span class="sxs-lookup"><span data-stu-id="5975a-115">This command creates a resource lock on a website.</span></span>

### <span data-ttu-id="5975a-116">Beispiel 2: Erstellen einer Ressourcensperre für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="5975a-116">Example 2: Create a resource lock on a database</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "Lock note" -LockName "db-lock" -ResourceName "server1/ContosoDB"  -ResourceGroupName "RG1" -ResourceType "Microsoft.Sql/servers/databases"
```

<span data-ttu-id="5975a-117">Dieser Befehl erstellt eine Ressourcensperre für eine Azure-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5975a-117">This command creates a resource lock on a Azure database.</span></span>

## <span data-ttu-id="5975a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5975a-118">PARAMETERS</span></span>

### <span data-ttu-id="5975a-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5975a-119">-ApiVersion</span></span>
<span data-ttu-id="5975a-120">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="5975a-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5975a-121">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="5975a-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5975a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5975a-122">-DefaultProfile</span></span>
<span data-ttu-id="5975a-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5975a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5975a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="5975a-124">-Force</span></span>
<span data-ttu-id="5975a-125">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="5975a-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5975a-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="5975a-126">-LockId</span></span>
<span data-ttu-id="5975a-127">Gibt die ID der Sperre an.</span><span class="sxs-lookup"><span data-stu-id="5975a-127">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="5975a-128">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="5975a-128">-LockLevel</span></span>
<span data-ttu-id="5975a-129">Gibt die Ebene für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="5975a-129">Specifies the level for the lock.</span></span>
<span data-ttu-id="5975a-130">Derzeit sind gültige Werte "CanNotDelete, ReadOnly".</span><span class="sxs-lookup"><span data-stu-id="5975a-130">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="5975a-131">-LockName</span><span class="sxs-lookup"><span data-stu-id="5975a-131">-LockName</span></span>
<span data-ttu-id="5975a-132">Gibt den Namen der Sperre an.</span><span class="sxs-lookup"><span data-stu-id="5975a-132">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="5975a-133">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="5975a-133">-LockNotes</span></span>
<span data-ttu-id="5975a-134">Gibt die Notizen für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="5975a-134">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="5975a-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="5975a-135">-Pre</span></span>
<span data-ttu-id="5975a-136">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5975a-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5975a-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5975a-137">-ResourceGroupName</span></span>
<span data-ttu-id="5975a-138">Gibt den Namen einer Ressourcengruppe an, für die die Sperre gilt oder die die Ressourcengruppe enthält, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="5975a-138">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="5975a-139">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5975a-139">-ResourceName</span></span>
<span data-ttu-id="5975a-140">Gibt den Namen der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="5975a-140">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="5975a-141">Um beispielsweise eine Datenbank anzugeben, verwenden Sie das folgende Format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="5975a-141">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="5975a-142">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5975a-142">-ResourceType</span></span>
<span data-ttu-id="5975a-143">Gibt den Ressourcentyp der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="5975a-143">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="5975a-144">-Scope</span><span class="sxs-lookup"><span data-stu-id="5975a-144">-Scope</span></span>
<span data-ttu-id="5975a-145">Gibt den Bereich an, auf den die Sperre angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5975a-145">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="5975a-146">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: Name der Name der Abonnement-ID-Ressourcengruppe, Name des Servernamens, Um eine Ressourcengruppe anzugeben, verwenden Sie das folgende Format: Name der `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` `/databases/` `/subscriptions/` Abonnement-ID-Ressourcengruppe. `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="5975a-146">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="5975a-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5975a-147">-Confirm</span></span>
<span data-ttu-id="5975a-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5975a-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5975a-149">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5975a-149">-WhatIf</span></span>
<span data-ttu-id="5975a-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5975a-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5975a-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5975a-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5975a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5975a-152">CommonParameters</span></span>
<span data-ttu-id="5975a-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5975a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5975a-154">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5975a-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5975a-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5975a-155">INPUTS</span></span>

### <span data-ttu-id="5975a-156">System.String</span><span class="sxs-lookup"><span data-stu-id="5975a-156">System.String</span></span>

### <span data-ttu-id="5975a-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span><span class="sxs-lookup"><span data-stu-id="5975a-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="5975a-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5975a-158">OUTPUTS</span></span>

### <span data-ttu-id="5975a-159">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="5975a-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5975a-160">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5975a-160">NOTES</span></span>

## <span data-ttu-id="5975a-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5975a-161">RELATED LINKS</span></span>

[<span data-ttu-id="5975a-162">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5975a-162">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="5975a-163">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5975a-163">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="5975a-164">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5975a-164">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


