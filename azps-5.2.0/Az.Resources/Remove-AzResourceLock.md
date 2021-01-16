---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 5047ce0ebeb4f93d1d73473edbec50eaf65c6875
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307907"
---
# <span data-ttu-id="44161-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="44161-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="44161-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44161-102">SYNOPSIS</span></span>
<span data-ttu-id="44161-103">Entfernt eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="44161-103">Removes a resource lock.</span></span>

## <span data-ttu-id="44161-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44161-104">SYNTAX</span></span>

### <span data-ttu-id="44161-105">ByLockId (Standard)</span><span class="sxs-lookup"><span data-stu-id="44161-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44161-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="44161-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44161-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="44161-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44161-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="44161-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44161-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="44161-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44161-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="44161-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44161-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44161-111">DESCRIPTION</span></span>
<span data-ttu-id="44161-112">Das **Cmdlet "Remove-AzResourceLock"** entfernt eine Azure-Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="44161-112">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="44161-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="44161-113">EXAMPLES</span></span>

### <span data-ttu-id="44161-114">Beispiel 1: Entfernen einer Sperre</span><span class="sxs-lookup"><span data-stu-id="44161-114">Example 1: Remove a lock</span></span>
```powershell
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="44161-115">Mit diesem Befehl wird die Sperre namens "ContosoSiteLock" entfernt.</span><span class="sxs-lookup"><span data-stu-id="44161-115">This command removes the lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="44161-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="44161-116">Example 2</span></span>

<span data-ttu-id="44161-117">Entfernt eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="44161-117">Removes a resource lock.</span></span> <span data-ttu-id="44161-118">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="44161-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
Remove-AzResourceLock -LockName 'ContosoSiteLock' -ResourceGroupName myresourcegroup -ResourceName '/subscriptions/00000000-0000-0000-0000-00000000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test' -ResourceType 'Microsoft.ClassicCompute/storageAccounts'
```

## <span data-ttu-id="44161-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44161-119">PARAMETERS</span></span>

### <span data-ttu-id="44161-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="44161-120">-ApiVersion</span></span>
<span data-ttu-id="44161-121">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="44161-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="44161-122">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="44161-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="44161-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44161-123">-DefaultProfile</span></span>
<span data-ttu-id="44161-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="44161-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44161-125">-Force</span><span class="sxs-lookup"><span data-stu-id="44161-125">-Force</span></span>
<span data-ttu-id="44161-126">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="44161-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="44161-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="44161-127">-LockId</span></span>
<span data-ttu-id="44161-128">Gibt die ID der Sperre an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="44161-128">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="44161-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="44161-129">-LockName</span></span>
<span data-ttu-id="44161-130">Gibt den Namen der Sperre an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="44161-130">Specifies the name of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="44161-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="44161-131">-Pre</span></span>
<span data-ttu-id="44161-132">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="44161-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="44161-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44161-133">-ResourceGroupName</span></span>
<span data-ttu-id="44161-134">Gibt den Namen der Ressourcengruppe an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="44161-134">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="44161-135">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="44161-135">-ResourceName</span></span>
<span data-ttu-id="44161-136">Gibt den Namen der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="44161-136">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="44161-137">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende `/` Format: Serverdatenbank</span><span class="sxs-lookup"><span data-stu-id="44161-137">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="44161-138">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="44161-138">-ResourceType</span></span>
<span data-ttu-id="44161-139">Gibt den Ressourcentyp der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="44161-139">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="44161-140">-Scope</span><span class="sxs-lookup"><span data-stu-id="44161-140">-Scope</span></span>
<span data-ttu-id="44161-141">Gibt den Bereich an, auf den die Sperre angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="44161-141">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="44161-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44161-142">-Confirm</span></span>
<span data-ttu-id="44161-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="44161-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44161-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="44161-144">-WhatIf</span></span>
<span data-ttu-id="44161-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44161-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44161-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44161-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44161-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44161-147">CommonParameters</span></span>
<span data-ttu-id="44161-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44161-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44161-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44161-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44161-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="44161-150">INPUTS</span></span>

### <span data-ttu-id="44161-151">System.String</span><span class="sxs-lookup"><span data-stu-id="44161-151">System.String</span></span>

## <span data-ttu-id="44161-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="44161-152">OUTPUTS</span></span>

### <span data-ttu-id="44161-153">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="44161-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="44161-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="44161-154">NOTES</span></span>

## <span data-ttu-id="44161-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="44161-155">RELATED LINKS</span></span>

[<span data-ttu-id="44161-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="44161-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="44161-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="44161-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="44161-158">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="44161-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


