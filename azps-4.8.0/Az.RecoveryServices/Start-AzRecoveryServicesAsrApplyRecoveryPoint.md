---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: b06501fafbc573e10ac7d5dba3435dbf96342ba0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411856"
---
# <span data-ttu-id="8e248-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8e248-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="8e248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e248-102">SYNOPSIS</span></span>
<span data-ttu-id="8e248-103">Ändert einen Wiederherstellungspunkt für ein über einem geschützten Element fehlgeschlagenes Element, bevor ein Failovervorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e248-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="8e248-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e248-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e248-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e248-105">DESCRIPTION</span></span>
<span data-ttu-id="8e248-106">**Start-AzRecoveryServicesAsrApplyRecoveryPoint** ändert den Wiederherstellungspunkt für ein über einem geschützten Element fehlgeschlagenes Element, bevor der Failovervorgang gesichert wird.</span><span class="sxs-lookup"><span data-stu-id="8e248-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="8e248-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e248-107">EXAMPLES</span></span>

### <span data-ttu-id="8e248-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e248-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="8e248-109">Beginnt mit dem Anwenden des angegebenen Wiederherstellungspunkts auf das replikationsgeschützte Element und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="8e248-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8e248-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e248-110">PARAMETERS</span></span>

### <span data-ttu-id="8e248-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8e248-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="8e248-112">Gibt die primäre Zertifikatdatei an, wenn Datenverschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8e248-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="8e248-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8e248-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="8e248-114">Gibt die sekundäre Zertifikatdatei an, wenn Datenverschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8e248-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="8e248-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e248-115">-DefaultProfile</span></span>
<span data-ttu-id="8e248-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e248-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8e248-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8e248-117">-RecoveryPoint</span></span>
<span data-ttu-id="8e248-118">Gibt das Wiederherstellungspunktobjekt an, das dem anzuwendenden Wiederherstellungspunkt entspricht.</span><span class="sxs-lookup"><span data-stu-id="8e248-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

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

### <span data-ttu-id="8e248-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8e248-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8e248-120">Gibt das asr-replikationsgeschützte Elementobjekt an.</span><span class="sxs-lookup"><span data-stu-id="8e248-120">Specifies the ASR replication protected item object.</span></span>

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

### <span data-ttu-id="8e248-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e248-121">-Confirm</span></span>
<span data-ttu-id="8e248-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e248-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e248-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8e248-123">-WhatIf</span></span>
<span data-ttu-id="8e248-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e248-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e248-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e248-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e248-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e248-126">CommonParameters</span></span>
<span data-ttu-id="8e248-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e248-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e248-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e248-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e248-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e248-129">INPUTS</span></span>

### <span data-ttu-id="8e248-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8e248-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8e248-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e248-131">OUTPUTS</span></span>

### <span data-ttu-id="8e248-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="8e248-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8e248-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8e248-133">NOTES</span></span>

## <span data-ttu-id="8e248-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8e248-134">RELATED LINKS</span></span>


