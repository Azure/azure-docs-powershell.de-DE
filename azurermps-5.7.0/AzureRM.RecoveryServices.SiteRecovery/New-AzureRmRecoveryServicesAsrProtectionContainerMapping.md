---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 64448977a14a702d67473621e71c7740fc6f43c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663765"
---
# <span data-ttu-id="23fa2-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="23fa2-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="23fa2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="23fa2-103">Erstellt eine Azure Site Recovery Protection-Container Zuordnung, indem die angegebene Replikationsrichtlinie dem angegebenen ASR-Schutzcontainer zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="23fa2-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23fa2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23fa2-104">SYNTAX</span></span>

### <span data-ttu-id="23fa2-105">EnterpriseToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="23fa2-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23fa2-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="23fa2-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23fa2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23fa2-107">DESCRIPTION</span></span>
<span data-ttu-id="23fa2-108">Das Cmdlet **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** erstellt eine Azure Site Recovery Protection-Container Zuordnung, indem die angegebene Replikationsrichtlinie dem angegebenen Schutzcontainer zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="23fa2-108">The **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="23fa2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23fa2-109">EXAMPLES</span></span>

### <span data-ttu-id="23fa2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="23fa2-110">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer

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

<span data-ttu-id="23fa2-111">Startet die Erstellung der Schutzcontainer Zuordnung mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="23fa2-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="23fa2-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="23fa2-112">Example 2</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PrimaryProtectionContainerMapping -policy $Policy1 -PrimaryProtectionContainer $pc

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

<span data-ttu-id="23fa2-113">Startet die Erstellung der Schutzcontainer Zuordnung mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="23fa2-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="23fa2-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="23fa2-114">PARAMETERS</span></span>

### <span data-ttu-id="23fa2-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="23fa2-115">-Confirm</span></span>
<span data-ttu-id="23fa2-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23fa2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23fa2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23fa2-117">-DefaultProfile</span></span>
<span data-ttu-id="23fa2-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="23fa2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="23fa2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="23fa2-119">-Name</span></span>
<span data-ttu-id="23fa2-120">Gibt den Namen der Schutz Container Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="23fa2-120">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23fa2-121">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="23fa2-121">-Policy</span></span>
<span data-ttu-id="23fa2-122">Gibt das ASR-Replikationsrichtlinien Objekt für die Replikationsrichtlinie an, die in der Zuordnung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="23fa2-122">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23fa2-123">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="23fa2-123">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="23fa2-124">Gibt das ASR-Schutzcontainer Objekt für den primären Schutzcontainer an, der in der Zuordnung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="23fa2-124">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23fa2-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="23fa2-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="23fa2-126">Gibt das ASR-Schutzcontainer Objekt für den in der Zuordnung zu verwendenden Wiederherstellungs Schutzcontainer an (wird bei der Replikation an einen Wiederherstellungsspeicherort verwendet, bei dem es sich nicht um Azure handelt).</span><span class="sxs-lookup"><span data-stu-id="23fa2-126">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23fa2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23fa2-127">-WhatIf</span></span>
<span data-ttu-id="23fa2-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23fa2-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23fa2-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23fa2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23fa2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23fa2-130">CommonParameters</span></span>
<span data-ttu-id="23fa2-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23fa2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23fa2-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23fa2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23fa2-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23fa2-133">INPUTS</span></span>

### <span data-ttu-id="23fa2-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="23fa2-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="23fa2-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23fa2-135">OUTPUTS</span></span>

### <span data-ttu-id="23fa2-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="23fa2-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="23fa2-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="23fa2-137">NOTES</span></span>

## <span data-ttu-id="23fa2-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23fa2-138">RELATED LINKS</span></span>

[<span data-ttu-id="23fa2-139">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="23fa2-139">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="23fa2-140">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="23fa2-140">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
