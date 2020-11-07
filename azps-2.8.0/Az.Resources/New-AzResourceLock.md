---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: a0d796d49114cc11fcc50aef85a3ab502593dc35
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824987"
---
# <span data-ttu-id="f0976-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f0976-101">New-AzResourceLock</span></span>

## <span data-ttu-id="f0976-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f0976-102">SYNOPSIS</span></span>
<span data-ttu-id="f0976-103">Erstellt eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="f0976-103">Creates a resource lock.</span></span>

## <span data-ttu-id="f0976-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0976-104">SYNTAX</span></span>

### <span data-ttu-id="f0976-105">BySpecifiedScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="f0976-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0976-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f0976-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0976-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="f0976-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0976-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="f0976-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0976-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="f0976-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0976-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="f0976-110">ByTenantLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0976-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="f0976-111">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0976-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0976-112">DESCRIPTION</span></span>
<span data-ttu-id="f0976-113">Das Cmdlet **New-AzResourceLock** erstellt eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="f0976-113">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="f0976-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0976-114">EXAMPLES</span></span>

### <span data-ttu-id="f0976-115">Beispiel 1: Erstellen einer Ressourcensperre auf einer Website</span><span class="sxs-lookup"><span data-stu-id="f0976-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="f0976-116">Dieser Befehl erstellt eine Ressourcensperre auf einer Website.</span><span class="sxs-lookup"><span data-stu-id="f0976-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="f0976-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0976-117">PARAMETERS</span></span>

### <span data-ttu-id="f0976-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f0976-118">-ApiVersion</span></span>
<span data-ttu-id="f0976-119">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="f0976-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f0976-120">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="f0976-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f0976-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0976-121">-DefaultProfile</span></span>
<span data-ttu-id="f0976-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f0976-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0976-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f0976-123">-Force</span></span>
<span data-ttu-id="f0976-124">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f0976-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f0976-125">-Sperre</span><span class="sxs-lookup"><span data-stu-id="f0976-125">-LockId</span></span>
<span data-ttu-id="f0976-126">Gibt die ID der Sperre an.</span><span class="sxs-lookup"><span data-stu-id="f0976-126">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="f0976-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="f0976-127">-LockLevel</span></span>
<span data-ttu-id="f0976-128">Gibt die Ebene für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="f0976-128">Specifies the level for the lock.</span></span>
<span data-ttu-id="f0976-129">Gültige Werte sind derzeit können, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="f0976-129">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="f0976-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="f0976-130">-LockName</span></span>
<span data-ttu-id="f0976-131">Gibt den Namen der Sperre an.</span><span class="sxs-lookup"><span data-stu-id="f0976-131">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="f0976-132">-Sie LockNotes</span><span class="sxs-lookup"><span data-stu-id="f0976-132">-LockNotes</span></span>
<span data-ttu-id="f0976-133">Gibt die Notizen für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="f0976-133">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="f0976-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="f0976-134">-Pre</span></span>
<span data-ttu-id="f0976-135">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f0976-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f0976-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0976-136">-ResourceGroupName</span></span>
<span data-ttu-id="f0976-137">Gibt den Namen einer Ressourcengruppe an, für die die Sperre gilt oder die die Ressourcengruppe enthält, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="f0976-137">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="f0976-138">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f0976-138">-ResourceName</span></span>
<span data-ttu-id="f0976-139">Gibt den Namen der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="f0976-139">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="f0976-140">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="f0976-140">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="f0976-141">-</span><span class="sxs-lookup"><span data-stu-id="f0976-141">-ResourceType</span></span>
<span data-ttu-id="f0976-142">Gibt den Ressourcentyp der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="f0976-142">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="f0976-143">-Scope</span><span class="sxs-lookup"><span data-stu-id="f0976-143">-Scope</span></span>
<span data-ttu-id="f0976-144">Gibt den Bereich an, auf den die Sperre angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0976-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="f0976-145">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: `/subscriptions/` Abonnement-ID- `/resourceGroups/` Ressourcengruppenname `/providers/Microsoft.Sql/servers/` Servername-Datenbankname `/databases/` zum Angeben einer Ressourcengruppe verwenden Sie das folgende Format: `/subscriptions/` Name der `/resourceGroups/` Ressourcengruppe "Abonnement-ID"</span><span class="sxs-lookup"><span data-stu-id="f0976-145">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="f0976-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="f0976-146">-TenantLevel</span></span>
<span data-ttu-id="f0976-147">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="f0976-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="f0976-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0976-148">-Confirm</span></span>
<span data-ttu-id="f0976-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0976-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0976-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0976-150">-WhatIf</span></span>
<span data-ttu-id="f0976-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0976-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0976-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0976-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0976-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0976-153">CommonParameters</span></span>
<span data-ttu-id="f0976-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0976-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0976-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0976-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0976-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f0976-156">INPUTS</span></span>

### <span data-ttu-id="f0976-157">System. String</span><span class="sxs-lookup"><span data-stu-id="f0976-157">System.String</span></span>

### <span data-ttu-id="f0976-158">Microsoft. Azure. Commands. ResourceManager. Cmdlets. Entities. Locks. LockLevel</span><span class="sxs-lookup"><span data-stu-id="f0976-158">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="f0976-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f0976-159">OUTPUTS</span></span>

### <span data-ttu-id="f0976-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f0976-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f0976-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="f0976-161">NOTES</span></span>

## <span data-ttu-id="f0976-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f0976-162">RELATED LINKS</span></span>

[<span data-ttu-id="f0976-163">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f0976-163">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="f0976-164">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f0976-164">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="f0976-165">Satz-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f0976-165">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


