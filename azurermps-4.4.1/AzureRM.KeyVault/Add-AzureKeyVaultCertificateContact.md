---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: af66ad82d37c29d1dcd455cb3ccf7ae11676828c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504118"
---
# <span data-ttu-id="c141c-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c141c-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="c141c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c141c-102">SYNOPSIS</span></span>
<span data-ttu-id="c141c-103">Fügt einen Kontakt für Zertifikat Benachrichtigungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="c141c-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c141c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c141c-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c141c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c141c-105">DESCRIPTION</span></span>
<span data-ttu-id="c141c-106">Das Cmdlet **Add-AzureKeyVaultCertificateContact** fügt einen Kontakt für einen schlüsseltresor für Zertifikat Benachrichtigungen im Azure Key Vault hinzu.</span><span class="sxs-lookup"><span data-stu-id="c141c-106">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="c141c-107">Der Kontakt erhält Updates zu Ereignissen wie Zertifikat in der Nähe von Ablauf, Zertifikat erneuert usw.</span><span class="sxs-lookup"><span data-stu-id="c141c-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="c141c-108">Diese Ereignisse werden durch die Zertifikatrichtlinie bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c141c-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="c141c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c141c-109">EXAMPLES</span></span>

### <span data-ttu-id="c141c-110">Beispiel 1: Hinzufügen eines Key Vault-Zertifikats Kontakts</span><span class="sxs-lookup"><span data-stu-id="c141c-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="c141c-111">Mit diesem Befehl wird Patti Fuller als Zertifikat Kontakt für den ContosoKV01-schlüsseltresor hinzugefügt, und das **KeyVaultCertificateContact** -Objekt wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c141c-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="c141c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c141c-112">PARAMETERS</span></span>

### <span data-ttu-id="c141c-113">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="c141c-113">-EmailAddress</span></span>
<span data-ttu-id="c141c-114">Gibt die e-Mail-Adresse des Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="c141c-114">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c141c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c141c-115">-PassThru</span></span>
<span data-ttu-id="c141c-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c141c-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c141c-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="c141c-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c141c-118">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="c141c-118">-VaultName</span></span>
<span data-ttu-id="c141c-119">Gibt den Namen des Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="c141c-119">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="c141c-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c141c-120">-Confirm</span></span>
<span data-ttu-id="c141c-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c141c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c141c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c141c-122">-WhatIf</span></span>
<span data-ttu-id="c141c-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c141c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c141c-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c141c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c141c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c141c-125">-DefaultProfile</span></span>
<span data-ttu-id="c141c-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c141c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c141c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c141c-127">CommonParameters</span></span>
<span data-ttu-id="c141c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c141c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c141c-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c141c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c141c-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c141c-130">INPUTS</span></span>

## <span data-ttu-id="c141c-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c141c-131">OUTPUTS</span></span>

### <span data-ttu-id="c141c-132">Liste<Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="c141c-132">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="c141c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c141c-133">NOTES</span></span>

## <span data-ttu-id="c141c-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c141c-134">RELATED LINKS</span></span>

[<span data-ttu-id="c141c-135">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c141c-135">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="c141c-136">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c141c-136">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

