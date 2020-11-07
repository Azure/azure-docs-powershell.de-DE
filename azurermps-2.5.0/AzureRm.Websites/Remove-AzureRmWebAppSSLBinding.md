---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappsslbinding
schema: 2.0.0
ms.openlocfilehash: 06bb13207a666b4537c267e391818865e4165e74
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848052"
---
# <span data-ttu-id="9da2b-101">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="9da2b-101">Remove-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="9da2b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9da2b-102">SYNOPSIS</span></span>
<span data-ttu-id="9da2b-103">Entfernt eine SSL-Bindung aus einem hochgeladenen Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="9da2b-103">Removes an SSL binding from an uploaded certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9da2b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9da2b-104">SYNTAX</span></span>

### <span data-ttu-id="9da2b-105">S1</span><span class="sxs-lookup"><span data-stu-id="9da2b-105">S1</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9da2b-106">S2</span><span class="sxs-lookup"><span data-stu-id="9da2b-106">S2</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9da2b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9da2b-107">DESCRIPTION</span></span>
<span data-ttu-id="9da2b-108">Das Cmdlet **Remove-AzureRmWebAppSSLBinding** entfernt eine SSL-Bindung (Secure Sockets Layer) aus einer Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9da2b-108">The **Remove-AzureRmWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="9da2b-109">SSL-Bindungen werden verwendet, um eine Web-App einem Zertifikat zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="9da2b-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="9da2b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9da2b-110">EXAMPLES</span></span>

### <span data-ttu-id="9da2b-111">Beispiel 1: Entfernen einer SSL-Bindung für eine Web-App</span><span class="sxs-lookup"><span data-stu-id="9da2b-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="9da2b-112">Dieser Befehl entfernt die SSL-Bindung für das Web App-ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="9da2b-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="9da2b-113">Da der *DeleteCertificate* -Parameter nicht enthalten ist, wird das Zertifikat gelöscht, wenn keine SSL-Bindungen mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="9da2b-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="9da2b-114">Beispiel 2: Entfernen einer SSL-Bindung, ohne das Zertifikat zu entfernen</span><span class="sxs-lookup"><span data-stu-id="9da2b-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="9da2b-115">Ähnlich wie Beispiel 1 entfernt dieser Befehl auch die SSL-Bindung für das Web App-ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="9da2b-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="9da2b-116">In diesem Fall ist der *DeleteCertificate* -Parameter jedoch enthalten, und der Parameterwert ist auf $false eingestellt.</span><span class="sxs-lookup"><span data-stu-id="9da2b-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="9da2b-117">Das bedeutet, dass das Zertifikat nicht gelöscht wird, unabhängig davon, ob SSL-Bindungen vorhanden sind oder nicht.</span><span class="sxs-lookup"><span data-stu-id="9da2b-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="9da2b-118">Beispiel 3: Verwenden eines Objektverweises zum Entfernen einer SSL-Bindung</span><span class="sxs-lookup"><span data-stu-id="9da2b-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzureRmWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="9da2b-119">In diesem Beispiel wird ein Objektverweis auf die Web App-Website verwendet, um die SSL-Bindung für eine Web-App zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="9da2b-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>

<span data-ttu-id="9da2b-120">Der erste Befehl verwendet das Get-AzureRmWebApp-Cmdlet, um einen Objektverweis auf die Web-App mit dem Namen ContosoWebApp zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9da2b-120">The first command uses the Get-AzureRmWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="9da2b-121">Dieser Objektverweis wird in einer Variablen mit dem Namen $webapp gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9da2b-121">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="9da2b-122">Der zweite Befehl verwendet den Objektverweis und das Cmdlet **Remove-AzureRmWebAppSSLBinding** , um die SSL-Bindung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="9da2b-122">The second command uses the object reference and the **Remove-AzureRmWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="9da2b-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="9da2b-123">PARAMETERS</span></span>

### <span data-ttu-id="9da2b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9da2b-124">-DefaultProfile</span></span>
<span data-ttu-id="9da2b-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9da2b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da2b-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="9da2b-126">-DeleteCertificate</span></span>
<span data-ttu-id="9da2b-127">Gibt die Aktion an, die durchgeführt werden soll, wenn die zu entfernende SSL-Bindung die einzige vom Zertifikat verwendete Bindung ist.</span><span class="sxs-lookup"><span data-stu-id="9da2b-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="9da2b-128">Wenn *DeleteCertificate* auf $false eingestellt ist, wird das Zertifikat nicht gelöscht, wenn die Bindung gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="9da2b-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="9da2b-129">Wenn *DeleteCertificate* auf $true gesetzt ist oder nicht im Befehl enthalten ist, wird das Zertifikat zusammen mit der SSL-Bindung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9da2b-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>

<span data-ttu-id="9da2b-130">Das Zertifikat wird nur gelöscht, wenn die zu entfernenden SSL-Bindung die einzige vom Zertifikat verwendete Bindung ist.</span><span class="sxs-lookup"><span data-stu-id="9da2b-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="9da2b-131">Wenn das Zertifikat mehr als eine Bindung aufweist, wird das Zertifikat unabhängig vom Wert des *DeleteCertificate* -Parameters nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="9da2b-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da2b-132">-Force</span><span class="sxs-lookup"><span data-stu-id="9da2b-132">-Force</span></span>
<span data-ttu-id="9da2b-133">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9da2b-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da2b-134">-Name</span><span class="sxs-lookup"><span data-stu-id="9da2b-134">-Name</span></span>
<span data-ttu-id="9da2b-135">Gibt den Namen der Web-App an.</span><span class="sxs-lookup"><span data-stu-id="9da2b-135">Specifies the name of the Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da2b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9da2b-136">-ResourceGroupName</span></span>
<span data-ttu-id="9da2b-137">Gibt den Namen der Ressourcengruppe an, der das Zertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9da2b-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="9da2b-138">Im gleichen Befehl können *ResourceGroupName* Sie den Parameter ResourceGroupName *und den Parameter* "Webanwendung" nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="9da2b-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da2b-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="9da2b-139">-Slot</span></span>
<span data-ttu-id="9da2b-140">Gibt den Bereitstellungs Steckplatz für Web App an.</span><span class="sxs-lookup"><span data-stu-id="9da2b-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="9da2b-141">Verwenden Sie das Get-AzureRMWebAppSlot-Cmdlet, um einen Bereitstellungs Steckplatz abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9da2b-141">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da2b-142">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="9da2b-142">-WebApp</span></span>
<span data-ttu-id="9da2b-143">Gibt eine Web-App an.</span><span class="sxs-lookup"><span data-stu-id="9da2b-143">Specifies a Web App.</span></span>
<span data-ttu-id="9da2b-144">Verwenden Sie das Get-AzureRmWebApp-Cmdlet, um eine Web-App abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9da2b-144">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="9da2b-145">Sie können den Webanwendungs Parameter nicht im gleichen Befehl *wie der* *ResourceGroupName* -Parameter und/oder den Webanwendungs *-Parameter verwenden* .</span><span class="sxs-lookup"><span data-stu-id="9da2b-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9da2b-146">-Webbasierter</span><span class="sxs-lookup"><span data-stu-id="9da2b-146">-WebAppName</span></span>
<span data-ttu-id="9da2b-147">Gibt den Namen der Web-App an.</span><span class="sxs-lookup"><span data-stu-id="9da2b-147">Specifies the name of the Web App.</span></span>

<span data-ttu-id="9da2b-148">Im gleichen Befehl können *Sie den Parameter "* Webanwendungs" und *den "Webanwendungs Parameter"* nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="9da2b-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da2b-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9da2b-149">-Confirm</span></span>
<span data-ttu-id="9da2b-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9da2b-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da2b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9da2b-151">-WhatIf</span></span>
<span data-ttu-id="9da2b-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9da2b-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9da2b-153">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9da2b-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9da2b-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9da2b-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da2b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da2b-155">CommonParameters</span></span>
<span data-ttu-id="9da2b-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9da2b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da2b-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9da2b-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da2b-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9da2b-158">INPUTS</span></span>

### <span data-ttu-id="9da2b-159">Website</span><span class="sxs-lookup"><span data-stu-id="9da2b-159">Site</span></span>
<span data-ttu-id="9da2b-160">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9da2b-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="9da2b-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9da2b-161">OUTPUTS</span></span>

## <span data-ttu-id="9da2b-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="9da2b-162">NOTES</span></span>

## <span data-ttu-id="9da2b-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9da2b-163">RELATED LINKS</span></span>

[<span data-ttu-id="9da2b-164">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="9da2b-164">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="9da2b-165">Neu – AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="9da2b-165">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="9da2b-166">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9da2b-166">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="9da2b-167">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9da2b-167">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


