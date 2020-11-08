---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: a5265f6c824160ccd06022d54613818131f4da94
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995313"
---
# <span data-ttu-id="e1703-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e1703-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="e1703-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1703-102">SYNOPSIS</span></span>
<span data-ttu-id="e1703-103">Ruft die verfügbaren (gefundenen) ASR-Speicher Klassifikationen im Recovery Services Vault ab.</span><span class="sxs-lookup"><span data-stu-id="e1703-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="e1703-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1703-104">SYNTAX</span></span>

### <span data-ttu-id="e1703-105">ByFabricObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1703-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1703-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="e1703-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1703-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e1703-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1703-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1703-108">DESCRIPTION</span></span>
<span data-ttu-id="e1703-109">Das Cmdlet " **Get-AzRecoveryServicesAsrStorageClassification** " ruft Details der erkannten ASR-Speicher Klassifikationen im Recovery Services Vault ab.</span><span class="sxs-lookup"><span data-stu-id="e1703-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="e1703-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1703-110">EXAMPLES</span></span>

### <span data-ttu-id="e1703-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e1703-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="e1703-112">Listen Sie die ermittelten Speicher Klassifikationen auf, die dem angegebenen ASR-Fabric entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e1703-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="e1703-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1703-113">PARAMETERS</span></span>

### <span data-ttu-id="e1703-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1703-114">-DefaultProfile</span></span>
<span data-ttu-id="e1703-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1703-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e1703-116">-Stoff</span><span class="sxs-lookup"><span data-stu-id="e1703-116">-Fabric</span></span>
<span data-ttu-id="e1703-117">Gibt ein ASR-Fabric-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e1703-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="e1703-118">Das Cmdlet ruft die Details der erkannten Speicher Klassifizierungen ab, die dem angegebenen ASR-Fabric entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e1703-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="e1703-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e1703-119">-FriendlyName</span></span>
<span data-ttu-id="e1703-120">Gibt den Anzeigenamen des abzurufenden Speicher Klassifizierungs Objekts an.</span><span class="sxs-lookup"><span data-stu-id="e1703-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="e1703-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e1703-121">-Name</span></span>
<span data-ttu-id="e1703-122">Gibt den Namen des abzurufenden Speicher Klassifizierungs Objekts an.</span><span class="sxs-lookup"><span data-stu-id="e1703-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="e1703-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1703-123">CommonParameters</span></span>
<span data-ttu-id="e1703-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1703-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1703-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1703-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1703-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1703-126">INPUTS</span></span>

### <span data-ttu-id="e1703-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e1703-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="e1703-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1703-128">OUTPUTS</span></span>

### <span data-ttu-id="e1703-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e1703-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="e1703-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1703-130">NOTES</span></span>

## <span data-ttu-id="e1703-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1703-131">RELATED LINKS</span></span>
