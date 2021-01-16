---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 2fff18033febbab23083127628959d2fca9305a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367099"
---
# <span data-ttu-id="e1b4f-101">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="e1b4f-101">New-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="e1b4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1b4f-102">SYNOPSIS</span></span>
<span data-ttu-id="e1b4f-103">Erstellt eine SSL-Zertifikatbindung für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

## <span data-ttu-id="e1b4f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1b4f-104">SYNTAX</span></span>

### <span data-ttu-id="e1b4f-105">S1</span><span class="sxs-lookup"><span data-stu-id="e1b4f-105">S1</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1b4f-106">S2</span><span class="sxs-lookup"><span data-stu-id="e1b4f-106">S2</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1b4f-107">S3</span><span class="sxs-lookup"><span data-stu-id="e1b4f-107">S3</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1b4f-108">S4</span><span class="sxs-lookup"><span data-stu-id="e1b4f-108">S4</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1b4f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1b4f-109">DESCRIPTION</span></span>
<span data-ttu-id="e1b4f-110">Das **Cmdlet "New-AzWebAppSSLBinding"** erstellt eine SECURE Socket Layer (SSL)-Zertifikatbindung für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-110">The **New-AzWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="e1b4f-111">Das Cmdlet erstellt auf zwei Arten eine SSL-Bindung:</span><span class="sxs-lookup"><span data-stu-id="e1b4f-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="e1b4f-112">Sie können eine Web App an ein vorhandenes Zertifikat binden.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="e1b4f-113">Sie können ein neues Zertifikat hochladen und dann die Web App an dieses neue Zertifikat binden.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="e1b4f-114">Unabhängig davon, welchen Ansatz Sie verwenden, müssen das Zertifikat und die Web App derselben Azure-Ressourcengruppe zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="e1b4f-115">Wenn Sie über eine Web App in der Ressourcengruppe A verfügen und diese Web App an ein Zertifikat in der Ressourcengruppe B binden möchten, besteht die einzige Möglichkeit hierin, eine Kopie des Zertifikats in die Ressourcengruppe A hochzuladen. Wenn Sie ein neues Zertifikat hochladen, beachten Sie die folgenden Anforderungen für ein Azure SSL-Zertifikat:</span><span class="sxs-lookup"><span data-stu-id="e1b4f-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="e1b4f-116">Das Zertifikat muss einen privaten Schlüssel enthalten.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="e1b4f-117">Für das Zertifikat muss das Format PFX (Personal Information Exchange) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="e1b4f-118">Der Betreffname des Zertifikats muss mit der Domäne übereinstimmen, die für den Zugriff auf die Web App verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="e1b4f-119">Für das Zertifikat muss mindestens eine 2048-Bit-Verschlüsselung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="e1b4f-120">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e1b4f-120">EXAMPLES</span></span>

### <span data-ttu-id="e1b4f-121">Beispiel 1: Binden eines Zertifikats an eine Web App</span><span class="sxs-lookup"><span data-stu-id="e1b4f-121">Example 1: Bind a certificate to a Web App</span></span>
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="e1b4f-122">Mit diesem Befehl wird ein vorhandenes Azure-Zertifikat (ein Zertifikat mit Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) an die Web App namens ContosoWebApp gebunden.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

### <span data-ttu-id="e1b4f-123">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e1b4f-123">Example 2</span></span>

<span data-ttu-id="e1b4f-124">Erstellt eine SSL-Zertifikatbindung für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-124">Creates an SSL certificate binding for an Azure Web App.</span></span> <span data-ttu-id="e1b4f-125">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="e1b4f-125">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## <span data-ttu-id="e1b4f-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1b4f-126">PARAMETERS</span></span>

### <span data-ttu-id="e1b4f-127">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e1b4f-127">-CertificateFilePath</span></span>
<span data-ttu-id="e1b4f-128">Gibt den Dateipfad für das hoch zuladende Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-128">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="e1b4f-129">Der *Parameter "CertificateFilePath"* ist nur erforderlich, wenn das Zertifikat noch nicht in Azure hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-129">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b4f-130">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e1b4f-130">-CertificatePassword</span></span>
<span data-ttu-id="e1b4f-131">Gibt das Entschlüsselungskennwort für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-131">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b4f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1b4f-132">-DefaultProfile</span></span>
<span data-ttu-id="e1b4f-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1b4f-134">-Name</span><span class="sxs-lookup"><span data-stu-id="e1b4f-134">-Name</span></span>
<span data-ttu-id="e1b4f-135">Gibt den Namen der Web App an.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-135">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="e1b4f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1b4f-136">-ResourceGroupName</span></span>
<span data-ttu-id="e1b4f-137">Gibt den Namen der Ressourcengruppe an, der das Zertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="e1b4f-138">Sie können den Parameter *"ResourceGroupName"* und den Parameter *"WebApp" nicht* in demselben Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b4f-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="e1b4f-139">-Slot</span></span>
<span data-ttu-id="e1b4f-140">Gibt den Namen des Bereitstellungsplatzes für Web App an.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-140">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="e1b4f-141">Sie können das cmdlet Get-AzWebAppSlot verwenden, um einen Slot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-141">You can use the Get-AzWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="e1b4f-142">Bereitstellungsplätze bieten Ihnen die Möglichkeit, Web Apps inszenieren und überprüfen zu können, ohne dass sie über das Internet zugänglich sind.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-142">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="e1b4f-143">Normalerweise stellen Sie Ihre Änderungen auf einer Stagingwebsite zur Verfügung, überprüfen diese Änderungen und stellen sie dann auf der Produktionswebsite (internetbarrierefrei) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-143">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b4f-144">-SslState</span><span class="sxs-lookup"><span data-stu-id="e1b4f-144">-SslState</span></span>
<span data-ttu-id="e1b4f-145">Gibt an, ob das Zertifikat aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-145">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="e1b4f-146">Legen Sie *den Parameter "SSLState"* auf "1" zum Aktivieren des Zertifikats oder *"SSLState"* auf "0" zum Deaktivieren des Zertifikats festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-146">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b4f-147">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="e1b4f-147">-Thumbprint</span></span>
<span data-ttu-id="e1b4f-148">Gibt den eindeutigen Bezeichner für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-148">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S2, S4
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b4f-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e1b4f-149">-WebApp</span></span>
<span data-ttu-id="e1b4f-150">Gibt eine Web App an.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-150">Specifies a Web App.</span></span>
<span data-ttu-id="e1b4f-151">Um eine Web App zu erhalten, verwenden Sie das Get-AzWebApp-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-151">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="e1b4f-152">Sie können den Parameter *"WebApp"* nicht in demselben Befehl wie den *Parameter "ResourceGroupName"* und/oder *"WebAppName" verwenden.*</span><span class="sxs-lookup"><span data-stu-id="e1b4f-152">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S3, S4
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1b4f-153">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="e1b4f-153">-WebAppName</span></span>
<span data-ttu-id="e1b4f-154">Gibt den Namen der Web App an, für die die neue SSL-Bindung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-154">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="e1b4f-155">Sie können den Parameter *"WebAppName"* und den Parameter *"WebApp"* nicht im gleichen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-155">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b4f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1b4f-156">CommonParameters</span></span>
<span data-ttu-id="e1b4f-157">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1b4f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1b4f-158">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1b4f-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1b4f-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e1b4f-159">INPUTS</span></span>

### <span data-ttu-id="e1b4f-160">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e1b4f-160">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e1b4f-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e1b4f-161">OUTPUTS</span></span>

### <span data-ttu-id="e1b4f-162">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="e1b4f-162">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="e1b4f-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e1b4f-163">NOTES</span></span>

## <span data-ttu-id="e1b4f-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e1b4f-164">RELATED LINKS</span></span>

[<span data-ttu-id="e1b4f-165">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="e1b4f-165">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="e1b4f-166">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="e1b4f-166">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="e1b4f-167">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e1b4f-167">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="e1b4f-168">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e1b4f-168">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


