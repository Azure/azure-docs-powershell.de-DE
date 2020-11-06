---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: 87b030229eb2a1f4bb91122aaec8a119134d27fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481186"
---
# <span data-ttu-id="36fb1-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="36fb1-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="36fb1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="36fb1-103">Ruft ein Zertifikat aus einem schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="36fb1-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36fb1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36fb1-104">SYNTAX</span></span>

### <span data-ttu-id="36fb1-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="36fb1-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36fb1-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="36fb1-106">ByCertificateNameAndVersion</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36fb1-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="36fb1-107">ByCertificateAllVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36fb1-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="36fb1-108">ByNameInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36fb1-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="36fb1-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36fb1-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="36fb1-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36fb1-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36fb1-111">DESCRIPTION</span></span>
<span data-ttu-id="36fb1-112">Das Cmdlet " **Get-AzureKeyVaultCertificate** " Ruft das angegebene Zertifikat oder die Versionen eines Zertifikats aus einem schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="36fb1-112">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="36fb1-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36fb1-113">EXAMPLES</span></span>

### <span data-ttu-id="36fb1-114">Beispiel 1: Abrufen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="36fb1-114">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="36fb1-115">Dieser Befehl ruft das Zertifikat mit dem Namen TestCert01 aus dem schlüsseltresor mit dem Namen ContosoKV01 ab.</span><span class="sxs-lookup"><span data-stu-id="36fb1-115">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="36fb1-116">Beispiel 2: Abrufen aller Zertifikate, die gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurden.</span><span class="sxs-lookup"><span data-stu-id="36fb1-116">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="36fb1-117">Dieser Befehl ruft alle Zertifikate ab, die zuvor gelöscht, aber nicht bereinigt wurden, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="36fb1-117">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="36fb1-118">Beispiel 3: Ruft das Zertifikat MyCert ab, das gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurde.</span><span class="sxs-lookup"><span data-stu-id="36fb1-118">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="36fb1-119">Dieser Befehl ruft das Zertifikat mit dem Namen "MyCert" ab, das zuvor gelöscht, aber nicht bereinigt wurde, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="36fb1-119">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="36fb1-120">Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum dieses gelöschten Zertifikats zurück.</span><span class="sxs-lookup"><span data-stu-id="36fb1-120">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="36fb1-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="36fb1-121">PARAMETERS</span></span>

### <span data-ttu-id="36fb1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36fb1-122">-DefaultProfile</span></span>
<span data-ttu-id="36fb1-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="36fb1-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36fb1-124">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="36fb1-124">-IncludeVersions</span></span>
<span data-ttu-id="36fb1-125">Gibt an, dass dieser Vorgang alle Versionen des Zertifikats abruft.</span><span class="sxs-lookup"><span data-stu-id="36fb1-125">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36fb1-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="36fb1-126">-InputObject</span></span>
<span data-ttu-id="36fb1-127">Keyvault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="36fb1-127">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36fb1-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="36fb1-128">-InRemovedState</span></span>
<span data-ttu-id="36fb1-129">Gibt an, ob zuvor gelöschte Zertifikate in die Ausgabe eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="36fb1-129">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByName, ByNameInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36fb1-130">-Name</span><span class="sxs-lookup"><span data-stu-id="36fb1-130">-Name</span></span>
<span data-ttu-id="36fb1-131">Gibt den Namen des abzurufenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="36fb1-131">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByNameInputObject
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36fb1-132">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="36fb1-132">-VaultName</span></span>
<span data-ttu-id="36fb1-133">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="36fb1-133">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36fb1-134">-Version</span><span class="sxs-lookup"><span data-stu-id="36fb1-134">-Version</span></span>
<span data-ttu-id="36fb1-135">Gibt die Version eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="36fb1-135">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36fb1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36fb1-136">CommonParameters</span></span>
<span data-ttu-id="36fb1-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36fb1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36fb1-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36fb1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36fb1-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36fb1-139">INPUTS</span></span>

### <span data-ttu-id="36fb1-140">Keine</span><span class="sxs-lookup"><span data-stu-id="36fb1-140">None</span></span>
<span data-ttu-id="36fb1-141">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="36fb1-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="36fb1-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36fb1-142">OUTPUTS</span></span>

### <span data-ttu-id="36fb1-143">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="36fb1-143">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem]</span></span>

### <span data-ttu-id="36fb1-144">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="36fb1-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="36fb1-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="36fb1-145">NOTES</span></span>

## <span data-ttu-id="36fb1-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36fb1-146">RELATED LINKS</span></span>

[<span data-ttu-id="36fb1-147">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="36fb1-147">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="36fb1-148">Importieren-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="36fb1-148">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="36fb1-149">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="36fb1-149">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="36fb1-150">Undo-AzureKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="36fb1-150">Undo-AzureKeyVaultSecretCertificate</span></span>](./Undo-AzureKeyVaultSecretCertificate.md)
