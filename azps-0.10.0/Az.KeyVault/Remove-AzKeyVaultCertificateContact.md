---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 0b92fcb3725d42ac7c2978600f7903d6bf7f6142
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842116"
---
# <span data-ttu-id="d9111-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="d9111-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="d9111-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9111-102">SYNOPSIS</span></span>
<span data-ttu-id="d9111-103">Löscht einen Kontakt, der für Zertifikat Benachrichtigungen aus einem schlüsseltresor registriert ist.</span><span class="sxs-lookup"><span data-stu-id="d9111-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="d9111-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9111-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9111-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9111-105">DESCRIPTION</span></span>
<span data-ttu-id="d9111-106">Das Cmdlet **Remove-AzKeyVaultCertificateContact** löscht einen Kontakt, der für Zertifikat Benachrichtigungen aus einem schlüsseltresor registriert ist.</span><span class="sxs-lookup"><span data-stu-id="d9111-106">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="d9111-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9111-107">EXAMPLES</span></span>

### <span data-ttu-id="d9111-108">Beispiel 1: Entfernen eines Zertifikat Kontakts</span><span class="sxs-lookup"><span data-stu-id="d9111-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="d9111-109">Mit diesem Befehl wird Patti Fuller als Zertifikat Kontakt für den contoso01-schlüsseltresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="d9111-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="d9111-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9111-110">PARAMETERS</span></span>

### <span data-ttu-id="d9111-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9111-111">-DefaultProfile</span></span>
<span data-ttu-id="d9111-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d9111-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9111-113">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="d9111-113">-EmailAddress</span></span>
<span data-ttu-id="d9111-114">Gibt die e-Mail-Adresse des zu entfernenden Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="d9111-114">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="d9111-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9111-115">-PassThru</span></span>
<span data-ttu-id="d9111-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d9111-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d9111-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="d9111-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d9111-118">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="d9111-118">-VaultName</span></span>
<span data-ttu-id="d9111-119">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="d9111-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="d9111-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d9111-120">-Confirm</span></span>
<span data-ttu-id="d9111-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9111-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9111-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9111-122">-WhatIf</span></span>
<span data-ttu-id="d9111-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9111-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9111-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9111-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9111-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9111-125">CommonParameters</span></span>
<span data-ttu-id="d9111-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9111-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9111-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9111-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9111-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9111-128">INPUTS</span></span>

### <span data-ttu-id="d9111-129">Keine</span><span class="sxs-lookup"><span data-stu-id="d9111-129">None</span></span>
<span data-ttu-id="d9111-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d9111-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9111-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9111-131">OUTPUTS</span></span>

### <span data-ttu-id="d9111-132">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="d9111-132">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="d9111-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9111-133">NOTES</span></span>

## <span data-ttu-id="d9111-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9111-134">RELATED LINKS</span></span>

[<span data-ttu-id="d9111-135">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="d9111-135">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="d9111-136">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="d9111-136">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

