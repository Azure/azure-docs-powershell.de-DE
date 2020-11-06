---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: db2b9066524bd21daa1fa65b87554d9b028754de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504410"
---
# <span data-ttu-id="412f4-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="412f4-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="412f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="412f4-102">SYNOPSIS</span></span>
<span data-ttu-id="412f4-103">Stellt ein gelöschtes Zertifikat in einem schlüsseltresor in einen aktiven Zustand ein.</span><span class="sxs-lookup"><span data-stu-id="412f4-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="412f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="412f4-104">SYNTAX</span></span>

### <span data-ttu-id="412f4-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="412f4-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="412f4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="412f4-106">InputObject</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="412f4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="412f4-107">DESCRIPTION</span></span>
<span data-ttu-id="412f4-108">Mit dem Cmdlet **"Undo-AzureKeyVaultCertificateRemoval"** wird ein zuvor gelöschtes Zertifikat wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="412f4-108">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="412f4-109">Das wiederhergestellte Zertifikat ist aktiv und kann für alle Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="412f4-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="412f4-110">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="412f4-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="412f4-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="412f4-111">EXAMPLES</span></span>

### <span data-ttu-id="412f4-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="412f4-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/24/2018 10:58:13 AM

                [Not After]
                  11/24/2018 10:08:13 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/mycertificate/7fe415d5518240c1a6fce89986b8d334
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/mycertificate/7fe415d5518240c1a6fce89986b8d334
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Recoverable+Purgeable
Enabled       : True
Expires       : 11/24/2018 6:08:13 PM
NotBefore     : 5/24/2018 5:58:13 PM
Created       : 5/24/2018 6:08:13 PM
Updated       : 5/24/2018 6:08:13 PM
Tags          :
VaultName     : MyKeyVault
Name          : MyCertificate
Version       : 7fe415d5518240c1a6fce89986b8d334
Id            : https://mykeyvault.vault.azure.net:443/certificates/mycertificate/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="412f4-113">Mit diesem Befehl wird das zuvor gelöschte Zertifikat "myCertificate" wieder in einen aktiven und nutzbaren Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="412f4-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="412f4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="412f4-114">PARAMETERS</span></span>

### <span data-ttu-id="412f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="412f4-115">-DefaultProfile</span></span>
<span data-ttu-id="412f4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="412f4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="412f4-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="412f4-117">-InputObject</span></span>
<span data-ttu-id="412f4-118">Gelöschtes Zertifikatobjekt</span><span class="sxs-lookup"><span data-stu-id="412f4-118">Deleted Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="412f4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="412f4-119">-Name</span></span>
<span data-ttu-id="412f4-120">Zertifikatname.</span><span class="sxs-lookup"><span data-stu-id="412f4-120">Certificate name.</span></span>
<span data-ttu-id="412f4-121">Cmdlet erstellt den FQDN eines Zertifikats aus Vault Name, aktuell ausgewählter Umgebung und Zertifikatname.</span><span class="sxs-lookup"><span data-stu-id="412f4-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="412f4-122">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="412f4-122">-VaultName</span></span>
<span data-ttu-id="412f4-123">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="412f4-123">Vault name.</span></span>
<span data-ttu-id="412f4-124">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="412f4-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="412f4-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="412f4-125">-Confirm</span></span>
<span data-ttu-id="412f4-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="412f4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="412f4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="412f4-127">-WhatIf</span></span>
<span data-ttu-id="412f4-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="412f4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="412f4-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="412f4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="412f4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="412f4-130">CommonParameters</span></span>
<span data-ttu-id="412f4-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="412f4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="412f4-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="412f4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="412f4-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="412f4-133">INPUTS</span></span>

### <span data-ttu-id="412f4-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="412f4-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="412f4-135">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="412f4-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="412f4-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="412f4-136">OUTPUTS</span></span>

### <span data-ttu-id="412f4-137">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="412f4-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="412f4-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="412f4-138">NOTES</span></span>

## <span data-ttu-id="412f4-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="412f4-139">RELATED LINKS</span></span>

[<span data-ttu-id="412f4-140">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="412f4-140">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="412f4-141">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="412f4-141">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
