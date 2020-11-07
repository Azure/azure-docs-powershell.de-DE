---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: f3034d7197a26e8dd2ba803f478b6a71c8d50e8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663048"
---
# <span data-ttu-id="c232f-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="c232f-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="c232f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c232f-102">SYNOPSIS</span></span>
<span data-ttu-id="c232f-103">Entfernt eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="c232f-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c232f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c232f-104">SYNTAX</span></span>

### <span data-ttu-id="c232f-105">ByLockId (Standard)</span><span class="sxs-lookup"><span data-stu-id="c232f-105">ByLockId (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c232f-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c232f-106">ByResourceGroup</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c232f-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="c232f-107">ByResourceGroupLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c232f-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="c232f-108">BySpecifiedScope</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c232f-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="c232f-109">BySubscription</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c232f-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="c232f-110">BySubscriptionLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c232f-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="c232f-111">ByTenantLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c232f-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c232f-112">DESCRIPTION</span></span>
<span data-ttu-id="c232f-113">Das Cmdlet **Remove-AzureRmResourceLock** entfernt eine Azure-Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="c232f-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="c232f-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c232f-114">EXAMPLES</span></span>

### <span data-ttu-id="c232f-115">Beispiel 1: Entfernen einer Sperre</span><span class="sxs-lookup"><span data-stu-id="c232f-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="c232f-116">Dieser Befehl entfernt die Sperre mit dem Namen ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="c232f-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="c232f-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="c232f-117">PARAMETERS</span></span>

### <span data-ttu-id="c232f-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c232f-118">-ApiVersion</span></span>
<span data-ttu-id="c232f-119">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="c232f-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c232f-120">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="c232f-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c232f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c232f-121">-DefaultProfile</span></span>
<span data-ttu-id="c232f-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c232f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c232f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c232f-123">-Force</span></span>
<span data-ttu-id="c232f-124">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c232f-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c232f-125">-Information</span><span class="sxs-lookup"><span data-stu-id="c232f-125">-InformationAction</span></span>
<span data-ttu-id="c232f-126">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="c232f-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c232f-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c232f-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c232f-128">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="c232f-128">Continue</span></span>
- <span data-ttu-id="c232f-129">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="c232f-129">Ignore</span></span>
- <span data-ttu-id="c232f-130">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="c232f-130">Inquire</span></span>
- <span data-ttu-id="c232f-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c232f-131">SilentlyContinue</span></span>
- <span data-ttu-id="c232f-132">Beenden</span><span class="sxs-lookup"><span data-stu-id="c232f-132">Stop</span></span>
- <span data-ttu-id="c232f-133">Anhalten</span><span class="sxs-lookup"><span data-stu-id="c232f-133">Suspend</span></span>

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

### <span data-ttu-id="c232f-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c232f-134">-InformationVariable</span></span>
<span data-ttu-id="c232f-135">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="c232f-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c232f-136">-Sperre</span><span class="sxs-lookup"><span data-stu-id="c232f-136">-LockId</span></span>
<span data-ttu-id="c232f-137">Gibt die ID der Sperre an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c232f-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c232f-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="c232f-138">-LockName</span></span>
<span data-ttu-id="c232f-139">Gibt den Namen der Sperre an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c232f-139">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c232f-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="c232f-140">-Pre</span></span>
<span data-ttu-id="c232f-141">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c232f-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c232f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c232f-142">-ResourceGroupName</span></span>
<span data-ttu-id="c232f-143">Gibt den Namen der Ressourcengruppe an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="c232f-143">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="c232f-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c232f-144">-ResourceName</span></span>
<span data-ttu-id="c232f-145">Gibt den Namen der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="c232f-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="c232f-146">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="c232f-146">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="c232f-147">Server `/` Datenbank</span><span class="sxs-lookup"><span data-stu-id="c232f-147">Server`/`Database</span></span>

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

### <span data-ttu-id="c232f-148">-</span><span class="sxs-lookup"><span data-stu-id="c232f-148">-ResourceType</span></span>
<span data-ttu-id="c232f-149">Gibt den Ressourcentyp der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="c232f-149">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="c232f-150">-Scope</span><span class="sxs-lookup"><span data-stu-id="c232f-150">-Scope</span></span>
<span data-ttu-id="c232f-151">Gibt den Bereich an, auf den die Sperre angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c232f-151">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="c232f-152">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="c232f-152">-TenantLevel</span></span>
<span data-ttu-id="c232f-153">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c232f-153">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="c232f-154">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c232f-154">-Confirm</span></span>
<span data-ttu-id="c232f-155">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c232f-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c232f-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c232f-156">-WhatIf</span></span>
<span data-ttu-id="c232f-157">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c232f-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c232f-158">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c232f-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c232f-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c232f-159">CommonParameters</span></span>
<span data-ttu-id="c232f-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c232f-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c232f-161">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c232f-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c232f-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c232f-162">INPUTS</span></span>

### <span data-ttu-id="c232f-163">Keine</span><span class="sxs-lookup"><span data-stu-id="c232f-163">None</span></span>
<span data-ttu-id="c232f-164">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c232f-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c232f-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c232f-165">OUTPUTS</span></span>

### <span data-ttu-id="c232f-166">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c232f-166">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c232f-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="c232f-167">NOTES</span></span>

## <span data-ttu-id="c232f-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c232f-168">RELATED LINKS</span></span>

[<span data-ttu-id="c232f-169">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="c232f-169">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="c232f-170">Neu – AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="c232f-170">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="c232f-171">Satz-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="c232f-171">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


