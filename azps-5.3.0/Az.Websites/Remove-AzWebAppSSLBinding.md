---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460372"
---
# <span data-ttu-id="10d27-101">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="10d27-101">Remove-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="10d27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10d27-102">SYNOPSIS</span></span>
<span data-ttu-id="10d27-103">Entfernt eine SSL-Bindung aus einem hochgeladenen Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="10d27-103">Removes an SSL binding from an uploaded certificate.</span></span>

## <span data-ttu-id="10d27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10d27-104">SYNTAX</span></span>

### <span data-ttu-id="10d27-105">S1</span><span class="sxs-lookup"><span data-stu-id="10d27-105">S1</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10d27-106">S2</span><span class="sxs-lookup"><span data-stu-id="10d27-106">S2</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10d27-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10d27-107">DESCRIPTION</span></span>
<span data-ttu-id="10d27-108">Das **Cmdlet "Remove-AzWebAppSSLBinding"** entfernt eine Secure Sockets Layer (SSL)-Bindung aus einer Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="10d27-108">The **Remove-AzWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="10d27-109">SSL-Bindungen werden verwendet, um eine Web App einem Zertifikat zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="10d27-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="10d27-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="10d27-110">EXAMPLES</span></span>

### <span data-ttu-id="10d27-111">Beispiel 1: Entfernen einer SSL-Bindung für eine Web App</span><span class="sxs-lookup"><span data-stu-id="10d27-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="10d27-112">Mit diesem Befehl wird die SSL-Bindung für die Web App ContosoWebApp entfernt.</span><span class="sxs-lookup"><span data-stu-id="10d27-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="10d27-113">Da der *Parameter "DeleteCertificate"* nicht enthalten ist, wird das Zertifikat gelöscht, wenn es keine SSL-Bindungen mehr enthält.</span><span class="sxs-lookup"><span data-stu-id="10d27-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="10d27-114">Beispiel 2: Entfernen einer SSL-Bindung ohne Entfernen des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="10d27-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="10d27-115">Ähnlich wie in Beispiel 1 entfernt dieser Befehl auch die SSL-Bindung für die Web App ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="10d27-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="10d27-116">In diesem Fall ist jedoch der *Parameter "DeleteCertificate"* enthalten, und der Parameterwert wird auf "$False.</span><span class="sxs-lookup"><span data-stu-id="10d27-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="10d27-117">Das bedeutet, dass das Zertifikat nicht gelöscht wird, unabhängig davon, ob es über SSL-Bindungen verfügt oder nicht.</span><span class="sxs-lookup"><span data-stu-id="10d27-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="10d27-118">Beispiel 3: Verwenden eines Objektverweises zum Entfernen einer SSL-Bindung</span><span class="sxs-lookup"><span data-stu-id="10d27-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="10d27-119">In diesem Beispiel wird ein Objektverweis auf die Web App-Website verwendet, um die -SSL-Bindung für eine Web App zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="10d27-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>
<span data-ttu-id="10d27-120">Der erste Befehl verwendet das Get-AzWebApp Cmdlet, um einen Objektverweis auf die Web App namens "ContosoWebApp" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="10d27-120">The first command uses the Get-AzWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="10d27-121">Dieser Objektverweis wird in einer Variablen mit dem Namen $WebApp.</span><span class="sxs-lookup"><span data-stu-id="10d27-121">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="10d27-122">Der zweite Befehl verwendet den Objektverweis und das **Cmdlet "Remove-AzWebAppSSLBinding"** zum Entfernen der SSL-Bindung.</span><span class="sxs-lookup"><span data-stu-id="10d27-122">The second command uses the object reference and the **Remove-AzWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="10d27-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10d27-123">PARAMETERS</span></span>

### <span data-ttu-id="10d27-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d27-124">-DefaultProfile</span></span>
<span data-ttu-id="10d27-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10d27-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10d27-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="10d27-126">-DeleteCertificate</span></span>
<span data-ttu-id="10d27-127">Gibt die Aktion an, die erfolgt, wenn die ssl-Bindung, die entfernt wird, die einzige vom Zertifikat verwendete Bindung ist.</span><span class="sxs-lookup"><span data-stu-id="10d27-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="10d27-128">Wenn *DeleteCertificate* auf $False festgelegt ist, wird das Zertifikat beim Löschen der Bindung nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="10d27-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="10d27-129">Wenn *DeleteCertificate* auf $True oder nicht im Befehl enthalten ist, wird das Zertifikat zusammen mit der SSL-Bindung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="10d27-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>
<span data-ttu-id="10d27-130">Das Zertifikat wird nur gelöscht, wenn die zu entfernende SSL-Bindung die einzige vom Zertifikat verwendete Bindung ist.</span><span class="sxs-lookup"><span data-stu-id="10d27-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="10d27-131">Wenn das Zertifikat mehrere Bindungen enthält, wird das Zertifikat unabhängig vom Wert des Parameters *"DeleteCertificate" nicht* entfernt.</span><span class="sxs-lookup"><span data-stu-id="10d27-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d27-132">-Force</span><span class="sxs-lookup"><span data-stu-id="10d27-132">-Force</span></span>
<span data-ttu-id="10d27-133">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="10d27-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d27-134">-Name</span><span class="sxs-lookup"><span data-stu-id="10d27-134">-Name</span></span>
<span data-ttu-id="10d27-135">Gibt den Namen der Web App an.</span><span class="sxs-lookup"><span data-stu-id="10d27-135">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d27-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10d27-136">-ResourceGroupName</span></span>
<span data-ttu-id="10d27-137">Gibt den Namen der Ressourcengruppe an, der das Zertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="10d27-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="10d27-138">Sie können den Parameter *"ResourceGroupName"* und den Parameter *"WebApp"* nicht im gleichen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="10d27-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d27-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="10d27-139">-Slot</span></span>
<span data-ttu-id="10d27-140">Gibt den Bereitstellungsplatz für Web App an.</span><span class="sxs-lookup"><span data-stu-id="10d27-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="10d27-141">Um einen Bereitstellungsplatz zu erhalten, verwenden Sie das Get-AzWebAppSlot Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10d27-141">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d27-142">-WebApp</span><span class="sxs-lookup"><span data-stu-id="10d27-142">-WebApp</span></span>
<span data-ttu-id="10d27-143">Gibt eine Web App an.</span><span class="sxs-lookup"><span data-stu-id="10d27-143">Specifies a Web App.</span></span>
<span data-ttu-id="10d27-144">Um eine Web App zu erhalten, verwenden Sie das Get-AzWebApp Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10d27-144">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="10d27-145">Sie können den Parameter *"WebApp"* nicht in demselben Befehl wie den *Parameter "ResourceGroupName"* und/oder *"WebAppName" verwenden.*</span><span class="sxs-lookup"><span data-stu-id="10d27-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10d27-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="10d27-146">-WebAppName</span></span>
<span data-ttu-id="10d27-147">Gibt den Namen der Web App an.</span><span class="sxs-lookup"><span data-stu-id="10d27-147">Specifies the name of the Web App.</span></span>
<span data-ttu-id="10d27-148">Sie können den Parameter *"WebAppName"* und den Parameter *"WebApp" nicht* im gleichen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="10d27-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d27-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10d27-149">-Confirm</span></span>
<span data-ttu-id="10d27-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="10d27-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10d27-151">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="10d27-151">-WhatIf</span></span>
<span data-ttu-id="10d27-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="10d27-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10d27-153">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="10d27-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10d27-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="10d27-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10d27-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d27-155">CommonParameters</span></span>
<span data-ttu-id="10d27-156">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10d27-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d27-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10d27-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d27-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="10d27-158">INPUTS</span></span>

### <span data-ttu-id="10d27-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="10d27-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="10d27-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="10d27-160">OUTPUTS</span></span>

### <span data-ttu-id="10d27-161">System.Void</span><span class="sxs-lookup"><span data-stu-id="10d27-161">System.Void</span></span>

## <span data-ttu-id="10d27-162">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="10d27-162">NOTES</span></span>

## <span data-ttu-id="10d27-163">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="10d27-163">RELATED LINKS</span></span>

[<span data-ttu-id="10d27-164">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="10d27-164">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="10d27-165">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="10d27-165">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="10d27-166">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="10d27-166">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="10d27-167">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="10d27-167">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


