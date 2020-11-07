---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
ms.openlocfilehash: d0f9e69ff36348cb4eb49920b85709b9b268adf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664105"
---
# <span data-ttu-id="c66e5-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="c66e5-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="c66e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c66e5-102">SYNOPSIS</span></span>
<span data-ttu-id="c66e5-103">Erstellt eine schlüsseltresor-Zertifikatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="c66e5-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c66e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c66e5-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c66e5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c66e5-105">DESCRIPTION</span></span>
<span data-ttu-id="c66e5-106">Das Cmdlet **New-AzureRmVmssVaultCertificateConfig** gibt den geheimen Schlüssel an, der auf den virtuellen Computern des virtuellen Computers (Scale-Sets) gespeichert werden muss.</span><span class="sxs-lookup"><span data-stu-id="c66e5-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="c66e5-107">Die Ausgabe dieses Cmdlets ist für die Verwendung mit dem Add-AzureRmVmssSecret-Cmdlet vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="c66e5-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="c66e5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c66e5-108">EXAMPLES</span></span>

### <span data-ttu-id="c66e5-109">Beispiel 1: Erstellen einer schlüsseltresor-Zertifikatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="c66e5-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="c66e5-110">Mit diesem Befehl wird eine Key Vault-Zertifikatkonfiguration erstellt, die den Zertifikatspeicher mit dem Namen mycerts verwendet, der sich unter der angegebenen Zertifikat-URL befindet.</span><span class="sxs-lookup"><span data-stu-id="c66e5-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="c66e5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c66e5-111">PARAMETERS</span></span>

### <span data-ttu-id="c66e5-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="c66e5-112">-CertificateStore</span></span>
<span data-ttu-id="c66e5-113">Gibt den Zertifikatspeicher auf den virtuellen Computern im Skalierungs Satz an, in dem das Zertifikat hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c66e5-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="c66e5-114">Dies gilt nur für Skalierungs Sätze von Windows-virtuellen Computern.</span><span class="sxs-lookup"><span data-stu-id="c66e5-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c66e5-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="c66e5-115">-CertificateUrl</span></span>
<span data-ttu-id="c66e5-116">Gibt den URI eines im schlüsseltresor gespeicherten Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="c66e5-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="c66e5-117">Es handelt sich um die Base64-Codierung des folgenden JSON-Objekts, das in UTF-8 codiert ist: {"Daten": " \<Base64-encoded-certificate\> ", "Datentyp": "PFX", "Kennwort": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="c66e5-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c66e5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c66e5-118">-DefaultProfile</span></span>
<span data-ttu-id="c66e5-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c66e5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c66e5-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c66e5-120">-Confirm</span></span>
<span data-ttu-id="c66e5-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c66e5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c66e5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c66e5-122">-WhatIf</span></span>
<span data-ttu-id="c66e5-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c66e5-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c66e5-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c66e5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c66e5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c66e5-125">CommonParameters</span></span>
<span data-ttu-id="c66e5-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c66e5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c66e5-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c66e5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c66e5-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c66e5-128">INPUTS</span></span>

### <span data-ttu-id="c66e5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c66e5-129">System.String</span></span>

## <span data-ttu-id="c66e5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c66e5-130">OUTPUTS</span></span>

### <span data-ttu-id="c66e5-131">Microsoft. Azure. Management. Compute. Models. VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c66e5-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="c66e5-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="c66e5-132">NOTES</span></span>

## <span data-ttu-id="c66e5-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c66e5-133">RELATED LINKS</span></span>

[<span data-ttu-id="c66e5-134">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="c66e5-134">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
