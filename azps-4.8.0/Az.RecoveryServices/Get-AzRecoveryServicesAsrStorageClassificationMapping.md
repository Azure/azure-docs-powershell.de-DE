---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166176"
---
# <span data-ttu-id="f548f-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f548f-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="f548f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f548f-102">SYNOPSIS</span></span>
<span data-ttu-id="f548f-103">Ruft ASR-Speicher Klassifikations Zuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="f548f-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="f548f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f548f-104">SYNTAX</span></span>

### <span data-ttu-id="f548f-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="f548f-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f548f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f548f-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f548f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f548f-107">DESCRIPTION</span></span>
<span data-ttu-id="f548f-108">Das Cmdlet " **Get-AzRecoveryServicesAsrStorageClassificationMapping** " Ruft die Details einer ASR-Speicher Klassifikations Zuordnung ab.</span><span class="sxs-lookup"><span data-stu-id="f548f-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="f548f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f548f-109">EXAMPLES</span></span>

### <span data-ttu-id="f548f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f548f-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="f548f-111">Listet alle Speicher Klassifikations Zuordnungen auf, die der angegebenen speicherklassifizierung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f548f-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="f548f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f548f-112">PARAMETERS</span></span>

### <span data-ttu-id="f548f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f548f-113">-DefaultProfile</span></span>
<span data-ttu-id="f548f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f548f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f548f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f548f-115">-Name</span></span>
<span data-ttu-id="f548f-116">Gibt den Namen der abzurufenden Speicher Klassifikations Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="f548f-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="f548f-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="f548f-117">-StorageClassification</span></span>
<span data-ttu-id="f548f-118">Gibt ein ASR-Speicher Klassifikations Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f548f-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="f548f-119">Das Cmdlet ruft ASR-Speicher Klassifikations Zuordnungen ab, die der angegebenen speicherklassifizierung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f548f-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="f548f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f548f-120">CommonParameters</span></span>
<span data-ttu-id="f548f-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f548f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f548f-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f548f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f548f-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f548f-123">INPUTS</span></span>

### <span data-ttu-id="f548f-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="f548f-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="f548f-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f548f-125">OUTPUTS</span></span>

### <span data-ttu-id="f548f-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f548f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="f548f-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="f548f-127">NOTES</span></span>

## <span data-ttu-id="f548f-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f548f-128">RELATED LINKS</span></span>

[<span data-ttu-id="f548f-129">Neu – AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f548f-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="f548f-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f548f-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
