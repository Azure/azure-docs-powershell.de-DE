---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultCertificate.md
ms.openlocfilehash: 8c4bb4813c2d07577d80743906a4f8155bc81282
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846016"
---
# <span data-ttu-id="451ec-101">Update-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="451ec-101">Update-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="451ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="451ec-102">SYNOPSIS</span></span>
<span data-ttu-id="451ec-103">Ändert bearbeitbare Attribute eines Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="451ec-103">Modifies editable attributes of a certificate.</span></span>

## <span data-ttu-id="451ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="451ec-104">SYNTAX</span></span>

### <span data-ttu-id="451ec-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="451ec-105">ByName (Default)</span></span>
```
Update-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="451ec-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="451ec-106">ByInputObject</span></span>
```
Update-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="451ec-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="451ec-107">DESCRIPTION</span></span>
<span data-ttu-id="451ec-108">Das Cmdlet **Update-AzKeyVaultCertificate** ändert die bearbeitbaren Attribute eines Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="451ec-108">The **Update-AzKeyVaultCertificate** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="451ec-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="451ec-109">EXAMPLES</span></span>

### <span data-ttu-id="451ec-110">Beispiel 1: Ändern der Tags, die einem Zertifikat zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="451ec-110">Example 1: Modify the tags associated with a certificate</span></span>
```powershell
PS C:\> $Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Update-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags -PassThru

Name        : TestCert01
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Id          : https://ContosoKV01.vault.azure.net:443/certificates/TestCert01
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/TestCert01
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/TestCert01
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="451ec-111">Der erste Befehl weist der $Tags-Variablen ein Array von Schlüssel-Wert-Paaren zu.</span><span class="sxs-lookup"><span data-stu-id="451ec-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="451ec-112">Der zweite Befehl legt den Tag-Wert des Zertifikats mit dem Namen TestCert01 auf $Tags fest.</span><span class="sxs-lookup"><span data-stu-id="451ec-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

## <span data-ttu-id="451ec-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="451ec-113">PARAMETERS</span></span>

### <span data-ttu-id="451ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="451ec-114">-DefaultProfile</span></span>
<span data-ttu-id="451ec-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="451ec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="451ec-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="451ec-116">-Enable</span></span>
<span data-ttu-id="451ec-117">Falls vorhanden, aktivieren Sie ein Zertifikat, wenn der Wert wahr ist.</span><span class="sxs-lookup"><span data-stu-id="451ec-117">If present, enable a certificate if value is true.</span></span>
<span data-ttu-id="451ec-118">Deaktivieren Sie ein Zertifikat, wenn der Wert falsch ist.</span><span class="sxs-lookup"><span data-stu-id="451ec-118">Disable a certificate if value is false.</span></span>
<span data-ttu-id="451ec-119">Wenn keine Angabe erfolgt, bleibt der vorhandene Wert des Zertifikats aktiviert/deaktiviert unverändert.</span><span class="sxs-lookup"><span data-stu-id="451ec-119">If not specified, the existing value of the certificate's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="451ec-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="451ec-120">-InputObject</span></span>
<span data-ttu-id="451ec-121">Certificate-Objekt</span><span class="sxs-lookup"><span data-stu-id="451ec-121">Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="451ec-122">-Name</span><span class="sxs-lookup"><span data-stu-id="451ec-122">-Name</span></span>
<span data-ttu-id="451ec-123">Zertifikatname.</span><span class="sxs-lookup"><span data-stu-id="451ec-123">Certificate name.</span></span>
<span data-ttu-id="451ec-124">Cmdlet erstellt den FQDN eines geheimen Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung und geheimem Namen.</span><span class="sxs-lookup"><span data-stu-id="451ec-124">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="451ec-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="451ec-125">-PassThru</span></span>
<span data-ttu-id="451ec-126">Das Cmdlet gibt das Objekt nicht standardmäßig zurück.</span><span class="sxs-lookup"><span data-stu-id="451ec-126">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="451ec-127">Wenn dieser Schalter angegeben ist, geben Sie Certificate-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="451ec-127">If this switch is specified, return certificate object.</span></span>

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

### <span data-ttu-id="451ec-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="451ec-128">-Tag</span></span>
<span data-ttu-id="451ec-129">Eine Hashtable, die Zertifikat Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="451ec-129">A hashtable representing certificate tags.</span></span>
<span data-ttu-id="451ec-130">Wenn Sie nicht angegeben wird, bleiben die vorhandenen Tags des sertificate unverändert.</span><span class="sxs-lookup"><span data-stu-id="451ec-130">If not specified, the existing tags of the sertificate remain unchanged.</span></span>
<span data-ttu-id="451ec-131">Entfernen Sie ein Tag, indem Sie eine leere Hashtable angeben.</span><span class="sxs-lookup"><span data-stu-id="451ec-131">Remove a tag by specifying an empty Hashtable.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="451ec-132">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="451ec-132">-VaultName</span></span>
<span data-ttu-id="451ec-133">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="451ec-133">Vault name.</span></span>
<span data-ttu-id="451ec-134">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="451ec-134">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="451ec-135">-Version</span><span class="sxs-lookup"><span data-stu-id="451ec-135">-Version</span></span>
<span data-ttu-id="451ec-136">Zertifikat Version.</span><span class="sxs-lookup"><span data-stu-id="451ec-136">Certificate version.</span></span>
<span data-ttu-id="451ec-137">Cmdlet erstellt den FQDN eines Zertifikats aus Vault-Name, aktuell ausgewählter Umgebung, Zertifikatsname und Zertifikat Version.</span><span class="sxs-lookup"><span data-stu-id="451ec-137">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment, certificate name and certificate version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="451ec-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="451ec-138">-Confirm</span></span>
<span data-ttu-id="451ec-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="451ec-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="451ec-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="451ec-140">-WhatIf</span></span>
<span data-ttu-id="451ec-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="451ec-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="451ec-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="451ec-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="451ec-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="451ec-143">CommonParameters</span></span>
<span data-ttu-id="451ec-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="451ec-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="451ec-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="451ec-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="451ec-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="451ec-146">INPUTS</span></span>

### <span data-ttu-id="451ec-147">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="451ec-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="451ec-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="451ec-148">OUTPUTS</span></span>

### <span data-ttu-id="451ec-149">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="451ec-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="451ec-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="451ec-150">NOTES</span></span>

## <span data-ttu-id="451ec-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="451ec-151">RELATED LINKS</span></span>
