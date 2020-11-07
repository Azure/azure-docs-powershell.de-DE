---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappsslbinding
schema: 2.0.0
ms.openlocfilehash: 0a396b93a0ce1435302b1ee2f81d8700ec10a60d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850523"
---
# <span data-ttu-id="27ef7-101">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="27ef7-101">New-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="27ef7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="27ef7-102">SYNOPSIS</span></span>
<span data-ttu-id="27ef7-103">Erstellt eine SSL-Zertifikat Bindung für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="27ef7-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27ef7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="27ef7-104">SYNTAX</span></span>

### <span data-ttu-id="27ef7-105">S1</span><span class="sxs-lookup"><span data-stu-id="27ef7-105">S1</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27ef7-106">S2</span><span class="sxs-lookup"><span data-stu-id="27ef7-106">S2</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27ef7-107">S3</span><span class="sxs-lookup"><span data-stu-id="27ef7-107">S3</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27ef7-108">S4</span><span class="sxs-lookup"><span data-stu-id="27ef7-108">S4</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27ef7-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27ef7-109">DESCRIPTION</span></span>
<span data-ttu-id="27ef7-110">Das Cmdlet **New-AzureRmWebAppSSLBinding** erstellt eine SSL-Zertifikat Bindung (Secure Socket Layer) für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="27ef7-110">The **New-AzureRmWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="27ef7-111">Das Cmdlet erstellt eine SSL-Bindung auf zwei Arten:</span><span class="sxs-lookup"><span data-stu-id="27ef7-111">The cmdlet creates an SSL binding in two ways:</span></span> 

- <span data-ttu-id="27ef7-112">Sie können eine Web-App an ein vorhandenes Zertifikat binden.</span><span class="sxs-lookup"><span data-stu-id="27ef7-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="27ef7-113">Sie können ein neues Zertifikat hochladen und dann die Web-App an dieses neue Zertifikat binden.</span><span class="sxs-lookup"><span data-stu-id="27ef7-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>

<span data-ttu-id="27ef7-114">Unabhängig davon, welche Methode Sie verwenden, muss das Zertifikat und die Web-App derselben Azure-Ressourcengruppe zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="27ef7-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="27ef7-115">Wenn Sie eine Web-App in der Ressourcengruppe a haben und diese Web-App an ein Zertifikat in der Ressourcengruppe B binden möchten, besteht die einzige Möglichkeit darin, eine Kopie des Zertifikats in die Ressourcengruppe a hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="27ef7-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A.</span></span>

<span data-ttu-id="27ef7-116">Wenn Sie ein neues Zertifikat hochladen, sollten Sie die folgenden Anforderungen für ein Azure SSL-Zertifikat berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="27ef7-116">If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 

- <span data-ttu-id="27ef7-117">Das Zertifikat muss einen privaten Schlüssel enthalten.</span><span class="sxs-lookup"><span data-stu-id="27ef7-117">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="27ef7-118">Das Zertifikat muss das PFX-Format (Personal Information Exchange) verwenden.</span><span class="sxs-lookup"><span data-stu-id="27ef7-118">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="27ef7-119">Der Antragstellername des Zertifikats muss mit der Domäne übereinstimmen, die für den Zugriff auf die Web-App verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="27ef7-119">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="27ef7-120">Das Zertifikat muss mindestens eine 2048-Bit-Verschlüsselung verwenden.</span><span class="sxs-lookup"><span data-stu-id="27ef7-120">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="27ef7-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27ef7-121">EXAMPLES</span></span>

### <span data-ttu-id="27ef7-122">Beispiel 1: Binden eines Zertifikats an eine Web-App</span><span class="sxs-lookup"><span data-stu-id="27ef7-122">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="27ef7-123">Dieser Befehl bindet ein vorhandenes Azure-Zertifikat (ein Zertifikat mit dem Fingerabdruck E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) an die Web-App mit dem Namen ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="27ef7-123">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

## <span data-ttu-id="27ef7-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="27ef7-124">PARAMETERS</span></span>

### <span data-ttu-id="27ef7-125">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="27ef7-125">-CertificateFilePath</span></span>
<span data-ttu-id="27ef7-126">Gibt den Dateipfad für das Zertifikat an, das hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="27ef7-126">Specifies the file path for the certificate to be uploaded.</span></span>

<span data-ttu-id="27ef7-127">Der *CertificateFilePath* -Parameter ist nur erforderlich, wenn das Zertifikat noch nicht in Azure hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="27ef7-127">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ef7-128">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="27ef7-128">-CertificatePassword</span></span>
<span data-ttu-id="27ef7-129">Gibt das Entschlüsselungskennwort für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="27ef7-129">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ef7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27ef7-130">-DefaultProfile</span></span>
<span data-ttu-id="27ef7-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="27ef7-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27ef7-132">-Name</span><span class="sxs-lookup"><span data-stu-id="27ef7-132">-Name</span></span>
<span data-ttu-id="27ef7-133">Gibt den Namen der Web-App an.</span><span class="sxs-lookup"><span data-stu-id="27ef7-133">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="27ef7-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27ef7-134">-ResourceGroupName</span></span>
<span data-ttu-id="27ef7-135">Gibt den Namen der Ressourcengruppe an, der das Zertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="27ef7-135">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="27ef7-136">Im gleichen Befehl können *ResourceGroupName* Sie den Parameter ResourceGroupName *und den Parameter* "Webanwendung" nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="27ef7-136">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ef7-137">-Slot</span><span class="sxs-lookup"><span data-stu-id="27ef7-137">-Slot</span></span>
<span data-ttu-id="27ef7-138">Gibt den Namen des Web App-Bereitstellungs Steckplatzes an.</span><span class="sxs-lookup"><span data-stu-id="27ef7-138">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="27ef7-139">Sie können das Get-AzureRMWebAppSlot-Cmdlet verwenden, um einen Steckplatz abzurufen.</span><span class="sxs-lookup"><span data-stu-id="27ef7-139">You can use the Get-AzureRMWebAppSlot cmdlet to get a slot.</span></span>

<span data-ttu-id="27ef7-140">Bereitstellungs Steckplätze bieten Ihnen die Möglichkeit, Web-Apps zu inszenieren und zu überprüfen, ohne dass diese apps über das Internet zugänglich sind.</span><span class="sxs-lookup"><span data-stu-id="27ef7-140">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="27ef7-141">In der Regel werden Sie Ihre Änderungen auf einer Staging-Website bereitstellen, diese Änderungen überprüfen und dann auf der Produktionswebsite (Internet-barrierefrei) bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="27ef7-141">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ef7-142">-SslState</span><span class="sxs-lookup"><span data-stu-id="27ef7-142">-SslState</span></span>
<span data-ttu-id="27ef7-143">Gibt an, ob das Zertifikat aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="27ef7-143">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="27ef7-144">Setzen Sie den *SSLState* -Parameter auf 1, um das Zertifikat zu aktivieren, oder setzen Sie *SSLState* auf 0, um das Zertifikat zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="27ef7-144">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: SslState
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ef7-145">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="27ef7-145">-Thumbprint</span></span>
<span data-ttu-id="27ef7-146">Gibt den eindeutigen Bezeichner für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="27ef7-146">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: S2, S4
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ef7-147">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="27ef7-147">-WebApp</span></span>
<span data-ttu-id="27ef7-148">Gibt eine Web-App an.</span><span class="sxs-lookup"><span data-stu-id="27ef7-148">Specifies a Web App.</span></span>
<span data-ttu-id="27ef7-149">Verwenden Sie das Get-AzureRmWebApp-Cmdlet, um eine Web-App abzurufen.</span><span class="sxs-lookup"><span data-stu-id="27ef7-149">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="27ef7-150">Sie können den Webanwendungs Parameter nicht im gleichen Befehl *wie der* *ResourceGroupName* -Parameter und/oder den Webanwendungs *-Parameter verwenden* .</span><span class="sxs-lookup"><span data-stu-id="27ef7-150">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27ef7-151">-Webbasierter</span><span class="sxs-lookup"><span data-stu-id="27ef7-151">-WebAppName</span></span>
<span data-ttu-id="27ef7-152">Gibt den Namen der Web-App an, für die die neue SSL-Bindung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="27ef7-152">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>

<span data-ttu-id="27ef7-153">Im gleichen Befehl können *Sie den Parameter "* Webanwendungs" und *den "Webanwendungs Parameter"* nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="27ef7-153">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ef7-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ef7-154">CommonParameters</span></span>
<span data-ttu-id="27ef7-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27ef7-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ef7-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27ef7-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ef7-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="27ef7-157">INPUTS</span></span>

### <span data-ttu-id="27ef7-158">Website</span><span class="sxs-lookup"><span data-stu-id="27ef7-158">Site</span></span>
<span data-ttu-id="27ef7-159">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="27ef7-159">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="27ef7-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="27ef7-160">OUTPUTS</span></span>

## <span data-ttu-id="27ef7-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="27ef7-161">NOTES</span></span>

## <span data-ttu-id="27ef7-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="27ef7-162">RELATED LINKS</span></span>

[<span data-ttu-id="27ef7-163">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="27ef7-163">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="27ef7-164">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="27ef7-164">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="27ef7-165">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="27ef7-165">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="27ef7-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="27ef7-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


