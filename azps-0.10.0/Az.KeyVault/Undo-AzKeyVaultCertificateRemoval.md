---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 5757a9fb050d69cdf0ef0e648b0d446de1e3ee24
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842088"
---
# <span data-ttu-id="d17d2-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="d17d2-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="d17d2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d17d2-102">SYNOPSIS</span></span>
<span data-ttu-id="d17d2-103">Stellt ein gelöschtes Zertifikat in einem schlüsseltresor in einen aktiven Zustand ein.</span><span class="sxs-lookup"><span data-stu-id="d17d2-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="d17d2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d17d2-104">SYNTAX</span></span>

```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d17d2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d17d2-105">DESCRIPTION</span></span>
<span data-ttu-id="d17d2-106">Mit dem Cmdlet **"Undo-AzKeyVaultCertificateRemoval"** wird ein zuvor gelöschtes Zertifikat wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="d17d2-106">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="d17d2-107">Das wiederhergestellte Zertifikat ist aktiv und kann für alle Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d17d2-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="d17d2-108">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="d17d2-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="d17d2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d17d2-109">EXAMPLES</span></span>

### <span data-ttu-id="d17d2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d17d2-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="d17d2-111">Mit diesem Befehl wird das zuvor gelöschte Zertifikat "myCertificate" wieder in einen aktiven und nutzbaren Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="d17d2-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="d17d2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d17d2-112">PARAMETERS</span></span>

### <span data-ttu-id="d17d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d17d2-113">-DefaultProfile</span></span>
<span data-ttu-id="d17d2-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d17d2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d17d2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d17d2-115">-Name</span></span>
<span data-ttu-id="d17d2-116">Zertifikatname.</span><span class="sxs-lookup"><span data-stu-id="d17d2-116">Certificate name.</span></span>
<span data-ttu-id="d17d2-117">Cmdlet erstellt den FQDN eines Zertifikats aus Vault Name, aktuell ausgewählter Umgebung und Zertifikatname.</span><span class="sxs-lookup"><span data-stu-id="d17d2-117">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d17d2-118">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="d17d2-118">-VaultName</span></span>
<span data-ttu-id="d17d2-119">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="d17d2-119">Vault name.</span></span>
<span data-ttu-id="d17d2-120">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="d17d2-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d17d2-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d17d2-121">-Confirm</span></span>
<span data-ttu-id="d17d2-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d17d2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d17d2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d17d2-123">-WhatIf</span></span>
<span data-ttu-id="d17d2-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d17d2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d17d2-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d17d2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d17d2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d17d2-126">CommonParameters</span></span>
<span data-ttu-id="d17d2-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d17d2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d17d2-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d17d2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d17d2-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d17d2-129">INPUTS</span></span>

### <span data-ttu-id="d17d2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d17d2-130">System.String</span></span>

## <span data-ttu-id="d17d2-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d17d2-131">OUTPUTS</span></span>

### <span data-ttu-id="d17d2-132">Microsoft. Azure. Commands. keyvault. Models. Certificate</span><span class="sxs-lookup"><span data-stu-id="d17d2-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="d17d2-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="d17d2-133">NOTES</span></span>

## <span data-ttu-id="d17d2-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d17d2-134">RELATED LINKS</span></span>

[<span data-ttu-id="d17d2-135">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d17d2-135">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="d17d2-136">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d17d2-136">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
