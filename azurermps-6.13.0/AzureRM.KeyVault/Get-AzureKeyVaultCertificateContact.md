---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 31619366c1d2a1a025cb7ff563a04b166abb2a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664059"
---
# <span data-ttu-id="661b1-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="661b1-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="661b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="661b1-102">SYNOPSIS</span></span>
<span data-ttu-id="661b1-103">Ruft Kontakte ab, die für Zertifikat Benachrichtigungen für einen schlüsseltresor registriert sind.</span><span class="sxs-lookup"><span data-stu-id="661b1-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="661b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="661b1-104">SYNTAX</span></span>

### <span data-ttu-id="661b1-105">Vaultname (Standard)</span><span class="sxs-lookup"><span data-stu-id="661b1-105">VaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="661b1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="661b1-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="661b1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="661b1-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="661b1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="661b1-108">DESCRIPTION</span></span>
<span data-ttu-id="661b1-109">Das Cmdlet " **Get-AzureKeyVaultCertificateContact** " ruft Kontakte ab, die für Zertifikat Benachrichtigungen für einen schlüsseltresor im Azure Key Vault registriert sind.</span><span class="sxs-lookup"><span data-stu-id="661b1-109">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="661b1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="661b1-110">EXAMPLES</span></span>

### <span data-ttu-id="661b1-111">Beispiel 1: Abrufen aller Zertifikat Kontakte</span><span class="sxs-lookup"><span data-stu-id="661b1-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="661b1-112">Dieser Befehl ruft alle Kontakte für die Zertifikats Objekte im Contoso-Schlüsselspeicher ab und speichert Sie dann in der $Contacts-Variablen.</span><span class="sxs-lookup"><span data-stu-id="661b1-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="661b1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="661b1-113">PARAMETERS</span></span>

### <span data-ttu-id="661b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="661b1-114">-DefaultProfile</span></span>
<span data-ttu-id="661b1-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="661b1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="661b1-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="661b1-116">-InputObject</span></span>
<span data-ttu-id="661b1-117">Keyvault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="661b1-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="661b1-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="661b1-118">-ResourceId</span></span>
<span data-ttu-id="661b1-119">Keyvault-ID.</span><span class="sxs-lookup"><span data-stu-id="661b1-119">KeyVault Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="661b1-120">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="661b1-120">-VaultName</span></span>
<span data-ttu-id="661b1-121">Gibt den Namen des Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="661b1-121">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="661b1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="661b1-122">CommonParameters</span></span>
<span data-ttu-id="661b1-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="661b1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="661b1-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="661b1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="661b1-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="661b1-125">INPUTS</span></span>

### <span data-ttu-id="661b1-126">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="661b1-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="661b1-127">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="661b1-127">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="661b1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="661b1-128">System.String</span></span>

## <span data-ttu-id="661b1-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="661b1-129">OUTPUTS</span></span>

### <span data-ttu-id="661b1-130">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="661b1-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="661b1-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="661b1-131">NOTES</span></span>

## <span data-ttu-id="661b1-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="661b1-132">RELATED LINKS</span></span>

[<span data-ttu-id="661b1-133">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="661b1-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="661b1-134">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="661b1-134">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

