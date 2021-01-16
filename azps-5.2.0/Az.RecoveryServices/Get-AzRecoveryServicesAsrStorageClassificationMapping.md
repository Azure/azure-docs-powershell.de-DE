---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306163"
---
# <span data-ttu-id="4c294-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="4c294-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="4c294-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c294-102">SYNOPSIS</span></span>
<span data-ttu-id="4c294-103">Ruft die Zuordnungen der ASR-Speicherklassifizierung ab.</span><span class="sxs-lookup"><span data-stu-id="4c294-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="4c294-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c294-104">SYNTAX</span></span>

### <span data-ttu-id="4c294-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="4c294-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c294-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="4c294-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c294-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4c294-107">DESCRIPTION</span></span>
<span data-ttu-id="4c294-108">Das **Cmdlet "Get-AzRecoveryServicesAsrStorageClassificationMapping"** ruft die Details einer ASR-Speicherklassifizierungszuordnung ab.</span><span class="sxs-lookup"><span data-stu-id="4c294-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="4c294-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4c294-109">EXAMPLES</span></span>

### <span data-ttu-id="4c294-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4c294-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="4c294-111">Listet alle Speicherklassifizierungszuordnungen auf, die der angegebenen Speicherklassifizierung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4c294-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="4c294-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c294-112">PARAMETERS</span></span>

### <span data-ttu-id="4c294-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c294-113">-DefaultProfile</span></span>
<span data-ttu-id="4c294-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c294-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4c294-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4c294-115">-Name</span></span>
<span data-ttu-id="4c294-116">Gibt den Namen der speicherklassifizierungszuordnung an, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="4c294-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="4c294-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="4c294-117">-StorageClassification</span></span>
<span data-ttu-id="4c294-118">Gibt ein AsR-Speicherklassifikationsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="4c294-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="4c294-119">Das Cmdlet ruft die Zuordnungen der ASR-Speicherklassifizierung ab, die der angegebenen Speicherklassifizierung</span><span class="sxs-lookup"><span data-stu-id="4c294-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="4c294-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c294-120">CommonParameters</span></span>
<span data-ttu-id="4c294-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c294-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c294-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c294-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c294-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4c294-123">INPUTS</span></span>

### <span data-ttu-id="4c294-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="4c294-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="4c294-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4c294-125">OUTPUTS</span></span>

### <span data-ttu-id="4c294-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="4c294-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="4c294-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4c294-127">NOTES</span></span>

## <span data-ttu-id="4c294-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4c294-128">RELATED LINKS</span></span>

[<span data-ttu-id="4c294-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="4c294-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="4c294-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="4c294-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
