---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 6a59b49da2ae283af50487bec21da6c1d2457878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664266"
---
# <span data-ttu-id="6259c-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="6259c-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="6259c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6259c-102">SYNOPSIS</span></span>
<span data-ttu-id="6259c-103">Ruft Kontakte ab, die für Zertifikat Benachrichtigungen für einen schlüsseltresor registriert sind.</span><span class="sxs-lookup"><span data-stu-id="6259c-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6259c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6259c-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6259c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6259c-105">DESCRIPTION</span></span>
<span data-ttu-id="6259c-106">Das Cmdlet " **Get-AzureKeyVaultCertificateContact** " ruft Kontakte ab, die für Zertifikat Benachrichtigungen für einen schlüsseltresor im Azure Key Vault registriert sind.</span><span class="sxs-lookup"><span data-stu-id="6259c-106">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="6259c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6259c-107">EXAMPLES</span></span>

### <span data-ttu-id="6259c-108">Beispiel 1: Abrufen aller Zertifikat Kontakte</span><span class="sxs-lookup"><span data-stu-id="6259c-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="6259c-109">Dieser Befehl ruft alle Kontakte für die Zertifikats Objekte im Contoso-Schlüsselspeicher ab und speichert Sie dann in der $Contacts-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6259c-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="6259c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6259c-110">PARAMETERS</span></span>

### <span data-ttu-id="6259c-111">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="6259c-111">-VaultName</span></span>
<span data-ttu-id="6259c-112">Gibt den Namen des Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="6259c-112">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="6259c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6259c-113">-DefaultProfile</span></span>
<span data-ttu-id="6259c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6259c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6259c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6259c-115">CommonParameters</span></span>
<span data-ttu-id="6259c-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6259c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6259c-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6259c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6259c-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6259c-118">INPUTS</span></span>

## <span data-ttu-id="6259c-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6259c-119">OUTPUTS</span></span>

### <span data-ttu-id="6259c-120">Liste<Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="6259c-120">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="6259c-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="6259c-121">NOTES</span></span>

## <span data-ttu-id="6259c-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6259c-122">RELATED LINKS</span></span>

[<span data-ttu-id="6259c-123">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="6259c-123">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="6259c-124">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="6259c-124">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

