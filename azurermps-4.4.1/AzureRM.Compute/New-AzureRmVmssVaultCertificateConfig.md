---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
ms.openlocfilehash: 5dd9b4f8dded86a0a900a3bb3942b633c29f7020
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504209"
---
# <span data-ttu-id="37152-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="37152-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="37152-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37152-102">SYNOPSIS</span></span>
<span data-ttu-id="37152-103">Erstellt eine schlüsseltresor-Zertifikatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="37152-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37152-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37152-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37152-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37152-105">DESCRIPTION</span></span>
<span data-ttu-id="37152-106">Das Cmdlet **New-AzureRmVmssVaultCertificateConfig** gibt den geheimen Schlüssel an, der auf den virtuellen Computern des virtuellen Computers (Scale-Sets) gespeichert werden muss.</span><span class="sxs-lookup"><span data-stu-id="37152-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="37152-107">Die Ausgabe dieses Cmdlets ist für die Verwendung mit dem Add-AzureRmVmssSecret-Cmdlet vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="37152-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="37152-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37152-108">EXAMPLES</span></span>

### <span data-ttu-id="37152-109">Beispiel 1: Erstellen einer schlüsseltresor-Zertifikatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="37152-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="37152-110">Mit diesem Befehl wird eine Key Vault-Zertifikatkonfiguration erstellt, die den Zertifikatspeicher mit dem Namen mycerts verwendet, der sich unter der angegebenen Zertifikat-URL befindet.</span><span class="sxs-lookup"><span data-stu-id="37152-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="37152-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="37152-111">PARAMETERS</span></span>

### <span data-ttu-id="37152-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="37152-112">-CertificateStore</span></span>
<span data-ttu-id="37152-113">Gibt den Zertifikatspeicher auf den virtuellen Computern im Skalierungs Satz an, in dem das Zertifikat hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="37152-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="37152-114">Dies gilt nur für Skalierungs Sätze von Windows-virtuellen Computern.</span><span class="sxs-lookup"><span data-stu-id="37152-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="37152-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="37152-115">-CertificateUrl</span></span>
<span data-ttu-id="37152-116">Gibt den URI eines im schlüsseltresor gespeicherten Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="37152-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="37152-117">Hierbei handelt es sich um die Base64-Codierung des folgenden JSON-Objekts, das in UTF-8 codiert ist:</span><span class="sxs-lookup"><span data-stu-id="37152-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="37152-118">{"Data": " \<Base64-encoded-certificate\> "; "Datentyp": "PFX"; "Kennwort": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="37152-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="37152-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37152-119">-DefaultProfile</span></span>
<span data-ttu-id="37152-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37152-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37152-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="37152-121">-Confirm</span></span>
<span data-ttu-id="37152-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37152-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37152-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37152-123">-WhatIf</span></span>
<span data-ttu-id="37152-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37152-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37152-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37152-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37152-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37152-126">CommonParameters</span></span>
<span data-ttu-id="37152-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37152-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37152-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37152-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37152-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37152-129">INPUTS</span></span>

## <span data-ttu-id="37152-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37152-130">OUTPUTS</span></span>

###  
<span data-ttu-id="37152-131">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="37152-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="37152-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="37152-132">NOTES</span></span>

## <span data-ttu-id="37152-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37152-133">RELATED LINKS</span></span>

[<span data-ttu-id="37152-134">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="37152-134">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
