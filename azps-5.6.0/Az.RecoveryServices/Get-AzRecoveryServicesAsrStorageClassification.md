---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: 441e3108053aa55c93ab0f9ee150bebd592a091e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935568"
---
# <span data-ttu-id="8be50-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="8be50-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="8be50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8be50-102">SYNOPSIS</span></span>
<span data-ttu-id="8be50-103">Ruft die verfügbaren (ermittelten) ASR-Speicherklassifizierungen im Recovery Services-Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="8be50-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="8be50-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8be50-104">SYNTAX</span></span>

### <span data-ttu-id="8be50-105">ByFabricObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="8be50-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8be50-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="8be50-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8be50-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8be50-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8be50-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8be50-108">DESCRIPTION</span></span>
<span data-ttu-id="8be50-109">Das **Get-AzRecoveryServicesAsrStorageClassification-Cmdlet** ruft Details der ermittelten ASR-Speicherklassifizierungen im Recovery Services-Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="8be50-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="8be50-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8be50-110">EXAMPLES</span></span>

### <span data-ttu-id="8be50-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8be50-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="8be50-112">Listen Sie die ermittelten Speicherklassifizierungen auf, die der angegebenen ASR-Fabric entspricht.</span><span class="sxs-lookup"><span data-stu-id="8be50-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="8be50-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8be50-113">PARAMETERS</span></span>

### <span data-ttu-id="8be50-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be50-114">-DefaultProfile</span></span>
<span data-ttu-id="8be50-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8be50-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8be50-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="8be50-116">-Fabric</span></span>
<span data-ttu-id="8be50-117">Gibt ein ASR-Fabric-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8be50-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="8be50-118">Das Cmdlet ruft die Details der ermittelten Speicherklassifizierungen ab, die der angegebenen ASR-Fabric entspricht.</span><span class="sxs-lookup"><span data-stu-id="8be50-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8be50-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8be50-119">-FriendlyName</span></span>
<span data-ttu-id="8be50-120">Gibt den Anzeigenamen des zu erhaltenden Speicherklassifizierungsobjekts an.</span><span class="sxs-lookup"><span data-stu-id="8be50-120">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be50-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8be50-121">-Name</span></span>
<span data-ttu-id="8be50-122">Gibt den Namen des zu erhaltenden Speicherklassifizierungsobjekts an.</span><span class="sxs-lookup"><span data-stu-id="8be50-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="8be50-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be50-123">CommonParameters</span></span>
<span data-ttu-id="8be50-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be50-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be50-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8be50-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be50-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8be50-126">INPUTS</span></span>

### <span data-ttu-id="8be50-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="8be50-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="8be50-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8be50-128">OUTPUTS</span></span>

### <span data-ttu-id="8be50-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="8be50-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="8be50-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8be50-130">NOTES</span></span>

## <span data-ttu-id="8be50-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8be50-131">RELATED LINKS</span></span>
