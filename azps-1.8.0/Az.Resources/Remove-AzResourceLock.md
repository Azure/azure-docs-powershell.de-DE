---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 32a3dbb458c4848a5578309593b205b4ced5be03
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659537"
---
# <span data-ttu-id="4ab47-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="4ab47-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="4ab47-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ab47-102">SYNOPSIS</span></span>
<span data-ttu-id="4ab47-103">Entfernt eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="4ab47-103">Removes a resource lock.</span></span>

## <span data-ttu-id="4ab47-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ab47-104">SYNTAX</span></span>

### <span data-ttu-id="4ab47-105">ByLockId (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ab47-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ab47-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4ab47-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ab47-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="4ab47-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ab47-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="4ab47-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ab47-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="4ab47-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ab47-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="4ab47-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ab47-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="4ab47-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ab47-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ab47-112">DESCRIPTION</span></span>
<span data-ttu-id="4ab47-113">Das Cmdlet **Remove-AzResourceLock** entfernt eine Azure-Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="4ab47-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="4ab47-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ab47-114">EXAMPLES</span></span>

### <span data-ttu-id="4ab47-115">Beispiel 1: Entfernen einer Sperre</span><span class="sxs-lookup"><span data-stu-id="4ab47-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="4ab47-116">Dieser Befehl entfernt die Sperre mit dem Namen ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="4ab47-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="4ab47-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ab47-117">PARAMETERS</span></span>

### <span data-ttu-id="4ab47-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4ab47-118">-ApiVersion</span></span>
<span data-ttu-id="4ab47-119">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="4ab47-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4ab47-120">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="4ab47-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4ab47-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ab47-121">-DefaultProfile</span></span>
<span data-ttu-id="4ab47-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4ab47-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ab47-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4ab47-123">-Force</span></span>
<span data-ttu-id="4ab47-124">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="4ab47-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4ab47-125">-Sperre</span><span class="sxs-lookup"><span data-stu-id="4ab47-125">-LockId</span></span>
<span data-ttu-id="4ab47-126">Gibt die ID der Sperre an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4ab47-126">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4ab47-127">-LockName</span><span class="sxs-lookup"><span data-stu-id="4ab47-127">-LockName</span></span>
<span data-ttu-id="4ab47-128">Gibt den Namen der Sperre an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4ab47-128">Specifies the name of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4ab47-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="4ab47-129">-Pre</span></span>
<span data-ttu-id="4ab47-130">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4ab47-130">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4ab47-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ab47-131">-ResourceGroupName</span></span>
<span data-ttu-id="4ab47-132">Gibt den Namen der Ressourcengruppe an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="4ab47-132">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="4ab47-133">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4ab47-133">-ResourceName</span></span>
<span data-ttu-id="4ab47-134">Gibt den Namen der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="4ab47-134">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="4ab47-135">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: Server `/` Datenbank</span><span class="sxs-lookup"><span data-stu-id="4ab47-135">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="4ab47-136">-</span><span class="sxs-lookup"><span data-stu-id="4ab47-136">-ResourceType</span></span>
<span data-ttu-id="4ab47-137">Gibt den Ressourcentyp der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="4ab47-137">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="4ab47-138">-Scope</span><span class="sxs-lookup"><span data-stu-id="4ab47-138">-Scope</span></span>
<span data-ttu-id="4ab47-139">Gibt den Bereich an, auf den die Sperre angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ab47-139">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="4ab47-140">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="4ab47-140">-TenantLevel</span></span>
<span data-ttu-id="4ab47-141">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4ab47-141">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="4ab47-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4ab47-142">-Confirm</span></span>
<span data-ttu-id="4ab47-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ab47-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ab47-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ab47-144">-WhatIf</span></span>
<span data-ttu-id="4ab47-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ab47-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ab47-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ab47-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ab47-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ab47-147">CommonParameters</span></span>
<span data-ttu-id="4ab47-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ab47-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ab47-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ab47-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ab47-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ab47-150">INPUTS</span></span>

### <span data-ttu-id="4ab47-151">System. String</span><span class="sxs-lookup"><span data-stu-id="4ab47-151">System.String</span></span>

## <span data-ttu-id="4ab47-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ab47-152">OUTPUTS</span></span>

### <span data-ttu-id="4ab47-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4ab47-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4ab47-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ab47-154">NOTES</span></span>

## <span data-ttu-id="4ab47-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ab47-155">RELATED LINKS</span></span>

[<span data-ttu-id="4ab47-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="4ab47-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="4ab47-157">Neu – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="4ab47-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="4ab47-158">Satz-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="4ab47-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


