---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
ms.openlocfilehash: 493d4bcd641e8132bffd49100a04732759ce7e91
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849288"
---
# <span data-ttu-id="35abc-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="35abc-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="35abc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35abc-102">SYNOPSIS</span></span>
<span data-ttu-id="35abc-103">Stellt ein gelöschtes Zertifikat in einem schlüsseltresor in einen aktiven Zustand ein.</span><span class="sxs-lookup"><span data-stu-id="35abc-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35abc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35abc-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35abc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35abc-105">DESCRIPTION</span></span>
<span data-ttu-id="35abc-106">Mit dem Cmdlet **"Undo-AzureKeyVaultCertificateRemoval"** wird ein zuvor gelöschtes Zertifikat wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="35abc-106">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="35abc-107">Das wiederhergestellte Zertifikat ist aktiv und kann für alle Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="35abc-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="35abc-108">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="35abc-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="35abc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35abc-109">EXAMPLES</span></span>

### <span data-ttu-id="35abc-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="35abc-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="35abc-111">Mit diesem Befehl wird das zuvor gelöschte Zertifikat "myCertificate" wieder in einen aktiven und nutzbaren Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="35abc-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="35abc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="35abc-112">PARAMETERS</span></span>

### <span data-ttu-id="35abc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35abc-113">-DefaultProfile</span></span>
<span data-ttu-id="35abc-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="35abc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35abc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="35abc-115">-Name</span></span>
<span data-ttu-id="35abc-116">Zertifikatname.</span><span class="sxs-lookup"><span data-stu-id="35abc-116">Certificate name.</span></span>
<span data-ttu-id="35abc-117">Cmdlet erstellt den FQDN eines Zertifikats aus Vault Name, aktuell ausgewählter Umgebung und Zertifikatname.</span><span class="sxs-lookup"><span data-stu-id="35abc-117">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="35abc-118">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="35abc-118">-VaultName</span></span>
<span data-ttu-id="35abc-119">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="35abc-119">Vault name.</span></span>
<span data-ttu-id="35abc-120">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="35abc-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="35abc-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="35abc-121">-Confirm</span></span>
<span data-ttu-id="35abc-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="35abc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35abc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35abc-123">-WhatIf</span></span>
<span data-ttu-id="35abc-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="35abc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35abc-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35abc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35abc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35abc-126">CommonParameters</span></span>
<span data-ttu-id="35abc-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35abc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35abc-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35abc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35abc-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35abc-129">INPUTS</span></span>

### <span data-ttu-id="35abc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="35abc-130">System.String</span></span>

## <span data-ttu-id="35abc-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35abc-131">OUTPUTS</span></span>

### <span data-ttu-id="35abc-132">Microsoft. Azure. Commands. keyvault. Models. Certificate</span><span class="sxs-lookup"><span data-stu-id="35abc-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="35abc-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="35abc-133">NOTES</span></span>

## <span data-ttu-id="35abc-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35abc-134">RELATED LINKS</span></span>

[<span data-ttu-id="35abc-135">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="35abc-135">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="35abc-136">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="35abc-136">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
