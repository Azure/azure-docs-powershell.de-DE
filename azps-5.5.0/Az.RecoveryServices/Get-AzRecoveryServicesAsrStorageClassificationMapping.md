---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160233"
---
# <span data-ttu-id="5d5d2-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5d5d2-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="5d5d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="5d5d2-103">Ruft die Zuordnungen der ASR-Speicherklassifizierung ab.</span><span class="sxs-lookup"><span data-stu-id="5d5d2-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="5d5d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d5d2-104">SYNTAX</span></span>

### <span data-ttu-id="5d5d2-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d5d2-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d5d2-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="5d5d2-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d5d2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d5d2-107">DESCRIPTION</span></span>
<span data-ttu-id="5d5d2-108">Das **Cmdlet "Get-AzRecoveryServicesAsrStorageClassificationMapping"** ruft die Details einer ASR-Speicherklassifizierungszuordnung ab.</span><span class="sxs-lookup"><span data-stu-id="5d5d2-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="5d5d2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5d5d2-109">EXAMPLES</span></span>

### <span data-ttu-id="5d5d2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d5d2-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="5d5d2-111">Listet alle Speicherklassifizierungszuordnungen auf, die der angegebenen Speicherklassifizierung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5d5d2-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="5d5d2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d5d2-112">PARAMETERS</span></span>

### <span data-ttu-id="5d5d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d5d2-113">-DefaultProfile</span></span>
<span data-ttu-id="5d5d2-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d5d2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5d5d2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5d5d2-115">-Name</span></span>
<span data-ttu-id="5d5d2-116">Gibt den Namen der speicherklassifizierungszuordnung an, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="5d5d2-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="5d5d2-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="5d5d2-117">-StorageClassification</span></span>
<span data-ttu-id="5d5d2-118">Gibt ein AsR-Speicherklassifikationsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="5d5d2-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="5d5d2-119">Das Cmdlet ruft die Zuordnungen der ASR-Speicherklassifizierung ab, die der angegebenen Speicherklassifizierung</span><span class="sxs-lookup"><span data-stu-id="5d5d2-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="5d5d2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d5d2-120">CommonParameters</span></span>
<span data-ttu-id="5d5d2-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d5d2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d5d2-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d5d2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d5d2-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5d5d2-123">INPUTS</span></span>

### <span data-ttu-id="5d5d2-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="5d5d2-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="5d5d2-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5d5d2-125">OUTPUTS</span></span>

### <span data-ttu-id="5d5d2-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5d5d2-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="5d5d2-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5d5d2-127">NOTES</span></span>

## <span data-ttu-id="5d5d2-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5d5d2-128">RELATED LINKS</span></span>

[<span data-ttu-id="5d5d2-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5d5d2-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="5d5d2-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5d5d2-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
