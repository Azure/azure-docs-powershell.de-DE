---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 1fbf5a5541fe3e1360e696f9c06a26d6ea131dc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502721"
---
# <span data-ttu-id="772be-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="772be-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="772be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="772be-102">SYNOPSIS</span></span>
<span data-ttu-id="772be-103">Löscht einen Kontakt, der für Zertifikat Benachrichtigungen aus einem schlüsseltresor registriert ist.</span><span class="sxs-lookup"><span data-stu-id="772be-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="772be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="772be-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="772be-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="772be-105">DESCRIPTION</span></span>
<span data-ttu-id="772be-106">Das Cmdlet **Remove-AzureKeyVaultCertificateContact** löscht einen Kontakt, der für Zertifikat Benachrichtigungen aus einem schlüsseltresor registriert ist.</span><span class="sxs-lookup"><span data-stu-id="772be-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="772be-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="772be-107">EXAMPLES</span></span>

### <span data-ttu-id="772be-108">Beispiel 1: Entfernen eines Zertifikat Kontakts</span><span class="sxs-lookup"><span data-stu-id="772be-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="772be-109">Mit diesem Befehl wird Patti Fuller als Zertifikat Kontakt für den contoso01-schlüsseltresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="772be-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="772be-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="772be-110">PARAMETERS</span></span>

### <span data-ttu-id="772be-111">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="772be-111">-EmailAddress</span></span>
<span data-ttu-id="772be-112">Gibt die e-Mail-Adresse des zu entfernenden Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="772be-112">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="772be-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="772be-113">-PassThru</span></span>
<span data-ttu-id="772be-114">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="772be-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="772be-115">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="772be-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="772be-116">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="772be-116">-VaultName</span></span>
<span data-ttu-id="772be-117">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="772be-117">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="772be-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="772be-118">-Confirm</span></span>
<span data-ttu-id="772be-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="772be-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="772be-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="772be-120">-WhatIf</span></span>
<span data-ttu-id="772be-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="772be-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="772be-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="772be-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="772be-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="772be-123">-DefaultProfile</span></span>
<span data-ttu-id="772be-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="772be-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="772be-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="772be-125">CommonParameters</span></span>
<span data-ttu-id="772be-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="772be-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="772be-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="772be-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="772be-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="772be-128">INPUTS</span></span>

## <span data-ttu-id="772be-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="772be-129">OUTPUTS</span></span>

### <span data-ttu-id="772be-130">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="772be-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="772be-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="772be-131">NOTES</span></span>

## <span data-ttu-id="772be-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="772be-132">RELATED LINKS</span></span>

[<span data-ttu-id="772be-133">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="772be-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="772be-134">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="772be-134">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

