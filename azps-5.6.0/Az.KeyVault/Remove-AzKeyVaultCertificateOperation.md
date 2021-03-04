---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: 922631712b241f6f0b516e2787a20113af8a8740
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918880"
---
# <span data-ttu-id="650c2-101">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="650c2-101">Remove-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="650c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="650c2-102">SYNOPSIS</span></span>
<span data-ttu-id="650c2-103">Löscht einen Zertifikatvorgang aus einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="650c2-103">Deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="650c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="650c2-104">SYNTAX</span></span>

### <span data-ttu-id="650c2-105">Standard</span><span class="sxs-lookup"><span data-stu-id="650c2-105">Default</span></span>
```
Remove-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="650c2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="650c2-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="650c2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="650c2-107">DESCRIPTION</span></span>
<span data-ttu-id="650c2-108">Das **Cmdlet Remove-AzKeyVaultCertificateOperation** löscht einen Zertifikatvorgang aus einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="650c2-108">The **Remove-AzKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="650c2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="650c2-109">EXAMPLES</span></span>

### <span data-ttu-id="650c2-110">Beispiel 1: Entfernen eines Zertifikatvorgangs</span><span class="sxs-lookup"><span data-stu-id="650c2-110">Example 1: Remove a certificate operation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force

Id                        : https://contosokv01.vault.azure.net/certificates/testcert01/pending
Status                    : completed
StatusDetails             :
RequestId                 : f5dfd2ae486149a594dc98e800dceaaa
Target                    : https://contosokv01.vault.azure.net/certificates/testcert01
Issuer                    : Self
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
                            ==
ErrorCode                 :
ErrorMessage              :
Name                      :
VaultName                 :
```

<span data-ttu-id="650c2-111">Mit diesem Befehl wird der Zertifikatvorgang mit dem Namen TestCert01 aus dem ContosoKV01-Schlüsseltresor entfernt, ohne zur Bestätigung aufgefordert zu werden.</span><span class="sxs-lookup"><span data-stu-id="650c2-111">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="650c2-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="650c2-112">PARAMETERS</span></span>

### <span data-ttu-id="650c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="650c2-113">-DefaultProfile</span></span>
<span data-ttu-id="650c2-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="650c2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="650c2-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="650c2-115">-Force</span></span>
<span data-ttu-id="650c2-116">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="650c2-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="650c2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="650c2-117">-InputObject</span></span>
<span data-ttu-id="650c2-118">Vorgangsobjekt</span><span class="sxs-lookup"><span data-stu-id="650c2-118">Operation object</span></span>

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

### <span data-ttu-id="650c2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="650c2-119">-Name</span></span>
<span data-ttu-id="650c2-120">Gibt den Namen eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="650c2-120">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="650c2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="650c2-121">-PassThru</span></span>
<span data-ttu-id="650c2-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="650c2-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="650c2-123">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="650c2-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="650c2-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="650c2-124">-VaultName</span></span>
<span data-ttu-id="650c2-125">Gibt den Namen eines Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="650c2-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="650c2-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="650c2-126">-Confirm</span></span>
<span data-ttu-id="650c2-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="650c2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="650c2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="650c2-128">-WhatIf</span></span>
<span data-ttu-id="650c2-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="650c2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="650c2-130">Das Cmdlet wird nicht ausgeführt. Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="650c2-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="650c2-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="650c2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="650c2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="650c2-132">CommonParameters</span></span>
<span data-ttu-id="650c2-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="650c2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="650c2-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="650c2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="650c2-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="650c2-135">INPUTS</span></span>

### <span data-ttu-id="650c2-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="650c2-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="650c2-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="650c2-137">OUTPUTS</span></span>

### <span data-ttu-id="650c2-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="650c2-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="650c2-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="650c2-139">NOTES</span></span>

## <span data-ttu-id="650c2-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="650c2-140">RELATED LINKS</span></span>

[<span data-ttu-id="650c2-141">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="650c2-141">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="650c2-142">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="650c2-142">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)

