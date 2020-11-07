---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: 37cc2025b97e16a2af313a2f4dd2cf7dfe815b7b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842108"
---
# <span data-ttu-id="7f1bd-101">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7f1bd-101">Remove-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="7f1bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="7f1bd-103">Löscht einen Zertifikat Vorgang aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="7f1bd-103">Deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="7f1bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f1bd-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f1bd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f1bd-105">DESCRIPTION</span></span>
<span data-ttu-id="7f1bd-106">Das Cmdlet **Remove-AzKeyVaultCertificateOperation** löscht einen Zertifikat Vorgang aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="7f1bd-106">The **Remove-AzKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="7f1bd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f1bd-107">EXAMPLES</span></span>

### <span data-ttu-id="7f1bd-108">Beispiel 1: Entfernen eines Zertifikat Vorgangs</span><span class="sxs-lookup"><span data-stu-id="7f1bd-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="7f1bd-109">Mit diesem Befehl wird der Zertifikat Vorgang mit dem Namen TestCert01 aus dem ContosoKV01-schlüsseltresor entfernt, ohne dass eine Bestätigung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="7f1bd-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="7f1bd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f1bd-110">PARAMETERS</span></span>

### <span data-ttu-id="7f1bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f1bd-111">-DefaultProfile</span></span>
<span data-ttu-id="7f1bd-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7f1bd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f1bd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7f1bd-113">-Force</span></span>
<span data-ttu-id="7f1bd-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="7f1bd-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1bd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7f1bd-115">-Name</span></span>
<span data-ttu-id="7f1bd-116">Gibt den Namen eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="7f1bd-116">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="7f1bd-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f1bd-117">-PassThru</span></span>
<span data-ttu-id="7f1bd-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7f1bd-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7f1bd-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="7f1bd-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1bd-120">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="7f1bd-120">-VaultName</span></span>
<span data-ttu-id="7f1bd-121">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="7f1bd-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="7f1bd-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7f1bd-122">-Confirm</span></span>
<span data-ttu-id="7f1bd-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f1bd-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1bd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f1bd-124">-WhatIf</span></span>
<span data-ttu-id="7f1bd-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f1bd-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f1bd-126">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f1bd-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f1bd-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f1bd-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1bd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f1bd-128">CommonParameters</span></span>
<span data-ttu-id="7f1bd-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f1bd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f1bd-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f1bd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f1bd-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f1bd-131">INPUTS</span></span>

### <span data-ttu-id="7f1bd-132">Keine</span><span class="sxs-lookup"><span data-stu-id="7f1bd-132">None</span></span>
<span data-ttu-id="7f1bd-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7f1bd-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7f1bd-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f1bd-134">OUTPUTS</span></span>

### <span data-ttu-id="7f1bd-135">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7f1bd-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="7f1bd-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f1bd-136">NOTES</span></span>

## <span data-ttu-id="7f1bd-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f1bd-137">RELATED LINKS</span></span>

[<span data-ttu-id="7f1bd-138">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7f1bd-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="7f1bd-139">Stopp-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7f1bd-139">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)

