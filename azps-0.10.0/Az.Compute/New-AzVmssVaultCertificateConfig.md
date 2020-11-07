---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 0889bfa5abfdf90480eb508ebad7a62607912722
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844443"
---
# <span data-ttu-id="f98b5-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="f98b5-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="f98b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f98b5-102">SYNOPSIS</span></span>
<span data-ttu-id="f98b5-103">Erstellt eine schlüsseltresor-Zertifikatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f98b5-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="f98b5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f98b5-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f98b5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f98b5-105">DESCRIPTION</span></span>
<span data-ttu-id="f98b5-106">Das Cmdlet **New-AzVmssVaultCertificateConfig** gibt den geheimen Schlüssel an, der auf den virtuellen Computern des virtuellen Computers (Scale-Sets) gespeichert werden muss.</span><span class="sxs-lookup"><span data-stu-id="f98b5-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="f98b5-107">Die Ausgabe dieses Cmdlets ist für die Verwendung mit dem Add-AzVmssSecret-Cmdlet vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="f98b5-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="f98b5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f98b5-108">EXAMPLES</span></span>

### <span data-ttu-id="f98b5-109">Beispiel 1: Erstellen einer schlüsseltresor-Zertifikatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f98b5-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="f98b5-110">Mit diesem Befehl wird eine Key Vault-Zertifikatkonfiguration erstellt, die den Zertifikatspeicher mit dem Namen mycerts verwendet, der sich unter der angegebenen Zertifikat-URL befindet.</span><span class="sxs-lookup"><span data-stu-id="f98b5-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="f98b5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f98b5-111">PARAMETERS</span></span>

### <span data-ttu-id="f98b5-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="f98b5-112">-CertificateStore</span></span>
<span data-ttu-id="f98b5-113">Gibt den Zertifikatspeicher auf den virtuellen Computern im Skalierungs Satz an, in dem das Zertifikat hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f98b5-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="f98b5-114">Dies gilt nur für Skalierungs Sätze von Windows-virtuellen Computern.</span><span class="sxs-lookup"><span data-stu-id="f98b5-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f98b5-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="f98b5-115">-CertificateUrl</span></span>
<span data-ttu-id="f98b5-116">Gibt den URI eines im schlüsseltresor gespeicherten Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="f98b5-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="f98b5-117">Hierbei handelt es sich um die Base64-Codierung des folgenden JSON-Objekts, das in UTF-8 codiert ist:</span><span class="sxs-lookup"><span data-stu-id="f98b5-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="f98b5-118">{"Daten": " \< Base64-codiert-Certificate \> "," Datentyp ":" PFX "," Password ":" \< PFX-Datei-Kennwort \> "}</span><span class="sxs-lookup"><span data-stu-id="f98b5-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f98b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f98b5-119">-DefaultProfile</span></span>
<span data-ttu-id="f98b5-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f98b5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f98b5-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f98b5-121">-Confirm</span></span>
<span data-ttu-id="f98b5-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f98b5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f98b5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f98b5-123">-WhatIf</span></span>
<span data-ttu-id="f98b5-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f98b5-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f98b5-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f98b5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f98b5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98b5-126">CommonParameters</span></span>
<span data-ttu-id="f98b5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f98b5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98b5-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f98b5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98b5-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f98b5-129">INPUTS</span></span>

### <span data-ttu-id="f98b5-130">Keine</span><span class="sxs-lookup"><span data-stu-id="f98b5-130">None</span></span>
<span data-ttu-id="f98b5-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f98b5-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f98b5-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f98b5-132">OUTPUTS</span></span>

###  
<span data-ttu-id="f98b5-133">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="f98b5-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f98b5-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="f98b5-134">NOTES</span></span>

## <span data-ttu-id="f98b5-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f98b5-135">RELATED LINKS</span></span>

[<span data-ttu-id="f98b5-136">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="f98b5-136">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
