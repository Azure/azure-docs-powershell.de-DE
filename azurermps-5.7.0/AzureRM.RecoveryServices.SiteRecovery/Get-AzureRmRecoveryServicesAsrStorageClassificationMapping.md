---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 53a877543cc3811ccf52d240025135fefa3ede0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482849"
---
# <span data-ttu-id="cfbfb-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="cfbfb-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="cfbfb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cfbfb-102">SYNOPSIS</span></span>
<span data-ttu-id="cfbfb-103">Ruft ASR-Speicher Klassifikations Zuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="cfbfb-103">Gets ASR storage classification mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfbfb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfbfb-104">SYNTAX</span></span>

### <span data-ttu-id="cfbfb-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="cfbfb-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfbfb-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="cfbfb-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfbfb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cfbfb-107">DESCRIPTION</span></span>
<span data-ttu-id="cfbfb-108">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** " Ruft die Details einer ASR-Speicher Klassifikations Zuordnung ab.</span><span class="sxs-lookup"><span data-stu-id="cfbfb-108">The **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="cfbfb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cfbfb-109">EXAMPLES</span></span>

### <span data-ttu-id="cfbfb-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cfbfb-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="cfbfb-111">Listet alle Speicher Klassifikations Zuordnungen auf, die der angegebenen speicherklassifizierung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cfbfb-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="cfbfb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfbfb-112">PARAMETERS</span></span>

### <span data-ttu-id="cfbfb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfbfb-113">-DefaultProfile</span></span>
<span data-ttu-id="cfbfb-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cfbfb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="cfbfb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="cfbfb-115">-Name</span></span>
<span data-ttu-id="cfbfb-116">Gibt den Namen der abzurufenden Speicher Klassifikations Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="cfbfb-116">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfbfb-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="cfbfb-117">-StorageClassification</span></span>
<span data-ttu-id="cfbfb-118">Gibt ein ASR-Speicher Klassifikations Objekt an.</span><span class="sxs-lookup"><span data-stu-id="cfbfb-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="cfbfb-119">Das Cmdlet ruft ASR-Speicher Klassifikations Zuordnungen ab, die der angegebenen speicherklassifizierung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cfbfb-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="cfbfb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfbfb-120">CommonParameters</span></span>
<span data-ttu-id="cfbfb-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfbfb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfbfb-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfbfb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfbfb-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cfbfb-123">INPUTS</span></span>

### <span data-ttu-id="cfbfb-124">Keine</span><span class="sxs-lookup"><span data-stu-id="cfbfb-124">None</span></span>

## <span data-ttu-id="cfbfb-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cfbfb-125">OUTPUTS</span></span>

### <span data-ttu-id="cfbfb-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cfbfb-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cfbfb-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="cfbfb-127">NOTES</span></span>

## <span data-ttu-id="cfbfb-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cfbfb-128">RELATED LINKS</span></span>

[<span data-ttu-id="cfbfb-129">Neu – AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="cfbfb-129">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="cfbfb-130">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="cfbfb-130">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
