---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: 70d6d39ed3e2083bf0f52e9e56808b7d36f1cc24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482901"
---
# <span data-ttu-id="1d598-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1d598-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="1d598-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1d598-102">SYNOPSIS</span></span>
<span data-ttu-id="1d598-103">Löscht einen Zertifikat Vorgang aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="1d598-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d598-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d598-104">SYNTAX</span></span>

### <span data-ttu-id="1d598-105">Standard</span><span class="sxs-lookup"><span data-stu-id="1d598-105">Default</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d598-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1d598-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d598-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d598-107">DESCRIPTION</span></span>
<span data-ttu-id="1d598-108">Das Cmdlet **Remove-AzureKeyVaultCertificateOperation** löscht einen Zertifikat Vorgang aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="1d598-108">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="1d598-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d598-109">EXAMPLES</span></span>

### <span data-ttu-id="1d598-110">Beispiel 1: Entfernen eines Zertifikat Vorgangs</span><span class="sxs-lookup"><span data-stu-id="1d598-110">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="1d598-111">Mit diesem Befehl wird der Zertifikat Vorgang mit dem Namen TestCert01 aus dem ContosoKV01-schlüsseltresor entfernt, ohne dass eine Bestätigung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="1d598-111">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="1d598-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d598-112">PARAMETERS</span></span>

### <span data-ttu-id="1d598-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d598-113">-DefaultProfile</span></span>
<span data-ttu-id="1d598-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1d598-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d598-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1d598-115">-Force</span></span>
<span data-ttu-id="1d598-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="1d598-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1d598-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1d598-117">-InputObject</span></span>
<span data-ttu-id="1d598-118">Operation-Objekt</span><span class="sxs-lookup"><span data-stu-id="1d598-118">Operation object</span></span>

```yaml
Type: PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d598-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1d598-119">-Name</span></span>
<span data-ttu-id="1d598-120">Gibt den Namen eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="1d598-120">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d598-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d598-121">-PassThru</span></span>
<span data-ttu-id="1d598-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="1d598-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1d598-123">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="1d598-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1d598-124">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="1d598-124">-VaultName</span></span>
<span data-ttu-id="1d598-125">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="1d598-125">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d598-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1d598-126">-Confirm</span></span>
<span data-ttu-id="1d598-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d598-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d598-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d598-128">-WhatIf</span></span>
<span data-ttu-id="1d598-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d598-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d598-130">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d598-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d598-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d598-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d598-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d598-132">CommonParameters</span></span>
<span data-ttu-id="1d598-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d598-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d598-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d598-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d598-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1d598-135">INPUTS</span></span>

### <span data-ttu-id="1d598-136">Keine</span><span class="sxs-lookup"><span data-stu-id="1d598-136">None</span></span>
<span data-ttu-id="1d598-137">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1d598-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1d598-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1d598-138">OUTPUTS</span></span>

### <span data-ttu-id="1d598-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1d598-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="1d598-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="1d598-140">NOTES</span></span>

## <span data-ttu-id="1d598-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1d598-141">RELATED LINKS</span></span>

[<span data-ttu-id="1d598-142">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1d598-142">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="1d598-143">Stopp-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1d598-143">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

