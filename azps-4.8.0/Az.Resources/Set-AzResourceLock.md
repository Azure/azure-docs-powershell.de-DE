---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: c532633de593294c6b5dbe0e09b9615a1d5355a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165628"
---
# <span data-ttu-id="11d5d-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="11d5d-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="11d5d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="11d5d-102">SYNOPSIS</span></span>
<span data-ttu-id="11d5d-103">Ändert eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="11d5d-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="11d5d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11d5d-104">SYNTAX</span></span>

### <span data-ttu-id="11d5d-105">BySpecifiedScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="11d5d-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11d5d-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="11d5d-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11d5d-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="11d5d-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11d5d-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="11d5d-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11d5d-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="11d5d-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11d5d-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="11d5d-110">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11d5d-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11d5d-111">DESCRIPTION</span></span>
<span data-ttu-id="11d5d-112">Das Cmdlet " **Satz-AzResourceLock** " ändert eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="11d5d-112">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="11d5d-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11d5d-113">EXAMPLES</span></span>

### <span data-ttu-id="11d5d-114">Beispiel 1: Aktualisieren von Notizen für eine Sperre</span><span class="sxs-lookup"><span data-stu-id="11d5d-114">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="11d5d-115">Mit diesem Befehl wird die Notiz für eine Sperre mit dem Namen ContosoSiteLock aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="11d5d-115">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="11d5d-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="11d5d-116">PARAMETERS</span></span>

### <span data-ttu-id="11d5d-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="11d5d-117">-ApiVersion</span></span>
<span data-ttu-id="11d5d-118">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="11d5d-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="11d5d-119">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="11d5d-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="11d5d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11d5d-120">-DefaultProfile</span></span>
<span data-ttu-id="11d5d-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="11d5d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11d5d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="11d5d-122">-Force</span></span>
<span data-ttu-id="11d5d-123">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="11d5d-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="11d5d-124">-Sperre</span><span class="sxs-lookup"><span data-stu-id="11d5d-124">-LockId</span></span>
<span data-ttu-id="11d5d-125">Gibt die ID der Sperre an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="11d5d-125">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="11d5d-126">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="11d5d-126">-LockLevel</span></span>
<span data-ttu-id="11d5d-127">Gibt die Ebene für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="11d5d-127">Specifies the level for the lock.</span></span>
<span data-ttu-id="11d5d-128">Derzeit ist der einzige gültige Wert können.</span><span class="sxs-lookup"><span data-stu-id="11d5d-128">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="11d5d-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="11d5d-129">-LockName</span></span>
<span data-ttu-id="11d5d-130">Gibt den Namen der Sperre an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="11d5d-130">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="11d5d-131">-Sie LockNotes</span><span class="sxs-lookup"><span data-stu-id="11d5d-131">-LockNotes</span></span>
<span data-ttu-id="11d5d-132">Gibt die Notizen für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="11d5d-132">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="11d5d-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="11d5d-133">-Pre</span></span>
<span data-ttu-id="11d5d-134">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="11d5d-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="11d5d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11d5d-135">-ResourceGroupName</span></span>
<span data-ttu-id="11d5d-136">Gibt den Namen der Ressourcengruppe an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="11d5d-136">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="11d5d-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="11d5d-137">-ResourceName</span></span>
<span data-ttu-id="11d5d-138">Gibt den Namen der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="11d5d-138">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="11d5d-139">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: Server `/` Datenbank</span><span class="sxs-lookup"><span data-stu-id="11d5d-139">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="11d5d-140">-</span><span class="sxs-lookup"><span data-stu-id="11d5d-140">-ResourceType</span></span>
<span data-ttu-id="11d5d-141">Gibt den Ressourcentyp an, für den die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="11d5d-141">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="11d5d-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="11d5d-142">-Scope</span></span>
<span data-ttu-id="11d5d-143">Gibt den Bereich an, auf den die Sperre angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="11d5d-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="11d5d-144">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: `/subscriptions/` Abonnement-ID- `/resourceGroups/` Ressourcengruppenname `/providers/Microsoft.Sql/servers/` Servername-Datenbankname `/databases/` zum Angeben einer Ressourcengruppe verwenden Sie das folgende Format: `/subscriptions/` Name der `/resourceGroups/` Ressourcengruppe "Abonnement-ID"</span><span class="sxs-lookup"><span data-stu-id="11d5d-144">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="11d5d-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="11d5d-145">-Confirm</span></span>
<span data-ttu-id="11d5d-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="11d5d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11d5d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11d5d-147">-WhatIf</span></span>
<span data-ttu-id="11d5d-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11d5d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11d5d-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="11d5d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11d5d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d5d-150">CommonParameters</span></span>
<span data-ttu-id="11d5d-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11d5d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d5d-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11d5d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d5d-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="11d5d-153">INPUTS</span></span>

### <span data-ttu-id="11d5d-154">System. String</span><span class="sxs-lookup"><span data-stu-id="11d5d-154">System.String</span></span>

### <span data-ttu-id="11d5d-155">Microsoft. Azure. Commands. ResourceManager. Cmdlets. Entities. Locks. LockLevel</span><span class="sxs-lookup"><span data-stu-id="11d5d-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="11d5d-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="11d5d-156">OUTPUTS</span></span>

### <span data-ttu-id="11d5d-157">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="11d5d-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="11d5d-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="11d5d-158">NOTES</span></span>

## <span data-ttu-id="11d5d-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="11d5d-159">RELATED LINKS</span></span>

[<span data-ttu-id="11d5d-160">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="11d5d-160">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="11d5d-161">Neu – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="11d5d-161">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="11d5d-162">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="11d5d-162">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


