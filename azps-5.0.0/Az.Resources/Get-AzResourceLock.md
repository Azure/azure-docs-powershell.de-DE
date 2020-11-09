---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 2dbbb41ce1ad2ee6fc2279e711722090f4f1a6cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301101"
---
# <span data-ttu-id="3feaa-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="3feaa-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="3feaa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3feaa-102">SYNOPSIS</span></span>
<span data-ttu-id="3feaa-103">Ruft eine Ressourcensperre ab.</span><span class="sxs-lookup"><span data-stu-id="3feaa-103">Gets a resource lock.</span></span>

## <span data-ttu-id="3feaa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3feaa-104">SYNTAX</span></span>

### <span data-ttu-id="3feaa-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3feaa-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3feaa-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="3feaa-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3feaa-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="3feaa-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3feaa-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="3feaa-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3feaa-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="3feaa-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3feaa-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="3feaa-110">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3feaa-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3feaa-111">DESCRIPTION</span></span>
<span data-ttu-id="3feaa-112">Das Cmdlet " **Get-AzResourceLock** " ruft Azure-Ressourcen Sperren ab.</span><span class="sxs-lookup"><span data-stu-id="3feaa-112">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="3feaa-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3feaa-113">EXAMPLES</span></span>

### <span data-ttu-id="3feaa-114">Beispiel 1: Abrufen einer Sperre</span><span class="sxs-lookup"><span data-stu-id="3feaa-114">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="3feaa-115">Dieser Befehl ruft die Ressourcensperre mit dem Namen ContosoSiteLock ab.</span><span class="sxs-lookup"><span data-stu-id="3feaa-115">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="3feaa-116">Beispiel 2: Abrufen von Sperren auf Ressourcengruppen Ebene oder höher</span><span class="sxs-lookup"><span data-stu-id="3feaa-116">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="3feaa-117">Mit diesem Befehl werden die Ressourcen Sperren für die Ressourcengruppe oder das Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3feaa-117">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="3feaa-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="3feaa-118">PARAMETERS</span></span>

### <span data-ttu-id="3feaa-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3feaa-119">-ApiVersion</span></span>
<span data-ttu-id="3feaa-120">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="3feaa-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3feaa-121">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="3feaa-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3feaa-122">-AtScope</span><span class="sxs-lookup"><span data-stu-id="3feaa-122">-AtScope</span></span>
<span data-ttu-id="3feaa-123">Gibt an, dass dieses Cmdlet alle Sperren über den angegebenen Bereich zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3feaa-123">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="3feaa-124">Wenn Sie diesen Parameter nicht angeben, gibt das Cmdlet alle Sperren an, über oder unter dem Bereich zurück.</span><span class="sxs-lookup"><span data-stu-id="3feaa-124">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="3feaa-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3feaa-125">-DefaultProfile</span></span>
<span data-ttu-id="3feaa-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3feaa-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3feaa-127">-Sperre</span><span class="sxs-lookup"><span data-stu-id="3feaa-127">-LockId</span></span>
<span data-ttu-id="3feaa-128">Gibt die ID der Sperre an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="3feaa-128">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3feaa-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="3feaa-129">-LockName</span></span>
<span data-ttu-id="3feaa-130">Gibt den Namen der Sperre an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="3feaa-130">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3feaa-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="3feaa-131">-Pre</span></span>
<span data-ttu-id="3feaa-132">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="3feaa-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3feaa-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3feaa-133">-ResourceGroupName</span></span>
<span data-ttu-id="3feaa-134">Gibt den Namen der Ressourcengruppe an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="3feaa-134">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="3feaa-135">Dieses Cmdlet ruft Sperren für diese Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="3feaa-135">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="3feaa-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3feaa-136">-ResourceName</span></span>
<span data-ttu-id="3feaa-137">Gibt den Namen der Ressource an, für die diese Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="3feaa-137">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="3feaa-138">Dieses Cmdlet ruft Sperren für diese Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="3feaa-138">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="3feaa-139">-</span><span class="sxs-lookup"><span data-stu-id="3feaa-139">-ResourceType</span></span>
<span data-ttu-id="3feaa-140">Gibt den Ressourcentyp der Ressource an, für die diese Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="3feaa-140">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="3feaa-141">Dieses Cmdlet ruft Sperren für diese Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="3feaa-141">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="3feaa-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="3feaa-142">-Scope</span></span>
<span data-ttu-id="3feaa-143">Gibt den Bereich an, auf den die Sperre angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3feaa-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="3feaa-144">Das Cmdlet ruft Sperren für diesen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="3feaa-144">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="3feaa-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3feaa-145">CommonParameters</span></span>
<span data-ttu-id="3feaa-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3feaa-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3feaa-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3feaa-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3feaa-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3feaa-148">INPUTS</span></span>

### <span data-ttu-id="3feaa-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3feaa-149">System.String</span></span>

## <span data-ttu-id="3feaa-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3feaa-150">OUTPUTS</span></span>

### <span data-ttu-id="3feaa-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3feaa-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3feaa-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="3feaa-152">NOTES</span></span>

## <span data-ttu-id="3feaa-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3feaa-153">RELATED LINKS</span></span>

[<span data-ttu-id="3feaa-154">Neu – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="3feaa-154">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="3feaa-155">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="3feaa-155">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="3feaa-156">Satz-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="3feaa-156">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


