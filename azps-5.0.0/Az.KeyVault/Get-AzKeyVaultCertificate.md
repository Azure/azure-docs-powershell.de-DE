---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: ede0598162fdecc760f33646c86171501ec46db4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180434"
---
# <span data-ttu-id="b6c08-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b6c08-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="b6c08-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6c08-102">SYNOPSIS</span></span>
<span data-ttu-id="b6c08-103">Ruft ein Zertifikat aus einem schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="b6c08-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="b6c08-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6c08-104">SYNTAX</span></span>

### <span data-ttu-id="b6c08-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b6c08-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6c08-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="b6c08-106">ByCertificateNameAndVersion</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6c08-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="b6c08-107">ByCertificateAllVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6c08-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="b6c08-108">ByNameInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6c08-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="b6c08-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6c08-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="b6c08-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6c08-111">ByNameResourceId</span><span class="sxs-lookup"><span data-stu-id="b6c08-111">ByNameResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6c08-112">ByCertificateNameAndVersionResourceId</span><span class="sxs-lookup"><span data-stu-id="b6c08-112">ByCertificateNameAndVersionResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6c08-113">ByCertificateAllVersionsResourceId</span><span class="sxs-lookup"><span data-stu-id="b6c08-113">ByCertificateAllVersionsResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6c08-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6c08-114">DESCRIPTION</span></span>
<span data-ttu-id="b6c08-115">Das Cmdlet " **Get-AzKeyVaultCertificate** " Ruft das angegebene Zertifikat oder die Versionen eines Zertifikats aus einem schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="b6c08-115">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="b6c08-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6c08-116">EXAMPLES</span></span>

### <span data-ttu-id="b6c08-117">Beispiel 1: Abrufen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="b6c08-117">Example 1: Get a certificate</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId       : https://contoso.vault.azure.net:443/keys/TestCert01/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
SecretId    : https://contoso.vault.azure.net:443/secrets/TestCert01/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

### <span data-ttu-id="b6c08-118">Beispiel 2: Abrufen von CERT und speichern als PFX</span><span class="sxs-lookup"><span data-stu-id="b6c08-118">Example 2: Get cert and save it as pfx</span></span>
<span data-ttu-id="b6c08-119">Dieser Befehl ruft das Zertifikat mit dem Namen TestCert01 aus dem schlüsseltresor mit dem Namen ContosoKV01 ab.</span><span class="sxs-lookup"><span data-stu-id="b6c08-119">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span> <span data-ttu-id="b6c08-120">Führen Sie den folgenden Befehl aus, um das Zertifikat als PFX-Datei herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="b6c08-120">To download the certificate as pfx file, run following command.</span></span> <span data-ttu-id="b6c08-121">Diese Befehle greifen auf die Verschlüsselung zu und speichern dann den Inhalt als PFX-Datei.</span><span class="sxs-lookup"><span data-stu-id="b6c08-121">These commands access SecretId and then save the content as a pfx file.</span></span>

```powershell
$cert = Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
$secret = Get-AzKeyVaultSecret -VaultName $vaultName -Name $cert.Name
$secretValueText = '';
$ssPtr = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue)
try {
    $secretValueText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR($ssPtr)
} finally {
    [System.Runtime.InteropServices.Marshal]::ZeroFreeBSTR($ssPtr)
}
$secretByte = [Convert]::FromBase64String($secretValueText)
$x509Cert = new-object System.Security.Cryptography.X509Certificates.X509Certificate2
$x509Cert.Import($secretByte, "", "Exportable,PersistKeySet")
$type = [System.Security.Cryptography.X509Certificates.X509ContentType]::Pfx
$pfxFileByte = $x509Cert.Export($type, $password)

# Write to a file
[System.IO.File]::WriteAllBytes("KeyVault.pfx", $pfxFileByte)
```

### <span data-ttu-id="b6c08-122">Beispiel 3: Abrufen aller Zertifikate, die gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurden.</span><span class="sxs-lookup"><span data-stu-id="b6c08-122">Example 3: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -InRemovedState

DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test1

ScheduledPurgeDate : 8/22/2018 6:10:47 PM
DeletedDate        : 5/24/2018 6:10:47 PM
Enabled            : True
Expires            : 11/24/2018 6:09:44 PM
NotBefore          : 5/24/2018 5:59:44 PM
Created            : 5/24/2018 6:09:44 PM
Updated            : 5/24/2018 6:09:44 PM
Tags               :
VaultName          : contoso
Name               : test2
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test2
```

<span data-ttu-id="b6c08-123">Dieser Befehl ruft alle Zertifikate ab, die zuvor gelöscht, aber nicht bereinigt wurden, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="b6c08-123">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="b6c08-124">Beispiel 4: Ruft das Zertifikat MyCert ab, das gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurde.</span><span class="sxs-lookup"><span data-stu-id="b6c08-124">Example 4: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -Name 'test1' -InRemovedState

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       5/24/2018 10:58:13 AM

                     [Not After]
                       11/24/2018 10:08:13 AM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
SecretId           : https://contoso.vault.azure.net:443/secrets/test1/7fe415d5518240c1a6fce89986b8d334
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Recoverable+Purgeable
ScheduledPurgeDate : 8/22/2018 6:08:32 PM
DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            : 7fe415d5518240c1a6fce89986b8d334
Id                 : https://contoso.vault.azure.net:443/certificates/test1/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="b6c08-125">Dieser Befehl ruft das Zertifikat mit dem Namen "MyCert" ab, das zuvor gelöscht, aber nicht bereinigt wurde, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="b6c08-125">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="b6c08-126">Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum dieses gelöschten Zertifikats zurück.</span><span class="sxs-lookup"><span data-stu-id="b6c08-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

### <span data-ttu-id="b6c08-127">Beispiel 5: Auflisten von Zertifikaten mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="b6c08-127">Example 5: List certificates using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "test*"

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test1
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test1

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test2
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test2

This command gets all certificates starting with "test" from the key vault named ContosoKV01.
```

## <span data-ttu-id="b6c08-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6c08-128">PARAMETERS</span></span>

### <span data-ttu-id="b6c08-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6c08-129">-DefaultProfile</span></span>
<span data-ttu-id="b6c08-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b6c08-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6c08-131">-IncludePending</span><span class="sxs-lookup"><span data-stu-id="b6c08-131">-IncludePending</span></span>
<span data-ttu-id="b6c08-132">Gibt an, ob ausstehende Zertifikate in die Ausgabe eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b6c08-132">Specifies whether to include pending certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c08-133">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="b6c08-133">-IncludeVersions</span></span>
<span data-ttu-id="b6c08-134">Gibt an, dass dieser Vorgang alle Versionen des Zertifikats abruft.</span><span class="sxs-lookup"><span data-stu-id="b6c08-134">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c08-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b6c08-135">-InputObject</span></span>
<span data-ttu-id="b6c08-136">Keyvault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b6c08-136">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c08-137">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b6c08-137">-InRemovedState</span></span>
<span data-ttu-id="b6c08-138">Gibt an, ob zuvor gelöschte Zertifikate in die Ausgabe eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b6c08-138">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c08-139">-Name</span><span class="sxs-lookup"><span data-stu-id="b6c08-139">-Name</span></span>
<span data-ttu-id="b6c08-140">Gibt den Namen des abzurufenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="b6c08-140">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c08-141">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b6c08-141">-ResourceId</span></span>
<span data-ttu-id="b6c08-142">Keyvault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b6c08-142">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameResourceId, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c08-143">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="b6c08-143">-VaultName</span></span>
<span data-ttu-id="b6c08-144">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="b6c08-144">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c08-145">-Version</span><span class="sxs-lookup"><span data-stu-id="b6c08-145">-Version</span></span>
<span data-ttu-id="b6c08-146">Gibt die Version eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="b6c08-146">Specifies the version of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject, ByCertificateNameAndVersionResourceId
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c08-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6c08-147">CommonParameters</span></span>
<span data-ttu-id="b6c08-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6c08-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6c08-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6c08-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6c08-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6c08-150">INPUTS</span></span>

### <span data-ttu-id="b6c08-151">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b6c08-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="b6c08-152">System. String</span><span class="sxs-lookup"><span data-stu-id="b6c08-152">System.String</span></span>

## <span data-ttu-id="b6c08-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6c08-153">OUTPUTS</span></span>

### <span data-ttu-id="b6c08-154">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b6c08-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

### <span data-ttu-id="b6c08-155">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b6c08-155">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

### <span data-ttu-id="b6c08-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b6c08-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

### <span data-ttu-id="b6c08-157">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b6c08-157">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="b6c08-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6c08-158">NOTES</span></span>

## <span data-ttu-id="b6c08-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6c08-159">RELATED LINKS</span></span>

[<span data-ttu-id="b6c08-160">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b6c08-160">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="b6c08-161">Importieren-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b6c08-161">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="b6c08-162">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b6c08-162">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="b6c08-163">Undo-AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="b6c08-163">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
