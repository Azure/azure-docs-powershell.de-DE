---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
ms.openlocfilehash: 9681a88a1a4768617383a25122a0224ae264e088
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495697"
---
# <span data-ttu-id="02c4b-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="02c4b-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="02c4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="02c4b-103">Ruft eine Ressourcensperre ab.</span><span class="sxs-lookup"><span data-stu-id="02c4b-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02c4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02c4b-104">SYNTAX</span></span>

### <span data-ttu-id="02c4b-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="02c4b-105">ByResourceGroup</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="02c4b-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="02c4b-106">ByResourceGroupLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="02c4b-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="02c4b-107">BySpecifiedScope</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="02c4b-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="02c4b-108">BySubscription</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="02c4b-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="02c4b-109">BySubscriptionLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="02c4b-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="02c4b-110">ByTenantLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="02c4b-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="02c4b-111">ByLockId</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="02c4b-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02c4b-112">DESCRIPTION</span></span>
<span data-ttu-id="02c4b-113">Das Cmdlet " **Get-AzureRmResourceLock** " ruft Azure-Ressourcen Sperren ab.</span><span class="sxs-lookup"><span data-stu-id="02c4b-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="02c4b-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02c4b-114">EXAMPLES</span></span>

### <span data-ttu-id="02c4b-115">Beispiel 1: Abrufen einer Sperre</span><span class="sxs-lookup"><span data-stu-id="02c4b-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="02c4b-116">Dieser Befehl ruft die Ressourcensperre mit dem Namen ContosoSiteLock ab.</span><span class="sxs-lookup"><span data-stu-id="02c4b-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="02c4b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="02c4b-117">PARAMETERS</span></span>

### <span data-ttu-id="02c4b-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="02c4b-118">-ApiVersion</span></span>
<span data-ttu-id="02c4b-119">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="02c4b-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="02c4b-120">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="02c4b-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="02c4b-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="02c4b-121">-AtScope</span></span>
<span data-ttu-id="02c4b-122">Gibt an, dass dieses Cmdlet alle Sperren über den angegebenen Bereich zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="02c4b-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="02c4b-123">Wenn Sie diesen Parameter nicht angeben, gibt das Cmdlet alle Sperren an, über oder unter dem Bereich zurück.</span><span class="sxs-lookup"><span data-stu-id="02c4b-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="02c4b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c4b-124">-DefaultProfile</span></span>
<span data-ttu-id="02c4b-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="02c4b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02c4b-126">-Information</span><span class="sxs-lookup"><span data-stu-id="02c4b-126">-InformationAction</span></span>
<span data-ttu-id="02c4b-127">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="02c4b-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="02c4b-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="02c4b-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="02c4b-129">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="02c4b-129">Continue</span></span>
- <span data-ttu-id="02c4b-130">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="02c4b-130">Ignore</span></span>
- <span data-ttu-id="02c4b-131">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="02c4b-131">Inquire</span></span>
- <span data-ttu-id="02c4b-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="02c4b-132">SilentlyContinue</span></span>
- <span data-ttu-id="02c4b-133">Beenden</span><span class="sxs-lookup"><span data-stu-id="02c4b-133">Stop</span></span>
- <span data-ttu-id="02c4b-134">Anhalten</span><span class="sxs-lookup"><span data-stu-id="02c4b-134">Suspend</span></span>

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

### <span data-ttu-id="02c4b-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="02c4b-135">-InformationVariable</span></span>
<span data-ttu-id="02c4b-136">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="02c4b-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="02c4b-137">-Sperre</span><span class="sxs-lookup"><span data-stu-id="02c4b-137">-LockId</span></span>
<span data-ttu-id="02c4b-138">Gibt die ID der Sperre an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="02c4b-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="02c4b-139">-LockName</span><span class="sxs-lookup"><span data-stu-id="02c4b-139">-LockName</span></span>
<span data-ttu-id="02c4b-140">Gibt den Namen der Sperre an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="02c4b-140">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="02c4b-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="02c4b-141">-Pre</span></span>
<span data-ttu-id="02c4b-142">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="02c4b-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="02c4b-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02c4b-143">-ResourceGroupName</span></span>
<span data-ttu-id="02c4b-144">Gibt den Namen der Ressourcengruppe an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="02c4b-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="02c4b-145">Dieses Cmdlet ruft Sperren für diese Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="02c4b-145">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="02c4b-146">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="02c4b-146">-ResourceName</span></span>
<span data-ttu-id="02c4b-147">Gibt den Namen der Ressource an, für die diese Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="02c4b-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="02c4b-148">Dieses Cmdlet ruft Sperren für diese Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="02c4b-148">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="02c4b-149">-</span><span class="sxs-lookup"><span data-stu-id="02c4b-149">-ResourceType</span></span>
<span data-ttu-id="02c4b-150">Gibt den Ressourcentyp der Ressource an, für die diese Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="02c4b-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="02c4b-151">Dieses Cmdlet ruft Sperren für diese Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="02c4b-151">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="02c4b-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="02c4b-152">-Scope</span></span>
<span data-ttu-id="02c4b-153">Gibt den Bereich an, auf den die Sperre angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="02c4b-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="02c4b-154">Das Cmdlet ruft Sperren für diesen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="02c4b-154">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="02c4b-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="02c4b-155">-TenantLevel</span></span>
<span data-ttu-id="02c4b-156">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="02c4b-156">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="02c4b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c4b-157">CommonParameters</span></span>
<span data-ttu-id="02c4b-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02c4b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c4b-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02c4b-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c4b-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02c4b-160">INPUTS</span></span>

## <span data-ttu-id="02c4b-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02c4b-161">OUTPUTS</span></span>

## <span data-ttu-id="02c4b-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="02c4b-162">NOTES</span></span>

## <span data-ttu-id="02c4b-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02c4b-163">RELATED LINKS</span></span>

[<span data-ttu-id="02c4b-164">Neu – AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="02c4b-164">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="02c4b-165">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="02c4b-165">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="02c4b-166">Satz-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="02c4b-166">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


