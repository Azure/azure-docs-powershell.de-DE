---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7ac4db45f9eb0332217c5097802904cd2146aca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504794"
---
# <span data-ttu-id="0d9db-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="0d9db-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="0d9db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d9db-102">SYNOPSIS</span></span>
<span data-ttu-id="0d9db-103">Ruft ASR-Replikationsrichtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="0d9db-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d9db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d9db-104">SYNTAX</span></span>

### <span data-ttu-id="0d9db-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="0d9db-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [<CommonParameters>]
```

### <span data-ttu-id="0d9db-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0d9db-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="0d9db-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="0d9db-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="0d9db-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d9db-108">DESCRIPTION</span></span>
<span data-ttu-id="0d9db-109">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrPolicy** " Ruft die Liste der konfigurierten Azure Site Recovery-Replikationsrichtlinien oder einer bestimmten Replikationsrichtlinie nach Namen ab.</span><span class="sxs-lookup"><span data-stu-id="0d9db-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="0d9db-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d9db-110">EXAMPLES</span></span>

### <span data-ttu-id="0d9db-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0d9db-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy -Name $PolicyName
```

<span data-ttu-id="0d9db-112">Retruns Sie die Replikationsrichtlinie mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="0d9db-112">Retruns the replication policy with the specified name.</span></span>

## <span data-ttu-id="0d9db-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d9db-113">PARAMETERS</span></span>

### <span data-ttu-id="0d9db-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0d9db-114">-FriendlyName</span></span>
<span data-ttu-id="0d9db-115">Gibt den Anzeigenamen der ASR-Replikationsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="0d9db-115">Specifies the friendly name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d9db-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0d9db-116">-Name</span></span>
<span data-ttu-id="0d9db-117">Gibt den Namen der ASR-Replikationsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="0d9db-117">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d9db-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d9db-118">CommonParameters</span></span>
<span data-ttu-id="0d9db-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d9db-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d9db-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d9db-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d9db-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d9db-121">INPUTS</span></span>

### <span data-ttu-id="0d9db-122">Keine</span><span class="sxs-lookup"><span data-stu-id="0d9db-122">None</span></span>

## <span data-ttu-id="0d9db-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d9db-123">OUTPUTS</span></span>

### <span data-ttu-id="0d9db-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0d9db-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0d9db-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d9db-125">NOTES</span></span>

## <span data-ttu-id="0d9db-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d9db-126">RELATED LINKS</span></span>

[<span data-ttu-id="0d9db-127">Neu – AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="0d9db-127">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="0d9db-128">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="0d9db-128">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
