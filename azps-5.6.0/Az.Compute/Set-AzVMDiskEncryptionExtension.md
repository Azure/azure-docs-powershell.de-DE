---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: d24344392682e04f2eecc34f491e6048ca543d4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921376"
---
# <span data-ttu-id="927d9-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="927d9-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="927d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="927d9-102">SYNOPSIS</span></span>
<span data-ttu-id="927d9-103">Aktiviert die Verschlüsselung auf einem ausgeführten virtuellen IaaS-Computer in Azure.</span><span class="sxs-lookup"><span data-stu-id="927d9-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="927d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="927d9-104">SYNTAX</span></span>

### <span data-ttu-id="927d9-105">SinglePassParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="927d9-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="927d9-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="927d9-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="927d9-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="927d9-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="927d9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="927d9-108">DESCRIPTION</span></span>
<span data-ttu-id="927d9-109">Das **Cmdlet Set-AzVMDiskEncryptionExtension** ermöglicht die Verschlüsselung auf einer ausgeführten Infrastruktur als Dienstcomputer (IaaS) in Azure.</span><span class="sxs-lookup"><span data-stu-id="927d9-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>  <span data-ttu-id="927d9-110">Die Verschlüsselung wird durch Installieren der Datenträgerverschlüsselungserweiterung auf dem virtuellen Computer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="927d9-110">It enables encryption by installing the disk encryption extension on the virtual machine.</span></span> 

<span data-ttu-id="927d9-111">Für dieses Cmdlet ist eine Bestätigung durch die Benutzer erforderlich, da einer der Schritte zum Aktivieren der Verschlüsselung einen Neustart des virtuellen Computers erfordert.</span><span class="sxs-lookup"><span data-stu-id="927d9-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>

<span data-ttu-id="927d9-112">Es wird empfohlen, Ihre Arbeit auf dem virtuellen Computer zu speichern, bevor Sie dieses Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="927d9-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

<span data-ttu-id="927d9-113">Linux: Der **Parameter VolumeType** ist beim Verschlüsseln virtueller Linux-Computer erforderlich und muss auf einen Wert ("Os", "Data" oder "All") festgelegt werden, der von der Linux-Verteilung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="927d9-113">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="927d9-114">Windows: Der **Parameter VolumeType** wird möglicherweise nicht angegeben, in diesem Fall ist der Vorgang standardmäßig auf "Alle" festgelegt. Wenn der Parameter VolumeType für einen virtuellen Windows-Computer vorhanden ist, muss er entweder auf "Alle" oder "Betriebssystem" festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="927d9-114">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

## <span data-ttu-id="927d9-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="927d9-115">EXAMPLES</span></span>

### <span data-ttu-id="927d9-116">Beispiel 1: Aktivieren der Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="927d9-116">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="927d9-117">In diesem Beispiel wird die Verschlüsselung auf einer VM ohne Angabe von AD-Anmeldeinformationen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="927d9-117">This example enables encryption on a VM without specifying AD credentials.</span></span>

### <span data-ttu-id="927d9-118">Beispiel 2: Aktivieren der Verschlüsselung mit Pipelineeingabe</span><span class="sxs-lookup"><span data-stu-id="927d9-118">Example 2: Enable encryption with pipelined input</span></span>
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

<span data-ttu-id="927d9-119">In diesem Beispiel werden Parameter mithilfe von Pipelineeingaben zum Aktivieren der Verschlüsselung auf einer VM ohne Angabe von AD-Anmeldeinformationen übermittelt.</span><span class="sxs-lookup"><span data-stu-id="927d9-119">This example sends parameters using pipelined input to enable encryption on a VM, without specifying AD credentials.</span></span>

### <span data-ttu-id="927d9-120">Beispiel 3: Aktivieren der Verschlüsselung mithilfe der Azure AD-Client-ID und des Geheimen Clientschlüssels</span><span class="sxs-lookup"><span data-stu-id="927d9-120">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="927d9-121">In diesem Beispiel werden die Azure AD-Client-ID und der geheime Clientschlüssel verwendet, um die Verschlüsselung auf einer VM zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="927d9-121">This example uses Azure AD client ID and client secret to enable encryption on a VM.</span></span>

### <span data-ttu-id="927d9-122">Beispiel 4: Aktivieren der Verschlüsselung mithilfe der Azure AD-Client-ID und des Fingerabdrucks für die Clientzertifizierung</span><span class="sxs-lookup"><span data-stu-id="927d9-122">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

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
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="927d9-123">In diesem Beispiel werden Azure AD-Client-ID- und Clientzertifizierungsfingerabdrücke verwendet, um die Verschlüsselung auf einer VM zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="927d9-123">This example uses Azure AD client ID and client certification thumbprints to enable encryption on a VM.</span></span>

### <span data-ttu-id="927d9-124">Beispiel 5: Aktivieren der Verschlüsselung mithilfe der Azure AD-Client-ID, des geheimen Clientschlüssels und des Umbruchschlüssels der Datenträgerverschlüsselung mithilfe des Schlüsselverschlüsselungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="927d9-124">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="927d9-125">In diesem Beispiel werden die Azure AD-Client-ID und der geheime Clientschlüssel verwendet, um die Verschlüsselung auf einer VM zu aktivieren, und der Datenträgerverschlüsselungsschlüssel wird mithilfe eines Schlüsselverschlüsselungsschlüssels umschließen.</span><span class="sxs-lookup"><span data-stu-id="927d9-125">This example uses Azure AD client ID and client secret to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

### <span data-ttu-id="927d9-126">Beispiel 6: Aktivieren der Verschlüsselung mit Azure AD-Client-ID, Client-Cert-Fingerabdruck und Umschließen des Datenträgerverschlüsselungsschlüssels mithilfe des Schlüsselverschlüsselungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="927d9-126">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
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
$VolumeType = "All"

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
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="927d9-127">In diesem Beispiel werden azure AD-Client-ID und Client-Cert-Fingerabdruck verwendet, um die Verschlüsselung auf einer VM zu aktivieren, und der Datenträgerverschlüsselungsschlüssel wird mithilfe eines Schlüsselverschlüsselungsschlüssels umschließt.</span><span class="sxs-lookup"><span data-stu-id="927d9-127">This example uses Azure AD client ID and client cert thumbprint to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

## <span data-ttu-id="927d9-128">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="927d9-128">PARAMETERS</span></span>

### <span data-ttu-id="927d9-129">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="927d9-129">-AadClientCertThumbprint</span></span>
<span data-ttu-id="927d9-130">Gibt den Fingerabdruck des AzureActive Directory (Azure AD)-Anwendungsclientzertifikats an, das über Berechtigungen zum Schreiben von Geheiminformationen in **KeyVault verfügt.**</span><span class="sxs-lookup"><span data-stu-id="927d9-130">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="927d9-131">Als Voraussetzung muss das Azure AD-Clientzertifikat zuvor im Zertifikatspeicher des lokalen Computers des virtuellen `my` Computers bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="927d9-131">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="927d9-132">Das Add-AzVMSecret-Cmdlet kann zum Bereitstellen eines Zertifikats auf einem virtuellen Computer in Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="927d9-132">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="927d9-133">Weitere Informationen finden Sie in der Hilfe zum **Add-AzVMSecret-Cmdlet.**</span><span class="sxs-lookup"><span data-stu-id="927d9-133">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="927d9-134">Das Zertifikat muss zuvor auf dem lokalen Computer meines Zertifikatspeichers auf dem virtuellen Computer bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="927d9-134">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

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

### <span data-ttu-id="927d9-135">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="927d9-135">-AadClientID</span></span>
<span data-ttu-id="927d9-136">Gibt die Client-ID der Azure AD-Anwendung an, die über berechtigungen zum Schreiben von Geheimschlüsseln in **KeyVault verfügt.**</span><span class="sxs-lookup"><span data-stu-id="927d9-136">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="927d9-137">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="927d9-137">-AadClientSecret</span></span>
<span data-ttu-id="927d9-138">Gibt den Geheimschlüssel des Clients der Azure AD-Anwendung an, die über berechtigungen zum Schreiben von Geheimnissen in **KeyVault verfügt.**</span><span class="sxs-lookup"><span data-stu-id="927d9-138">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="927d9-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="927d9-139">-DefaultProfile</span></span>
<span data-ttu-id="927d9-140">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="927d9-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="927d9-141">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="927d9-141">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="927d9-142">Gibt an, dass dieses Cmdlet das automatische Upgrade der Nebenversion der Erweiterung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="927d9-142">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="927d9-143">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="927d9-143">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="927d9-144">Gibt die Ressourcen-ID des **KeyVault** an, in den die Verschlüsselungsschlüssel des virtuellen Computers hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="927d9-144">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="927d9-145">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="927d9-145">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="927d9-146">Gibt die **KeyVault-URL** an, in die die Verschlüsselungsschlüssel des virtuellen Computers hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="927d9-146">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="927d9-147">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="927d9-147">-EncryptFormatAll</span></span>
<span data-ttu-id="927d9-148">Encrypt-Format alle Datenlaufwerke, die noch nicht verschlüsselt sind</span><span class="sxs-lookup"><span data-stu-id="927d9-148">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="927d9-149">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="927d9-149">-ExtensionPublisherName</span></span>
<span data-ttu-id="927d9-150">Der Name des Herausgebers der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="927d9-150">The extension publisher name.</span></span> <span data-ttu-id="927d9-151">Geben Sie diesen Parameter nur an, um den Standardwert von "Microsoft.Azure.Security" außer Kraft zu setzen.</span><span class="sxs-lookup"><span data-stu-id="927d9-151">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="927d9-152">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="927d9-152">-ExtensionType</span></span>
<span data-ttu-id="927d9-153">Der Erweiterungstyp.</span><span class="sxs-lookup"><span data-stu-id="927d9-153">The extension type.</span></span> <span data-ttu-id="927d9-154">Geben Sie diesen Parameter an, um den Standardwert von "AzureDiskEncryption" für Windows-VMs und "AzureDiskEncryptionForLinux" für Linux-VMs außer Kraft zu setzen.</span><span class="sxs-lookup"><span data-stu-id="927d9-154">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="927d9-155">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="927d9-155">-Force</span></span>
<span data-ttu-id="927d9-156">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="927d9-156">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="927d9-157">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="927d9-157">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="927d9-158">Gibt den Algorithmus an, der zum Umschließen und Entpacken des Schlüsselverschlüsselungsschlüssels des virtuellen Computers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="927d9-158">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="927d9-159">Der Standardwert ist RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="927d9-159">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="927d9-160">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="927d9-160">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="927d9-161">Gibt die URL des Schlüsselverschlüsselungsschlüssels an, mit dem der Verschlüsselungsschlüssel des virtuellen Computers um- und entpackt wird.</span><span class="sxs-lookup"><span data-stu-id="927d9-161">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="927d9-162">Dies muss die VOLLVERSIONS-URL sein.</span><span class="sxs-lookup"><span data-stu-id="927d9-162">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="927d9-163">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="927d9-163">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="927d9-164">Gibt die Ressourcen-ID des **KeyVault** an, der den Schlüsselverschlüsselungsschlüssel enthält, der zum Umschließen und Entpacken des Verschlüsselungsschlüssels für virtuelle Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="927d9-164">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="927d9-165">Dies muss eine vollversionierte URL sein.</span><span class="sxs-lookup"><span data-stu-id="927d9-165">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="927d9-166">-Name</span><span class="sxs-lookup"><span data-stu-id="927d9-166">-Name</span></span>
<span data-ttu-id="927d9-167">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="927d9-167">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span> <span data-ttu-id="927d9-168">Wenn der *Parameter Name* nicht angegeben wird, heißt die installierte Erweiterung AzureDiskEncryption auf virtuellen Windows-Computern und AzureDiskEncryptionForLinux auf virtuellen Linux-Computern.</span><span class="sxs-lookup"><span data-stu-id="927d9-168">If the *Name* parameter is omitted, the installed extension will be named AzureDiskEncryption on Windows virtual machines and AzureDiskEncryptionForLinux on Linux virtual machines.</span></span>


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

### <span data-ttu-id="927d9-169">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="927d9-169">-Passphrase</span></span>
<span data-ttu-id="927d9-170">Gibt die Passphrase an, die nur zum Verschlüsseln virtueller Linux-Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="927d9-170">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="927d9-171">Dieser Parameter wird nicht für virtuelle Computer verwendet, auf der das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="927d9-171">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="927d9-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="927d9-172">-ResourceGroupName</span></span>
<span data-ttu-id="927d9-173">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="927d9-173">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="927d9-174">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="927d9-174">-SequenceVersion</span></span>
<span data-ttu-id="927d9-175">Gibt die Sequenznummer der Verschlüsselungsvorgänge für einen virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="927d9-175">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="927d9-176">Dies ist für jeden Verschlüsselungsvorgang, der auf demselben virtuellen Computer ausgeführt wird, eindeutig.</span><span class="sxs-lookup"><span data-stu-id="927d9-176">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="927d9-177">Das Get-AzVMExtension-Cmdlet kann zum Abrufen der vorherigen verwendeten Sequenznummer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="927d9-177">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="927d9-178">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="927d9-178">-SkipVmBackup</span></span>
<span data-ttu-id="927d9-179">Überspringen der Sicherungserstellung für Linux-VMs</span><span class="sxs-lookup"><span data-stu-id="927d9-179">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="927d9-180">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="927d9-180">-TypeHandlerVersion</span></span>
<span data-ttu-id="927d9-181">Gibt die Version der Verschlüsselungserweiterung an.</span><span class="sxs-lookup"><span data-stu-id="927d9-181">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="927d9-182">-VMName</span><span class="sxs-lookup"><span data-stu-id="927d9-182">-VMName</span></span>
<span data-ttu-id="927d9-183">Gibt den Namen des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="927d9-183">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="927d9-184">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="927d9-184">-VolumeType</span></span>
<span data-ttu-id="927d9-185">Gibt den Typ der Virtuellen Computervolumes an, auf denen verschlüsselungsvorgang ausgeführt werden soll: Betriebssystem, Daten oder Alle.</span><span class="sxs-lookup"><span data-stu-id="927d9-185">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="927d9-186">Linux: Der **Parameter VolumeType** ist beim Verschlüsseln virtueller Linux-Computer erforderlich und muss auf einen Wert ("Os", "Data" oder "All") festgelegt werden, der von der Linux-Verteilung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="927d9-186">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="927d9-187">Windows: Der **Parameter VolumeType** wird möglicherweise nicht angegeben, in diesem Fall ist der Vorgang standardmäßig auf "Alle" festgelegt. Wenn der Parameter VolumeType für einen virtuellen Windows-Computer vorhanden ist, muss er entweder auf "Alle" oder "Betriebssystem" festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="927d9-187">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

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

### <span data-ttu-id="927d9-188">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="927d9-188">-Confirm</span></span>
<span data-ttu-id="927d9-189">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="927d9-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="927d9-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="927d9-190">-WhatIf</span></span>
<span data-ttu-id="927d9-191">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="927d9-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="927d9-192">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="927d9-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="927d9-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="927d9-193">CommonParameters</span></span>
<span data-ttu-id="927d9-194">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="927d9-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="927d9-195">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="927d9-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="927d9-196">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="927d9-196">INPUTS</span></span>

### <span data-ttu-id="927d9-197">System.String</span><span class="sxs-lookup"><span data-stu-id="927d9-197">System.String</span></span>

### <span data-ttu-id="927d9-198">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="927d9-198">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="927d9-199">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="927d9-199">OUTPUTS</span></span>

### <span data-ttu-id="927d9-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="927d9-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="927d9-201">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="927d9-201">NOTES</span></span>

## <span data-ttu-id="927d9-202">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="927d9-202">RELATED LINKS</span></span>

[<span data-ttu-id="927d9-203">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="927d9-203">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="927d9-204">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="927d9-204">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="927d9-205">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="927d9-205">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


