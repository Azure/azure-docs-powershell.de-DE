---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: aa2cd93d21ba22405fff0f3c5fcf336d00f2f6b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481698"
---
# <span data-ttu-id="5e1ad-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5e1ad-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="5e1ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e1ad-102">SYNOPSIS</span></span>
<span data-ttu-id="5e1ad-103">Erstellt eine Azure Site Recovery Protection-Container Zuordnung, indem die angegebene Replikationsrichtlinie dem angegebenen ASR-Schutzcontainer zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e1ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e1ad-104">SYNTAX</span></span>

### <span data-ttu-id="5e1ad-105">EnterpriseToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e1ad-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e1ad-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="5e1ad-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e1ad-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e1ad-107">DESCRIPTION</span></span>
<span data-ttu-id="5e1ad-108">Das Cmdlet **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** erstellt eine Azure Site Recovery Protection-Container Zuordnung, indem die angegebene Replikationsrichtlinie dem angegebenen Schutzcontainer zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-108">The **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="5e1ad-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e1ad-109">EXAMPLES</span></span>

### <span data-ttu-id="5e1ad-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e1ad-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="5e1ad-111">Startet die Erstellung der Schutzcontainer Zuordnung mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5e1ad-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e1ad-112">PARAMETERS</span></span>

### <span data-ttu-id="5e1ad-113">-Name</span><span class="sxs-lookup"><span data-stu-id="5e1ad-113">-Name</span></span>
<span data-ttu-id="5e1ad-114">Gibt den Namen der Schutz Container Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-114">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="5e1ad-115">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="5e1ad-115">-Policy</span></span>
<span data-ttu-id="5e1ad-116">Gibt das ASR-Replikationsrichtlinien Objekt für die Replikationsrichtlinie an, die in der Zuordnung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-116">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

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

### <span data-ttu-id="5e1ad-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5e1ad-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="5e1ad-118">Gibt das ASR-Schutzcontainer Objekt für den primären Schutzcontainer an, der in der Zuordnung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-118">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

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

### <span data-ttu-id="5e1ad-119">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5e1ad-119">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="5e1ad-120">Gibt das ASR-Schutzcontainer Objekt für den in der Zuordnung zu verwendenden Wiederherstellungs Schutzcontainer an (wird bei der Replikation an einen Wiederherstellungsspeicherort verwendet, bei dem es sich nicht um Azure handelt).</span><span class="sxs-lookup"><span data-stu-id="5e1ad-120">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

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

### <span data-ttu-id="5e1ad-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e1ad-121">-Confirm</span></span>
<span data-ttu-id="5e1ad-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e1ad-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e1ad-123">-WhatIf</span></span>
<span data-ttu-id="5e1ad-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e1ad-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e1ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e1ad-126">CommonParameters</span></span>
<span data-ttu-id="5e1ad-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e1ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e1ad-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e1ad-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e1ad-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e1ad-129">INPUTS</span></span>

### <span data-ttu-id="5e1ad-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="5e1ad-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="5e1ad-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e1ad-131">OUTPUTS</span></span>

### <span data-ttu-id="5e1ad-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5e1ad-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5e1ad-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e1ad-133">NOTES</span></span>

## <span data-ttu-id="5e1ad-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e1ad-134">RELATED LINKS</span></span>

[<span data-ttu-id="5e1ad-135">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5e1ad-135">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="5e1ad-136">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5e1ad-136">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
