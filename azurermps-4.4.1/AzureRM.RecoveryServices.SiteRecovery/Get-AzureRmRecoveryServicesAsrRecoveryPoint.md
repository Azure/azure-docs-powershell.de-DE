---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 96a30621bc545b635262fd7937e0e55739d0be7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504790"
---
# <span data-ttu-id="960bf-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="960bf-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="960bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="960bf-102">SYNOPSIS</span></span>
<span data-ttu-id="960bf-103">Ruft die verfügbaren Wiederherstellungspunkte für ein geschütztes Replikations Element ab.</span><span class="sxs-lookup"><span data-stu-id="960bf-103">Gets the available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="960bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="960bf-104">SYNTAX</span></span>

### <span data-ttu-id="960bf-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="960bf-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [<CommonParameters>]
```

### <span data-ttu-id="960bf-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="960bf-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -Name <String>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [<CommonParameters>]
```

## <span data-ttu-id="960bf-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="960bf-107">DESCRIPTION</span></span>
<span data-ttu-id="960bf-108">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrRecoveryPoint** " Ruft die Liste der verfügbaren Wiederherstellungspunkte für ein geschütztes Replikations Element ab.</span><span class="sxs-lookup"><span data-stu-id="960bf-108">The **Get-AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="960bf-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="960bf-109">EXAMPLES</span></span>

### <span data-ttu-id="960bf-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="960bf-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="960bf-111">Ruft Wiederherstellungspunkte für das angegebene ASR-Replikations geschützte Element ab.</span><span class="sxs-lookup"><span data-stu-id="960bf-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="960bf-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="960bf-112">PARAMETERS</span></span>

### <span data-ttu-id="960bf-113">-Name</span><span class="sxs-lookup"><span data-stu-id="960bf-113">-Name</span></span>
<span data-ttu-id="960bf-114">Gibt den Namen des abzurufenden Wiederherstellungspunkts an.</span><span class="sxs-lookup"><span data-stu-id="960bf-114">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="960bf-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="960bf-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="960bf-116">Gibt das Azure Site Recovery Replication Protected Item-Objekt an, für das die Liste der verfügbaren Wiederherstellungspunkte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="960bf-116">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="960bf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="960bf-117">CommonParameters</span></span>
<span data-ttu-id="960bf-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="960bf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="960bf-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="960bf-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="960bf-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="960bf-120">INPUTS</span></span>

### <span data-ttu-id="960bf-121">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="960bf-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="960bf-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="960bf-122">OUTPUTS</span></span>

### <span data-ttu-id="960bf-123">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="960bf-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="960bf-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="960bf-124">NOTES</span></span>

## <span data-ttu-id="960bf-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="960bf-125">RELATED LINKS</span></span>

[<span data-ttu-id="960bf-126">Bearbeiten-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="960bf-126">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="960bf-127">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="960bf-127">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="960bf-128">Neu – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="960bf-128">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="960bf-129">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="960bf-129">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="960bf-130">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="960bf-130">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
