---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/stop-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: e260b32e847705240d93451b32bef9ae31d7fa07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152697"
---
# <span data-ttu-id="e0652-101">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e0652-101">Stop-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="e0652-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0652-102">SYNOPSIS</span></span>
<span data-ttu-id="e0652-103">Bricht einen Zertifikatvorgang im Schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="e0652-103">Cancels a certificate operation in key vault.</span></span>

## <span data-ttu-id="e0652-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0652-104">SYNTAX</span></span>

### <span data-ttu-id="e0652-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="e0652-105">Default (Default)</span></span>
```
Stop-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0652-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e0652-106">InputObject</span></span>
```
Stop-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0652-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0652-107">DESCRIPTION</span></span>
<span data-ttu-id="e0652-108">Das **Cmdlet "Stop-AzKeyVaultCertificateOperation"** bricht einen Zertifikatvorgang im Azure Key Vault-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="e0652-108">The **Stop-AzKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="e0652-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e0652-109">EXAMPLES</span></span>

### <span data-ttu-id="e0652-110">Beispiel 1: Abbrechen eines Zertifikatvorgangs</span><span class="sxs-lookup"><span data-stu-id="e0652-110">Example 1: Cancel a certificate operation</span></span>
```powershell
PS C:\> Stop-AzKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force

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

<span data-ttu-id="e0652-111">Mit diesem Befehl wird der TestCert02-Zertifikatvorgang abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="e0652-111">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="e0652-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0652-112">PARAMETERS</span></span>

### <span data-ttu-id="e0652-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0652-113">-DefaultProfile</span></span>
<span data-ttu-id="e0652-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e0652-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0652-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e0652-115">-Force</span></span>
<span data-ttu-id="e0652-116">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="e0652-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e0652-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0652-117">-InputObject</span></span>
<span data-ttu-id="e0652-118">Vorgangsobjekt</span><span class="sxs-lookup"><span data-stu-id="e0652-118">Operation object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0652-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e0652-119">-Name</span></span>
<span data-ttu-id="e0652-120">Gibt den Namen eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="e0652-120">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="e0652-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e0652-121">-VaultName</span></span>
<span data-ttu-id="e0652-122">Gibt den Namen eines Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="e0652-122">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="e0652-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0652-123">-Confirm</span></span>
<span data-ttu-id="e0652-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0652-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0652-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e0652-125">-WhatIf</span></span>
<span data-ttu-id="e0652-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0652-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0652-127">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0652-127">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0652-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0652-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0652-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0652-129">CommonParameters</span></span>
<span data-ttu-id="e0652-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0652-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0652-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0652-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0652-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e0652-132">INPUTS</span></span>

### <span data-ttu-id="e0652-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e0652-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="e0652-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e0652-134">OUTPUTS</span></span>

### <span data-ttu-id="e0652-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e0652-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="e0652-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e0652-136">NOTES</span></span>

## <span data-ttu-id="e0652-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e0652-137">RELATED LINKS</span></span>

[<span data-ttu-id="e0652-138">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e0652-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="e0652-139">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e0652-139">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)

