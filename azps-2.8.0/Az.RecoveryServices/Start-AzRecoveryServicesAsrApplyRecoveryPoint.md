---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: d669e450e096e4d9c0c61a3e1d485e3caaaa9ae3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825224"
---
# <span data-ttu-id="9293c-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9293c-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="9293c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9293c-102">SYNOPSIS</span></span>
<span data-ttu-id="9293c-103">Ändert einen Wiederherstellungspunkt für ein fehlerhaft über geschütztes Element, bevor der Failovervorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9293c-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="9293c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9293c-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9293c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9293c-105">DESCRIPTION</span></span>
<span data-ttu-id="9293c-106">Die **Start-AzRecoveryServicesAsrApplyRecoveryPoint** ändert den Wiederherstellungspunkt für ein fehlerhaft über geschütztes Element, bevor ein Commit für den Failovervorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9293c-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="9293c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9293c-107">EXAMPLES</span></span>

### <span data-ttu-id="9293c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9293c-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="9293c-109">Startet die Anwendung des angegebenen Wiederherstellungspunkts auf das geschützte Replikat Element und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9293c-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9293c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9293c-110">PARAMETERS</span></span>

### <span data-ttu-id="9293c-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="9293c-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="9293c-112">Gibt die primäre Zertifikatsdatei an, wenn die Datenverschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9293c-112">Specifies the primary certificate file if data encryption is being used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9293c-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="9293c-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="9293c-114">Gibt die sekundäre Zertifikatsdatei an, wenn die Datenverschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9293c-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9293c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9293c-115">-DefaultProfile</span></span>
<span data-ttu-id="9293c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9293c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9293c-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9293c-117">-RecoveryPoint</span></span>
<span data-ttu-id="9293c-118">Gibt das Wiederherstellungspunkt Objekt an, das dem anzuwendenden Wiederherstellungspunkt entspricht.</span><span class="sxs-lookup"><span data-stu-id="9293c-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9293c-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9293c-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="9293c-120">Gibt das Objekt der ASR-Replikations geschützten Elemente an.</span><span class="sxs-lookup"><span data-stu-id="9293c-120">Specifies the ASR replication protected item object.</span></span>

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

### <span data-ttu-id="9293c-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9293c-121">-Confirm</span></span>
<span data-ttu-id="9293c-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9293c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9293c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9293c-123">-WhatIf</span></span>
<span data-ttu-id="9293c-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9293c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9293c-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9293c-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9293c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9293c-126">CommonParameters</span></span>
<span data-ttu-id="9293c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9293c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9293c-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9293c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9293c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9293c-129">INPUTS</span></span>

### <span data-ttu-id="9293c-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9293c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="9293c-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9293c-131">OUTPUTS</span></span>

### <span data-ttu-id="9293c-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9293c-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9293c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="9293c-133">NOTES</span></span>

## <span data-ttu-id="9293c-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9293c-134">RELATED LINKS</span></span>

[<span data-ttu-id="9293c-135">Azure Site Recovery-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="9293c-135">Azure Site Recovery Cmdlets</span></span>](./Az.SiteRecovery.md)
