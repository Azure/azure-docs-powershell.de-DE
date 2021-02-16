---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: babd3d8a42ddbd740c8189a41de76c78170ecae5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398817"
---
# <span data-ttu-id="4d102-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4d102-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="4d102-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d102-102">SYNOPSIS</span></span>
<span data-ttu-id="4d102-103">Ruft ein Zertifikat aus einem Schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="4d102-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="4d102-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d102-104">SYNTAX</span></span>

### <span data-ttu-id="4d102-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4d102-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d102-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="4d102-106">ByCertificateName</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d102-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="4d102-107">ByCertificateVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d102-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="4d102-108">ByDeletedCertificates</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d102-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d102-109">DESCRIPTION</span></span>
<span data-ttu-id="4d102-110">Das **Cmdlet "Get-AzKeyVaultCertificate"** ruft das angegebene Zertifikat oder die Versionen eines Zertifikats aus einem Schlüsseltresor im Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="4d102-110">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="4d102-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4d102-111">EXAMPLES</span></span>

### <span data-ttu-id="4d102-112">Beispiel 1: Erhalten eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="4d102-112">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="4d102-113">Dieser Befehl ruft das Zertifikat mit dem Namen "TestCert01" aus dem Schlüsseltresor "ContosoKV01" ab.</span><span class="sxs-lookup"><span data-stu-id="4d102-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="4d102-114">Beispiel 2: Alle Zertifikate erhalten, die für diesen Schlüsseltresor gelöscht, aber nicht gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="4d102-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="4d102-115">Dieser Befehl ruft alle Zertifikate ab, die zuvor gelöscht, aber nicht gelöscht wurden, im Schlüsseltresor namens Contoso.</span><span class="sxs-lookup"><span data-stu-id="4d102-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="4d102-116">Beispiel 3: Ruft das Zertifikat "MyCert" ab, das gelöscht, aber nicht für diesen Schlüsseltresor gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="4d102-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="4d102-117">Dieser Befehl ruft das Zertifikat mit dem Namen "MyCert" ab, das im Schlüsseltresor "Contoso" bereits gelöscht, aber nicht gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="4d102-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="4d102-118">Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum dieses gelöschten Zertifikats zurück.</span><span class="sxs-lookup"><span data-stu-id="4d102-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="4d102-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d102-119">PARAMETERS</span></span>

### <span data-ttu-id="4d102-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d102-120">-DefaultProfile</span></span>
<span data-ttu-id="4d102-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4d102-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d102-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="4d102-122">-IncludeVersions</span></span>
<span data-ttu-id="4d102-123">Gibt an, dass dieser Vorgang alle Versionen des Zertifikats erhält.</span><span class="sxs-lookup"><span data-stu-id="4d102-123">Indicates that this operation gets all versions of the certificate.</span></span>

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

### <span data-ttu-id="4d102-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="4d102-124">-InRemovedState</span></span>
<span data-ttu-id="4d102-125">Gibt an, ob zuvor gelöschte Zertifikate in die Ausgabe enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="4d102-125">Specifies whether to include previously deleted certificates in the output</span></span>

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

### <span data-ttu-id="4d102-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4d102-126">-Name</span></span>
<span data-ttu-id="4d102-127">Gibt den Namen des zu erhaltenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="4d102-127">Specifies the name of the certificate to get.</span></span>

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

### <span data-ttu-id="4d102-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4d102-128">-VaultName</span></span>
<span data-ttu-id="4d102-129">Gibt den Namen eines Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="4d102-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="4d102-130">-Version</span><span class="sxs-lookup"><span data-stu-id="4d102-130">-Version</span></span>
<span data-ttu-id="4d102-131">Gibt die Version eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="4d102-131">Specifies the version of a certificate.</span></span>

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

### <span data-ttu-id="4d102-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d102-132">CommonParameters</span></span>
<span data-ttu-id="4d102-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d102-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d102-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d102-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d102-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4d102-135">INPUTS</span></span>

### <span data-ttu-id="4d102-136">Keine</span><span class="sxs-lookup"><span data-stu-id="4d102-136">None</span></span>
<span data-ttu-id="4d102-137">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4d102-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4d102-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4d102-138">OUTPUTS</span></span>

### <span data-ttu-id="4d102-139">System.Collections.generic.List'1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="4d102-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="4d102-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4d102-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="4d102-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4d102-141">NOTES</span></span>

## <span data-ttu-id="4d102-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4d102-142">RELATED LINKS</span></span>

[<span data-ttu-id="4d102-143">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4d102-143">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="4d102-144">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4d102-144">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="4d102-145">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4d102-145">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

