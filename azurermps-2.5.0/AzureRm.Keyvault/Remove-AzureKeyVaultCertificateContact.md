---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: 9bfb62388ce4a7a8994f4a618a4c1a00ac5868d6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848236"
---
# <span data-ttu-id="9503f-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9503f-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="9503f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9503f-102">SYNOPSIS</span></span>
<span data-ttu-id="9503f-103">Löscht einen Kontakt, der für Zertifikat Benachrichtigungen aus einem schlüsseltresor registriert ist.</span><span class="sxs-lookup"><span data-stu-id="9503f-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9503f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9503f-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9503f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9503f-105">DESCRIPTION</span></span>
<span data-ttu-id="9503f-106">Das Cmdlet **Remove-AzureKeyVaultCertificateContact** löscht einen Kontakt, der für Zertifikat Benachrichtigungen aus einem schlüsseltresor registriert ist.</span><span class="sxs-lookup"><span data-stu-id="9503f-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="9503f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9503f-107">EXAMPLES</span></span>

### <span data-ttu-id="9503f-108">Beispiel 1: Entfernen eines Zertifikat Kontakts</span><span class="sxs-lookup"><span data-stu-id="9503f-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="9503f-109">Mit diesem Befehl wird Patti Fuller als Zertifikat Kontakt für den contoso01-schlüsseltresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="9503f-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="9503f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9503f-110">PARAMETERS</span></span>

### <span data-ttu-id="9503f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9503f-111">-DefaultProfile</span></span>
<span data-ttu-id="9503f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9503f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9503f-113">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="9503f-113">-EmailAddress</span></span>
<span data-ttu-id="9503f-114">Gibt die e-Mail-Adresse des zu entfernenden Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="9503f-114">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="9503f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9503f-115">-PassThru</span></span>
<span data-ttu-id="9503f-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="9503f-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9503f-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="9503f-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9503f-118">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="9503f-118">-VaultName</span></span>
<span data-ttu-id="9503f-119">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="9503f-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="9503f-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9503f-120">-Confirm</span></span>
<span data-ttu-id="9503f-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9503f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9503f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9503f-122">-WhatIf</span></span>
<span data-ttu-id="9503f-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9503f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9503f-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9503f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9503f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9503f-125">CommonParameters</span></span>
<span data-ttu-id="9503f-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9503f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9503f-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9503f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9503f-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9503f-128">INPUTS</span></span>

## <span data-ttu-id="9503f-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9503f-129">OUTPUTS</span></span>

### <span data-ttu-id="9503f-130">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="9503f-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="9503f-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="9503f-131">NOTES</span></span>

## <span data-ttu-id="9503f-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9503f-132">RELATED LINKS</span></span>

[<span data-ttu-id="9503f-133">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9503f-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="9503f-134">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9503f-134">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

