---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 2afdc351c50e42ec5b2f67208d2be2af9f024813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476661"
---
# <span data-ttu-id="ef7c0-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ef7c0-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="ef7c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef7c0-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7c0-103">Ändert einen Wiederherstellungspunkt für ein fehlerhaft über geschütztes Element, bevor der Failovervorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef7c0-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef7c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef7c0-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef7c0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef7c0-105">DESCRIPTION</span></span>
<span data-ttu-id="ef7c0-106">Die **Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** ändert den Wiederherstellungspunkt für ein fehlerhaft über geschütztes Element, bevor ein Commit für den Failovervorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef7c0-106">The **Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="ef7c0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef7c0-107">EXAMPLES</span></span>

### <span data-ttu-id="ef7c0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ef7c0-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="ef7c0-109">Startet die Anwendung des angegebenen Wiederherstellungspunkts auf das geschützte Replikat Element und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef7c0-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ef7c0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef7c0-110">PARAMETERS</span></span>

### <span data-ttu-id="ef7c0-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ef7c0-111">-Confirm</span></span>
<span data-ttu-id="ef7c0-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef7c0-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7c0-113">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ef7c0-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="ef7c0-114">Gibt die primäre Zertifikatsdatei an, wenn die Datenverschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef7c0-114">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="ef7c0-115">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ef7c0-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="ef7c0-116">Gibt die sekundäre Zertifikatsdatei an, wenn die Datenverschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef7c0-116">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="ef7c0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef7c0-117">-DefaultProfile</span></span>
<span data-ttu-id="ef7c0-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ef7c0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="ef7c0-119">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ef7c0-119">-RecoveryPoint</span></span>
<span data-ttu-id="ef7c0-120">Gibt das Wiederherstellungspunkt Objekt an, das dem anzuwendenden Wiederherstellungspunkt entspricht.</span><span class="sxs-lookup"><span data-stu-id="ef7c0-120">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

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

### <span data-ttu-id="ef7c0-121">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ef7c0-121">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ef7c0-122">Gibt das Objekt der ASR-Replikations geschützten Elemente an.</span><span class="sxs-lookup"><span data-stu-id="ef7c0-122">Specifies the ASR replication protected item object.</span></span>

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

### <span data-ttu-id="ef7c0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef7c0-123">-WhatIf</span></span>
<span data-ttu-id="ef7c0-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef7c0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef7c0-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef7c0-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7c0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef7c0-126">CommonParameters</span></span>
<span data-ttu-id="ef7c0-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef7c0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef7c0-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef7c0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef7c0-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef7c0-129">INPUTS</span></span>

### <span data-ttu-id="ef7c0-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ef7c0-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ef7c0-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef7c0-131">OUTPUTS</span></span>

### <span data-ttu-id="ef7c0-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ef7c0-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ef7c0-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef7c0-133">NOTES</span></span>

## <span data-ttu-id="ef7c0-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef7c0-134">RELATED LINKS</span></span>

[<span data-ttu-id="ef7c0-135">Azure Site Recovery-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ef7c0-135">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
