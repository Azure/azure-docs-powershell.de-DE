---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 553a9561939ffcef3337b0c13d384c5f5f47340e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664949"
---
# <span data-ttu-id="46f79-101">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="46f79-101">Remove-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="46f79-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46f79-102">SYNOPSIS</span></span>
<span data-ttu-id="46f79-103">Entfernt eine SSL-Bindung aus einem hochgeladenen Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="46f79-103">Removes an SSL binding from an uploaded certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46f79-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46f79-104">SYNTAX</span></span>

### <span data-ttu-id="46f79-105">S1</span><span class="sxs-lookup"><span data-stu-id="46f79-105">S1</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46f79-106">S2</span><span class="sxs-lookup"><span data-stu-id="46f79-106">S2</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46f79-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46f79-107">DESCRIPTION</span></span>
<span data-ttu-id="46f79-108">Das Cmdlet **Remove-AzureRmWebAppSSLBinding** entfernt eine SSL-Bindung (Secure Sockets Layer) aus einer Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="46f79-108">The **Remove-AzureRmWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="46f79-109">SSL-Bindungen werden verwendet, um eine Web-App einem Zertifikat zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="46f79-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="46f79-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46f79-110">EXAMPLES</span></span>

### <span data-ttu-id="46f79-111">Beispiel 1: Entfernen einer SSL-Bindung für eine Web-App</span><span class="sxs-lookup"><span data-stu-id="46f79-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="46f79-112">Dieser Befehl entfernt die SSL-Bindung für das Web App-ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="46f79-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="46f79-113">Da der *DeleteCertificate* -Parameter nicht enthalten ist, wird das Zertifikat gelöscht, wenn keine SSL-Bindungen mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="46f79-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="46f79-114">Beispiel 2: Entfernen einer SSL-Bindung, ohne das Zertifikat zu entfernen</span><span class="sxs-lookup"><span data-stu-id="46f79-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="46f79-115">Ähnlich wie Beispiel 1 entfernt dieser Befehl auch die SSL-Bindung für das Web App-ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="46f79-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="46f79-116">In diesem Fall ist der *DeleteCertificate* -Parameter jedoch enthalten, und der Parameterwert ist auf $false eingestellt.</span><span class="sxs-lookup"><span data-stu-id="46f79-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="46f79-117">Das bedeutet, dass das Zertifikat nicht gelöscht wird, unabhängig davon, ob SSL-Bindungen vorhanden sind oder nicht.</span><span class="sxs-lookup"><span data-stu-id="46f79-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="46f79-118">Beispiel 3: Verwenden eines Objektverweises zum Entfernen einer SSL-Bindung</span><span class="sxs-lookup"><span data-stu-id="46f79-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzureRmWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="46f79-119">In diesem Beispiel wird ein Objektverweis auf die Web App-Website verwendet, um die SSL-Bindung für eine Web-App zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="46f79-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>

<span data-ttu-id="46f79-120">Der erste Befehl verwendet das Get-AzureRmWebApp-Cmdlet, um einen Objektverweis auf die Web-App mit dem Namen ContosoWebApp zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="46f79-120">The first command uses the Get-AzureRmWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="46f79-121">Dieser Objektverweis wird in einer Variablen mit dem Namen $webapp gespeichert.</span><span class="sxs-lookup"><span data-stu-id="46f79-121">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="46f79-122">Der zweite Befehl verwendet den Objektverweis und das Cmdlet **Remove-AzureRmWebAppSSLBinding** , um die SSL-Bindung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="46f79-122">The second command uses the object reference and the **Remove-AzureRmWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="46f79-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="46f79-123">PARAMETERS</span></span>

### <span data-ttu-id="46f79-124">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="46f79-124">-DeleteCertificate</span></span>
<span data-ttu-id="46f79-125">Gibt die Aktion an, die durchgeführt werden soll, wenn die zu entfernende SSL-Bindung die einzige vom Zertifikat verwendete Bindung ist.</span><span class="sxs-lookup"><span data-stu-id="46f79-125">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="46f79-126">Wenn *DeleteCertificate* auf $false eingestellt ist, wird das Zertifikat nicht gelöscht, wenn die Bindung gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="46f79-126">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="46f79-127">Wenn *DeleteCertificate* auf $true gesetzt ist oder nicht im Befehl enthalten ist, wird das Zertifikat zusammen mit der SSL-Bindung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="46f79-127">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>

<span data-ttu-id="46f79-128">Das Zertifikat wird nur gelöscht, wenn die zu entfernenden SSL-Bindung die einzige vom Zertifikat verwendete Bindung ist.</span><span class="sxs-lookup"><span data-stu-id="46f79-128">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="46f79-129">Wenn das Zertifikat mehr als eine Bindung aufweist, wird das Zertifikat unabhängig vom Wert des *DeleteCertificate* -Parameters nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="46f79-129">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

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

### <span data-ttu-id="46f79-130">-Force</span><span class="sxs-lookup"><span data-stu-id="46f79-130">-Force</span></span>
<span data-ttu-id="46f79-131">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="46f79-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="46f79-132">-Name</span><span class="sxs-lookup"><span data-stu-id="46f79-132">-Name</span></span>
<span data-ttu-id="46f79-133">Gibt den Namen der Web-App an.</span><span class="sxs-lookup"><span data-stu-id="46f79-133">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="46f79-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46f79-134">-ResourceGroupName</span></span>
<span data-ttu-id="46f79-135">Gibt den Namen der Ressourcengruppe an, der das Zertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="46f79-135">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="46f79-136">Im gleichen Befehl können *ResourceGroupName* Sie den Parameter ResourceGroupName *und den Parameter* "Webanwendung" nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="46f79-136">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="46f79-137">-Slot</span><span class="sxs-lookup"><span data-stu-id="46f79-137">-Slot</span></span>
<span data-ttu-id="46f79-138">Gibt den Bereitstellungs Steckplatz für Web App an.</span><span class="sxs-lookup"><span data-stu-id="46f79-138">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="46f79-139">Verwenden Sie das Get-AzureRMWebAppSlot-Cmdlet, um einen Bereitstellungs Steckplatz abzurufen.</span><span class="sxs-lookup"><span data-stu-id="46f79-139">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="46f79-140">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="46f79-140">-WebApp</span></span>
<span data-ttu-id="46f79-141">Gibt eine Web-App an.</span><span class="sxs-lookup"><span data-stu-id="46f79-141">Specifies a Web App.</span></span>
<span data-ttu-id="46f79-142">Verwenden Sie das Get-AzureRmWebApp-Cmdlet, um eine Web-App abzurufen.</span><span class="sxs-lookup"><span data-stu-id="46f79-142">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="46f79-143">Sie können den Webanwendungs Parameter nicht im gleichen Befehl *wie der* *ResourceGroupName* -Parameter und/oder den Webanwendungs *-Parameter verwenden* .</span><span class="sxs-lookup"><span data-stu-id="46f79-143">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46f79-144">-Webbasierter</span><span class="sxs-lookup"><span data-stu-id="46f79-144">-WebAppName</span></span>
<span data-ttu-id="46f79-145">Gibt den Namen der Web-App an.</span><span class="sxs-lookup"><span data-stu-id="46f79-145">Specifies the name of the Web App.</span></span>

<span data-ttu-id="46f79-146">Im gleichen Befehl können *Sie den Parameter "* Webanwendungs" und *den "Webanwendungs Parameter"* nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="46f79-146">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="46f79-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46f79-147">-Confirm</span></span>
<span data-ttu-id="46f79-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46f79-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46f79-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46f79-149">-WhatIf</span></span>
<span data-ttu-id="46f79-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46f79-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46f79-151">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46f79-151">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46f79-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46f79-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46f79-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f79-153">-DefaultProfile</span></span>
<span data-ttu-id="46f79-154">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46f79-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46f79-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f79-155">CommonParameters</span></span>
<span data-ttu-id="46f79-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46f79-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f79-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46f79-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f79-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46f79-158">INPUTS</span></span>

### <span data-ttu-id="46f79-159">Website</span><span class="sxs-lookup"><span data-stu-id="46f79-159">Site</span></span>
<span data-ttu-id="46f79-160">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="46f79-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="46f79-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46f79-161">OUTPUTS</span></span>

## <span data-ttu-id="46f79-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="46f79-162">NOTES</span></span>

## <span data-ttu-id="46f79-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46f79-163">RELATED LINKS</span></span>

[<span data-ttu-id="46f79-164">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="46f79-164">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="46f79-165">Neu – AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="46f79-165">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="46f79-166">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="46f79-166">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="46f79-167">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46f79-167">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


