---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: a5265f6c824160ccd06022d54613818131f4da94
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306171"
---
# <span data-ttu-id="2f735-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2f735-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="2f735-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f735-102">SYNOPSIS</span></span>
<span data-ttu-id="2f735-103">Ruft die verfügbaren (ermittelten) ASR-Speicherklassifizierungen im Wiederherstellungsdiensttresor ab.</span><span class="sxs-lookup"><span data-stu-id="2f735-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="2f735-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f735-104">SYNTAX</span></span>

### <span data-ttu-id="2f735-105">ByFabricObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f735-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f735-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="2f735-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f735-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="2f735-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f735-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f735-108">DESCRIPTION</span></span>
<span data-ttu-id="2f735-109">Das **Cmdlet "Get-AzRecoveryServicesAsrStorageClassification"** ruft Details der ermittelten ASR-Speicherklassifizierungen im Wiederherstellungsdiensttresor ab.</span><span class="sxs-lookup"><span data-stu-id="2f735-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="2f735-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2f735-110">EXAMPLES</span></span>

### <span data-ttu-id="2f735-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2f735-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="2f735-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span><span class="sxs-lookup"><span data-stu-id="2f735-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="2f735-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f735-113">PARAMETERS</span></span>

### <span data-ttu-id="2f735-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f735-114">-DefaultProfile</span></span>
<span data-ttu-id="2f735-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f735-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2f735-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="2f735-116">-Fabric</span></span>
<span data-ttu-id="2f735-117">Gibt ein ASR-Fabric-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2f735-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="2f735-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span><span class="sxs-lookup"><span data-stu-id="2f735-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="2f735-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2f735-119">-FriendlyName</span></span>
<span data-ttu-id="2f735-120">Gibt den Anzeigenamen des speicherklassifizierungsobjekts an, das sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="2f735-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="2f735-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2f735-121">-Name</span></span>
<span data-ttu-id="2f735-122">Gibt den Namen des speicherklassifizierungsobjekts an, das sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="2f735-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="2f735-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f735-123">CommonParameters</span></span>
<span data-ttu-id="2f735-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f735-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f735-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f735-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f735-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2f735-126">INPUTS</span></span>

### <span data-ttu-id="2f735-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="2f735-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="2f735-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2f735-128">OUTPUTS</span></span>

### <span data-ttu-id="2f735-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2f735-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="2f735-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2f735-130">NOTES</span></span>

## <span data-ttu-id="2f735-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2f735-131">RELATED LINKS</span></span>
