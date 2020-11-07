---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: ed52e229f114666782cb24388db585fd08fa685b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850411"
---
# <span data-ttu-id="54ce0-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="54ce0-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="54ce0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="54ce0-103">Ruft ein Zertifikat aus einem schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="54ce0-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54ce0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54ce0-104">SYNTAX</span></span>

### <span data-ttu-id="54ce0-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="54ce0-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54ce0-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="54ce0-106">ByCertificateName</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54ce0-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="54ce0-107">ByCertificateVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54ce0-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="54ce0-108">ByDeletedCertificates</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54ce0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54ce0-109">DESCRIPTION</span></span>
<span data-ttu-id="54ce0-110">Das Cmdlet " **Get-AzureKeyVaultCertificate** " Ruft das angegebene Zertifikat oder die Versionen eines Zertifikats aus einem schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="54ce0-110">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="54ce0-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54ce0-111">EXAMPLES</span></span>

### <span data-ttu-id="54ce0-112">Beispiel 1: Abrufen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="54ce0-112">Example 1: Get a certificate</span></span>
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

<span data-ttu-id="54ce0-113">Dieser Befehl ruft das Zertifikat mit dem Namen TestCert01 aus dem schlüsseltresor mit dem Namen ContosoKV01 ab.</span><span class="sxs-lookup"><span data-stu-id="54ce0-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="54ce0-114">Beispiel 2: Abrufen aller Zertifikate, die gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurden.</span><span class="sxs-lookup"><span data-stu-id="54ce0-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="54ce0-115">Dieser Befehl ruft alle Zertifikate ab, die zuvor gelöscht, aber nicht bereinigt wurden, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="54ce0-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="54ce0-116">Beispiel 3: Ruft das Zertifikat MyCert ab, das gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurde.</span><span class="sxs-lookup"><span data-stu-id="54ce0-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="54ce0-117">Dieser Befehl ruft das Zertifikat mit dem Namen "MyCert" ab, das zuvor gelöscht, aber nicht bereinigt wurde, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="54ce0-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="54ce0-118">Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum dieses gelöschten Zertifikats zurück.</span><span class="sxs-lookup"><span data-stu-id="54ce0-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="54ce0-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="54ce0-119">PARAMETERS</span></span>

### <span data-ttu-id="54ce0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54ce0-120">-DefaultProfile</span></span>
<span data-ttu-id="54ce0-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="54ce0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54ce0-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="54ce0-122">-IncludeVersions</span></span>
<span data-ttu-id="54ce0-123">Gibt an, dass dieser Vorgang alle Versionen des Zertifikats abruft.</span><span class="sxs-lookup"><span data-stu-id="54ce0-123">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ce0-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="54ce0-124">-InRemovedState</span></span>
<span data-ttu-id="54ce0-125">Gibt an, ob zuvor gelöschte Zertifikate in die Ausgabe eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="54ce0-125">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ce0-126">-Name</span><span class="sxs-lookup"><span data-stu-id="54ce0-126">-Name</span></span>
<span data-ttu-id="54ce0-127">Gibt den Namen des abzurufenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="54ce0-127">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54ce0-128">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="54ce0-128">-VaultName</span></span>
<span data-ttu-id="54ce0-129">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="54ce0-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="54ce0-130">-Version</span><span class="sxs-lookup"><span data-stu-id="54ce0-130">-Version</span></span>
<span data-ttu-id="54ce0-131">Gibt die Version eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="54ce0-131">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54ce0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54ce0-132">CommonParameters</span></span>
<span data-ttu-id="54ce0-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54ce0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54ce0-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54ce0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54ce0-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54ce0-135">INPUTS</span></span>

## <span data-ttu-id="54ce0-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54ce0-136">OUTPUTS</span></span>

### <span data-ttu-id="54ce0-137">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="54ce0-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="54ce0-138">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="54ce0-138">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="54ce0-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="54ce0-139">NOTES</span></span>

## <span data-ttu-id="54ce0-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54ce0-140">RELATED LINKS</span></span>

[<span data-ttu-id="54ce0-141">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="54ce0-141">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="54ce0-142">Importieren-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="54ce0-142">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="54ce0-143">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="54ce0-143">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)


