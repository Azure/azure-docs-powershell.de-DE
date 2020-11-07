---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: e02b60055818d1ed79e93e6853353795e78c5830
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842164"
---
# <span data-ttu-id="1d41a-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1d41a-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="1d41a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1d41a-102">SYNOPSIS</span></span>
<span data-ttu-id="1d41a-103">Ruft Kontakte ab, die für Zertifikat Benachrichtigungen für einen schlüsseltresor registriert sind.</span><span class="sxs-lookup"><span data-stu-id="1d41a-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="1d41a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d41a-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d41a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d41a-105">DESCRIPTION</span></span>
<span data-ttu-id="1d41a-106">Das Cmdlet " **Get-AzKeyVaultCertificateContact** " ruft Kontakte ab, die für Zertifikat Benachrichtigungen für einen schlüsseltresor im Azure Key Vault registriert sind.</span><span class="sxs-lookup"><span data-stu-id="1d41a-106">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="1d41a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d41a-107">EXAMPLES</span></span>

### <span data-ttu-id="1d41a-108">Beispiel 1: Abrufen aller Zertifikat Kontakte</span><span class="sxs-lookup"><span data-stu-id="1d41a-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="1d41a-109">Dieser Befehl ruft alle Kontakte für die Zertifikats Objekte im Contoso-Schlüsselspeicher ab und speichert Sie dann in der $Contacts-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1d41a-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="1d41a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d41a-110">PARAMETERS</span></span>

### <span data-ttu-id="1d41a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d41a-111">-DefaultProfile</span></span>
<span data-ttu-id="1d41a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1d41a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d41a-113">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="1d41a-113">-VaultName</span></span>
<span data-ttu-id="1d41a-114">Gibt den Namen des Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="1d41a-114">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="1d41a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d41a-115">CommonParameters</span></span>
<span data-ttu-id="1d41a-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d41a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d41a-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d41a-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d41a-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1d41a-118">INPUTS</span></span>

### <span data-ttu-id="1d41a-119">Keine</span><span class="sxs-lookup"><span data-stu-id="1d41a-119">None</span></span>
<span data-ttu-id="1d41a-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1d41a-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1d41a-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1d41a-121">OUTPUTS</span></span>

### <span data-ttu-id="1d41a-122">Liste<Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="1d41a-122">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="1d41a-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="1d41a-123">NOTES</span></span>

## <span data-ttu-id="1d41a-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1d41a-124">RELATED LINKS</span></span>

[<span data-ttu-id="1d41a-125">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1d41a-125">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="1d41a-126">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1d41a-126">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

