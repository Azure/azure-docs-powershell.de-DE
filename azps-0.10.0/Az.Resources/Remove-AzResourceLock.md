---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 6b9a0b792b1a8a5572ce26561202284f3103d764
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843235"
---
# <span data-ttu-id="d6660-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="d6660-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="d6660-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6660-102">SYNOPSIS</span></span>
<span data-ttu-id="d6660-103">Entfernt eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="d6660-103">Removes a resource lock.</span></span>

## <span data-ttu-id="d6660-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6660-104">SYNTAX</span></span>

### <span data-ttu-id="d6660-105">ByLockId (Standard)</span><span class="sxs-lookup"><span data-stu-id="d6660-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6660-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d6660-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6660-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="d6660-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6660-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="d6660-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6660-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="d6660-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6660-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="d6660-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6660-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="d6660-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6660-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6660-112">DESCRIPTION</span></span>
<span data-ttu-id="d6660-113">Das Cmdlet **Remove-AzResourceLock** entfernt eine Azure-Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="d6660-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="d6660-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6660-114">EXAMPLES</span></span>

### <span data-ttu-id="d6660-115">Beispiel 1: Entfernen einer Sperre</span><span class="sxs-lookup"><span data-stu-id="d6660-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="d6660-116">Dieser Befehl entfernt die Sperre mit dem Namen ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="d6660-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="d6660-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6660-117">PARAMETERS</span></span>

### <span data-ttu-id="d6660-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d6660-118">-ApiVersion</span></span>
<span data-ttu-id="d6660-119">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="d6660-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d6660-120">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="d6660-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d6660-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6660-121">-DefaultProfile</span></span>
<span data-ttu-id="d6660-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d6660-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6660-123">-Force</span><span class="sxs-lookup"><span data-stu-id="d6660-123">-Force</span></span>
<span data-ttu-id="d6660-124">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d6660-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d6660-125">-Information</span><span class="sxs-lookup"><span data-stu-id="d6660-125">-InformationAction</span></span>
<span data-ttu-id="d6660-126">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="d6660-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="d6660-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d6660-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d6660-128">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="d6660-128">Continue</span></span>
- <span data-ttu-id="d6660-129">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="d6660-129">Ignore</span></span>
- <span data-ttu-id="d6660-130">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="d6660-130">Inquire</span></span>
- <span data-ttu-id="d6660-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d6660-131">SilentlyContinue</span></span>
- <span data-ttu-id="d6660-132">Beenden</span><span class="sxs-lookup"><span data-stu-id="d6660-132">Stop</span></span>
- <span data-ttu-id="d6660-133">Anhalten</span><span class="sxs-lookup"><span data-stu-id="d6660-133">Suspend</span></span>

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

### <span data-ttu-id="d6660-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d6660-134">-InformationVariable</span></span>
<span data-ttu-id="d6660-135">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="d6660-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d6660-136">-Sperre</span><span class="sxs-lookup"><span data-stu-id="d6660-136">-LockId</span></span>
<span data-ttu-id="d6660-137">Gibt die ID der Sperre an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d6660-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d6660-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="d6660-138">-LockName</span></span>
<span data-ttu-id="d6660-139">Gibt den Namen der Sperre an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d6660-139">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6660-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="d6660-140">-Pre</span></span>
<span data-ttu-id="d6660-141">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d6660-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d6660-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6660-142">-ResourceGroupName</span></span>
<span data-ttu-id="d6660-143">Gibt den Namen der Ressourcengruppe an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="d6660-143">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="d6660-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d6660-144">-ResourceName</span></span>
<span data-ttu-id="d6660-145">Gibt den Namen der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="d6660-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="d6660-146">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: Server `/` Datenbank</span><span class="sxs-lookup"><span data-stu-id="d6660-146">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="d6660-147">-</span><span class="sxs-lookup"><span data-stu-id="d6660-147">-ResourceType</span></span>
<span data-ttu-id="d6660-148">Gibt den Ressourcentyp der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="d6660-148">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="d6660-149">-Scope</span><span class="sxs-lookup"><span data-stu-id="d6660-149">-Scope</span></span>
<span data-ttu-id="d6660-150">Gibt den Bereich an, auf den die Sperre angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6660-150">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="d6660-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="d6660-151">-TenantLevel</span></span>
<span data-ttu-id="d6660-152">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d6660-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="d6660-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d6660-153">-Confirm</span></span>
<span data-ttu-id="d6660-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6660-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6660-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6660-155">-WhatIf</span></span>
<span data-ttu-id="d6660-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d6660-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6660-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6660-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6660-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6660-158">CommonParameters</span></span>
<span data-ttu-id="d6660-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6660-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6660-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6660-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6660-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6660-161">INPUTS</span></span>

## <span data-ttu-id="d6660-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6660-162">OUTPUTS</span></span>

## <span data-ttu-id="d6660-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6660-163">NOTES</span></span>

## <span data-ttu-id="d6660-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6660-164">RELATED LINKS</span></span>

[<span data-ttu-id="d6660-165">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="d6660-165">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="d6660-166">Neu – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="d6660-166">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="d6660-167">Satz-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="d6660-167">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


