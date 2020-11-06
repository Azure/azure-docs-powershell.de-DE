---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: 91fee65a201de8babc7ef7aa09973f1e98f95cb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504089"
---
# <span data-ttu-id="3e570-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="3e570-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="3e570-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3e570-102">SYNOPSIS</span></span>
<span data-ttu-id="3e570-103">Stellt ein gelöschtes Zertifikat in einem schlüsseltresor in einen aktiven Zustand ein.</span><span class="sxs-lookup"><span data-stu-id="3e570-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e570-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e570-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e570-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e570-105">DESCRIPTION</span></span>
<span data-ttu-id="3e570-106">Mit dem Cmdlet **"Undo-AzureKeyVaultCertificateRemoval"** wird ein zuvor gelöschtes Zertifikat wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="3e570-106">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="3e570-107">Das wiederhergestellte Zertifikat ist aktiv und kann für alle Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e570-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="3e570-108">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="3e570-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="3e570-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e570-109">EXAMPLES</span></span>

### <span data-ttu-id="3e570-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3e570-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="3e570-111">Mit diesem Befehl wird das zuvor gelöschte Zertifikat "myCertificate" wieder in einen aktiven und nutzbaren Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="3e570-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="3e570-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e570-112">PARAMETERS</span></span>

### <span data-ttu-id="3e570-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3e570-113">-Name</span></span>
<span data-ttu-id="3e570-114">Zertifikatname.</span><span class="sxs-lookup"><span data-stu-id="3e570-114">Certificate name.</span></span>
<span data-ttu-id="3e570-115">Cmdlet erstellt den FQDN eines Zertifikats aus Vault Name, aktuell ausgewählter Umgebung und Zertifikatname.</span><span class="sxs-lookup"><span data-stu-id="3e570-115">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e570-116">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="3e570-116">-VaultName</span></span>
<span data-ttu-id="3e570-117">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="3e570-117">Vault name.</span></span>
<span data-ttu-id="3e570-118">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="3e570-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e570-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3e570-119">-Confirm</span></span>
<span data-ttu-id="3e570-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e570-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e570-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e570-121">-WhatIf</span></span>
<span data-ttu-id="3e570-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3e570-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e570-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e570-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e570-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e570-124">-DefaultProfile</span></span>
<span data-ttu-id="3e570-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3e570-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e570-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e570-126">CommonParameters</span></span>
<span data-ttu-id="3e570-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e570-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e570-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e570-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e570-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3e570-129">INPUTS</span></span>

### <span data-ttu-id="3e570-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3e570-130">System.String</span></span>

## <span data-ttu-id="3e570-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3e570-131">OUTPUTS</span></span>

### <span data-ttu-id="3e570-132">Microsoft. Azure. Commands. keyvault. Models. Certificate</span><span class="sxs-lookup"><span data-stu-id="3e570-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="3e570-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="3e570-133">NOTES</span></span>

## <span data-ttu-id="3e570-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3e570-134">RELATED LINKS</span></span>

[<span data-ttu-id="3e570-135">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3e570-135">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="3e570-136">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3e570-136">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
