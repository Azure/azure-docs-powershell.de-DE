---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceVaultSecretGroupObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
ms.openlocfilehash: f4d45cddd893ece419fab38759425bb104b64522
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940584"
---
# <span data-ttu-id="3559d-101">New-AzCloudServiceVaultSecretGroupObject</span><span class="sxs-lookup"><span data-stu-id="3559d-101">New-AzCloudServiceVaultSecretGroupObject</span></span>

## <span data-ttu-id="3559d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3559d-102">SYNOPSIS</span></span>
<span data-ttu-id="3559d-103">Erstellen eines Speicherobjekts für die Gruppe "Geheimer Tresor"</span><span class="sxs-lookup"><span data-stu-id="3559d-103">Create a in-memory object for Vault Secret Group</span></span>

## <span data-ttu-id="3559d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3559d-104">SYNTAX</span></span>

```
New-AzCloudServiceVaultSecretGroupObject [-CertificateUrl <String[]>] [-Id <String>] [<CommonParameters>]
```

## <span data-ttu-id="3559d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3559d-105">DESCRIPTION</span></span>
<span data-ttu-id="3559d-106">Erstellen eines Speicherobjekts für geheime Gruppe</span><span class="sxs-lookup"><span data-stu-id="3559d-106">Create a in-memory object for Secret Group</span></span>

## <span data-ttu-id="3559d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3559d-107">EXAMPLES</span></span>

### <span data-ttu-id="3559d-108">Beispiel 1: Erstellen eines geheimen Gruppenobjekts für den Tresor</span><span class="sxs-lookup"><span data-stu-id="3559d-108">Example 1: Create vault secret group object</span></span>
```powershell
$keyVault = Get-AzKeyVault -VaultName 'ContosoKeyVault'
$certificate = Get-AzKeyVaultCertificate -VaultName 'ContosoKeyVault' -Name 'ContosoCert'
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
```

<span data-ttu-id="3559d-109">Mit diesem Befehl wird das geheime Gruppenobjekt des Tresors erstellt, das zum Erstellen oder Aktualisieren eines Clouddiensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3559d-109">This command creates vault secret group object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="3559d-110">Weitere Informationen finden Sie unter New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="3559d-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="3559d-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3559d-111">PARAMETERS</span></span>

### <span data-ttu-id="3559d-112">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="3559d-112">-CertificateUrl</span></span>
<span data-ttu-id="3559d-113">Dies ist die URL eines Zertifikats, das als Geheimer in den Schlüsseltresor hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="3559d-113">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

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

### <span data-ttu-id="3559d-114">-ID</span><span class="sxs-lookup"><span data-stu-id="3559d-114">-Id</span></span>
<span data-ttu-id="3559d-115">Key Vault Resource Id.</span><span class="sxs-lookup"><span data-stu-id="3559d-115">Key Vault Resource Id.</span></span>

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

### <span data-ttu-id="3559d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3559d-116">CommonParameters</span></span>
<span data-ttu-id="3559d-117">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3559d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3559d-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3559d-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3559d-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3559d-119">INPUTS</span></span>

## <span data-ttu-id="3559d-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3559d-120">OUTPUTS</span></span>

### <span data-ttu-id="3559d-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span><span class="sxs-lookup"><span data-stu-id="3559d-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span></span>

## <span data-ttu-id="3559d-122">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3559d-122">NOTES</span></span>

<span data-ttu-id="3559d-123">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3559d-123">ALIASES</span></span>

## <span data-ttu-id="3559d-124">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3559d-124">RELATED LINKS</span></span>

