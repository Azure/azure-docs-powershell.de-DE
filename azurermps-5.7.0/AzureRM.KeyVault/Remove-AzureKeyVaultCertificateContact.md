---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: c91aa7e43a36e1218f304c3675f1d3c9635002c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502562"
---
# <span data-ttu-id="2edac-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2edac-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="2edac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2edac-102">SYNOPSIS</span></span>
<span data-ttu-id="2edac-103">Löscht einen Kontakt, der für Zertifikat Benachrichtigungen aus einem schlüsseltresor registriert ist.</span><span class="sxs-lookup"><span data-stu-id="2edac-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2edac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2edac-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2edac-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2edac-105">DESCRIPTION</span></span>
<span data-ttu-id="2edac-106">Das Cmdlet **Remove-AzureKeyVaultCertificateContact** löscht einen Kontakt, der für Zertifikat Benachrichtigungen aus einem schlüsseltresor registriert ist.</span><span class="sxs-lookup"><span data-stu-id="2edac-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="2edac-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2edac-107">EXAMPLES</span></span>

### <span data-ttu-id="2edac-108">Beispiel 1: Entfernen eines Zertifikat Kontakts</span><span class="sxs-lookup"><span data-stu-id="2edac-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="2edac-109">Mit diesem Befehl wird Patti Fuller als Zertifikat Kontakt für den contoso01-schlüsseltresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="2edac-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="2edac-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2edac-110">PARAMETERS</span></span>

### <span data-ttu-id="2edac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2edac-111">-DefaultProfile</span></span>
<span data-ttu-id="2edac-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2edac-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2edac-113">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="2edac-113">-EmailAddress</span></span>
<span data-ttu-id="2edac-114">Gibt die e-Mail-Adresse des zu entfernenden Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="2edac-114">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="2edac-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2edac-115">-PassThru</span></span>
<span data-ttu-id="2edac-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2edac-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2edac-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="2edac-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2edac-118">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="2edac-118">-VaultName</span></span>
<span data-ttu-id="2edac-119">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="2edac-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="2edac-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2edac-120">-Confirm</span></span>
<span data-ttu-id="2edac-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2edac-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2edac-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2edac-122">-WhatIf</span></span>
<span data-ttu-id="2edac-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2edac-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2edac-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2edac-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2edac-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2edac-125">CommonParameters</span></span>
<span data-ttu-id="2edac-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2edac-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2edac-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2edac-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2edac-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2edac-128">INPUTS</span></span>

### <span data-ttu-id="2edac-129">Keine</span><span class="sxs-lookup"><span data-stu-id="2edac-129">None</span></span>
<span data-ttu-id="2edac-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2edac-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2edac-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2edac-131">OUTPUTS</span></span>

### <span data-ttu-id="2edac-132">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="2edac-132">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact]</span></span>

## <span data-ttu-id="2edac-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="2edac-133">NOTES</span></span>

## <span data-ttu-id="2edac-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2edac-134">RELATED LINKS</span></span>

[<span data-ttu-id="2edac-135">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2edac-135">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="2edac-136">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2edac-136">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

