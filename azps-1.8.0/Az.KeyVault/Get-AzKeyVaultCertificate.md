---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: ccd2762449e24f881a3308c0d11476a1e4626fed
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402404"
---
# <span data-ttu-id="7a214-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7a214-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="7a214-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a214-102">SYNOPSIS</span></span>
<span data-ttu-id="7a214-103">Ruft ein Zertifikat aus einem Schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="7a214-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="7a214-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a214-104">SYNTAX</span></span>

### <span data-ttu-id="7a214-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a214-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a214-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="7a214-106">ByCertificateNameAndVersion</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a214-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="7a214-107">ByCertificateAllVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a214-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="7a214-108">ByNameInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a214-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="7a214-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a214-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="7a214-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a214-111">ByNameResourceId</span><span class="sxs-lookup"><span data-stu-id="7a214-111">ByNameResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a214-112">ByCertificateNameAndVersionResourceId</span><span class="sxs-lookup"><span data-stu-id="7a214-112">ByCertificateNameAndVersionResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a214-113">ByCertificateAllVersionsResourceId</span><span class="sxs-lookup"><span data-stu-id="7a214-113">ByCertificateAllVersionsResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a214-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a214-114">DESCRIPTION</span></span>
<span data-ttu-id="7a214-115">Das **Cmdlet "Get-AzKeyVaultCertificate"** ruft das angegebene Zertifikat oder die Versionen eines Zertifikats aus einem Schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="7a214-115">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="7a214-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7a214-116">EXAMPLES</span></span>

### <span data-ttu-id="7a214-117">Beispiel 1: Erhalten eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="7a214-117">Example 1: Get a certificate</span></span>
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

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="7a214-118">Dieser Befehl ruft das Zertifikat mit dem Namen "TestCert01" aus dem Schlüsseltresor "ContosoKV01" ab.</span><span class="sxs-lookup"><span data-stu-id="7a214-118">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="7a214-119">Beispiel 2: Alle Zertifikate erhalten, die für diesen Schlüsseltresor gelöscht, aber nicht gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="7a214-119">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="7a214-120">Dieser Befehl ruft alle Zertifikate ab, die zuvor gelöscht, aber nicht gelöscht wurden, im Schlüsseltresor namens Contoso.</span><span class="sxs-lookup"><span data-stu-id="7a214-120">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="7a214-121">Beispiel 3: Ruft das Zertifikat "MyCert" ab, das gelöscht, aber nicht für diesen Schlüsseltresor gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="7a214-121">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="7a214-122">Dieser Befehl ruft das Zertifikat mit dem Namen "MyCert" ab, das im Schlüsseltresor "Contoso" bereits gelöscht, aber nicht gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="7a214-122">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="7a214-123">Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum dieses gelöschten Zertifikats zurück.</span><span class="sxs-lookup"><span data-stu-id="7a214-123">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

### <span data-ttu-id="7a214-124">Beispiel 4: Auflisten von Zertifikaten mithilfe der Filterung</span><span class="sxs-lookup"><span data-stu-id="7a214-124">Example 4: List certificates using filtering</span></span>
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

## <span data-ttu-id="7a214-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a214-125">PARAMETERS</span></span>

### <span data-ttu-id="7a214-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a214-126">-DefaultProfile</span></span>
<span data-ttu-id="7a214-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7a214-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a214-128">-IncludePending</span><span class="sxs-lookup"><span data-stu-id="7a214-128">-IncludePending</span></span>
<span data-ttu-id="7a214-129">Gibt an, ob ausstehende Zertifikate in die Ausgabe</span><span class="sxs-lookup"><span data-stu-id="7a214-129">Specifies whether to include pending certificates in the output</span></span>

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

### <span data-ttu-id="7a214-130">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="7a214-130">-IncludeVersions</span></span>
<span data-ttu-id="7a214-131">Gibt an, dass dieser Vorgang alle Versionen des Zertifikats erhält.</span><span class="sxs-lookup"><span data-stu-id="7a214-131">Indicates that this operation gets all versions of the certificate.</span></span>

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

### <span data-ttu-id="7a214-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a214-132">-InputObject</span></span>
<span data-ttu-id="7a214-133">KeyVault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7a214-133">KeyVault object.</span></span>

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

### <span data-ttu-id="7a214-134">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="7a214-134">-InRemovedState</span></span>
<span data-ttu-id="7a214-135">Gibt an, ob zuvor gelöschte Zertifikate in die Ausgabe enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="7a214-135">Specifies whether to include previously deleted certificates in the output</span></span>

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

### <span data-ttu-id="7a214-136">-Name</span><span class="sxs-lookup"><span data-stu-id="7a214-136">-Name</span></span>
<span data-ttu-id="7a214-137">Gibt den Namen des zu erhaltenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="7a214-137">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="7a214-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a214-138">-ResourceId</span></span>
<span data-ttu-id="7a214-139">KeyVault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7a214-139">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="7a214-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7a214-140">-VaultName</span></span>
<span data-ttu-id="7a214-141">Gibt den Namen eines Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="7a214-141">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="7a214-142">-Version</span><span class="sxs-lookup"><span data-stu-id="7a214-142">-Version</span></span>
<span data-ttu-id="7a214-143">Gibt die Version eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="7a214-143">Specifies the version of a certificate.</span></span>

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

### <span data-ttu-id="7a214-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a214-144">CommonParameters</span></span>
<span data-ttu-id="7a214-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a214-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a214-146">Weitere Informationen finden Sie unter [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a214-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a214-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7a214-147">INPUTS</span></span>

### <span data-ttu-id="7a214-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="7a214-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="7a214-149">System.String</span><span class="sxs-lookup"><span data-stu-id="7a214-149">System.String</span></span>

## <span data-ttu-id="7a214-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7a214-150">OUTPUTS</span></span>

### <span data-ttu-id="7a214-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7a214-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

### <span data-ttu-id="7a214-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7a214-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

### <span data-ttu-id="7a214-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7a214-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

### <span data-ttu-id="7a214-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7a214-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="7a214-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7a214-155">NOTES</span></span>

## <span data-ttu-id="7a214-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7a214-156">RELATED LINKS</span></span>

[<span data-ttu-id="7a214-157">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7a214-157">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="7a214-158">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7a214-158">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="7a214-159">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7a214-159">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

