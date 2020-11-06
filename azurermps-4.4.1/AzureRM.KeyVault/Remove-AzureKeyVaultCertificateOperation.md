---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: d40489471e94474e83243803b5c64cdad1d572d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502717"
---
# <span data-ttu-id="05fc6-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="05fc6-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="05fc6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="05fc6-103">Löscht einen Zertifikat Vorgang aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="05fc6-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05fc6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05fc6-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05fc6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05fc6-105">DESCRIPTION</span></span>
<span data-ttu-id="05fc6-106">Das Cmdlet **Remove-AzureKeyVaultCertificateOperation** löscht einen Zertifikat Vorgang aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="05fc6-106">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="05fc6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05fc6-107">EXAMPLES</span></span>

### <span data-ttu-id="05fc6-108">Beispiel 1: Entfernen eines Zertifikat Vorgangs</span><span class="sxs-lookup"><span data-stu-id="05fc6-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="05fc6-109">Mit diesem Befehl wird der Zertifikat Vorgang mit dem Namen TestCert01 aus dem ContosoKV01-schlüsseltresor entfernt, ohne dass eine Bestätigung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="05fc6-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="05fc6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="05fc6-110">PARAMETERS</span></span>

### <span data-ttu-id="05fc6-111">-Force</span><span class="sxs-lookup"><span data-stu-id="05fc6-111">-Force</span></span>
<span data-ttu-id="05fc6-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="05fc6-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="05fc6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="05fc6-113">-Name</span></span>
<span data-ttu-id="05fc6-114">Gibt den Namen eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="05fc6-114">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="05fc6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05fc6-115">-PassThru</span></span>
<span data-ttu-id="05fc6-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="05fc6-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="05fc6-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="05fc6-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="05fc6-118">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="05fc6-118">-VaultName</span></span>
<span data-ttu-id="05fc6-119">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="05fc6-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="05fc6-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="05fc6-120">-Confirm</span></span>
<span data-ttu-id="05fc6-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="05fc6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05fc6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05fc6-122">-WhatIf</span></span>
<span data-ttu-id="05fc6-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05fc6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05fc6-124">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05fc6-124">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05fc6-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="05fc6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05fc6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05fc6-126">-DefaultProfile</span></span>
<span data-ttu-id="05fc6-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="05fc6-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05fc6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05fc6-128">CommonParameters</span></span>
<span data-ttu-id="05fc6-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05fc6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05fc6-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05fc6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05fc6-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05fc6-131">INPUTS</span></span>

## <span data-ttu-id="05fc6-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05fc6-132">OUTPUTS</span></span>

### <span data-ttu-id="05fc6-133">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="05fc6-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="05fc6-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="05fc6-134">NOTES</span></span>

## <span data-ttu-id="05fc6-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05fc6-135">RELATED LINKS</span></span>

[<span data-ttu-id="05fc6-136">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="05fc6-136">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="05fc6-137">Stopp-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="05fc6-137">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

