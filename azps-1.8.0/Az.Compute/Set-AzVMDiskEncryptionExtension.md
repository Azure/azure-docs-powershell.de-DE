---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: da50845ff5012d466eed0c68103cdbd0baea4e7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820539"
---
# <span data-ttu-id="6bc31-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="6bc31-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="6bc31-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6bc31-102">SYNOPSIS</span></span>
<span data-ttu-id="6bc31-103">Aktiviert die Verschlüsselung auf einem ausgeführten IaaS-virtuellen Computer in Azure.</span><span class="sxs-lookup"><span data-stu-id="6bc31-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="6bc31-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bc31-104">SYNTAX</span></span>

### <span data-ttu-id="6bc31-105">SinglePassParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6bc31-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bc31-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bc31-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bc31-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bc31-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bc31-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6bc31-108">DESCRIPTION</span></span>
<span data-ttu-id="6bc31-109">Das Cmdlet " **Satz-AzVMDiskEncryptionExtension** " ermöglicht die Verschlüsselung auf einer ausgeführten Infrastruktur als IaaS-virtueller Computer in Azure.</span><span class="sxs-lookup"><span data-stu-id="6bc31-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="6bc31-110">Dieses Cmdlet ermöglicht die Verschlüsselung, indem die Datenträger Verschlüsselungs Erweiterung auf dem virtuellen Computer installiert wird.</span><span class="sxs-lookup"><span data-stu-id="6bc31-110">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="6bc31-111">Wenn kein *Name* -Parameter angegeben ist, wird eine Erweiterung mit dem Standardnamen AzureDiskEncryption für virtuelle Computer installiert, auf denen das Windows-Betriebssystem oder AzureDiskEncryptionForLinux für Linux-Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6bc31-111">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="6bc31-112">Dieses Cmdlet erfordert eine Bestätigung der Benutzer als einer der Schritte zum Aktivieren der Verschlüsselung erfordert einen Neustart des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="6bc31-112">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="6bc31-113">Es wird empfohlen, dass Sie Ihre Arbeit auf dem virtuellen Computer speichern, bevor Sie dieses Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6bc31-113">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="6bc31-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6bc31-114">EXAMPLES</span></span>

### <span data-ttu-id="6bc31-115">Beispiel 1: Aktivieren der Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="6bc31-115">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="6bc31-116">In diesem Beispiel wird das Aktivieren der Verschlüsselung ohne Angabe von anzeigen Anmeldeinformationen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6bc31-116">This example demonstrates enabling encryption without specifying AD credentials.</span></span>   

### <span data-ttu-id="6bc31-117">Beispiel 2: Aktivieren der Verschlüsselung mit Pipelined Input</span><span class="sxs-lookup"><span data-stu-id="6bc31-117">Example 2: Enable encryption with pipelined input</span></span>
```
$params = New-Object PSObject -Property @{
    ResourceGroupName = "[resource-group-name]"
    VMName = "[vm-name]"
    DiskEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    DiskEncryptionKeyVaultUrl = "https://[keyvault-name].vault.azure.net"
    KeyEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    KeyEncryptionKeyUrl = "https://[keyvault-name].vault.azure.net/keys/[kekname]/[kek-unique-id]"
    VolumeType = "All"
}

$params | Set-AzVmDiskEncryptionExtension
```

<span data-ttu-id="6bc31-118">In diesem Beispiel wird das Senden von Parametern mithilfe von Pipelined Input zum Aktivieren der Verschlüsselung ohne Angabe von anzeigen Anmeldeinformationen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6bc31-118">This example demonstrates sending parameters using pipelined input to enable encryption without specifying AD credentials.</span></span>  

### <span data-ttu-id="6bc31-119">Beispiel 3: Aktivieren der Verschlüsselung mithilfe der Azure AD-Client-ID und des Client Geheimnisses</span><span class="sxs-lookup"><span data-stu-id="6bc31-119">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="6bc31-120">In diesem Beispiel wird die Verschlüsselung mithilfe der Azure AD-Client-ID und des Client Geheimnisses aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6bc31-120">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="6bc31-121">Beispiel 4: Aktivieren der Verschlüsselung mithilfe der Azure AD-Client-ID und des Fingerabdrucks der Client Zertifizierung</span><span class="sxs-lookup"><span data-stu-id="6bc31-121">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue 
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="6bc31-122">In diesem Beispiel wird die Verschlüsselung mithilfe der Azure AD-Client-ID und der Client Zertifizierungs Fingerabdrücke aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6bc31-122">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="6bc31-123">Beispiel 5: Aktivieren der Verschlüsselung mit Azure AD-Client-ID, Client Secret und Umbrechen des Datenträger Verschlüsselungsschlüssels mithilfe des Schlüssel Verschlüsselungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="6bc31-123">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="6bc31-124">In diesem Beispiel wird die Verschlüsselung mithilfe von Azure AD-Client-ID, Client Secret und Umbrechen des Datenträger Verschlüsselungsschlüssels mithilfe des Schlüssel Verschlüsselungsschlüssels aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6bc31-124">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="6bc31-125">Beispiel 6: Aktivieren der Verschlüsselung mithilfe der Azure AD-Client-ID, des clientcert-Fingerabdrucks und umbrechen der Datenträger EncryptionKey mithilfe des Schlüssel Verschlüsselungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="6bc31-125">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="6bc31-126">In diesem Beispiel wird die Verschlüsselung mithilfe von Azure AD-Client-ID, Client CERT-Fingerabdruck und Umbrechen des Datenträger Verschlüsselungsschlüssels mithilfe des Schlüssel Verschlüsselungsschlüssels aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6bc31-126">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="6bc31-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="6bc31-127">PARAMETERS</span></span>

### <span data-ttu-id="6bc31-128">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="6bc31-128">-AadClientCertThumbprint</span></span>
<span data-ttu-id="6bc31-129">Gibt den Fingerabdruck des AzureActive Directory (Azure AD)-Anwendungsclient Zertifikats an, das über die Berechtigungen zum Schreiben von Geheimnissen in **keyvault** verfügt.</span><span class="sxs-lookup"><span data-stu-id="6bc31-129">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="6bc31-130">Voraussetzung ist, dass das Azure AD-Clientzertifikat zuvor auf dem lokalen Computerzertifikatspeicher des virtuellen Computers bereitgestellt werden muss `my` .</span><span class="sxs-lookup"><span data-stu-id="6bc31-130">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="6bc31-131">Mithilfe des Add-AzVMSecret-Cmdlets kann ein Zertifikat für einen virtuellen Computer in Azure bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6bc31-131">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="6bc31-132">Weitere Informationen finden Sie in der Hilfe zum Cmdlet **Add-AzVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="6bc31-132">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="6bc31-133">Das Zertifikat muss zuvor auf dem lokalen Computer meines Zertifikatsspeichers auf dem virtuellen Computer bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6bc31-133">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientCertParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-134">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="6bc31-134">-AadClientID</span></span>
<span data-ttu-id="6bc31-135">Gibt die Client-ID der Azure AD-Anwendung an, die über die Berechtigung zum Schreiben von Geheimnissen in **keyvault** verfügt.</span><span class="sxs-lookup"><span data-stu-id="6bc31-135">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet, AADClientCertParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-136">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="6bc31-136">-AadClientSecret</span></span>
<span data-ttu-id="6bc31-137">Gibt den Client Schlüssel der Azure AD-Anwendung an, die über die Berechtigung zum Schreiben von Geheimnissen in **keyvault** verfügt.</span><span class="sxs-lookup"><span data-stu-id="6bc31-137">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bc31-138">-DefaultProfile</span></span>
<span data-ttu-id="6bc31-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6bc31-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bc31-140">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="6bc31-140">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="6bc31-141">Gibt an, dass dieses Cmdlet die automatische Aktualisierung der Nebenversion der Erweiterung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6bc31-141">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-142">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="6bc31-142">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="6bc31-143">Gibt die Ressourcen-ID des **keyvaults** an, auf den die Verschlüsselungsschlüssel des virtuellen Computers hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6bc31-143">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-144">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="6bc31-144">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="6bc31-145">Gibt die **keyvault** -URL an, auf die die Verschlüsselungsschlüssel des virtuellen Computers hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6bc31-145">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-146">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="6bc31-146">-EncryptFormatAll</span></span>
<span data-ttu-id="6bc31-147">Encrypt-Format aller Datenlaufwerke, die noch nicht verschlüsselt sind</span><span class="sxs-lookup"><span data-stu-id="6bc31-147">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="6bc31-148">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="6bc31-148">-ExtensionPublisherName</span></span>
<span data-ttu-id="6bc31-149">Der Name des Erweiterungs Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="6bc31-149">The extension publisher name.</span></span> <span data-ttu-id="6bc31-150">Geben Sie diesen Parameter nur an, um den Standardwert "Microsoft. Azure. Security" zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="6bc31-150">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-151">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="6bc31-151">-ExtensionType</span></span>
<span data-ttu-id="6bc31-152">Der Erweiterungstyp.</span><span class="sxs-lookup"><span data-stu-id="6bc31-152">The extension type.</span></span> <span data-ttu-id="6bc31-153">Geben Sie diesen Parameter an, um den Standardwert "AzureDiskEncryption" für Windows-VMS und "AzureDiskEncryptionForLinux" für Linux-VMs zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="6bc31-153">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-154">-Force</span><span class="sxs-lookup"><span data-stu-id="6bc31-154">-Force</span></span>
<span data-ttu-id="6bc31-155">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="6bc31-155">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6bc31-156">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="6bc31-156">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="6bc31-157">Gibt den Algorithmus an, der zum Umbrechen des Schlüssel Verschlüsselungsschlüssels des virtuellen Computers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6bc31-157">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="6bc31-158">Der Standardwert ist RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="6bc31-158">The default value is RSA-OAEP.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-159">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="6bc31-159">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="6bc31-160">Gibt die URL des Schlüssel Verschlüsselungsschlüssels an, der zum Umbrechen des Verschlüsselungsschlüssels für den virtuellen Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6bc31-160">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="6bc31-161">Dies muss die Vollversion der URL sein.</span><span class="sxs-lookup"><span data-stu-id="6bc31-161">This must be the full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-162">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="6bc31-162">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="6bc31-163">Gibt die Ressourcen-ID des **keyvault** -Schlüssels an, der den Schlüssel Verschlüsselungsschlüssel enthält, der zum Umbrechen des Verschlüsselungsschlüssels für den virtuellen Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6bc31-163">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="6bc31-164">Hierbei muss es sich um eine Vollversion-URL handeln.</span><span class="sxs-lookup"><span data-stu-id="6bc31-164">This must be a full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-165">-Name</span><span class="sxs-lookup"><span data-stu-id="6bc31-165">-Name</span></span>
<span data-ttu-id="6bc31-166">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="6bc31-166">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="6bc31-167">Der Standardwert ist AzureDiskEncryption für virtuelle Computer, auf denen das Windows-Betriebssystem oder AzureDiskEncryptionForLinux für Linux-virtuelle Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6bc31-167">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-168">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="6bc31-168">-Passphrase</span></span>
<span data-ttu-id="6bc31-169">Gibt die für die Verschlüsselung von virtuellen Linux-Computern verwendete Passphrase an.</span><span class="sxs-lookup"><span data-stu-id="6bc31-169">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="6bc31-170">Dieser Parameter wird nicht für virtuelle Computer verwendet, auf denen das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6bc31-170">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bc31-171">-ResourceGroupName</span></span>
<span data-ttu-id="6bc31-172">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="6bc31-172">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-173">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="6bc31-173">-SequenceVersion</span></span>
<span data-ttu-id="6bc31-174">Gibt die Sequenznummer der Verschlüsselungsvorgänge für einen virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="6bc31-174">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="6bc31-175">Dies ist pro Verschlüsselungsvorgang, der auf demselben virtuellen Computer ausgeführt wird, eindeutig.</span><span class="sxs-lookup"><span data-stu-id="6bc31-175">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="6bc31-176">Das Get-AzVMExtension-Cmdlet kann verwendet werden, um die zuvor verwendete Sequenznummer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6bc31-176">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-177">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="6bc31-177">-SkipVmBackup</span></span>
<span data-ttu-id="6bc31-178">Überspringen der Erstellung von Sicherungen für Linux-VMs</span><span class="sxs-lookup"><span data-stu-id="6bc31-178">Skip backup creation for Linux VMs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-179">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="6bc31-179">-TypeHandlerVersion</span></span>
<span data-ttu-id="6bc31-180">Gibt die Version der Verschlüsselungs Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="6bc31-180">Specifies the version of the encryption extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-181">-VMName</span><span class="sxs-lookup"><span data-stu-id="6bc31-181">-VMName</span></span>
<span data-ttu-id="6bc31-182">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="6bc31-182">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-183">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="6bc31-183">-VolumeType</span></span>
<span data-ttu-id="6bc31-184">Gibt den Typ der virtuellen Maschinen-Volumes an, um den Verschlüsselungsvorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6bc31-184">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="6bc31-185">Zulässige Werte für virtuelle Computer, die das Windows-Betriebssystem ausführen, sind wie folgt: alle, das Betriebssystem und die Daten.</span><span class="sxs-lookup"><span data-stu-id="6bc31-185">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="6bc31-186">Die zulässigen Werte für virtuelle Linux-Computer lauten wie folgt: nur Daten.</span><span class="sxs-lookup"><span data-stu-id="6bc31-186">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc31-187">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6bc31-187">-Confirm</span></span>
<span data-ttu-id="6bc31-188">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6bc31-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bc31-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bc31-189">-WhatIf</span></span>
<span data-ttu-id="6bc31-190">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6bc31-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bc31-191">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6bc31-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bc31-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bc31-192">CommonParameters</span></span>
<span data-ttu-id="6bc31-193">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bc31-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bc31-194">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bc31-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bc31-195">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6bc31-195">INPUTS</span></span>

### <span data-ttu-id="6bc31-196">System. String</span><span class="sxs-lookup"><span data-stu-id="6bc31-196">System.String</span></span>

### <span data-ttu-id="6bc31-197">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="6bc31-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6bc31-198">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6bc31-198">OUTPUTS</span></span>

### <span data-ttu-id="6bc31-199">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6bc31-199">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6bc31-200">Notizen</span><span class="sxs-lookup"><span data-stu-id="6bc31-200">NOTES</span></span>

## <span data-ttu-id="6bc31-201">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6bc31-201">RELATED LINKS</span></span>

[<span data-ttu-id="6bc31-202">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="6bc31-202">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="6bc31-203">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="6bc31-203">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="6bc31-204">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="6bc31-204">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


