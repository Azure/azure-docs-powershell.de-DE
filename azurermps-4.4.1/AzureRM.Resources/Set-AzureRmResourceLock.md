---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
ms.openlocfilehash: 73d82366cc0120e057d0c083e7f6da0b3cdebb76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663829"
---
# <span data-ttu-id="c1586-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="c1586-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="c1586-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1586-102">SYNOPSIS</span></span>
<span data-ttu-id="c1586-103">Ändert eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="c1586-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1586-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1586-104">SYNTAX</span></span>

### <span data-ttu-id="c1586-105">Eine Sperre im angegebenen Bereich.</span><span class="sxs-lookup"><span data-stu-id="c1586-105">A lock at the specified scope.</span></span> <span data-ttu-id="c1586-106">Standard</span><span class="sxs-lookup"><span data-stu-id="c1586-106">(Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1586-107">Eine Sperre im Bereich der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c1586-107">A lock at the resource group scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1586-108">Eine Sperre für den Ressourcengruppen-Ressourcenbereich.</span><span class="sxs-lookup"><span data-stu-id="c1586-108">A lock at the resource group resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1586-109">Eine Sperre im Abonnement Bereich.</span><span class="sxs-lookup"><span data-stu-id="c1586-109">A lock at the subscription scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1586-110">Eine Sperre für den Ressourcenbereich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="c1586-110">A lock at the subscription resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1586-111">Eine Sperre im Mandanten Ressourcenbereich.</span><span class="sxs-lookup"><span data-stu-id="c1586-111">A lock at the tenant resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1586-112">Eine Sperre, nach ID.</span><span class="sxs-lookup"><span data-stu-id="c1586-112">A lock, by Id.</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1586-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1586-113">DESCRIPTION</span></span>
<span data-ttu-id="c1586-114">Das Cmdlet " **Satz-AzureRmResourceLock** " ändert eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="c1586-114">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="c1586-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1586-115">EXAMPLES</span></span>

### <span data-ttu-id="c1586-116">Beispiel 1: Aktualisieren von Notizen für eine Sperre</span><span class="sxs-lookup"><span data-stu-id="c1586-116">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="c1586-117">Mit diesem Befehl wird die Notiz für eine Sperre mit dem Namen ContosoSiteLock aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c1586-117">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="c1586-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1586-118">PARAMETERS</span></span>

### <span data-ttu-id="c1586-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c1586-119">-ApiVersion</span></span>
<span data-ttu-id="c1586-120">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="c1586-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c1586-121">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="c1586-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c1586-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c1586-122">-Force</span></span>
<span data-ttu-id="c1586-123">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c1586-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c1586-124">-Information</span><span class="sxs-lookup"><span data-stu-id="c1586-124">-InformationAction</span></span>
<span data-ttu-id="c1586-125">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="c1586-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c1586-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c1586-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c1586-127">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="c1586-127">Continue</span></span>
- <span data-ttu-id="c1586-128">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="c1586-128">Ignore</span></span>
- <span data-ttu-id="c1586-129">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="c1586-129">Inquire</span></span>
- <span data-ttu-id="c1586-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c1586-130">SilentlyContinue</span></span>
- <span data-ttu-id="c1586-131">Beenden</span><span class="sxs-lookup"><span data-stu-id="c1586-131">Stop</span></span>
- <span data-ttu-id="c1586-132">Anhalten</span><span class="sxs-lookup"><span data-stu-id="c1586-132">Suspend</span></span>

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

### <span data-ttu-id="c1586-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c1586-133">-InformationVariable</span></span>
<span data-ttu-id="c1586-134">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="c1586-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c1586-135">-Sperre</span><span class="sxs-lookup"><span data-stu-id="c1586-135">-LockId</span></span>
<span data-ttu-id="c1586-136">Gibt die ID der Sperre an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c1586-136">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1586-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="c1586-137">-LockLevel</span></span>
<span data-ttu-id="c1586-138">Gibt die Ebene für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="c1586-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="c1586-139">Derzeit ist der einzige gültige Wert können.</span><span class="sxs-lookup"><span data-stu-id="c1586-139">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="c1586-140">-LockName</span><span class="sxs-lookup"><span data-stu-id="c1586-140">-LockName</span></span>
<span data-ttu-id="c1586-141">Gibt den Namen der Sperre an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c1586-141">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope., A lock at the resource group scope., A lock at the resource group resource scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1586-142">-Sie LockNotes</span><span class="sxs-lookup"><span data-stu-id="c1586-142">-LockNotes</span></span>
<span data-ttu-id="c1586-143">Gibt die Notizen für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="c1586-143">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="c1586-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="c1586-144">-Pre</span></span>
<span data-ttu-id="c1586-145">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c1586-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c1586-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1586-146">-ResourceGroupName</span></span>
<span data-ttu-id="c1586-147">Gibt den Namen der Ressourcengruppe an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="c1586-147">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1586-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c1586-148">-ResourceName</span></span>
<span data-ttu-id="c1586-149">Gibt den Namen der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="c1586-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="c1586-150">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="c1586-150">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="c1586-151">Server `/` Datenbank</span><span class="sxs-lookup"><span data-stu-id="c1586-151">Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1586-152">-</span><span class="sxs-lookup"><span data-stu-id="c1586-152">-ResourceType</span></span>
<span data-ttu-id="c1586-153">Gibt den Ressourcentyp an, für den die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="c1586-153">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1586-154">-Scope</span><span class="sxs-lookup"><span data-stu-id="c1586-154">-Scope</span></span>
<span data-ttu-id="c1586-155">Gibt den Bereich an, auf den die Sperre angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1586-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="c1586-156">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="c1586-156">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="c1586-157">`/subscriptions/`Abonnement-ID- `/resourceGroups/` Ressourcengruppenname `/providers/Microsoft.Sql/servers/` Servername der Datenbankname `/databases/`</span><span class="sxs-lookup"><span data-stu-id="c1586-157">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="c1586-158">Verwenden Sie das folgende Format, um eine Ressourcengruppe anzugeben:</span><span class="sxs-lookup"><span data-stu-id="c1586-158">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="c1586-159">`/subscriptions/`Name der Ressourcengruppe der Abonnement-ID `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="c1586-159">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1586-160">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="c1586-160">-TenantLevel</span></span>
<span data-ttu-id="c1586-161">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c1586-161">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1586-162">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c1586-162">-Confirm</span></span>
<span data-ttu-id="c1586-163">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1586-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1586-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1586-164">-WhatIf</span></span>
<span data-ttu-id="c1586-165">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1586-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1586-166">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1586-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1586-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1586-167">-DefaultProfile</span></span>
<span data-ttu-id="c1586-168">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c1586-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1586-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1586-169">CommonParameters</span></span>
<span data-ttu-id="c1586-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1586-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1586-171">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1586-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1586-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1586-172">INPUTS</span></span>

## <span data-ttu-id="c1586-173">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1586-173">OUTPUTS</span></span>

### <span data-ttu-id="c1586-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c1586-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c1586-175">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1586-175">NOTES</span></span>

## <span data-ttu-id="c1586-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1586-176">RELATED LINKS</span></span>

[<span data-ttu-id="c1586-177">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="c1586-177">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="c1586-178">Neu – AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="c1586-178">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="c1586-179">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="c1586-179">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)


