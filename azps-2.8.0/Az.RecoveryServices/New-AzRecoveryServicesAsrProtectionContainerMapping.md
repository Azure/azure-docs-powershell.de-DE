---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 67cf974faa735bc8d07703094d9afe71127c7137
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824584"
---
# <span data-ttu-id="a64a6-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a64a6-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="a64a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a64a6-102">SYNOPSIS</span></span>
<span data-ttu-id="a64a6-103">Erstellt eine Azure Site Recovery Protection-Container Zuordnung, indem die angegebene Replikationsrichtlinie dem angegebenen ASR-Schutzcontainer zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="a64a6-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

## <span data-ttu-id="a64a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a64a6-104">SYNTAX</span></span>

### <span data-ttu-id="a64a6-105">EnterpriseToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="a64a6-105">EnterpriseToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a64a6-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="a64a6-106">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a64a6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a64a6-107">DESCRIPTION</span></span>
<span data-ttu-id="a64a6-108">Das Cmdlet **New-AzRecoveryServicesAsrProtectionContainerMapping** erstellt eine Azure Site Recovery Protection-Container Zuordnung, indem die angegebene Replikationsrichtlinie dem angegebenen Schutzcontainer zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="a64a6-108">The **New-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="a64a6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a64a6-109">EXAMPLES</span></span>

### <span data-ttu-id="a64a6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a64a6-110">Example 1</span></span>
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

<span data-ttu-id="a64a6-111">Startet die Erstellung der Schutzcontainer Zuordnung mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a64a6-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="a64a6-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a64a6-112">Example 2</span></span>
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

<span data-ttu-id="a64a6-113">Startet die Erstellung der Schutzcontainer Zuordnung mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a64a6-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a64a6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a64a6-114">PARAMETERS</span></span>

### <span data-ttu-id="a64a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a64a6-115">-DefaultProfile</span></span>
<span data-ttu-id="a64a6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a64a6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a64a6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a64a6-117">-Name</span></span>
<span data-ttu-id="a64a6-118">Gibt den Namen der Schutz Container Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="a64a6-118">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="a64a6-119">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="a64a6-119">-Policy</span></span>
<span data-ttu-id="a64a6-120">Gibt das ASR-Replikationsrichtlinien Objekt für die Replikationsrichtlinie an, die in der Zuordnung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a64a6-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

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

### <span data-ttu-id="a64a6-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a64a6-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="a64a6-122">Gibt das ASR-Schutzcontainer Objekt für den primären Schutzcontainer an, der in der Zuordnung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a64a6-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

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

### <span data-ttu-id="a64a6-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a64a6-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="a64a6-124">Gibt das ASR-Schutzcontainer Objekt für den in der Zuordnung zu verwendenden Wiederherstellungs Schutzcontainer an (wird bei der Replikation an einen Wiederherstellungsspeicherort verwendet, bei dem es sich nicht um Azure handelt).</span><span class="sxs-lookup"><span data-stu-id="a64a6-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

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

### <span data-ttu-id="a64a6-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a64a6-125">-Confirm</span></span>
<span data-ttu-id="a64a6-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a64a6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a64a6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a64a6-127">-WhatIf</span></span>
<span data-ttu-id="a64a6-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a64a6-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a64a6-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a64a6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a64a6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a64a6-130">CommonParameters</span></span>
<span data-ttu-id="a64a6-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a64a6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a64a6-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a64a6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a64a6-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a64a6-133">INPUTS</span></span>

### <span data-ttu-id="a64a6-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="a64a6-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="a64a6-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a64a6-135">OUTPUTS</span></span>

### <span data-ttu-id="a64a6-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a64a6-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a64a6-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="a64a6-137">NOTES</span></span>

## <span data-ttu-id="a64a6-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a64a6-138">RELATED LINKS</span></span>

[<span data-ttu-id="a64a6-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a64a6-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="a64a6-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a64a6-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
