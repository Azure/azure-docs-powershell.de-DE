---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
ms.openlocfilehash: 4aac9e7079451eebda0c77ae663666fbd55dc9e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476742"
---
# <span data-ttu-id="736ad-101">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="736ad-101">Set-AzureKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="736ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="736ad-102">SYNOPSIS</span></span>
<span data-ttu-id="736ad-103">Ändert bearbeitbare Attribute eines Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="736ad-103">Modifies editable attributes of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="736ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="736ad-104">SYNTAX</span></span>

### <span data-ttu-id="736ad-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="736ad-105">ByName (Default)</span></span>
```
Set-AzureKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="736ad-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="736ad-106">ByInputObject</span></span>
```
Set-AzureKeyVaultCertificateAttribute [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="736ad-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="736ad-107">DESCRIPTION</span></span>
<span data-ttu-id="736ad-108">Das Cmdlet " **Satz-AzureKeyVaultCertificateAttribute** " ändert die bearbeitbaren Attribute eines Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="736ad-108">The **Set-AzureKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="736ad-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="736ad-109">EXAMPLES</span></span>

### <span data-ttu-id="736ad-110">Beispiel 1: Ändern der Tags, die einem Zertifikat zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="736ad-110">Example 1: Modify the tags associated with a certificate</span></span>
```
PS C:\>$Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Set-AzureKeyVaultCertificateAttribute -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags
PS C:\> Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : "TestCert01"
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                5A2EF60501F241D6A4336841B36FEA41

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                A565D568082FEE2BE33B356ECC3703C2E9886555

Id          : https://ContosoKV01.vault.azure.net:443/certificates/tt02
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/tt02
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/tt02
Thumbprint  : A565D568082FEE2BE33B356ECC3703C2E9886555
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="736ad-111">Der erste Befehl weist der $Tags-Variablen ein Array von Schlüssel-Wert-Paaren zu.</span><span class="sxs-lookup"><span data-stu-id="736ad-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="736ad-112">Der zweite Befehl legt den Tag-Wert des Zertifikats mit dem Namen TestCert01 auf $Tags fest.</span><span class="sxs-lookup"><span data-stu-id="736ad-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="736ad-113">Der endgültige Befehl zeigt das TestCert01-Zertifikat mithilfe des Get-AzureKeyVaultCertificate-Cmdlets an, um den Vorgang zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="736ad-113">The final command displays the TestCert01 certificate by using the Get-AzureKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="736ad-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="736ad-114">PARAMETERS</span></span>

### <span data-ttu-id="736ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="736ad-115">-DefaultProfile</span></span>
<span data-ttu-id="736ad-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="736ad-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="736ad-117">-Enable</span><span class="sxs-lookup"><span data-stu-id="736ad-117">-Enable</span></span>
<span data-ttu-id="736ad-118">Gibt an, ob ein Zertifikat aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="736ad-118">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="736ad-119">Geben Sie $true an, die zu aktivieren oder zu deaktivieren $false.</span><span class="sxs-lookup"><span data-stu-id="736ad-119">Specify $True to enable or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="736ad-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="736ad-120">-InputObject</span></span>
<span data-ttu-id="736ad-121">Certificate-Objekt</span><span class="sxs-lookup"><span data-stu-id="736ad-121">Certificate object</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="736ad-122">-Name</span><span class="sxs-lookup"><span data-stu-id="736ad-122">-Name</span></span>
<span data-ttu-id="736ad-123">Gibt den Namen des zu ändernden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="736ad-123">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="736ad-124">Dieses Cmdlet erstellt den FQDN eines Zertifikats basierend auf dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung, dem Zertifikatnamen und der Zertifikat Version.</span><span class="sxs-lookup"><span data-stu-id="736ad-124">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="736ad-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="736ad-125">-PassThru</span></span>
<span data-ttu-id="736ad-126">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="736ad-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="736ad-127">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="736ad-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="736ad-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="736ad-128">-Tag</span></span>
<span data-ttu-id="736ad-129">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="736ad-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="736ad-130">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="736ad-130">For example:</span></span>

<span data-ttu-id="736ad-131">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="736ad-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="736ad-132">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="736ad-132">-VaultName</span></span>
<span data-ttu-id="736ad-133">Gibt den Namen des Schlüssel Tresors an, in dem dieses Cmdlet ein Zertifikat ändert.</span><span class="sxs-lookup"><span data-stu-id="736ad-133">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="736ad-134">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="736ad-134">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="736ad-135">-Version</span><span class="sxs-lookup"><span data-stu-id="736ad-135">-Version</span></span>
<span data-ttu-id="736ad-136">Gibt die Version eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="736ad-136">Specifies the version of a certificate.</span></span>
<span data-ttu-id="736ad-137">Dieses Cmdlet erstellt den FQDN eines Zertifikats basierend auf dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung, dem Zertifikatnamen und der Zertifikat Version.</span><span class="sxs-lookup"><span data-stu-id="736ad-137">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="736ad-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="736ad-138">-Confirm</span></span>
<span data-ttu-id="736ad-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="736ad-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="736ad-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="736ad-140">-WhatIf</span></span>
<span data-ttu-id="736ad-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="736ad-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="736ad-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="736ad-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="736ad-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="736ad-143">CommonParameters</span></span>
<span data-ttu-id="736ad-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="736ad-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="736ad-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="736ad-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="736ad-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="736ad-146">INPUTS</span></span>

### <span data-ttu-id="736ad-147">Keine</span><span class="sxs-lookup"><span data-stu-id="736ad-147">None</span></span>
<span data-ttu-id="736ad-148">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="736ad-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="736ad-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="736ad-149">OUTPUTS</span></span>

### <span data-ttu-id="736ad-150">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="736ad-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="736ad-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="736ad-151">NOTES</span></span>

## <span data-ttu-id="736ad-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="736ad-152">RELATED LINKS</span></span>

[<span data-ttu-id="736ad-153">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="736ad-153">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)
