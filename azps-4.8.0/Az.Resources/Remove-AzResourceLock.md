---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 8ad1a2ace4978b12210e568fb944568f5a2fec77
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165645"
---
# <span data-ttu-id="d7210-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="d7210-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="d7210-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7210-102">SYNOPSIS</span></span>
<span data-ttu-id="d7210-103">Entfernt eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="d7210-103">Removes a resource lock.</span></span>

## <span data-ttu-id="d7210-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7210-104">SYNTAX</span></span>

### <span data-ttu-id="d7210-105">ByLockId (Standard)</span><span class="sxs-lookup"><span data-stu-id="d7210-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7210-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d7210-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7210-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="d7210-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7210-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="d7210-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7210-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="d7210-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7210-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="d7210-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7210-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7210-111">DESCRIPTION</span></span>
<span data-ttu-id="d7210-112">Das Cmdlet **Remove-AzResourceLock** entfernt eine Azure-Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="d7210-112">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="d7210-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7210-113">EXAMPLES</span></span>

### <span data-ttu-id="d7210-114">Beispiel 1: Entfernen einer Sperre</span><span class="sxs-lookup"><span data-stu-id="d7210-114">Example 1: Remove a lock</span></span>
```powershell
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="d7210-115">Dieser Befehl entfernt die Sperre mit dem Namen ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="d7210-115">This command removes the lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="d7210-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d7210-116">Example 2</span></span>

<span data-ttu-id="d7210-117">Entfernt eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="d7210-117">Removes a resource lock.</span></span> <span data-ttu-id="d7210-118">automatisch</span><span class="sxs-lookup"><span data-stu-id="d7210-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Remove-AzResourceLock -LockName 'ContosoSiteLock' -ResourceGroupName myresourcegroup -ResourceName '/subscriptions/00000000-0000-0000-0000-00000000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test' -ResourceType 'Microsoft.ClassicCompute/storageAccounts'
```

## <span data-ttu-id="d7210-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7210-119">PARAMETERS</span></span>

### <span data-ttu-id="d7210-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d7210-120">-ApiVersion</span></span>
<span data-ttu-id="d7210-121">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="d7210-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d7210-122">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="d7210-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d7210-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7210-123">-DefaultProfile</span></span>
<span data-ttu-id="d7210-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d7210-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7210-125">-Force</span><span class="sxs-lookup"><span data-stu-id="d7210-125">-Force</span></span>
<span data-ttu-id="d7210-126">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d7210-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d7210-127">-Sperre</span><span class="sxs-lookup"><span data-stu-id="d7210-127">-LockId</span></span>
<span data-ttu-id="d7210-128">Gibt die ID der Sperre an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d7210-128">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d7210-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="d7210-129">-LockName</span></span>
<span data-ttu-id="d7210-130">Gibt den Namen der Sperre an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d7210-130">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7210-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="d7210-131">-Pre</span></span>
<span data-ttu-id="d7210-132">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d7210-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d7210-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7210-133">-ResourceGroupName</span></span>
<span data-ttu-id="d7210-134">Gibt den Namen der Ressourcengruppe an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="d7210-134">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="d7210-135">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d7210-135">-ResourceName</span></span>
<span data-ttu-id="d7210-136">Gibt den Namen der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="d7210-136">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="d7210-137">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: Server `/` Datenbank</span><span class="sxs-lookup"><span data-stu-id="d7210-137">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="d7210-138">-</span><span class="sxs-lookup"><span data-stu-id="d7210-138">-ResourceType</span></span>
<span data-ttu-id="d7210-139">Gibt den Ressourcentyp der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="d7210-139">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="d7210-140">-Scope</span><span class="sxs-lookup"><span data-stu-id="d7210-140">-Scope</span></span>
<span data-ttu-id="d7210-141">Gibt den Bereich an, auf den die Sperre angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7210-141">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="d7210-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d7210-142">-Confirm</span></span>
<span data-ttu-id="d7210-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7210-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7210-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7210-144">-WhatIf</span></span>
<span data-ttu-id="d7210-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7210-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7210-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7210-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7210-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7210-147">CommonParameters</span></span>
<span data-ttu-id="d7210-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7210-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7210-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7210-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7210-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7210-150">INPUTS</span></span>

### <span data-ttu-id="d7210-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d7210-151">System.String</span></span>

## <span data-ttu-id="d7210-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7210-152">OUTPUTS</span></span>

### <span data-ttu-id="d7210-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d7210-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d7210-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7210-154">NOTES</span></span>

## <span data-ttu-id="d7210-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7210-155">RELATED LINKS</span></span>

[<span data-ttu-id="d7210-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="d7210-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="d7210-157">Neu – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="d7210-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="d7210-158">Satz-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="d7210-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


