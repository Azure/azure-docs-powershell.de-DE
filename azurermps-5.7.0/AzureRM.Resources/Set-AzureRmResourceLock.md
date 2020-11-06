---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
ms.openlocfilehash: 12d1a696bd37cd6844a54f32f60bf70eaba6a0b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502454"
---
# <span data-ttu-id="9ec65-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="9ec65-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="9ec65-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ec65-102">SYNOPSIS</span></span>
<span data-ttu-id="9ec65-103">Ändert eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="9ec65-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ec65-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ec65-104">SYNTAX</span></span>

### <span data-ttu-id="9ec65-105">BySpecifiedScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ec65-105">BySpecifiedScope (Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ec65-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9ec65-106">ByResourceGroup</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ec65-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="9ec65-107">ByResourceGroupLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ec65-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="9ec65-108">BySubscription</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ec65-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="9ec65-109">BySubscriptionLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ec65-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="9ec65-110">ByTenantLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ec65-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="9ec65-111">ByLockId</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ec65-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ec65-112">DESCRIPTION</span></span>
<span data-ttu-id="9ec65-113">Das Cmdlet " **Satz-AzureRmResourceLock** " ändert eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="9ec65-113">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="9ec65-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ec65-114">EXAMPLES</span></span>

### <span data-ttu-id="9ec65-115">Beispiel 1: Aktualisieren von Notizen für eine Sperre</span><span class="sxs-lookup"><span data-stu-id="9ec65-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="9ec65-116">Mit diesem Befehl wird die Notiz für eine Sperre mit dem Namen ContosoSiteLock aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9ec65-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="9ec65-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ec65-117">PARAMETERS</span></span>

### <span data-ttu-id="9ec65-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9ec65-118">-ApiVersion</span></span>
<span data-ttu-id="9ec65-119">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="9ec65-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9ec65-120">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="9ec65-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec65-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ec65-121">-DefaultProfile</span></span>
<span data-ttu-id="9ec65-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9ec65-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec65-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9ec65-123">-Force</span></span>
<span data-ttu-id="9ec65-124">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9ec65-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec65-125">-Information</span><span class="sxs-lookup"><span data-stu-id="9ec65-125">-InformationAction</span></span>
<span data-ttu-id="9ec65-126">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="9ec65-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9ec65-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9ec65-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9ec65-128">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="9ec65-128">Continue</span></span>
- <span data-ttu-id="9ec65-129">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="9ec65-129">Ignore</span></span>
- <span data-ttu-id="9ec65-130">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="9ec65-130">Inquire</span></span>
- <span data-ttu-id="9ec65-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9ec65-131">SilentlyContinue</span></span>
- <span data-ttu-id="9ec65-132">Beenden</span><span class="sxs-lookup"><span data-stu-id="9ec65-132">Stop</span></span>
- <span data-ttu-id="9ec65-133">Anhalten</span><span class="sxs-lookup"><span data-stu-id="9ec65-133">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec65-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9ec65-134">-InformationVariable</span></span>
<span data-ttu-id="9ec65-135">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="9ec65-135">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec65-136">-Sperre</span><span class="sxs-lookup"><span data-stu-id="9ec65-136">-LockId</span></span>
<span data-ttu-id="9ec65-137">Gibt die ID der Sperre an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9ec65-137">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec65-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="9ec65-138">-LockLevel</span></span>
<span data-ttu-id="9ec65-139">Gibt die Ebene für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="9ec65-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="9ec65-140">Derzeit ist der einzige gültige Wert können.</span><span class="sxs-lookup"><span data-stu-id="9ec65-140">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec65-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="9ec65-141">-LockName</span></span>
<span data-ttu-id="9ec65-142">Gibt den Namen der Sperre an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9ec65-142">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec65-143">-Sie LockNotes</span><span class="sxs-lookup"><span data-stu-id="9ec65-143">-LockNotes</span></span>
<span data-ttu-id="9ec65-144">Gibt die Notizen für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="9ec65-144">Specifies the notes for the lock.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec65-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="9ec65-145">-Pre</span></span>
<span data-ttu-id="9ec65-146">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="9ec65-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec65-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ec65-147">-ResourceGroupName</span></span>
<span data-ttu-id="9ec65-148">Gibt den Namen der Ressourcengruppe an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="9ec65-148">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec65-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9ec65-149">-ResourceName</span></span>
<span data-ttu-id="9ec65-150">Gibt den Namen der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="9ec65-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="9ec65-151">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="9ec65-151">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="9ec65-152">Server `/` Datenbank</span><span class="sxs-lookup"><span data-stu-id="9ec65-152">Server`/`Database</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec65-153">-</span><span class="sxs-lookup"><span data-stu-id="9ec65-153">-ResourceType</span></span>
<span data-ttu-id="9ec65-154">Gibt den Ressourcentyp an, für den die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="9ec65-154">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec65-155">-Scope</span><span class="sxs-lookup"><span data-stu-id="9ec65-155">-Scope</span></span>
<span data-ttu-id="9ec65-156">Gibt den Bereich an, auf den die Sperre angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ec65-156">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="9ec65-157">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="9ec65-157">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="9ec65-158">`/subscriptions/`Abonnement-ID- `/resourceGroups/` Ressourcengruppenname `/providers/Microsoft.Sql/servers/` Servername der Datenbankname `/databases/`</span><span class="sxs-lookup"><span data-stu-id="9ec65-158">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="9ec65-159">Verwenden Sie das folgende Format, um eine Ressourcengruppe anzugeben:</span><span class="sxs-lookup"><span data-stu-id="9ec65-159">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="9ec65-160">`/subscriptions/`Name der Ressourcengruppe der Abonnement-ID `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="9ec65-160">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec65-161">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="9ec65-161">-TenantLevel</span></span>
<span data-ttu-id="9ec65-162">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="9ec65-162">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec65-163">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ec65-163">-Confirm</span></span>
<span data-ttu-id="9ec65-164">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ec65-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec65-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ec65-165">-WhatIf</span></span>
<span data-ttu-id="9ec65-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ec65-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ec65-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ec65-167">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec65-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ec65-168">CommonParameters</span></span>
<span data-ttu-id="9ec65-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ec65-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ec65-170">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ec65-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ec65-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ec65-171">INPUTS</span></span>

### <span data-ttu-id="9ec65-172">Keine</span><span class="sxs-lookup"><span data-stu-id="9ec65-172">None</span></span>
<span data-ttu-id="9ec65-173">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9ec65-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9ec65-174">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ec65-174">OUTPUTS</span></span>

### <span data-ttu-id="9ec65-175">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9ec65-175">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9ec65-176">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ec65-176">NOTES</span></span>

## <span data-ttu-id="9ec65-177">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ec65-177">RELATED LINKS</span></span>

[<span data-ttu-id="9ec65-178">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="9ec65-178">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="9ec65-179">Neu – AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="9ec65-179">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="9ec65-180">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="9ec65-180">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)


