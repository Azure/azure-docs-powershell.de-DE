---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: c871d8620e8c4507ec972f3888babfd259ede172
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004899"
---
# <span data-ttu-id="d87de-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d87de-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="d87de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d87de-102">SYNOPSIS</span></span>
<span data-ttu-id="d87de-103">Erstellt eine Azure Site Recovery Protection-Container Zuordnung, indem die angegebene Replikationsrichtlinie dem angegebenen ASR-Schutzcontainer zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="d87de-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

## <span data-ttu-id="d87de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d87de-104">SYNTAX</span></span>

### <span data-ttu-id="d87de-105">EnterpriseToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="d87de-105">EnterpriseToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d87de-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="d87de-106">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d87de-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d87de-107">DESCRIPTION</span></span>
<span data-ttu-id="d87de-108">Das Cmdlet **New-AzRecoveryServicesAsrProtectionContainerMapping** erstellt eine Azure Site Recovery Protection-Container Zuordnung, indem die angegebene Replikationsrichtlinie dem angegebenen Schutzcontainer zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="d87de-108">The **New-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="d87de-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d87de-109">EXAMPLES</span></span>

### <span data-ttu-id="d87de-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d87de-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="d87de-111">Startet die Erstellung der Schutzcontainer Zuordnung mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d87de-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="d87de-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d87de-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $PrimaryProtectionContainerMapping -policy $Policy1 -PrimaryProtectionContainer $pc

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="d87de-113">Startet die Erstellung der Schutzcontainer Zuordnung mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d87de-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d87de-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d87de-114">PARAMETERS</span></span>

### <span data-ttu-id="d87de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d87de-115">-DefaultProfile</span></span>
<span data-ttu-id="d87de-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d87de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d87de-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d87de-117">-Name</span></span>
<span data-ttu-id="d87de-118">Gibt den Namen der Schutz Container Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="d87de-118">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d87de-119">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d87de-119">-Policy</span></span>
<span data-ttu-id="d87de-120">Gibt das ASR-Replikationsrichtlinien Objekt für die Replikationsrichtlinie an, die in der Zuordnung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d87de-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d87de-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d87de-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="d87de-122">Gibt das ASR-Schutzcontainer Objekt für den primären Schutzcontainer an, der in der Zuordnung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d87de-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d87de-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d87de-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="d87de-124">Gibt das ASR-Schutzcontainer Objekt für den in der Zuordnung zu verwendenden Wiederherstellungs Schutzcontainer an (wird bei der Replikation an einen Wiederherstellungsspeicherort verwendet, bei dem es sich nicht um Azure handelt).</span><span class="sxs-lookup"><span data-stu-id="d87de-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d87de-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d87de-125">-Confirm</span></span>
<span data-ttu-id="d87de-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d87de-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d87de-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d87de-127">-WhatIf</span></span>
<span data-ttu-id="d87de-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d87de-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d87de-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d87de-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d87de-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d87de-130">CommonParameters</span></span>
<span data-ttu-id="d87de-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d87de-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d87de-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d87de-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d87de-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d87de-133">INPUTS</span></span>

### <span data-ttu-id="d87de-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="d87de-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="d87de-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d87de-135">OUTPUTS</span></span>

### <span data-ttu-id="d87de-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d87de-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d87de-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="d87de-137">NOTES</span></span>

## <span data-ttu-id="d87de-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d87de-138">RELATED LINKS</span></span>

[<span data-ttu-id="d87de-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d87de-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="d87de-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d87de-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
