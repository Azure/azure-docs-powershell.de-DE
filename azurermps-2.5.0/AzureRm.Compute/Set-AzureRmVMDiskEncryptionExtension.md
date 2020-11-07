---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdiskencryptionextension
schema: 2.0.0
ms.openlocfilehash: 76bdebc68f1fafef127863ef753c28fce7034fe0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850040"
---
# <span data-ttu-id="10a0d-101">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="10a0d-101">Set-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="10a0d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="10a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="10a0d-103">Aktiviert die Verschlüsselung auf einem ausgeführten IaaS-virtuellen Computer in Azure.</span><span class="sxs-lookup"><span data-stu-id="10a0d-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10a0d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="10a0d-104">SYNTAX</span></span>

### <span data-ttu-id="10a0d-105">AADClientSecretParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="10a0d-105">AADClientSecretParameterSet (Default)</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10a0d-106">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="10a0d-106">AADClientCertParameterSet</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10a0d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10a0d-107">DESCRIPTION</span></span>
<span data-ttu-id="10a0d-108">Das Cmdlet " **Satz-AzureRmVMDiskEncryptionExtension** " ermöglicht die Verschlüsselung auf einer ausgeführten Infrastruktur als IaaS-virtueller Computer in Azure.</span><span class="sxs-lookup"><span data-stu-id="10a0d-108">The **Set-AzureRmVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="10a0d-109">Dieses Cmdlet ermöglicht die Verschlüsselung, indem die Datenträger Verschlüsselungs Erweiterung auf dem virtuellen Computer installiert wird.</span><span class="sxs-lookup"><span data-stu-id="10a0d-109">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="10a0d-110">Wenn kein *Name* -Parameter angegeben ist, wird eine Erweiterung mit dem Standardnamen AzureDiskEncryption für virtuelle Computer installiert, auf denen das Windows-Betriebssystem oder AzureDiskEncryptionForLinux für Linux-Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="10a0d-110">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="10a0d-111">Dieses Cmdlet erfordert eine Bestätigung der Benutzer als einer der Schritte zum Aktivieren der Verschlüsselung erfordert einen Neustart des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="10a0d-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="10a0d-112">Es wird empfohlen, dass Sie Ihre Arbeit auf dem virtuellen Computer speichern, bevor Sie dieses Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="10a0d-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="10a0d-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10a0d-113">EXAMPLES</span></span>

### <span data-ttu-id="10a0d-114">Beispiel 1: Aktivieren der Verschlüsselung mithilfe der Azure AD-Client-ID und des Client Geheimnisses</span><span class="sxs-lookup"><span data-stu-id="10a0d-114">Example 1: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="10a0d-115">In diesem Beispiel wird die Verschlüsselung mithilfe der Azure AD-Client-ID und des Client Geheimnisses aktiviert.</span><span class="sxs-lookup"><span data-stu-id="10a0d-115">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="10a0d-116">Beispiel 2: Aktivieren der Verschlüsselung mithilfe der Azure AD-Client-ID und des Fingerabdrucks der Client Zertifizierung</span><span class="sxs-lookup"><span data-stu-id="10a0d-116">Example 2: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$aadClientCertThumbprint= $cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($fileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($jsonObject)
$JSONEncoded = [System.Convert]::ToBase64String($jsonObjectBytes)

$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="10a0d-117">In diesem Beispiel wird die Verschlüsselung mithilfe der Azure AD-Client-ID und der Client Zertifizierungs Fingerabdrücke aktiviert.</span><span class="sxs-lookup"><span data-stu-id="10a0d-117">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="10a0d-118">Beispiel 3: Aktivieren der Verschlüsselung mithilfe von Azure AD-Client-ID, Client Secret und Umbrechen des Datenträger Verschlüsselungsschlüssels mithilfe des Schlüssel Verschlüsselungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="10a0d-118">Example 3: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="10a0d-119">In diesem Beispiel wird die Verschlüsselung mithilfe von Azure AD-Client-ID, Client Secret und Umbrechen des Datenträger Verschlüsselungsschlüssels mithilfe des Schlüssel Verschlüsselungsschlüssels aktiviert.</span><span class="sxs-lookup"><span data-stu-id="10a0d-119">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="10a0d-120">Beispiel 4: Aktivieren der Verschlüsselung mithilfe der Azure AD-Client-ID, des clientcert-Fingerabdrucks und umbrechen der Datenträger EncryptionKey mithilfe des Schlüssel Verschlüsselungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="10a0d-120">Example 4: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$AADClientCertThumbprint= $Cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($FileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($JSONObject)
$JsonEncoded = [System.Convert]::ToBase64String($JSONObjectBytes)
$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzureKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="10a0d-121">In diesem Beispiel wird die Verschlüsselung mithilfe von Azure AD-Client-ID, Client CERT-Fingerabdruck und Umbrechen des Datenträger Verschlüsselungsschlüssels mithilfe des Schlüssel Verschlüsselungsschlüssels aktiviert.</span><span class="sxs-lookup"><span data-stu-id="10a0d-121">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="10a0d-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="10a0d-122">PARAMETERS</span></span>

### <span data-ttu-id="10a0d-123">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="10a0d-123">-AadClientCertThumbprint</span></span>
<span data-ttu-id="10a0d-124">Gibt den Fingerabdruck des AzureActive Directory (Azure AD)-Anwendungsclient Zertifikats an, das über die Berechtigungen zum Schreiben von Geheimnissen in **keyvault** verfügt.</span><span class="sxs-lookup"><span data-stu-id="10a0d-124">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="10a0d-125">Voraussetzung ist, dass das Azure AD-Clientzertifikat zuvor auf dem lokalen Computerzertifikatspeicher des virtuellen Computers bereitgestellt werden muss `my` .</span><span class="sxs-lookup"><span data-stu-id="10a0d-125">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="10a0d-126">Mithilfe des Add-AzureRmVMSecret-Cmdlets kann ein Zertifikat für einen virtuellen Computer in Azure bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="10a0d-126">The Add-AzureRmVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="10a0d-127">Weitere Informationen finden Sie in der Hilfe zum Cmdlet **Add-AzureRmVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="10a0d-127">For more details, see the **Add-AzureRmVMSecret** cmdlet help.</span></span>
<span data-ttu-id="10a0d-128">Das Zertifikat muss zuvor auf dem lokalen Computer meines Zertifikatsspeichers auf dem virtuellen Computer bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="10a0d-128">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: String
Parameter Sets: AADClientCertParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-129">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="10a0d-129">-AadClientID</span></span>
<span data-ttu-id="10a0d-130">Gibt die Client-ID der Azure AD-Anwendung an, die über die Berechtigung zum Schreiben von Geheimnissen in **keyvault** verfügt.</span><span class="sxs-lookup"><span data-stu-id="10a0d-130">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-131">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="10a0d-131">-AadClientSecret</span></span>
<span data-ttu-id="10a0d-132">Gibt den Client Schlüssel der Azure AD-Anwendung an, die über die Berechtigung zum Schreiben von Geheimnissen in **keyvault** verfügt.</span><span class="sxs-lookup"><span data-stu-id="10a0d-132">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: AADClientSecretParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a0d-133">-DefaultProfile</span></span>
<span data-ttu-id="10a0d-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="10a0d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10a0d-135">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="10a0d-135">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="10a0d-136">Gibt an, dass dieses Cmdlet die automatische Aktualisierung der Nebenversion der Erweiterung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="10a0d-136">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-137">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="10a0d-137">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="10a0d-138">Gibt die Ressourcen-ID des **keyvaults** an, auf den die Verschlüsselungsschlüssel des virtuellen Computers hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="10a0d-138">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-139">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="10a0d-139">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="10a0d-140">Gibt die **keyvault** -URL an, auf die die Verschlüsselungsschlüssel des virtuellen Computers hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="10a0d-140">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-141">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="10a0d-141">-EncryptFormatAll</span></span>
<span data-ttu-id="10a0d-142">Encrypt-Format aller Datenlaufwerke, die noch nicht verschlüsselt sind</span><span class="sxs-lookup"><span data-stu-id="10a0d-142">Encrypt-Format all data drives that are not already encrypted</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-143">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="10a0d-143">-ExtensionPublisherName</span></span>
<span data-ttu-id="10a0d-144">Der Name des Erweiterungs Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="10a0d-144">The extension publisher name.</span></span> <span data-ttu-id="10a0d-145">Geben Sie diesen Parameter nur an, um den Standardwert "Microsoft. Azure. Security" zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="10a0d-145">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-146">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="10a0d-146">-ExtensionType</span></span>
<span data-ttu-id="10a0d-147">Der Erweiterungstyp.</span><span class="sxs-lookup"><span data-stu-id="10a0d-147">The extension type.</span></span> <span data-ttu-id="10a0d-148">Geben Sie diesen Parameter an, um den Standardwert "AzureDiskEncryption" für Windows-VMS und "AzureDiskEncryptionForLinux" für Linux-VMs zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="10a0d-148">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-149">-Force</span><span class="sxs-lookup"><span data-stu-id="10a0d-149">-Force</span></span>
<span data-ttu-id="10a0d-150">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="10a0d-150">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-151">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="10a0d-151">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="10a0d-152">Gibt den Algorithmus an, der zum Umbrechen des Schlüssel Verschlüsselungsschlüssels des virtuellen Computers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="10a0d-152">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="10a0d-153">Der Standardwert ist RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="10a0d-153">The default value is RSA-OAEP.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-154">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="10a0d-154">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="10a0d-155">Gibt die URL des Schlüssel Verschlüsselungsschlüssels an, der zum Umbrechen des Verschlüsselungsschlüssels für den virtuellen Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="10a0d-155">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="10a0d-156">Dies muss die Vollversion der URL sein.</span><span class="sxs-lookup"><span data-stu-id="10a0d-156">This must be the full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-157">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="10a0d-157">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="10a0d-158">Gibt die Ressourcen-ID des **keyvault** -Schlüssels an, der den Schlüssel Verschlüsselungsschlüssel enthält, der zum Umbrechen des Verschlüsselungsschlüssels für den virtuellen Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="10a0d-158">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="10a0d-159">Hierbei muss es sich um eine Vollversion-URL handeln.</span><span class="sxs-lookup"><span data-stu-id="10a0d-159">This must be a full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-160">-Name</span><span class="sxs-lookup"><span data-stu-id="10a0d-160">-Name</span></span>
<span data-ttu-id="10a0d-161">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="10a0d-161">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="10a0d-162">Der Standardwert ist AzureDiskEncryption für virtuelle Computer, auf denen das Windows-Betriebssystem oder AzureDiskEncryptionForLinux für Linux-virtuelle Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="10a0d-162">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-163">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="10a0d-163">-Passphrase</span></span>
<span data-ttu-id="10a0d-164">Gibt die für die Verschlüsselung von virtuellen Linux-Computern verwendete Passphrase an.</span><span class="sxs-lookup"><span data-stu-id="10a0d-164">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="10a0d-165">Dieser Parameter wird nicht für virtuelle Computer verwendet, auf denen das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="10a0d-165">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10a0d-166">-ResourceGroupName</span></span>
<span data-ttu-id="10a0d-167">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="10a0d-167">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-168">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="10a0d-168">-SequenceVersion</span></span>
<span data-ttu-id="10a0d-169">Gibt die Sequenznummer der Verschlüsselungsvorgänge für einen virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="10a0d-169">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="10a0d-170">Dies ist pro Verschlüsselungsvorgang, der auf demselben virtuellen Computer ausgeführt wird, eindeutig.</span><span class="sxs-lookup"><span data-stu-id="10a0d-170">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="10a0d-171">Das Get-AzureRmVMExtension-Cmdlet kann verwendet werden, um die zuvor verwendete Sequenznummer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="10a0d-171">The Get-AzureRmVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-172">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="10a0d-172">-SkipVmBackup</span></span>
<span data-ttu-id="10a0d-173">Überspringen der Erstellung von Sicherungen für Linux-VMs</span><span class="sxs-lookup"><span data-stu-id="10a0d-173">Skip backup creation for Linux VMs</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-174">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="10a0d-174">-TypeHandlerVersion</span></span>
<span data-ttu-id="10a0d-175">Gibt die Version der Verschlüsselungs Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="10a0d-175">Specifies the version of the encryption extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-176">-VMName</span><span class="sxs-lookup"><span data-stu-id="10a0d-176">-VMName</span></span>
<span data-ttu-id="10a0d-177">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="10a0d-177">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-178">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="10a0d-178">-VolumeType</span></span>
<span data-ttu-id="10a0d-179">Gibt den Typ der virtuellen Maschinen-Volumes an, um den Verschlüsselungsvorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="10a0d-179">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="10a0d-180">Zulässige Werte für virtuelle Computer, die das Windows-Betriebssystem ausführen, sind wie folgt: alle, das Betriebssystem und die Daten.</span><span class="sxs-lookup"><span data-stu-id="10a0d-180">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="10a0d-181">Die zulässigen Werte für virtuelle Linux-Computer lauten wie folgt: nur Daten.</span><span class="sxs-lookup"><span data-stu-id="10a0d-181">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a0d-182">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="10a0d-182">-Confirm</span></span>
<span data-ttu-id="10a0d-183">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="10a0d-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10a0d-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10a0d-184">-WhatIf</span></span>
<span data-ttu-id="10a0d-185">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="10a0d-185">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="10a0d-186">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="10a0d-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10a0d-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a0d-187">CommonParameters</span></span>
<span data-ttu-id="10a0d-188">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10a0d-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a0d-189">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10a0d-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a0d-190">Eingaben</span><span class="sxs-lookup"><span data-stu-id="10a0d-190">INPUTS</span></span>

### <span data-ttu-id="10a0d-191">Keine</span><span class="sxs-lookup"><span data-stu-id="10a0d-191">None</span></span>
<span data-ttu-id="10a0d-192">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="10a0d-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="10a0d-193">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="10a0d-193">OUTPUTS</span></span>

### <span data-ttu-id="10a0d-194">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="10a0d-194">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="10a0d-195">Notizen</span><span class="sxs-lookup"><span data-stu-id="10a0d-195">NOTES</span></span>

## <span data-ttu-id="10a0d-196">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="10a0d-196">RELATED LINKS</span></span>

[<span data-ttu-id="10a0d-197">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="10a0d-197">Add-AzureRmVMSecret</span></span>](./Add-AzureRmVMSecret.md)

[<span data-ttu-id="10a0d-198">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="10a0d-198">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="10a0d-199">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="10a0d-199">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)


