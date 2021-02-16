---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceVaultSecretGroupObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
ms.openlocfilehash: 925d29e7d567613bbf10e88c65860ebe2ef40c2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167969"
---
# <span data-ttu-id="3c304-101">New-AzCloudServiceVaultSecretGroupObject</span><span class="sxs-lookup"><span data-stu-id="3c304-101">New-AzCloudServiceVaultSecretGroupObject</span></span>

## <span data-ttu-id="3c304-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c304-102">SYNOPSIS</span></span>
<span data-ttu-id="3c304-103">Erstellen eines Speicherobjekts für die geheime Tresorgruppe</span><span class="sxs-lookup"><span data-stu-id="3c304-103">Create a in-memory object for Vault Secret Group</span></span>

## <span data-ttu-id="3c304-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c304-104">SYNTAX</span></span>

```
New-AzCloudServiceVaultSecretGroupObject [-CertificateUrl <String[]>] [-Id <String>] [<CommonParameters>]
```

## <span data-ttu-id="3c304-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c304-105">DESCRIPTION</span></span>
<span data-ttu-id="3c304-106">Erstellen eines Speicherobjekts für die geheime Gruppe</span><span class="sxs-lookup"><span data-stu-id="3c304-106">Create a in-memory object for Secret Group</span></span>

## <span data-ttu-id="3c304-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3c304-107">EXAMPLES</span></span>

### <span data-ttu-id="3c304-108">Beispiel 1: Erstellen des geheimen Gruppenobjekts "Tresor"</span><span class="sxs-lookup"><span data-stu-id="3c304-108">Example 1: Create vault secret group object</span></span>
```powershell
$keyVault = Get-AzKeyVault -VaultName 'ContosoKeyVault'
$certificate = Get-AzKeyVaultCertificate -VaultName 'ContosoKeyVault' -Name 'ContosoCert'
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
```

<span data-ttu-id="3c304-109">Dieser Befehl erstellt das geheime Gruppenobjekt des Tresors, das zum Erstellen oder Aktualisieren eines Clouddiensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3c304-109">This command creates vault secret group object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="3c304-110">Weitere Details finden Sie unter "New-AzCloudService".</span><span class="sxs-lookup"><span data-stu-id="3c304-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="3c304-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c304-111">PARAMETERS</span></span>

### <span data-ttu-id="3c304-112">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="3c304-112">-CertificateUrl</span></span>
<span data-ttu-id="3c304-113">Dies ist die URL eines Zertifikats, das als geheimer Schlüssel in den Schlüsseltresor hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="3c304-113">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c304-114">-ID</span><span class="sxs-lookup"><span data-stu-id="3c304-114">-Id</span></span>
<span data-ttu-id="3c304-115">Ressourcen-ID des Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="3c304-115">Key Vault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c304-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c304-116">CommonParameters</span></span>
<span data-ttu-id="3c304-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c304-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c304-118">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c304-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c304-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3c304-119">INPUTS</span></span>

## <span data-ttu-id="3c304-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3c304-120">OUTPUTS</span></span>

### <span data-ttu-id="3c304-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span><span class="sxs-lookup"><span data-stu-id="3c304-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span></span>

## <span data-ttu-id="3c304-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3c304-122">NOTES</span></span>

<span data-ttu-id="3c304-123">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3c304-123">ALIASES</span></span>

## <span data-ttu-id="3c304-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3c304-124">RELATED LINKS</span></span>

