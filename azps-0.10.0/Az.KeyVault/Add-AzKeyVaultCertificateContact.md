---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 375cc5493bd3b3cac31f4318df57e155eda918c3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843915"
---
# <span data-ttu-id="02346-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="02346-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="02346-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02346-102">SYNOPSIS</span></span>
<span data-ttu-id="02346-103">Fügt einen Kontakt für Zertifikat Benachrichtigungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="02346-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="02346-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02346-104">SYNTAX</span></span>

```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02346-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02346-105">DESCRIPTION</span></span>
<span data-ttu-id="02346-106">Das Cmdlet **Add-AzKeyVaultCertificateContact** fügt einen Kontakt für einen schlüsseltresor für Zertifikat Benachrichtigungen im Azure Key Vault hinzu.</span><span class="sxs-lookup"><span data-stu-id="02346-106">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="02346-107">Der Kontakt erhält Updates zu Ereignissen wie Zertifikat in der Nähe von Ablauf, Zertifikat erneuert usw.</span><span class="sxs-lookup"><span data-stu-id="02346-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="02346-108">Diese Ereignisse werden durch die Zertifikatrichtlinie bestimmt.</span><span class="sxs-lookup"><span data-stu-id="02346-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="02346-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02346-109">EXAMPLES</span></span>

### <span data-ttu-id="02346-110">Beispiel 1: Hinzufügen eines Key Vault-Zertifikats Kontakts</span><span class="sxs-lookup"><span data-stu-id="02346-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="02346-111">Mit diesem Befehl wird Patti Fuller als Zertifikat Kontakt für den ContosoKV01-schlüsseltresor hinzugefügt, und das **KeyVaultCertificateContact** -Objekt wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="02346-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="02346-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="02346-112">PARAMETERS</span></span>

### <span data-ttu-id="02346-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02346-113">-DefaultProfile</span></span>
<span data-ttu-id="02346-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="02346-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02346-115">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="02346-115">-EmailAddress</span></span>
<span data-ttu-id="02346-116">Gibt die e-Mail-Adresse des Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="02346-116">Specifies the email address of the contact.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02346-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02346-117">-PassThru</span></span>
<span data-ttu-id="02346-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="02346-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="02346-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="02346-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="02346-120">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="02346-120">-VaultName</span></span>
<span data-ttu-id="02346-121">Gibt den Namen des Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="02346-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="02346-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="02346-122">-Confirm</span></span>
<span data-ttu-id="02346-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02346-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02346-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02346-124">-WhatIf</span></span>
<span data-ttu-id="02346-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02346-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02346-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02346-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02346-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02346-127">CommonParameters</span></span>
<span data-ttu-id="02346-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02346-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02346-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02346-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02346-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02346-130">INPUTS</span></span>

### <span data-ttu-id="02346-131">Keine</span><span class="sxs-lookup"><span data-stu-id="02346-131">None</span></span>
<span data-ttu-id="02346-132">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="02346-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="02346-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02346-133">OUTPUTS</span></span>

### <span data-ttu-id="02346-134">Liste<Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="02346-134">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="02346-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="02346-135">NOTES</span></span>

## <span data-ttu-id="02346-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02346-136">RELATED LINKS</span></span>

[<span data-ttu-id="02346-137">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="02346-137">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="02346-138">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="02346-138">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

