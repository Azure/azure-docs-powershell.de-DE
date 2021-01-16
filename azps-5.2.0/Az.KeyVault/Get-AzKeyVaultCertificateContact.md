---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ca7f0f87ebcbad3d613939f2e73a743763b134c9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289943"
---
# <span data-ttu-id="fcef5-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="fcef5-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="fcef5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcef5-102">SYNOPSIS</span></span>
<span data-ttu-id="fcef5-103">Ruft Kontakte ab, die für Zertifikatbenachrichtigungen für einen Schlüsseltresor registriert sind.</span><span class="sxs-lookup"><span data-stu-id="fcef5-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="fcef5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcef5-104">SYNTAX</span></span>

### <span data-ttu-id="fcef5-105">VaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fcef5-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fcef5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fcef5-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fcef5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fcef5-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fcef5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fcef5-108">DESCRIPTION</span></span>
<span data-ttu-id="fcef5-109">Das **Cmdlet "Get-AzKeyVaultCertificateContact"** ruft Kontakte ab, die für Zertifikatbenachrichtigungen für einen Schlüsseltresor im Azure Key Vault registriert sind.</span><span class="sxs-lookup"><span data-stu-id="fcef5-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="fcef5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fcef5-110">EXAMPLES</span></span>

### <span data-ttu-id="fcef5-111">Beispiel 1: Alle Zertifikatkontakte erhalten</span><span class="sxs-lookup"><span data-stu-id="fcef5-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="fcef5-112">Dieser Befehl ruft alle Kontakte für die Zertifikatobjekte im Schlüsseltresor von Contoso ab und speichert sie dann in der $Contacts Variable.</span><span class="sxs-lookup"><span data-stu-id="fcef5-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="fcef5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcef5-113">PARAMETERS</span></span>

### <span data-ttu-id="fcef5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcef5-114">-DefaultProfile</span></span>
<span data-ttu-id="fcef5-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fcef5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcef5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcef5-116">-InputObject</span></span>
<span data-ttu-id="fcef5-117">KeyVault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fcef5-117">KeyVault object.</span></span>

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

### <span data-ttu-id="fcef5-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fcef5-118">-ResourceId</span></span>
<span data-ttu-id="fcef5-119">KeyVault-ID.</span><span class="sxs-lookup"><span data-stu-id="fcef5-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="fcef5-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fcef5-120">-VaultName</span></span>
<span data-ttu-id="fcef5-121">Gibt den Namen des Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="fcef5-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="fcef5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcef5-122">CommonParameters</span></span>
<span data-ttu-id="fcef5-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcef5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcef5-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcef5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcef5-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fcef5-125">INPUTS</span></span>

### <span data-ttu-id="fcef5-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="fcef5-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="fcef5-127">System.String</span><span class="sxs-lookup"><span data-stu-id="fcef5-127">System.String</span></span>

## <span data-ttu-id="fcef5-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fcef5-128">OUTPUTS</span></span>

### <span data-ttu-id="fcef5-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="fcef5-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="fcef5-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fcef5-130">NOTES</span></span>

## <span data-ttu-id="fcef5-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fcef5-131">RELATED LINKS</span></span>

[<span data-ttu-id="fcef5-132">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="fcef5-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="fcef5-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="fcef5-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

