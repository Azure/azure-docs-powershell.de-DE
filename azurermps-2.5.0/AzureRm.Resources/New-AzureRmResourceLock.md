---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: 8556f71263aefe721225906aa1480c4f0bc19f7c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850251"
---
# <span data-ttu-id="731d1-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="731d1-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="731d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="731d1-102">SYNOPSIS</span></span>
<span data-ttu-id="731d1-103">Erstellt eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="731d1-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="731d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="731d1-104">SYNTAX</span></span>

### <span data-ttu-id="731d1-105">BySpecifiedScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="731d1-105">BySpecifiedScope (Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="731d1-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="731d1-106">ByResourceGroup</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="731d1-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="731d1-107">ByResourceGroupLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731d1-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="731d1-108">BySubscription</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="731d1-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="731d1-109">BySubscriptionLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731d1-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="731d1-110">ByTenantLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731d1-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="731d1-111">ByLockId</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="731d1-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="731d1-112">DESCRIPTION</span></span>
<span data-ttu-id="731d1-113">Das Cmdlet **New-AzureRmResourceLock** erstellt eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="731d1-113">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="731d1-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="731d1-114">EXAMPLES</span></span>

### <span data-ttu-id="731d1-115">Beispiel 1: Erstellen einer Ressourcensperre auf einer Website</span><span class="sxs-lookup"><span data-stu-id="731d1-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="731d1-116">Dieser Befehl erstellt eine Ressourcensperre auf einer Website.</span><span class="sxs-lookup"><span data-stu-id="731d1-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="731d1-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="731d1-117">PARAMETERS</span></span>

### <span data-ttu-id="731d1-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="731d1-118">-ApiVersion</span></span>
<span data-ttu-id="731d1-119">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="731d1-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="731d1-120">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="731d1-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="731d1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="731d1-121">-DefaultProfile</span></span>
<span data-ttu-id="731d1-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="731d1-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="731d1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="731d1-123">-Force</span></span>
<span data-ttu-id="731d1-124">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="731d1-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="731d1-125">-Information</span><span class="sxs-lookup"><span data-stu-id="731d1-125">-InformationAction</span></span>
<span data-ttu-id="731d1-126">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="731d1-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="731d1-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="731d1-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="731d1-128">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="731d1-128">Continue</span></span>
- <span data-ttu-id="731d1-129">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="731d1-129">Ignore</span></span>
- <span data-ttu-id="731d1-130">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="731d1-130">Inquire</span></span>
- <span data-ttu-id="731d1-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="731d1-131">SilentlyContinue</span></span>
- <span data-ttu-id="731d1-132">Beenden</span><span class="sxs-lookup"><span data-stu-id="731d1-132">Stop</span></span>
- <span data-ttu-id="731d1-133">Anhalten</span><span class="sxs-lookup"><span data-stu-id="731d1-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731d1-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="731d1-134">-InformationVariable</span></span>
<span data-ttu-id="731d1-135">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="731d1-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731d1-136">-Sperre</span><span class="sxs-lookup"><span data-stu-id="731d1-136">-LockId</span></span>
<span data-ttu-id="731d1-137">Gibt die ID der Sperre an.</span><span class="sxs-lookup"><span data-stu-id="731d1-137">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="731d1-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="731d1-138">-LockLevel</span></span>
<span data-ttu-id="731d1-139">Gibt die Ebene für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="731d1-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="731d1-140">Gültige Werte sind derzeit können, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="731d1-140">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="731d1-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="731d1-141">-LockName</span></span>
<span data-ttu-id="731d1-142">Gibt den Namen der Sperre an.</span><span class="sxs-lookup"><span data-stu-id="731d1-142">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="731d1-143">-Sie LockNotes</span><span class="sxs-lookup"><span data-stu-id="731d1-143">-LockNotes</span></span>
<span data-ttu-id="731d1-144">Gibt die Notizen für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="731d1-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="731d1-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="731d1-145">-Pre</span></span>
<span data-ttu-id="731d1-146">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="731d1-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="731d1-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="731d1-147">-ResourceGroupName</span></span>
<span data-ttu-id="731d1-148">Gibt den Namen einer Ressourcengruppe an, für die die Sperre gilt oder die die Ressourcengruppe enthält, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="731d1-148">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="731d1-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="731d1-149">-ResourceName</span></span>
<span data-ttu-id="731d1-150">Gibt den Namen der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="731d1-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="731d1-151">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="731d1-151">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="731d1-152">-</span><span class="sxs-lookup"><span data-stu-id="731d1-152">-ResourceType</span></span>
<span data-ttu-id="731d1-153">Gibt den Ressourcentyp der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="731d1-153">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="731d1-154">-Scope</span><span class="sxs-lookup"><span data-stu-id="731d1-154">-Scope</span></span>
<span data-ttu-id="731d1-155">Gibt den Bereich an, auf den die Sperre angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="731d1-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="731d1-156">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: `/subscriptions/` Abonnement-ID- `/resourceGroups/` Ressourcengruppenname `/providers/Microsoft.Sql/servers/` Servername-Datenbankname `/databases/` zum Angeben einer Ressourcengruppe verwenden Sie das folgende Format: `/subscriptions/` Name der `/resourceGroups/` Ressourcengruppe "Abonnement-ID"</span><span class="sxs-lookup"><span data-stu-id="731d1-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="731d1-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="731d1-157">-TenantLevel</span></span>
<span data-ttu-id="731d1-158">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="731d1-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="731d1-159">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="731d1-159">-Confirm</span></span>
<span data-ttu-id="731d1-160">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="731d1-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="731d1-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="731d1-161">-WhatIf</span></span>
<span data-ttu-id="731d1-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="731d1-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="731d1-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="731d1-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="731d1-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="731d1-164">CommonParameters</span></span>
<span data-ttu-id="731d1-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="731d1-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="731d1-166">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="731d1-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="731d1-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="731d1-167">INPUTS</span></span>

## <span data-ttu-id="731d1-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="731d1-168">OUTPUTS</span></span>

## <span data-ttu-id="731d1-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="731d1-169">NOTES</span></span>

## <span data-ttu-id="731d1-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="731d1-170">RELATED LINKS</span></span>

[<span data-ttu-id="731d1-171">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="731d1-171">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="731d1-172">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="731d1-172">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="731d1-173">Satz-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="731d1-173">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


