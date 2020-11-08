---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995307"
---
# <span data-ttu-id="bd95a-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="bd95a-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="bd95a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bd95a-102">SYNOPSIS</span></span>
<span data-ttu-id="bd95a-103">Ruft ASR-Speicher Klassifikations Zuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="bd95a-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="bd95a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd95a-104">SYNTAX</span></span>

### <span data-ttu-id="bd95a-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="bd95a-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd95a-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="bd95a-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd95a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd95a-107">DESCRIPTION</span></span>
<span data-ttu-id="bd95a-108">Das Cmdlet " **Get-AzRecoveryServicesAsrStorageClassificationMapping** " Ruft die Details einer ASR-Speicher Klassifikations Zuordnung ab.</span><span class="sxs-lookup"><span data-stu-id="bd95a-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="bd95a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd95a-109">EXAMPLES</span></span>

### <span data-ttu-id="bd95a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bd95a-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="bd95a-111">Listet alle Speicher Klassifikations Zuordnungen auf, die der angegebenen speicherklassifizierung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bd95a-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="bd95a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd95a-112">PARAMETERS</span></span>

### <span data-ttu-id="bd95a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd95a-113">-DefaultProfile</span></span>
<span data-ttu-id="bd95a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bd95a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bd95a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bd95a-115">-Name</span></span>
<span data-ttu-id="bd95a-116">Gibt den Namen der abzurufenden Speicher Klassifikations Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="bd95a-116">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd95a-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="bd95a-117">-StorageClassification</span></span>
<span data-ttu-id="bd95a-118">Gibt ein ASR-Speicher Klassifikations Objekt an.</span><span class="sxs-lookup"><span data-stu-id="bd95a-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="bd95a-119">Das Cmdlet ruft ASR-Speicher Klassifikations Zuordnungen ab, die der angegebenen speicherklassifizierung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bd95a-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd95a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd95a-120">CommonParameters</span></span>
<span data-ttu-id="bd95a-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd95a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd95a-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd95a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd95a-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bd95a-123">INPUTS</span></span>

### <span data-ttu-id="bd95a-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="bd95a-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="bd95a-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bd95a-125">OUTPUTS</span></span>

### <span data-ttu-id="bd95a-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="bd95a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="bd95a-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="bd95a-127">NOTES</span></span>

## <span data-ttu-id="bd95a-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bd95a-128">RELATED LINKS</span></span>

[<span data-ttu-id="bd95a-129">Neu – AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="bd95a-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="bd95a-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="bd95a-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
