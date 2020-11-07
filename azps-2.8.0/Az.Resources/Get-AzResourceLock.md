---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 7c9a9da46da232e6b8a7e81e9b698d2b76513c71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825039"
---
# <span data-ttu-id="55a1c-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="55a1c-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="55a1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="55a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="55a1c-103">Ruft eine Ressourcensperre ab.</span><span class="sxs-lookup"><span data-stu-id="55a1c-103">Gets a resource lock.</span></span>

## <span data-ttu-id="55a1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="55a1c-104">SYNTAX</span></span>

### <span data-ttu-id="55a1c-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="55a1c-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55a1c-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="55a1c-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55a1c-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="55a1c-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55a1c-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="55a1c-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55a1c-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="55a1c-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55a1c-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="55a1c-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55a1c-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="55a1c-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55a1c-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55a1c-112">DESCRIPTION</span></span>
<span data-ttu-id="55a1c-113">Das Cmdlet " **Get-AzResourceLock** " ruft Azure-Ressourcen Sperren ab.</span><span class="sxs-lookup"><span data-stu-id="55a1c-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="55a1c-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55a1c-114">EXAMPLES</span></span>

### <span data-ttu-id="55a1c-115">Beispiel 1: Abrufen einer Sperre</span><span class="sxs-lookup"><span data-stu-id="55a1c-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="55a1c-116">Dieser Befehl ruft die Ressourcensperre mit dem Namen ContosoSiteLock ab.</span><span class="sxs-lookup"><span data-stu-id="55a1c-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="55a1c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="55a1c-117">PARAMETERS</span></span>

### <span data-ttu-id="55a1c-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="55a1c-118">-ApiVersion</span></span>
<span data-ttu-id="55a1c-119">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="55a1c-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="55a1c-120">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="55a1c-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="55a1c-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="55a1c-121">-AtScope</span></span>
<span data-ttu-id="55a1c-122">Gibt an, dass dieses Cmdlet alle Sperren über den angegebenen Bereich zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="55a1c-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="55a1c-123">Wenn Sie diesen Parameter nicht angeben, gibt das Cmdlet alle Sperren an, über oder unter dem Bereich zurück.</span><span class="sxs-lookup"><span data-stu-id="55a1c-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="55a1c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a1c-124">-DefaultProfile</span></span>
<span data-ttu-id="55a1c-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="55a1c-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55a1c-126">-Sperre</span><span class="sxs-lookup"><span data-stu-id="55a1c-126">-LockId</span></span>
<span data-ttu-id="55a1c-127">Gibt die ID der Sperre an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="55a1c-127">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="55a1c-128">-LockName</span><span class="sxs-lookup"><span data-stu-id="55a1c-128">-LockName</span></span>
<span data-ttu-id="55a1c-129">Gibt den Namen der Sperre an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="55a1c-129">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="55a1c-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="55a1c-130">-Pre</span></span>
<span data-ttu-id="55a1c-131">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="55a1c-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="55a1c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a1c-132">-ResourceGroupName</span></span>
<span data-ttu-id="55a1c-133">Gibt den Namen der Ressourcengruppe an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="55a1c-133">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="55a1c-134">Dieses Cmdlet ruft Sperren für diese Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="55a1c-134">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="55a1c-135">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="55a1c-135">-ResourceName</span></span>
<span data-ttu-id="55a1c-136">Gibt den Namen der Ressource an, für die diese Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="55a1c-136">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="55a1c-137">Dieses Cmdlet ruft Sperren für diese Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="55a1c-137">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="55a1c-138">-</span><span class="sxs-lookup"><span data-stu-id="55a1c-138">-ResourceType</span></span>
<span data-ttu-id="55a1c-139">Gibt den Ressourcentyp der Ressource an, für die diese Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="55a1c-139">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="55a1c-140">Dieses Cmdlet ruft Sperren für diese Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="55a1c-140">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="55a1c-141">-Scope</span><span class="sxs-lookup"><span data-stu-id="55a1c-141">-Scope</span></span>
<span data-ttu-id="55a1c-142">Gibt den Bereich an, auf den die Sperre angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="55a1c-142">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="55a1c-143">Das Cmdlet ruft Sperren für diesen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="55a1c-143">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="55a1c-144">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="55a1c-144">-TenantLevel</span></span>
<span data-ttu-id="55a1c-145">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="55a1c-145">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="55a1c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a1c-146">CommonParameters</span></span>
<span data-ttu-id="55a1c-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55a1c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a1c-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55a1c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a1c-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="55a1c-149">INPUTS</span></span>

### <span data-ttu-id="55a1c-150">System. String</span><span class="sxs-lookup"><span data-stu-id="55a1c-150">System.String</span></span>

## <span data-ttu-id="55a1c-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="55a1c-151">OUTPUTS</span></span>

### <span data-ttu-id="55a1c-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="55a1c-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="55a1c-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="55a1c-153">NOTES</span></span>

## <span data-ttu-id="55a1c-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="55a1c-154">RELATED LINKS</span></span>

[<span data-ttu-id="55a1c-155">Neu – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="55a1c-155">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="55a1c-156">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="55a1c-156">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="55a1c-157">Satz-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="55a1c-157">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


