---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
ms.openlocfilehash: 7d5a575bfb5e26511f2051e8e45654af1e8c9f2e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848223"
---
# <span data-ttu-id="482df-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="482df-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="482df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="482df-102">SYNOPSIS</span></span>
<span data-ttu-id="482df-103">Löscht einen Zertifikat Vorgang aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="482df-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="482df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="482df-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="482df-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="482df-105">DESCRIPTION</span></span>
<span data-ttu-id="482df-106">Das Cmdlet **Remove-AzureKeyVaultCertificateOperation** löscht einen Zertifikat Vorgang aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="482df-106">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="482df-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="482df-107">EXAMPLES</span></span>

### <span data-ttu-id="482df-108">Beispiel 1: Entfernen eines Zertifikat Vorgangs</span><span class="sxs-lookup"><span data-stu-id="482df-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="482df-109">Mit diesem Befehl wird der Zertifikat Vorgang mit dem Namen TestCert01 aus dem ContosoKV01-schlüsseltresor entfernt, ohne dass eine Bestätigung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="482df-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="482df-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="482df-110">PARAMETERS</span></span>

### <span data-ttu-id="482df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="482df-111">-DefaultProfile</span></span>
<span data-ttu-id="482df-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="482df-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="482df-113">-Force</span><span class="sxs-lookup"><span data-stu-id="482df-113">-Force</span></span>
<span data-ttu-id="482df-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="482df-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="482df-115">-Name</span><span class="sxs-lookup"><span data-stu-id="482df-115">-Name</span></span>
<span data-ttu-id="482df-116">Gibt den Namen eines Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="482df-116">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="482df-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="482df-117">-PassThru</span></span>
<span data-ttu-id="482df-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="482df-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="482df-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="482df-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="482df-120">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="482df-120">-VaultName</span></span>
<span data-ttu-id="482df-121">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="482df-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="482df-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="482df-122">-Confirm</span></span>
<span data-ttu-id="482df-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="482df-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="482df-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="482df-124">-WhatIf</span></span>
<span data-ttu-id="482df-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="482df-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="482df-126">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="482df-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="482df-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="482df-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="482df-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="482df-128">CommonParameters</span></span>
<span data-ttu-id="482df-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="482df-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="482df-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="482df-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="482df-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="482df-131">INPUTS</span></span>

## <span data-ttu-id="482df-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="482df-132">OUTPUTS</span></span>

### <span data-ttu-id="482df-133">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="482df-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="482df-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="482df-134">NOTES</span></span>

## <span data-ttu-id="482df-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="482df-135">RELATED LINKS</span></span>

[<span data-ttu-id="482df-136">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="482df-136">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="482df-137">Stopp-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="482df-137">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

