---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 86A60FD6-551A-4A6B-A4D1-466F33CE714A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
ms.openlocfilehash: 97ebacf9f5c51778122bfb8e8157692b7f1dfd03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502346"
---
# <span data-ttu-id="26c2f-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="26c2f-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span></span>

## <span data-ttu-id="26c2f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="26c2f-103">Ändert einen Wiederherstellungspunkt für ein fehlerhaft über geschütztes Element, bevor der Failovervorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26c2f-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26c2f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26c2f-104">SYNTAX</span></span>

```
Start-AzureRmSiteRecoveryApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26c2f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26c2f-105">DESCRIPTION</span></span>
<span data-ttu-id="26c2f-106">Die **Start-AzureRmSiteRecoveryApplyRecoveryPoint** ändert einen Wiederherstellungspunkt für ein fehlerhaft über geschütztes Element, bevor ein Commit für den Failovervorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26c2f-106">The **Start-AzureRmSiteRecoveryApplyRecoveryPoint** changes a recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="26c2f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26c2f-107">EXAMPLES</span></span>

## <span data-ttu-id="26c2f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="26c2f-108">PARAMETERS</span></span>

### <span data-ttu-id="26c2f-109">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="26c2f-109">-DataEncryptionPrimaryCertFile</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26c2f-110">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="26c2f-110">-DataEncryptionSecondaryCertFile</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26c2f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26c2f-111">-DefaultProfile</span></span>
<span data-ttu-id="26c2f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="26c2f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26c2f-113">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="26c2f-113">-RecoveryPoint</span></span>
<span data-ttu-id="26c2f-114">Gibt das Wiederherstellungspunkt Objekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="26c2f-114">Specifies the recovery point object that this cmdlet changes.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26c2f-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="26c2f-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="26c2f-116">Gibt das Objekt mit dem Replikations geschützten Element an.</span><span class="sxs-lookup"><span data-stu-id="26c2f-116">Specifies the Replication Protected Item object.</span></span>

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

### <span data-ttu-id="26c2f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26c2f-117">CommonParameters</span></span>
<span data-ttu-id="26c2f-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26c2f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26c2f-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26c2f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26c2f-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26c2f-120">INPUTS</span></span>

### <span data-ttu-id="26c2f-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="26c2f-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="26c2f-122">Der Parameter "ReplicationProtectedItem" akzeptiert den Wert vom Typ "ASRReplicationProtectedItem" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="26c2f-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="26c2f-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26c2f-123">OUTPUTS</span></span>

### <span data-ttu-id="26c2f-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="26c2f-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="26c2f-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="26c2f-125">NOTES</span></span>

## <span data-ttu-id="26c2f-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26c2f-126">RELATED LINKS</span></span>

[<span data-ttu-id="26c2f-127">Azure Site Recovery-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="26c2f-127">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
