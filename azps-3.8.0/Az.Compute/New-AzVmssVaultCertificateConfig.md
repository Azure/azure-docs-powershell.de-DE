---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 23b2b3acd5bb15771d3383cc39c6e0a69073a750
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847680"
---
# <span data-ttu-id="0c612-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="0c612-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="0c612-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c612-102">SYNOPSIS</span></span>
<span data-ttu-id="0c612-103">Erstellt eine schlüsseltresor-Zertifikatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0c612-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="0c612-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c612-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c612-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c612-105">DESCRIPTION</span></span>
<span data-ttu-id="0c612-106">Das Cmdlet **New-AzVmssVaultCertificateConfig** gibt den geheimen Schlüssel an, der auf den virtuellen Computern des virtuellen Computers (Scale-Sets) gespeichert werden muss.</span><span class="sxs-lookup"><span data-stu-id="0c612-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="0c612-107">Die Ausgabe dieses Cmdlets ist für die Verwendung mit dem Add-AzVmssSecret-Cmdlet vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="0c612-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="0c612-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c612-108">EXAMPLES</span></span>

### <span data-ttu-id="0c612-109">Beispiel 1: Erstellen einer schlüsseltresor-Zertifikatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="0c612-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="0c612-110">Mit diesem Befehl wird eine Key Vault-Zertifikatkonfiguration erstellt, die den Zertifikatspeicher mit dem Namen mycerts verwendet, der sich unter der angegebenen Zertifikat-URL befindet.</span><span class="sxs-lookup"><span data-stu-id="0c612-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="0c612-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c612-111">PARAMETERS</span></span>

### <span data-ttu-id="0c612-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="0c612-112">-CertificateStore</span></span>
<span data-ttu-id="0c612-113">Gibt den Zertifikatspeicher auf den virtuellen Computern im Skalierungs Satz an, in dem das Zertifikat hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="0c612-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="0c612-114">Dies gilt nur für Skalierungs Sätze von Windows-virtuellen Computern.</span><span class="sxs-lookup"><span data-stu-id="0c612-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="0c612-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="0c612-115">-CertificateUrl</span></span>
<span data-ttu-id="0c612-116">Gibt den URI eines im schlüsseltresor gespeicherten Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="0c612-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="0c612-117">Es handelt sich um die Base64-Codierung des folgenden JSON-Objekts, das in UTF-8 codiert ist: {"Data": " \< Base64-codiert-Certificate \> ", "DataType": "PFX", "Kennwort": " \< PFX-Datei-Kennwort \> "}</span><span class="sxs-lookup"><span data-stu-id="0c612-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="0c612-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c612-118">-DefaultProfile</span></span>
<span data-ttu-id="0c612-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0c612-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c612-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0c612-120">-Confirm</span></span>
<span data-ttu-id="0c612-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0c612-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c612-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c612-122">-WhatIf</span></span>
<span data-ttu-id="0c612-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c612-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c612-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c612-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c612-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c612-125">CommonParameters</span></span>
<span data-ttu-id="0c612-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c612-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c612-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c612-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c612-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c612-128">INPUTS</span></span>

### <span data-ttu-id="0c612-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0c612-129">System.String</span></span>

## <span data-ttu-id="0c612-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c612-130">OUTPUTS</span></span>

### <span data-ttu-id="0c612-131">Microsoft. Azure. Management. Compute. Models. VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0c612-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="0c612-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c612-132">NOTES</span></span>

## <span data-ttu-id="0c612-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c612-133">RELATED LINKS</span></span>

[<span data-ttu-id="0c612-134">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="0c612-134">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
