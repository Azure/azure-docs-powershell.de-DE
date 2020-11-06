---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 96f793c763a3e9a710c7e401c29880ccc0136b38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503746"
---
# <span data-ttu-id="c16b5-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c16b5-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="c16b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c16b5-102">SYNOPSIS</span></span>
<span data-ttu-id="c16b5-103">Fügt einen Kontakt für Zertifikat Benachrichtigungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="c16b5-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c16b5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c16b5-104">SYNTAX</span></span>

### <span data-ttu-id="c16b5-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="c16b5-105">Interactive (Default)</span></span>
```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c16b5-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="c16b5-106">ByObject</span></span>
```
Add-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c16b5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c16b5-107">DESCRIPTION</span></span>
<span data-ttu-id="c16b5-108">Das Cmdlet **Add-AzureKeyVaultCertificateContact** fügt einen Kontakt für einen schlüsseltresor für Zertifikat Benachrichtigungen im Azure Key Vault hinzu.</span><span class="sxs-lookup"><span data-stu-id="c16b5-108">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="c16b5-109">Der Kontakt erhält Updates zu Ereignissen wie Zertifikat in der Nähe von Ablauf, Zertifikat erneuert usw.</span><span class="sxs-lookup"><span data-stu-id="c16b5-109">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="c16b5-110">Diese Ereignisse werden durch die Zertifikatrichtlinie bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c16b5-110">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="c16b5-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c16b5-111">EXAMPLES</span></span>

### <span data-ttu-id="c16b5-112">Beispiel 1: Hinzufügen eines Key Vault-Zertifikats Kontakts</span><span class="sxs-lookup"><span data-stu-id="c16b5-112">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="c16b5-113">Mit diesem Befehl wird Patti Fuller als Zertifikat Kontakt für den ContosoKV01-schlüsseltresor hinzugefügt, und das **KeyVaultCertificateContact** -Objekt wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c16b5-113">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="c16b5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c16b5-114">PARAMETERS</span></span>

### <span data-ttu-id="c16b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c16b5-115">-DefaultProfile</span></span>
<span data-ttu-id="c16b5-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c16b5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c16b5-117">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="c16b5-117">-EmailAddress</span></span>
<span data-ttu-id="c16b5-118">Gibt die e-Mail-Adresse des Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="c16b5-118">Specifies the email address of the contact.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c16b5-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c16b5-119">-InputObject</span></span>
<span data-ttu-id="c16b5-120">Keyvault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c16b5-120">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c16b5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c16b5-121">-PassThru</span></span>
<span data-ttu-id="c16b5-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c16b5-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c16b5-123">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="c16b5-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c16b5-124">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="c16b5-124">-VaultName</span></span>
<span data-ttu-id="c16b5-125">Gibt den Namen des Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="c16b5-125">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c16b5-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c16b5-126">-Confirm</span></span>
<span data-ttu-id="c16b5-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c16b5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c16b5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c16b5-128">-WhatIf</span></span>
<span data-ttu-id="c16b5-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c16b5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c16b5-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c16b5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c16b5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c16b5-131">CommonParameters</span></span>
<span data-ttu-id="c16b5-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c16b5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c16b5-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c16b5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c16b5-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c16b5-134">INPUTS</span></span>

### <span data-ttu-id="c16b5-135">Keine</span><span class="sxs-lookup"><span data-stu-id="c16b5-135">None</span></span>
<span data-ttu-id="c16b5-136">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c16b5-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c16b5-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c16b5-137">OUTPUTS</span></span>

### <span data-ttu-id="c16b5-138">Liste<Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="c16b5-138">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="c16b5-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="c16b5-139">NOTES</span></span>

## <span data-ttu-id="c16b5-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c16b5-140">RELATED LINKS</span></span>

[<span data-ttu-id="c16b5-141">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c16b5-141">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="c16b5-142">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c16b5-142">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

