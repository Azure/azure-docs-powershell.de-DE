---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006138"
---
# <span data-ttu-id="727be-101">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="727be-101">New-AzureCertificateSetting</span></span>

## <span data-ttu-id="727be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="727be-102">SYNOPSIS</span></span>
<span data-ttu-id="727be-103">Erstellt ein Zertifikat Einstellungsobjekt für ein Zertifikat befindet sich in einem Dienst.</span><span class="sxs-lookup"><span data-stu-id="727be-103">Creates a certificate setting object for a certificate is in a service.</span></span>

## <span data-ttu-id="727be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="727be-104">SYNTAX</span></span>

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="727be-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="727be-105">DESCRIPTION</span></span>
<span data-ttu-id="727be-106">Das Cmdlet **New-AzureCertificateSetting** erstellt ein Zertifikat Einstellungsobjekt für ein Zertifikat, das sich in einem Azure-Dienst befindet.</span><span class="sxs-lookup"><span data-stu-id="727be-106">The **New-AzureCertificateSetting** cmdlet creates a certificate setting object for a certificate that is in an Azure service.</span></span>

<span data-ttu-id="727be-107">Mithilfe des Cmdlets **Add-AzureProvisioningConfig** können Sie ein Certificate Setting-Objekt verwenden, um ein Configuration-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="727be-107">You can use a certificate setting object to create a configuration object by using the **Add-AzureProvisioningConfig** cmdlet.</span></span>
<span data-ttu-id="727be-108">Verwenden Sie ein Configuration-Objekt zum Erstellen eines virtuellen Computers mithilfe des Cmdlets **New-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="727be-108">Use a configuration object to create virtual machine by using the **New-AzureVM** cmdlet.</span></span>
<span data-ttu-id="727be-109">Mithilfe des Cmdlets **New-AzureQuickVM** können Sie ein Zertifikat Einstellungsobjekt zum Erstellen eines virtuellen Computers verwenden.</span><span class="sxs-lookup"><span data-stu-id="727be-109">You can use a certificate setting object to create a virtual machine by using the **New-AzureQuickVM** cmdlet.</span></span>

## <span data-ttu-id="727be-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="727be-110">EXAMPLES</span></span>

### <span data-ttu-id="727be-111">Beispiel 1: Erstellen eines Zertifikats Einstellungs Objekts</span><span class="sxs-lookup"><span data-stu-id="727be-111">Example 1: Create a certificate setting object</span></span>
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

<span data-ttu-id="727be-112">Mit diesem Befehl wird ein Zertifikat Einstellungsobjekt für ein vorhandenes Zertifikat erstellt.</span><span class="sxs-lookup"><span data-stu-id="727be-112">This command creates a certificate setting object for an existing certificate.</span></span>

### <span data-ttu-id="727be-113">Beispiel 2: Erstellen eines virtuellen Computers, der ein Konfigurations Einstellungsobjekt verwendet</span><span class="sxs-lookup"><span data-stu-id="727be-113">Example 2: Create a virtual machine that uses a configuration setting object</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="727be-114">Mit dem ersten Befehl wird das Zertifikat ContosoCert. CER dem Dienst mit dem Namen ContosoService mithilfe des Cmdlets **Add-AzureCertificate** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="727be-114">The first command adds the certificate ContosoCert.cer to the service named ContosoService by using the **Add-AzureCertificate** cmdlet.</span></span>

<span data-ttu-id="727be-115">Der zweite Befehl erstellt ein Zertifikat Einstellungsobjekt und speichert es dann in der $CertificateSetting-Variablen.</span><span class="sxs-lookup"><span data-stu-id="727be-115">The second command creates a certificate setting object, and then stores it in the $CertificateSetting variable.</span></span>

<span data-ttu-id="727be-116">Der dritte Befehl ruft mit dem Cmdlet **Get-AzureVMImage** ein Bild aus dem Bild-Repository ab.</span><span class="sxs-lookup"><span data-stu-id="727be-116">The third command gets an image from the image repository by using the **Get-AzureVMImage** cmdlet.</span></span>
<span data-ttu-id="727be-117">Dieser Befehl speichert das Bild in der $Image Variablen.</span><span class="sxs-lookup"><span data-stu-id="727be-117">This command store the image in the $Image variable.</span></span>

<span data-ttu-id="727be-118">Mit dem Final-Befehl wird ein Konfigurationsobjekt für virtuelle Computer basierend auf dem Bild in $Image mithilfe des Cmdlets **New-AzureVMConfig** erstellt.</span><span class="sxs-lookup"><span data-stu-id="727be-118">The final command creates a virtual machine configuration object based on the image in $Image by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="727be-119">Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das Cmdlet **Add-AzureProvisioningConfig** .</span><span class="sxs-lookup"><span data-stu-id="727be-119">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="727be-120">Dieses Cmdlet fügt der Konfiguration Bereitstellungsinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="727be-120">That cmdlet add provisioning information to the configuration.</span></span>
<span data-ttu-id="727be-121">Der Befehl übergibt das Objekt an das Cmdlet **New-AzureVM** , das den virtuellen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="727be-121">The command passes the object to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

## <span data-ttu-id="727be-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="727be-122">PARAMETERS</span></span>

### <span data-ttu-id="727be-123">-Information</span><span class="sxs-lookup"><span data-stu-id="727be-123">-InformationAction</span></span>
<span data-ttu-id="727be-124">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="727be-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="727be-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="727be-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="727be-126">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="727be-126">Continue</span></span>
- <span data-ttu-id="727be-127">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="727be-127">Ignore</span></span>
- <span data-ttu-id="727be-128">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="727be-128">Inquire</span></span>
- <span data-ttu-id="727be-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="727be-129">SilentlyContinue</span></span>
- <span data-ttu-id="727be-130">Beenden</span><span class="sxs-lookup"><span data-stu-id="727be-130">Stop</span></span>
- <span data-ttu-id="727be-131">Anhalten</span><span class="sxs-lookup"><span data-stu-id="727be-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="727be-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="727be-132">-InformationVariable</span></span>
<span data-ttu-id="727be-133">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="727be-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="727be-134">-StoreName</span><span class="sxs-lookup"><span data-stu-id="727be-134">-StoreName</span></span>
<span data-ttu-id="727be-135">Gibt den Zertifikatspeicher an, in dem das Zertifikat abgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="727be-135">Specifies the certificate store in which to put the certificate.</span></span>
<span data-ttu-id="727be-136">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="727be-136">Valid values are:</span></span> 

- <span data-ttu-id="727be-137">AddressBook</span><span class="sxs-lookup"><span data-stu-id="727be-137">AddressBook</span></span>
- <span data-ttu-id="727be-138">AuthRoot</span><span class="sxs-lookup"><span data-stu-id="727be-138">AuthRoot</span></span>
- <span data-ttu-id="727be-139">CertificateAuthority</span><span class="sxs-lookup"><span data-stu-id="727be-139">CertificateAuthority</span></span>
- <span data-ttu-id="727be-140">Nicht erlaubt</span><span class="sxs-lookup"><span data-stu-id="727be-140">Disallowed</span></span>
- <span data-ttu-id="727be-141">Meine</span><span class="sxs-lookup"><span data-stu-id="727be-141">My</span></span>
- <span data-ttu-id="727be-142">Stamm</span><span class="sxs-lookup"><span data-stu-id="727be-142">Root</span></span>
- <span data-ttu-id="727be-143">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="727be-143">TrustedPeople</span></span>
- <span data-ttu-id="727be-144">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="727be-144">TrustedPublisher</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="727be-145">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="727be-145">-Thumbprint</span></span>
<span data-ttu-id="727be-146">Gibt den Fingerabdruck des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="727be-146">Specifies the thumbprint of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="727be-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="727be-147">CommonParameters</span></span>
<span data-ttu-id="727be-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="727be-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="727be-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="727be-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="727be-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="727be-150">INPUTS</span></span>

## <span data-ttu-id="727be-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="727be-151">OUTPUTS</span></span>

## <span data-ttu-id="727be-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="727be-152">NOTES</span></span>

## <span data-ttu-id="727be-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="727be-153">RELATED LINKS</span></span>

[<span data-ttu-id="727be-154">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="727be-154">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="727be-155">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="727be-155">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="727be-156">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="727be-156">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="727be-157">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="727be-157">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="727be-158">Neu – AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="727be-158">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)

[<span data-ttu-id="727be-159">Neu – AzureVM</span><span class="sxs-lookup"><span data-stu-id="727be-159">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="727be-160">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="727be-160">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


