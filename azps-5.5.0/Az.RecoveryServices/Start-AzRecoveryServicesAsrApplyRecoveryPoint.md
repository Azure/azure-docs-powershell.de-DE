---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 893298c3349d2d7ceaa998a1f147ce8dd590f101
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158513"
---
# <span data-ttu-id="80179-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="80179-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="80179-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80179-102">SYNOPSIS</span></span>
<span data-ttu-id="80179-103">Ändert einen Wiederherstellungspunkt für ein über einem geschützten Element fehlgeschlagenes Element, bevor ein Failovervorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80179-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="80179-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80179-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80179-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80179-105">DESCRIPTION</span></span>
<span data-ttu-id="80179-106">**Start-AzRecoveryServicesAsrApplyRecoveryPoint** ändert den Wiederherstellungspunkt für ein über einem geschützten Element fehlgeschlagenes Element, bevor der Failovervorgang gesichert wird.</span><span class="sxs-lookup"><span data-stu-id="80179-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="80179-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="80179-107">EXAMPLES</span></span>

### <span data-ttu-id="80179-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="80179-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="80179-109">Beginnt mit dem Anwenden des angegebenen Wiederherstellungspunkts auf das replikationsgeschützte Element und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="80179-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="80179-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80179-110">PARAMETERS</span></span>

### <span data-ttu-id="80179-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="80179-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="80179-112">Gibt die primäre Zertifikatdatei an, wenn Datenverschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="80179-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="80179-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="80179-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="80179-114">Gibt die sekundäre Zertifikatdatei an, wenn Datenverschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="80179-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="80179-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80179-115">-DefaultProfile</span></span>
<span data-ttu-id="80179-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="80179-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="80179-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="80179-117">-RecoveryPoint</span></span>
<span data-ttu-id="80179-118">Gibt das Wiederherstellungspunktobjekt an, das dem anzuwendenden Wiederherstellungspunkt entspricht.</span><span class="sxs-lookup"><span data-stu-id="80179-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

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

### <span data-ttu-id="80179-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="80179-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="80179-120">Gibt das asr-replikationsgeschützte Elementobjekt an.</span><span class="sxs-lookup"><span data-stu-id="80179-120">Specifies the ASR replication protected item object.</span></span>

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

### <span data-ttu-id="80179-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80179-121">-Confirm</span></span>
<span data-ttu-id="80179-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80179-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80179-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="80179-123">-WhatIf</span></span>
<span data-ttu-id="80179-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80179-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80179-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80179-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80179-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80179-126">CommonParameters</span></span>
<span data-ttu-id="80179-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80179-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80179-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80179-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80179-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="80179-129">INPUTS</span></span>

### <span data-ttu-id="80179-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="80179-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="80179-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="80179-131">OUTPUTS</span></span>

### <span data-ttu-id="80179-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="80179-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="80179-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="80179-133">NOTES</span></span>

## <span data-ttu-id="80179-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="80179-134">RELATED LINKS</span></span>

[<span data-ttu-id="80179-135">Azure Site Recovery Cmdlets</span><span class="sxs-lookup"><span data-stu-id="80179-135">Azure Site Recovery Cmdlets</span></span>](./Az.SiteRecovery.md)
