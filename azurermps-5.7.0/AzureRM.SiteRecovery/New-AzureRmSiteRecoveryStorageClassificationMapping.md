---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4B4CB198-ABD3-4926-808D-2087151EA06B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 86d8cc4b48342b49e807635e6fb51c5f4028b172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480877"
---
# <span data-ttu-id="31333-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="31333-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="31333-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31333-102">SYNOPSIS</span></span>
<span data-ttu-id="31333-103">Erstellt eine Speicher Klassifikations Zuordnung in der Websitewiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="31333-103">Creates a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31333-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31333-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryStorageClassificationMapping [-Name <String>]
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31333-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31333-105">DESCRIPTION</span></span>
<span data-ttu-id="31333-106">Das Cmdlet **New-AzureRmSiteRecoveryStorageClassificationMapping** erstellt eine Speicher Klassifikations Zuordnung in Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="31333-106">The **New-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet creates a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="31333-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31333-107">EXAMPLES</span></span>

## <span data-ttu-id="31333-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="31333-108">PARAMETERS</span></span>

### <span data-ttu-id="31333-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31333-109">-DefaultProfile</span></span>
<span data-ttu-id="31333-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="31333-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31333-111">-Name</span><span class="sxs-lookup"><span data-stu-id="31333-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31333-112">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="31333-112">-PrimaryStorageClassification</span></span>
<span data-ttu-id="31333-113">Gibt die primäre Speicher Klassifikations Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="31333-113">Specifies the primary storage classification mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31333-114">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="31333-114">-RecoveryStorageClassification</span></span>
<span data-ttu-id="31333-115">Gibt eine Speicher Klassifikations Zuordnung für die Wiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="31333-115">Specifies a recovery storage classification mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31333-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31333-116">CommonParameters</span></span>
<span data-ttu-id="31333-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31333-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31333-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31333-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31333-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31333-119">INPUTS</span></span>

### <span data-ttu-id="31333-120">ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="31333-120">ASRStorageClassification</span></span>
<span data-ttu-id="31333-121">Der Parameter "PrimaryStorageClassification" akzeptiert den Wert vom Typ "ASRStorageClassification" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="31333-121">Parameter 'PrimaryStorageClassification' accepts value of type 'ASRStorageClassification' from the pipeline</span></span>

## <span data-ttu-id="31333-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31333-122">OUTPUTS</span></span>

### <span data-ttu-id="31333-123">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="31333-123">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="31333-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="31333-124">NOTES</span></span>

## <span data-ttu-id="31333-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31333-125">RELATED LINKS</span></span>

[<span data-ttu-id="31333-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="31333-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="31333-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="31333-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
