---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 7e9af7cd775726fc57b78f3fdead20f36dca13cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166579"
---
# <span data-ttu-id="2a0b5-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="2a0b5-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="2a0b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2a0b5-102">SYNOPSIS</span></span>
<span data-ttu-id="2a0b5-103">Stellt ein gelöschtes Zertifikat in einem schlüsseltresor in einen aktiven Zustand ein.</span><span class="sxs-lookup"><span data-stu-id="2a0b5-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="2a0b5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a0b5-104">SYNTAX</span></span>

### <span data-ttu-id="2a0b5-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="2a0b5-105">Default (Default)</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a0b5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2a0b5-106">InputObject</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a0b5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a0b5-107">DESCRIPTION</span></span>
<span data-ttu-id="2a0b5-108">Mit dem Cmdlet **"Undo-AzKeyVaultCertificateRemoval"** wird ein zuvor gelöschtes Zertifikat wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="2a0b5-108">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="2a0b5-109">Das wiederhergestellte Zertifikat ist aktiv und kann für alle Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a0b5-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="2a0b5-110">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="2a0b5-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="2a0b5-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2a0b5-111">EXAMPLES</span></span>

### <span data-ttu-id="2a0b5-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2a0b5-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'

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

<span data-ttu-id="2a0b5-113">Mit diesem Befehl wird das zuvor gelöschte Zertifikat "myCertificate" wieder in einen aktiven und nutzbaren Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="2a0b5-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="2a0b5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a0b5-114">PARAMETERS</span></span>

### <span data-ttu-id="2a0b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a0b5-115">-DefaultProfile</span></span>
<span data-ttu-id="2a0b5-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2a0b5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a0b5-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2a0b5-117">-InputObject</span></span>
<span data-ttu-id="2a0b5-118">Gelöschtes Zertifikatobjekt</span><span class="sxs-lookup"><span data-stu-id="2a0b5-118">Deleted Certificate object</span></span>

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

### <span data-ttu-id="2a0b5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2a0b5-119">-Name</span></span>
<span data-ttu-id="2a0b5-120">Zertifikatname.</span><span class="sxs-lookup"><span data-stu-id="2a0b5-120">Certificate name.</span></span>
<span data-ttu-id="2a0b5-121">Cmdlet erstellt den FQDN eines Zertifikats aus Vault Name, aktuell ausgewählter Umgebung und Zertifikatname.</span><span class="sxs-lookup"><span data-stu-id="2a0b5-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="2a0b5-122">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="2a0b5-122">-VaultName</span></span>
<span data-ttu-id="2a0b5-123">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="2a0b5-123">Vault name.</span></span>
<span data-ttu-id="2a0b5-124">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="2a0b5-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="2a0b5-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2a0b5-125">-Confirm</span></span>
<span data-ttu-id="2a0b5-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a0b5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a0b5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a0b5-127">-WhatIf</span></span>
<span data-ttu-id="2a0b5-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a0b5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a0b5-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a0b5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a0b5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a0b5-130">CommonParameters</span></span>
<span data-ttu-id="2a0b5-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a0b5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a0b5-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a0b5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a0b5-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2a0b5-133">INPUTS</span></span>

### <span data-ttu-id="2a0b5-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="2a0b5-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="2a0b5-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2a0b5-135">OUTPUTS</span></span>

### <span data-ttu-id="2a0b5-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2a0b5-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="2a0b5-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="2a0b5-137">NOTES</span></span>

## <span data-ttu-id="2a0b5-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2a0b5-138">RELATED LINKS</span></span>

[<span data-ttu-id="2a0b5-139">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2a0b5-139">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="2a0b5-140">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2a0b5-140">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
