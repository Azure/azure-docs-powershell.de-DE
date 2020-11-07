---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: f1220db034a2cdcc81ffbd7a146fee8e2c7201be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824911"
---
# <span data-ttu-id="0ca93-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0ca93-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="0ca93-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ca93-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca93-103">Ändert eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="0ca93-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="0ca93-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ca93-104">SYNTAX</span></span>

### <span data-ttu-id="0ca93-105">BySpecifiedScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ca93-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ca93-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0ca93-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ca93-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="0ca93-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ca93-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="0ca93-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ca93-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="0ca93-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ca93-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="0ca93-110">ByTenantLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ca93-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="0ca93-111">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ca93-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ca93-112">DESCRIPTION</span></span>
<span data-ttu-id="0ca93-113">Das Cmdlet " **Satz-AzResourceLock** " ändert eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="0ca93-113">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="0ca93-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ca93-114">EXAMPLES</span></span>

### <span data-ttu-id="0ca93-115">Beispiel 1: Aktualisieren von Notizen für eine Sperre</span><span class="sxs-lookup"><span data-stu-id="0ca93-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="0ca93-116">Mit diesem Befehl wird die Notiz für eine Sperre mit dem Namen ContosoSiteLock aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0ca93-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="0ca93-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ca93-117">PARAMETERS</span></span>

### <span data-ttu-id="0ca93-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0ca93-118">-ApiVersion</span></span>
<span data-ttu-id="0ca93-119">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="0ca93-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0ca93-120">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="0ca93-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0ca93-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ca93-121">-DefaultProfile</span></span>
<span data-ttu-id="0ca93-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0ca93-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ca93-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0ca93-123">-Force</span></span>
<span data-ttu-id="0ca93-124">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="0ca93-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0ca93-125">-Sperre</span><span class="sxs-lookup"><span data-stu-id="0ca93-125">-LockId</span></span>
<span data-ttu-id="0ca93-126">Gibt die ID der Sperre an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0ca93-126">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0ca93-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="0ca93-127">-LockLevel</span></span>
<span data-ttu-id="0ca93-128">Gibt die Ebene für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="0ca93-128">Specifies the level for the lock.</span></span>
<span data-ttu-id="0ca93-129">Derzeit ist der einzige gültige Wert können.</span><span class="sxs-lookup"><span data-stu-id="0ca93-129">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="0ca93-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="0ca93-130">-LockName</span></span>
<span data-ttu-id="0ca93-131">Gibt den Namen der Sperre an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0ca93-131">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ca93-132">-Sie LockNotes</span><span class="sxs-lookup"><span data-stu-id="0ca93-132">-LockNotes</span></span>
<span data-ttu-id="0ca93-133">Gibt die Notizen für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="0ca93-133">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="0ca93-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="0ca93-134">-Pre</span></span>
<span data-ttu-id="0ca93-135">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="0ca93-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0ca93-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ca93-136">-ResourceGroupName</span></span>
<span data-ttu-id="0ca93-137">Gibt den Namen der Ressourcengruppe an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="0ca93-137">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="0ca93-138">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0ca93-138">-ResourceName</span></span>
<span data-ttu-id="0ca93-139">Gibt den Namen der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="0ca93-139">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="0ca93-140">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: Server `/` Datenbank</span><span class="sxs-lookup"><span data-stu-id="0ca93-140">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ca93-141">-</span><span class="sxs-lookup"><span data-stu-id="0ca93-141">-ResourceType</span></span>
<span data-ttu-id="0ca93-142">Gibt den Ressourcentyp an, für den die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="0ca93-142">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ca93-143">-Scope</span><span class="sxs-lookup"><span data-stu-id="0ca93-143">-Scope</span></span>
<span data-ttu-id="0ca93-144">Gibt den Bereich an, auf den die Sperre angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ca93-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="0ca93-145">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: `/subscriptions/` Abonnement-ID- `/resourceGroups/` Ressourcengruppenname `/providers/Microsoft.Sql/servers/` Servername-Datenbankname `/databases/` zum Angeben einer Ressourcengruppe verwenden Sie das folgende Format: `/subscriptions/` Name der `/resourceGroups/` Ressourcengruppe "Abonnement-ID"</span><span class="sxs-lookup"><span data-stu-id="0ca93-145">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="0ca93-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="0ca93-146">-TenantLevel</span></span>
<span data-ttu-id="0ca93-147">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="0ca93-147">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca93-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0ca93-148">-Confirm</span></span>
<span data-ttu-id="0ca93-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0ca93-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ca93-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ca93-150">-WhatIf</span></span>
<span data-ttu-id="0ca93-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ca93-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ca93-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ca93-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ca93-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca93-153">CommonParameters</span></span>
<span data-ttu-id="0ca93-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ca93-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca93-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ca93-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca93-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ca93-156">INPUTS</span></span>

### <span data-ttu-id="0ca93-157">System. String</span><span class="sxs-lookup"><span data-stu-id="0ca93-157">System.String</span></span>

### <span data-ttu-id="0ca93-158">Microsoft. Azure. Commands. ResourceManager. Cmdlets. Entities. Locks. LockLevel</span><span class="sxs-lookup"><span data-stu-id="0ca93-158">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="0ca93-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ca93-159">OUTPUTS</span></span>

### <span data-ttu-id="0ca93-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0ca93-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0ca93-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ca93-161">NOTES</span></span>

## <span data-ttu-id="0ca93-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ca93-162">RELATED LINKS</span></span>

[<span data-ttu-id="0ca93-163">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0ca93-163">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="0ca93-164">Neu – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0ca93-164">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="0ca93-165">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0ca93-165">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


