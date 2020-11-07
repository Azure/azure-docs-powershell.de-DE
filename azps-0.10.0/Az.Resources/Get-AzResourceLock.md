---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: e774b333703714246de852d3f72ba704d7122b98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843407"
---
# <span data-ttu-id="aaa73-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="aaa73-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="aaa73-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aaa73-102">SYNOPSIS</span></span>
<span data-ttu-id="aaa73-103">Ruft eine Ressourcensperre ab.</span><span class="sxs-lookup"><span data-stu-id="aaa73-103">Gets a resource lock.</span></span>

## <span data-ttu-id="aaa73-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aaa73-104">SYNTAX</span></span>

### <span data-ttu-id="aaa73-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aaa73-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="aaa73-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="aaa73-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="aaa73-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="aaa73-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="aaa73-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="aaa73-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="aaa73-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="aaa73-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="aaa73-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="aaa73-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="aaa73-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="aaa73-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="aaa73-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aaa73-112">DESCRIPTION</span></span>
<span data-ttu-id="aaa73-113">Das Cmdlet " **Get-AzResourceLock** " ruft Azure-Ressourcen Sperren ab.</span><span class="sxs-lookup"><span data-stu-id="aaa73-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="aaa73-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aaa73-114">EXAMPLES</span></span>

### <span data-ttu-id="aaa73-115">Beispiel 1: Abrufen einer Sperre</span><span class="sxs-lookup"><span data-stu-id="aaa73-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="aaa73-116">Dieser Befehl ruft die Ressourcensperre mit dem Namen ContosoSiteLock ab.</span><span class="sxs-lookup"><span data-stu-id="aaa73-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="aaa73-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="aaa73-117">PARAMETERS</span></span>

### <span data-ttu-id="aaa73-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="aaa73-118">-ApiVersion</span></span>
<span data-ttu-id="aaa73-119">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="aaa73-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="aaa73-120">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="aaa73-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="aaa73-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="aaa73-121">-AtScope</span></span>
<span data-ttu-id="aaa73-122">Gibt an, dass dieses Cmdlet alle Sperren über den angegebenen Bereich zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="aaa73-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="aaa73-123">Wenn Sie diesen Parameter nicht angeben, gibt das Cmdlet alle Sperren an, über oder unter dem Bereich zurück.</span><span class="sxs-lookup"><span data-stu-id="aaa73-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="aaa73-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaa73-124">-DefaultProfile</span></span>
<span data-ttu-id="aaa73-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="aaa73-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aaa73-126">-Information</span><span class="sxs-lookup"><span data-stu-id="aaa73-126">-InformationAction</span></span>
<span data-ttu-id="aaa73-127">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="aaa73-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="aaa73-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="aaa73-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aaa73-129">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="aaa73-129">Continue</span></span>
- <span data-ttu-id="aaa73-130">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="aaa73-130">Ignore</span></span>
- <span data-ttu-id="aaa73-131">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="aaa73-131">Inquire</span></span>
- <span data-ttu-id="aaa73-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="aaa73-132">SilentlyContinue</span></span>
- <span data-ttu-id="aaa73-133">Beenden</span><span class="sxs-lookup"><span data-stu-id="aaa73-133">Stop</span></span>
- <span data-ttu-id="aaa73-134">Anhalten</span><span class="sxs-lookup"><span data-stu-id="aaa73-134">Suspend</span></span>

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

### <span data-ttu-id="aaa73-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="aaa73-135">-InformationVariable</span></span>
<span data-ttu-id="aaa73-136">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="aaa73-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="aaa73-137">-Sperre</span><span class="sxs-lookup"><span data-stu-id="aaa73-137">-LockId</span></span>
<span data-ttu-id="aaa73-138">Gibt die ID der Sperre an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="aaa73-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="aaa73-139">-LockName</span><span class="sxs-lookup"><span data-stu-id="aaa73-139">-LockName</span></span>
<span data-ttu-id="aaa73-140">Gibt den Namen der Sperre an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="aaa73-140">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="aaa73-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="aaa73-141">-Pre</span></span>
<span data-ttu-id="aaa73-142">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="aaa73-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="aaa73-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaa73-143">-ResourceGroupName</span></span>
<span data-ttu-id="aaa73-144">Gibt den Namen der Ressourcengruppe an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="aaa73-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="aaa73-145">Dieses Cmdlet ruft Sperren für diese Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="aaa73-145">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="aaa73-146">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="aaa73-146">-ResourceName</span></span>
<span data-ttu-id="aaa73-147">Gibt den Namen der Ressource an, für die diese Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="aaa73-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="aaa73-148">Dieses Cmdlet ruft Sperren für diese Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="aaa73-148">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="aaa73-149">-</span><span class="sxs-lookup"><span data-stu-id="aaa73-149">-ResourceType</span></span>
<span data-ttu-id="aaa73-150">Gibt den Ressourcentyp der Ressource an, für die diese Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="aaa73-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="aaa73-151">Dieses Cmdlet ruft Sperren für diese Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="aaa73-151">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="aaa73-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="aaa73-152">-Scope</span></span>
<span data-ttu-id="aaa73-153">Gibt den Bereich an, auf den die Sperre angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aaa73-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="aaa73-154">Das Cmdlet ruft Sperren für diesen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="aaa73-154">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="aaa73-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="aaa73-155">-TenantLevel</span></span>
<span data-ttu-id="aaa73-156">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="aaa73-156">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="aaa73-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa73-157">CommonParameters</span></span>
<span data-ttu-id="aaa73-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaa73-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa73-159">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaa73-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa73-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aaa73-160">INPUTS</span></span>

## <span data-ttu-id="aaa73-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aaa73-161">OUTPUTS</span></span>

## <span data-ttu-id="aaa73-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="aaa73-162">NOTES</span></span>

## <span data-ttu-id="aaa73-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aaa73-163">RELATED LINKS</span></span>

[<span data-ttu-id="aaa73-164">Neu – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="aaa73-164">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="aaa73-165">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="aaa73-165">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="aaa73-166">Satz-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="aaa73-166">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


