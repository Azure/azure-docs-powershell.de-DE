---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 3ef23bcbddc1f8a5c5c235c72dac32f535a71a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502718"
---
# <span data-ttu-id="f6414-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f6414-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="f6414-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f6414-102">SYNOPSIS</span></span>
<span data-ttu-id="f6414-103">Löscht einen Zertifikataussteller aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="f6414-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6414-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6414-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6414-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6414-105">DESCRIPTION</span></span>
<span data-ttu-id="f6414-106">Das Cmdlet **Remove-AzureKeyVaultCertificateIssuer** löscht einen Zertifikataussteller aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="f6414-106">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="f6414-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6414-107">EXAMPLES</span></span>

### <span data-ttu-id="f6414-108">Beispiel 1: Entfernen eines Zertifikatsausstellers</span><span class="sxs-lookup"><span data-stu-id="f6414-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="f6414-109">Mit diesem Befehl wird der Zertifikataussteller namens TestIssuer01 aus dem ContosoKV01-schlüsseltresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="f6414-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="f6414-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6414-110">PARAMETERS</span></span>

### <span data-ttu-id="f6414-111">-Force</span><span class="sxs-lookup"><span data-stu-id="f6414-111">-Force</span></span>
<span data-ttu-id="f6414-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f6414-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f6414-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f6414-113">-Name</span></span>
<span data-ttu-id="f6414-114">Gibt den Namen des zu entfernenden Emittenten an.</span><span class="sxs-lookup"><span data-stu-id="f6414-114">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6414-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6414-115">-PassThru</span></span>
<span data-ttu-id="f6414-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f6414-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f6414-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="f6414-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f6414-118">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="f6414-118">-VaultName</span></span>
<span data-ttu-id="f6414-119">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="f6414-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="f6414-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f6414-120">-Confirm</span></span>
<span data-ttu-id="f6414-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6414-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6414-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6414-122">-WhatIf</span></span>
<span data-ttu-id="f6414-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6414-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6414-124">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6414-124">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6414-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6414-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6414-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6414-126">-DefaultProfile</span></span>
<span data-ttu-id="f6414-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f6414-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6414-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6414-128">CommonParameters</span></span>
<span data-ttu-id="f6414-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6414-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6414-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6414-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6414-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f6414-131">INPUTS</span></span>

## <span data-ttu-id="f6414-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6414-132">OUTPUTS</span></span>

### <span data-ttu-id="f6414-133">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f6414-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="f6414-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="f6414-134">NOTES</span></span>

## <span data-ttu-id="f6414-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f6414-135">RELATED LINKS</span></span>

[<span data-ttu-id="f6414-136">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f6414-136">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="f6414-137">Satz-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f6414-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


