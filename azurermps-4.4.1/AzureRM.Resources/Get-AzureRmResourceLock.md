---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
ms.openlocfilehash: 51fc1b96734d269fda3e09d3a22122b18fe3943a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500750"
---
# <span data-ttu-id="5edae-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="5edae-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="5edae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5edae-102">SYNOPSIS</span></span>
<span data-ttu-id="5edae-103">Ruft eine Ressourcensperre ab.</span><span class="sxs-lookup"><span data-stu-id="5edae-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5edae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5edae-104">SYNTAX</span></span>

### <span data-ttu-id="5edae-105">Eine Sperre im Bereich der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5edae-105">A lock at the resource group scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5edae-106">Eine Sperre für den Ressourcengruppen-Ressourcenbereich.</span><span class="sxs-lookup"><span data-stu-id="5edae-106">A lock at the resource group resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5edae-107">Eine Sperre im angegebenen Bereich.</span><span class="sxs-lookup"><span data-stu-id="5edae-107">A lock at the specified scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5edae-108">Eine Sperre im Abonnement Bereich.</span><span class="sxs-lookup"><span data-stu-id="5edae-108">A lock at the subscription scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5edae-109">Eine Sperre für den Ressourcenbereich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="5edae-109">A lock at the subscription resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5edae-110">Eine Sperre im Mandanten Ressourcenbereich.</span><span class="sxs-lookup"><span data-stu-id="5edae-110">A lock at the tenant resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5edae-111">Eine Sperre, nach ID.</span><span class="sxs-lookup"><span data-stu-id="5edae-111">A lock, by Id.</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5edae-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5edae-112">DESCRIPTION</span></span>
<span data-ttu-id="5edae-113">Das Cmdlet " **Get-AzureRmResourceLock** " ruft Azure-Ressourcen Sperren ab.</span><span class="sxs-lookup"><span data-stu-id="5edae-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="5edae-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5edae-114">EXAMPLES</span></span>

### <span data-ttu-id="5edae-115">Beispiel 1: Abrufen einer Sperre</span><span class="sxs-lookup"><span data-stu-id="5edae-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="5edae-116">Dieser Befehl ruft die Ressourcensperre mit dem Namen ContosoSiteLock ab.</span><span class="sxs-lookup"><span data-stu-id="5edae-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="5edae-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="5edae-117">PARAMETERS</span></span>

### <span data-ttu-id="5edae-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5edae-118">-ApiVersion</span></span>
<span data-ttu-id="5edae-119">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="5edae-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5edae-120">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="5edae-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5edae-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="5edae-121">-AtScope</span></span>
<span data-ttu-id="5edae-122">Gibt an, dass dieses Cmdlet alle Sperren über den angegebenen Bereich zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5edae-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="5edae-123">Wenn Sie diesen Parameter nicht angeben, gibt das Cmdlet alle Sperren an, über oder unter dem Bereich zurück.</span><span class="sxs-lookup"><span data-stu-id="5edae-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="5edae-124">-Information</span><span class="sxs-lookup"><span data-stu-id="5edae-124">-InformationAction</span></span>
<span data-ttu-id="5edae-125">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="5edae-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5edae-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5edae-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5edae-127">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="5edae-127">Continue</span></span>
- <span data-ttu-id="5edae-128">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="5edae-128">Ignore</span></span>
- <span data-ttu-id="5edae-129">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="5edae-129">Inquire</span></span>
- <span data-ttu-id="5edae-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5edae-130">SilentlyContinue</span></span>
- <span data-ttu-id="5edae-131">Beenden</span><span class="sxs-lookup"><span data-stu-id="5edae-131">Stop</span></span>
- <span data-ttu-id="5edae-132">Anhalten</span><span class="sxs-lookup"><span data-stu-id="5edae-132">Suspend</span></span>

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

### <span data-ttu-id="5edae-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5edae-133">-InformationVariable</span></span>
<span data-ttu-id="5edae-134">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="5edae-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5edae-135">-Sperre</span><span class="sxs-lookup"><span data-stu-id="5edae-135">-LockId</span></span>
<span data-ttu-id="5edae-136">Gibt die ID der Sperre an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5edae-136">Specifies the ID of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-137">-LockName</span><span class="sxs-lookup"><span data-stu-id="5edae-137">-LockName</span></span>
<span data-ttu-id="5edae-138">Gibt den Namen der Sperre an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5edae-138">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope., A lock at the specified scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="5edae-139">-Pre</span></span>
<span data-ttu-id="5edae-140">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="5edae-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5edae-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5edae-141">-ResourceGroupName</span></span>
<span data-ttu-id="5edae-142">Gibt den Namen der Ressourcengruppe an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="5edae-142">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="5edae-143">Dieses Cmdlet ruft Sperren für diese Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="5edae-143">This cmdlet gets locks for this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5edae-144">-ResourceName</span></span>
<span data-ttu-id="5edae-145">Gibt den Namen der Ressource an, für die diese Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="5edae-145">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="5edae-146">Dieses Cmdlet ruft Sperren für diese Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="5edae-146">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-147">-</span><span class="sxs-lookup"><span data-stu-id="5edae-147">-ResourceType</span></span>
<span data-ttu-id="5edae-148">Gibt den Ressourcentyp der Ressource an, für die diese Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="5edae-148">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="5edae-149">Dieses Cmdlet ruft Sperren für diese Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="5edae-149">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-150">-Scope</span><span class="sxs-lookup"><span data-stu-id="5edae-150">-Scope</span></span>
<span data-ttu-id="5edae-151">Gibt den Bereich an, auf den die Sperre angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5edae-151">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="5edae-152">Das Cmdlet ruft Sperren für diesen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="5edae-152">The cmdlet gets locks for this scope.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-153">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="5edae-153">-TenantLevel</span></span>
<span data-ttu-id="5edae-154">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="5edae-154">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5edae-155">-DefaultProfile</span></span>
<span data-ttu-id="5edae-156">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5edae-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5edae-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5edae-157">CommonParameters</span></span>
<span data-ttu-id="5edae-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5edae-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5edae-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5edae-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5edae-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5edae-160">INPUTS</span></span>

## <span data-ttu-id="5edae-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5edae-161">OUTPUTS</span></span>

### <span data-ttu-id="5edae-162">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="5edae-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5edae-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="5edae-163">NOTES</span></span>

## <span data-ttu-id="5edae-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5edae-164">RELATED LINKS</span></span>

[<span data-ttu-id="5edae-165">Neu – AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="5edae-165">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="5edae-166">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="5edae-166">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="5edae-167">Satz-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="5edae-167">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


