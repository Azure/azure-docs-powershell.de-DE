---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 21a01ae07c383484a6ec8e17d9b09a93671bfbe2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480173"
---
# <span data-ttu-id="07117-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="07117-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="07117-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07117-102">SYNOPSIS</span></span>
<span data-ttu-id="07117-103">Ruft die verfügbaren Wiederherstellungspunkte für ein geschütztes Replikations Element ab.</span><span class="sxs-lookup"><span data-stu-id="07117-103">Gets the available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07117-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07117-104">SYNTAX</span></span>

### <span data-ttu-id="07117-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="07117-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07117-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="07117-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -Name <String>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07117-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07117-107">DESCRIPTION</span></span>
<span data-ttu-id="07117-108">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrRecoveryPoint** " Ruft die Liste der verfügbaren Wiederherstellungspunkte für ein geschütztes Replikations Element ab.</span><span class="sxs-lookup"><span data-stu-id="07117-108">The **Get-AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="07117-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07117-109">EXAMPLES</span></span>

### <span data-ttu-id="07117-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="07117-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="07117-111">Ruft Wiederherstellungspunkte für das angegebene ASR-Replikations geschützte Element ab.</span><span class="sxs-lookup"><span data-stu-id="07117-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="07117-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="07117-112">PARAMETERS</span></span>

### <span data-ttu-id="07117-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07117-113">-DefaultProfile</span></span>
<span data-ttu-id="07117-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07117-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07117-115">-Name</span><span class="sxs-lookup"><span data-stu-id="07117-115">-Name</span></span>
<span data-ttu-id="07117-116">Gibt den Namen des abzurufenden Wiederherstellungspunkts an.</span><span class="sxs-lookup"><span data-stu-id="07117-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="07117-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="07117-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="07117-118">Gibt das Azure Site Recovery Replication Protected Item-Objekt an, für das die Liste der verfügbaren Wiederherstellungspunkte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="07117-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07117-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07117-119">CommonParameters</span></span>
<span data-ttu-id="07117-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07117-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07117-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07117-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07117-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07117-122">INPUTS</span></span>

### <span data-ttu-id="07117-123">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="07117-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="07117-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07117-124">OUTPUTS</span></span>

### <span data-ttu-id="07117-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="07117-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="07117-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="07117-126">NOTES</span></span>

## <span data-ttu-id="07117-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07117-127">RELATED LINKS</span></span>

[<span data-ttu-id="07117-128">Bearbeiten-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07117-128">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="07117-129">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07117-129">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="07117-130">Neu – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07117-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="07117-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07117-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="07117-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07117-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
