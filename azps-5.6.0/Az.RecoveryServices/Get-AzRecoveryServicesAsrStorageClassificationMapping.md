---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: c5dea86066fd2b7bc6bd3b2bd3eb7ac94f401895
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924520"
---
# <span data-ttu-id="164c6-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="164c6-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="164c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="164c6-102">SYNOPSIS</span></span>
<span data-ttu-id="164c6-103">Ruft ASR-Speicherklassifizierungszuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="164c6-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="164c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="164c6-104">SYNTAX</span></span>

### <span data-ttu-id="164c6-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="164c6-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="164c6-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="164c6-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="164c6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="164c6-107">DESCRIPTION</span></span>
<span data-ttu-id="164c6-108">Das **Get-AzRecoveryServicesAsrStorageClassificationMapping-Cmdlet** ruft die Details einer ASR-Speicherklassifizierungszuordnung ab.</span><span class="sxs-lookup"><span data-stu-id="164c6-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="164c6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="164c6-109">EXAMPLES</span></span>

### <span data-ttu-id="164c6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="164c6-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="164c6-111">Listen Sie alle Speicherklassifizierungszuordnungen auf, die der angegebenen Speicherklassifizierung entspricht.</span><span class="sxs-lookup"><span data-stu-id="164c6-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="164c6-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="164c6-112">PARAMETERS</span></span>

### <span data-ttu-id="164c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="164c6-113">-DefaultProfile</span></span>
<span data-ttu-id="164c6-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="164c6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="164c6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="164c6-115">-Name</span></span>
<span data-ttu-id="164c6-116">Gibt den Namen der zu erhaltenden Speicherklassifizierungszuordnung an.</span><span class="sxs-lookup"><span data-stu-id="164c6-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="164c6-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="164c6-117">-StorageClassification</span></span>
<span data-ttu-id="164c6-118">Gibt ein ASR-Speicherklassifizierungsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="164c6-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="164c6-119">Das Cmdlet ruft ASR-Speicherklassifizierungszuordnungen ab, die der angegebenen Speicherklassifizierung entsprechend sind.</span><span class="sxs-lookup"><span data-stu-id="164c6-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="164c6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="164c6-120">CommonParameters</span></span>
<span data-ttu-id="164c6-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="164c6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="164c6-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="164c6-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="164c6-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="164c6-123">INPUTS</span></span>

### <span data-ttu-id="164c6-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="164c6-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="164c6-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="164c6-125">OUTPUTS</span></span>

### <span data-ttu-id="164c6-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="164c6-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="164c6-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="164c6-127">NOTES</span></span>

## <span data-ttu-id="164c6-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="164c6-128">RELATED LINKS</span></span>

[<span data-ttu-id="164c6-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="164c6-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="164c6-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="164c6-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
