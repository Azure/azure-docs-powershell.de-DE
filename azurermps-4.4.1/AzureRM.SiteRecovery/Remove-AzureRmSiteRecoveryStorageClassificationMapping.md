---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 441478B4-1453-4A11-AD52-53ADB85E194F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 59ae0324a5e42e87192e655352fce074413907ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663521"
---
# <span data-ttu-id="c5c65-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c5c65-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="c5c65-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5c65-102">SYNOPSIS</span></span>
<span data-ttu-id="c5c65-103">Entfernt eine Speicher Klassifikations Zuordnung aus der Websitewiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="c5c65-103">Removes a storage classification mapping from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5c65-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5c65-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryStorageClassificationMapping
 -StorageClassificationMapping <ASRStorageClassificationMapping> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5c65-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5c65-105">DESCRIPTION</span></span>
<span data-ttu-id="c5c65-106">Das Cmdlet **Remove-AzureRmSiteRecoveryStorageClassificationMapping** entfernt eine Speicher Klassifikations Zuordnung aus Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c5c65-106">The **Remove-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet removes a storage classification mapping from Azure Site Recovery.</span></span>

## <span data-ttu-id="c5c65-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5c65-107">EXAMPLES</span></span>

## <span data-ttu-id="c5c65-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5c65-108">PARAMETERS</span></span>

### <span data-ttu-id="c5c65-109">-StorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c5c65-109">-StorageClassificationMapping</span></span>
<span data-ttu-id="c5c65-110">Gibt eine Speicher Klassifikations Zuordnung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c5c65-110">Specifies a storage classification mapping that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5c65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5c65-111">-DefaultProfile</span></span>
<span data-ttu-id="c5c65-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5c65-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5c65-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5c65-113">CommonParameters</span></span>
<span data-ttu-id="c5c65-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5c65-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5c65-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5c65-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5c65-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5c65-116">INPUTS</span></span>

### <span data-ttu-id="c5c65-117">ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c5c65-117">ASRStorageClassificationMapping</span></span>
<span data-ttu-id="c5c65-118">Der Parameter "StorageClassificationMapping" akzeptiert den Wert vom Typ "ASRStorageClassificationMapping" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c5c65-118">Parameter 'StorageClassificationMapping' accepts value of type 'ASRStorageClassificationMapping' from the pipeline</span></span>

## <span data-ttu-id="c5c65-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5c65-119">OUTPUTS</span></span>

### <span data-ttu-id="c5c65-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c5c65-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c5c65-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5c65-121">NOTES</span></span>

## <span data-ttu-id="c5c65-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5c65-122">RELATED LINKS</span></span>

[<span data-ttu-id="c5c65-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c5c65-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="c5c65-124">Neu – AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c5c65-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)
