---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 748278cd6096a8ab67538df77aa3b81cc54d3ace
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922736"
---
# <span data-ttu-id="6bad7-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="6bad7-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="6bad7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bad7-102">SYNOPSIS</span></span>
<span data-ttu-id="6bad7-103">Ändert einen Wiederherstellungspunkt für ein über geschütztes Element fehlgeschlagenes Element, bevor der Failovervorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6bad7-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="6bad7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6bad7-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6bad7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6bad7-105">DESCRIPTION</span></span>
<span data-ttu-id="6bad7-106">Der **Start-AzRecoveryServicesAsrApplyRecoveryPoint** ändert den Wiederherstellungspunkt für ein fehlgeschlagenes über geschütztes Element, bevor der Failovervorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6bad7-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="6bad7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6bad7-107">EXAMPLES</span></span>

### <span data-ttu-id="6bad7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6bad7-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="6bad7-109">Beginnt mit dem Anwenden des angegebenen Wiederherstellungspunkts auf das replikationsgeschützte Element und gibt den ZUM Nachverfolgen des Vorgangs verwendeten ASR-Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="6bad7-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6bad7-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6bad7-110">PARAMETERS</span></span>

### <span data-ttu-id="6bad7-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="6bad7-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="6bad7-112">Gibt die primäre Zertifikatdatei an, wenn die Datenverschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6bad7-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="6bad7-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="6bad7-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="6bad7-114">Gibt die sekundäre Zertifikatdatei an, wenn datenverschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6bad7-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="6bad7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bad7-115">-DefaultProfile</span></span>
<span data-ttu-id="6bad7-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6bad7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6bad7-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="6bad7-117">-RecoveryPoint</span></span>
<span data-ttu-id="6bad7-118">Gibt das Wiederherstellungspunktobjekt an, das dem anzuwendenden Wiederherstellungspunkt entspricht.</span><span class="sxs-lookup"><span data-stu-id="6bad7-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

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

### <span data-ttu-id="6bad7-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6bad7-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="6bad7-120">Gibt das asr-replikationsgeschützte Elementobjekt an.</span><span class="sxs-lookup"><span data-stu-id="6bad7-120">Specifies the ASR replication protected item object.</span></span>

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

### <span data-ttu-id="6bad7-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6bad7-121">-Confirm</span></span>
<span data-ttu-id="6bad7-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6bad7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bad7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bad7-123">-WhatIf</span></span>
<span data-ttu-id="6bad7-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6bad7-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bad7-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6bad7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bad7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bad7-126">CommonParameters</span></span>
<span data-ttu-id="6bad7-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bad7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bad7-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6bad7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bad7-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6bad7-129">INPUTS</span></span>

### <span data-ttu-id="6bad7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6bad7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="6bad7-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6bad7-131">OUTPUTS</span></span>

### <span data-ttu-id="6bad7-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="6bad7-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6bad7-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6bad7-133">NOTES</span></span>

## <span data-ttu-id="6bad7-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6bad7-134">RELATED LINKS</span></span>

[<span data-ttu-id="6bad7-135">Azure Websitewiederherstellungs-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6bad7-135">Azure Site Recovery Cmdlets</span></span>](./Az.SiteRecovery.md)
