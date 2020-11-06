---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Stop-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Stop-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: b413c71deb70081689c2870e95c71a0ad14a1928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504097"
---
# <span data-ttu-id="5561f-101">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="5561f-101">Stop-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="5561f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5561f-102">SYNOPSIS</span></span>
<span data-ttu-id="5561f-103">Bricht eine Zertifikat Operation in Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="5561f-103">Cancels a certificate operation in key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5561f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5561f-104">SYNTAX</span></span>

```
Stop-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5561f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5561f-105">DESCRIPTION</span></span>
<span data-ttu-id="5561f-106">Mit dem Cmdlet " **Stop-AzureKeyVaultCertificateOperation** " wird ein Zertifikat Vorgang im Azure Key Vault-Dienst abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="5561f-106">The **Stop-AzureKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="5561f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5561f-107">EXAMPLES</span></span>

### <span data-ttu-id="5561f-108">Beispiel 1: Abbrechen eines Zertifikat Vorgangs</span><span class="sxs-lookup"><span data-stu-id="5561f-108">Example 1: Cancel a certificate operation</span></span>
```
PS C:\>Stop-AzureKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force
Status                    : inProgress
CancellationRequested     : True
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCVr6EVwsd48qDVORsF4V4w4N1aQCUirFW7b+kwoTvSOL4SfMiWcPmno0uxmQQoh
                            gz157bC3sKFLyBUsGCmS4i7uWkBOSEpCh8L3FKU4XMqRROlUM9AqswzB0e1sURCqevEJA80xFpfTgkeqpm44m4jr6p7gu+h1PBf9Dt7b43Gybde5DUlGrrOiTkOIAF0eU2iNVeHOapoj8m1XHmzO1BARs
                            oa0pSDxO/aMgeuq/QPkWG64Iiw55U20byKZ86u3Y4g192HsPwsrHkf9ZSYR2M9BYM3YGoT/dkCmAtP4LQAsOwf1+S0a/TwRtrnoOHbPFI6HYSY3TY1iqzZ9xItfgalAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAjxUX5PGhri9qJTxSleGEbMVkxhhn3nuPUgxujEzrcQVr
                            fZAACJHbOnga/QYwpxumKWnkX9YdWxb58PPn+nLV2gYP3eYEyJ4DR9XDcKpoQxZahUdqD3JZXhWPIcN05tw9Fuq8ziw94BjLZW3h3iDamqkBnysJYW58FBp1H8Ejqk0Iynbo0V223Innq/7QB2fVwe3ZJ
                            JecT8YxHJjVQ5psdDpEWgLUG/DFiAPHdwupI7JjvtvQmT3AotL0x5GNx2bWNH5hHIXsX4bnbxZgNQnTB2w3tQ3QeuKt8fUx2S0xtxPllaCUul6efa84TNqdMcMfyxCarIwDP6qdhS+CDU1uUA==
ErrorCode                 : 
ErrorMessage              :
```

<span data-ttu-id="5561f-109">Mit diesem Befehl wird der TestCert02-Zertifikat Vorgang abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="5561f-109">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="5561f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5561f-110">PARAMETERS</span></span>

### <span data-ttu-id="5561f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="5561f-111">-Force</span></span>
<span data-ttu-id="5561f-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="5561f-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5561f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="5561f-113">-Name</span></span>
<span data-ttu-id="5561f-114">Gibt den Namen eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="5561f-114">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5561f-115">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="5561f-115">-VaultName</span></span>
<span data-ttu-id="5561f-116">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="5561f-116">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5561f-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5561f-117">-Confirm</span></span>
<span data-ttu-id="5561f-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5561f-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5561f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5561f-119">-WhatIf</span></span>
<span data-ttu-id="5561f-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5561f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5561f-121">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5561f-121">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5561f-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5561f-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5561f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5561f-123">-DefaultProfile</span></span>
<span data-ttu-id="5561f-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5561f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5561f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5561f-125">CommonParameters</span></span>
<span data-ttu-id="5561f-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5561f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5561f-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5561f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5561f-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5561f-128">INPUTS</span></span>

## <span data-ttu-id="5561f-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5561f-129">OUTPUTS</span></span>

### <span data-ttu-id="5561f-130">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="5561f-130">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="5561f-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="5561f-131">NOTES</span></span>

## <span data-ttu-id="5561f-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5561f-132">RELATED LINKS</span></span>

[<span data-ttu-id="5561f-133">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="5561f-133">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="5561f-134">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="5561f-134">Remove-AzureKeyVaultCertificateOperation</span></span>](./Remove-AzureKeyVaultCertificateOperation.md)

