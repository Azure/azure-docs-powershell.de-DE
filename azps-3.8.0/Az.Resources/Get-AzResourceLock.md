---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: ea0ee8e46c70e6dd61e352ce0e7bd5da391c0c66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846176"
---
# <span data-ttu-id="4b4f4-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="4b4f4-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="4b4f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b4f4-102">SYNOPSIS</span></span>
<span data-ttu-id="4b4f4-103">Ruft eine Ressourcensperre ab.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-103">Gets a resource lock.</span></span>

## <span data-ttu-id="4b4f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b4f4-104">SYNTAX</span></span>

### <span data-ttu-id="4b4f4-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4b4f4-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b4f4-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="4b4f4-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b4f4-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="4b4f4-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b4f4-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="4b4f4-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b4f4-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="4b4f4-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b4f4-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="4b4f4-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b4f4-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="4b4f4-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b4f4-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b4f4-112">DESCRIPTION</span></span>
<span data-ttu-id="4b4f4-113">Das Cmdlet " **Get-AzResourceLock** " ruft Azure-Ressourcen Sperren ab.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="4b4f4-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b4f4-114">EXAMPLES</span></span>

### <span data-ttu-id="4b4f4-115">Beispiel 1: Abrufen einer Sperre</span><span class="sxs-lookup"><span data-stu-id="4b4f4-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="4b4f4-116">Dieser Befehl ruft die Ressourcensperre mit dem Namen ContosoSiteLock ab.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-116">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="4b4f4-117">Beispiel 2: Abrufen von Sperren auf Ressourcengruppen Ebene oder höher</span><span class="sxs-lookup"><span data-stu-id="4b4f4-117">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="4b4f4-118">Mit diesem Befehl werden die Ressourcen Sperren für die Ressourcengruppe oder das Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-118">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="4b4f4-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b4f4-119">PARAMETERS</span></span>

### <span data-ttu-id="4b4f4-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4b4f4-120">-ApiVersion</span></span>
<span data-ttu-id="4b4f4-121">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4b4f4-122">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4b4f4-123">-AtScope</span><span class="sxs-lookup"><span data-stu-id="4b4f4-123">-AtScope</span></span>
<span data-ttu-id="4b4f4-124">Gibt an, dass dieses Cmdlet alle Sperren über den angegebenen Bereich zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-124">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="4b4f4-125">Wenn Sie diesen Parameter nicht angeben, gibt das Cmdlet alle Sperren an, über oder unter dem Bereich zurück.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-125">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="4b4f4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b4f4-126">-DefaultProfile</span></span>
<span data-ttu-id="4b4f4-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4b4f4-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b4f4-128">-Sperre</span><span class="sxs-lookup"><span data-stu-id="4b4f4-128">-LockId</span></span>
<span data-ttu-id="4b4f4-129">Gibt die ID der Sperre an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-129">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4b4f4-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="4b4f4-130">-LockName</span></span>
<span data-ttu-id="4b4f4-131">Gibt den Namen der Sperre an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-131">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b4f4-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="4b4f4-132">-Pre</span></span>
<span data-ttu-id="4b4f4-133">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4b4f4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b4f4-134">-ResourceGroupName</span></span>
<span data-ttu-id="4b4f4-135">Gibt den Namen der Ressourcengruppe an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-135">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="4b4f4-136">Dieses Cmdlet ruft Sperren für diese Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-136">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="4b4f4-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4b4f4-137">-ResourceName</span></span>
<span data-ttu-id="4b4f4-138">Gibt den Namen der Ressource an, für die diese Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-138">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="4b4f4-139">Dieses Cmdlet ruft Sperren für diese Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-139">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="4b4f4-140">-</span><span class="sxs-lookup"><span data-stu-id="4b4f4-140">-ResourceType</span></span>
<span data-ttu-id="4b4f4-141">Gibt den Ressourcentyp der Ressource an, für die diese Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-141">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="4b4f4-142">Dieses Cmdlet ruft Sperren für diese Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-142">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="4b4f4-143">-Scope</span><span class="sxs-lookup"><span data-stu-id="4b4f4-143">-Scope</span></span>
<span data-ttu-id="4b4f4-144">Gibt den Bereich an, auf den die Sperre angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="4b4f4-145">Das Cmdlet ruft Sperren für diesen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-145">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="4b4f4-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="4b4f4-146">-TenantLevel</span></span>
<span data-ttu-id="4b4f4-147">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="4b4f4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b4f4-148">CommonParameters</span></span>
<span data-ttu-id="4b4f4-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b4f4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b4f4-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b4f4-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b4f4-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b4f4-151">INPUTS</span></span>

### <span data-ttu-id="4b4f4-152">System. String</span><span class="sxs-lookup"><span data-stu-id="4b4f4-152">System.String</span></span>

## <span data-ttu-id="4b4f4-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b4f4-153">OUTPUTS</span></span>

### <span data-ttu-id="4b4f4-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4b4f4-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4b4f4-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b4f4-155">NOTES</span></span>

## <span data-ttu-id="4b4f4-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b4f4-156">RELATED LINKS</span></span>

[<span data-ttu-id="4b4f4-157">Neu – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="4b4f4-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="4b4f4-158">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="4b4f4-158">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="4b4f4-159">Satz-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="4b4f4-159">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


