---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: 33024ce7002975848a98ff8bdfd6188196a96e6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664654"
---
# <span data-ttu-id="d4192-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="d4192-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="d4192-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4192-102">SYNOPSIS</span></span>
<span data-ttu-id="d4192-103">Stellt ein gelöschtes Zertifikat in einem schlüsseltresor in einen aktiven Zustand ein.</span><span class="sxs-lookup"><span data-stu-id="d4192-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4192-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4192-104">SYNTAX</span></span>

### <span data-ttu-id="d4192-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4192-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4192-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d4192-106">InputObject</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4192-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4192-107">DESCRIPTION</span></span>
<span data-ttu-id="d4192-108">Mit dem Cmdlet **"Undo-AzureKeyVaultCertificateRemoval"** wird ein zuvor gelöschtes Zertifikat wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="d4192-108">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="d4192-109">Das wiederhergestellte Zertifikat ist aktiv und kann für alle Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4192-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="d4192-110">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="d4192-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="d4192-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4192-111">EXAMPLES</span></span>

### <span data-ttu-id="d4192-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d4192-112">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="d4192-113">Mit diesem Befehl wird das zuvor gelöschte Zertifikat "myCertificate" wieder in einen aktiven und nutzbaren Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="d4192-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="d4192-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4192-114">PARAMETERS</span></span>

### <span data-ttu-id="d4192-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4192-115">-DefaultProfile</span></span>
<span data-ttu-id="d4192-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d4192-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4192-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d4192-117">-InputObject</span></span>
<span data-ttu-id="d4192-118">Gelöschtes Zertifikatobjekt</span><span class="sxs-lookup"><span data-stu-id="d4192-118">Deleted Certificate object</span></span>

```yaml
Type: PSDeletedKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4192-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d4192-119">-Name</span></span>
<span data-ttu-id="d4192-120">Zertifikatname.</span><span class="sxs-lookup"><span data-stu-id="d4192-120">Certificate name.</span></span>
<span data-ttu-id="d4192-121">Cmdlet erstellt den FQDN eines Zertifikats aus Vault Name, aktuell ausgewählter Umgebung und Zertifikatname.</span><span class="sxs-lookup"><span data-stu-id="d4192-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4192-122">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="d4192-122">-VaultName</span></span>
<span data-ttu-id="d4192-123">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="d4192-123">Vault name.</span></span>
<span data-ttu-id="d4192-124">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="d4192-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4192-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4192-125">-Confirm</span></span>
<span data-ttu-id="d4192-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4192-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4192-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4192-127">-WhatIf</span></span>
<span data-ttu-id="d4192-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4192-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4192-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4192-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4192-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4192-130">CommonParameters</span></span>
<span data-ttu-id="d4192-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4192-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4192-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4192-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4192-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4192-133">INPUTS</span></span>

### <span data-ttu-id="d4192-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d4192-134">System.String</span></span>

## <span data-ttu-id="d4192-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4192-135">OUTPUTS</span></span>

### <span data-ttu-id="d4192-136">Microsoft. Azure. Commands. keyvault. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="d4192-136">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="d4192-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4192-137">NOTES</span></span>

## <span data-ttu-id="d4192-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4192-138">RELATED LINKS</span></span>

[<span data-ttu-id="d4192-139">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d4192-139">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="d4192-140">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d4192-140">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
