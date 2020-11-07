---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: cf60626ec04a2466fc9565aef5daff896281345d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662576"
---
# <span data-ttu-id="e60a8-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e60a8-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e60a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e60a8-102">SYNOPSIS</span></span>
<span data-ttu-id="e60a8-103">Ruft Kontakte ab, die für Zertifikat Benachrichtigungen für einen schlüsseltresor registriert sind.</span><span class="sxs-lookup"><span data-stu-id="e60a8-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e60a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e60a8-104">SYNTAX</span></span>

### <span data-ttu-id="e60a8-105">Vaultname (Standard)</span><span class="sxs-lookup"><span data-stu-id="e60a8-105">VaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e60a8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e60a8-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e60a8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e60a8-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e60a8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e60a8-108">DESCRIPTION</span></span>
<span data-ttu-id="e60a8-109">Das Cmdlet " **Get-AzureKeyVaultCertificateContact** " ruft Kontakte ab, die für Zertifikat Benachrichtigungen für einen schlüsseltresor im Azure Key Vault registriert sind.</span><span class="sxs-lookup"><span data-stu-id="e60a8-109">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="e60a8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e60a8-110">EXAMPLES</span></span>

### <span data-ttu-id="e60a8-111">Beispiel 1: Abrufen aller Zertifikat Kontakte</span><span class="sxs-lookup"><span data-stu-id="e60a8-111">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="e60a8-112">Dieser Befehl ruft alle Kontakte für die Zertifikats Objekte im Contoso-Schlüsselspeicher ab und speichert Sie dann in der $Contacts-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e60a8-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="e60a8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e60a8-113">PARAMETERS</span></span>

### <span data-ttu-id="e60a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e60a8-114">-DefaultProfile</span></span>
<span data-ttu-id="e60a8-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e60a8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e60a8-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e60a8-116">-InputObject</span></span>
<span data-ttu-id="e60a8-117">Keyvault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e60a8-117">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e60a8-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e60a8-118">-ResourceId</span></span>
<span data-ttu-id="e60a8-119">Keyvault-ID.</span><span class="sxs-lookup"><span data-stu-id="e60a8-119">KeyVault Id.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e60a8-120">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="e60a8-120">-VaultName</span></span>
<span data-ttu-id="e60a8-121">Gibt den Namen des Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="e60a8-121">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e60a8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e60a8-122">CommonParameters</span></span>
<span data-ttu-id="e60a8-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e60a8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e60a8-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e60a8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e60a8-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e60a8-125">INPUTS</span></span>

### <span data-ttu-id="e60a8-126">Keine</span><span class="sxs-lookup"><span data-stu-id="e60a8-126">None</span></span>
<span data-ttu-id="e60a8-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="e60a8-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e60a8-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e60a8-128">OUTPUTS</span></span>

### <span data-ttu-id="e60a8-129">Liste<Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="e60a8-129">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="e60a8-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="e60a8-130">NOTES</span></span>

## <span data-ttu-id="e60a8-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e60a8-131">RELATED LINKS</span></span>

[<span data-ttu-id="e60a8-132">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e60a8-132">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="e60a8-133">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e60a8-133">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

