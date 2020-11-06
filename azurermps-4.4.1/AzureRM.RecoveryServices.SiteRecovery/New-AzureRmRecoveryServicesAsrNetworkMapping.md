---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ab2cca2fc0b517d8923d117978887c6dd0196ce5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501681"
---
# <span data-ttu-id="cdbad-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cdbad-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="cdbad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cdbad-102">SYNOPSIS</span></span>
<span data-ttu-id="cdbad-103">Erstellt eine ASR-Netzwerkzuordnung zwischen zwei Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="cdbad-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdbad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdbad-104">SYNTAX</span></span>

### <span data-ttu-id="cdbad-105">EnterpriseToEnterprise (Standard)</span><span class="sxs-lookup"><span data-stu-id="cdbad-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdbad-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="cdbad-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdbad-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cdbad-107">DESCRIPTION</span></span>
<span data-ttu-id="cdbad-108">Das Cmdlet **New-AzureRmRecoveryServicesAsrNetworkMapping** startet den Vorgang des Erstellens einer ASR-Netzwerkzuordnung zwischen zwei Netzwerken und gibt das ASR-Auftragsobjekt für den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cdbad-108">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="cdbad-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cdbad-109">EXAMPLES</span></span>

### <span data-ttu-id="cdbad-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cdbad-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="cdbad-111">Startet den Netzwerk Zuordnungs Erstellungsvorgang mit dem angegebenen Namen, Primär-und Wiederherstellungs Netz und gibt einen ASR-Auftrag zurück, um den Vorgang zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="cdbad-111">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

## <span data-ttu-id="cdbad-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdbad-112">PARAMETERS</span></span>

### <span data-ttu-id="cdbad-113">-Name</span><span class="sxs-lookup"><span data-stu-id="cdbad-113">-Name</span></span>
<span data-ttu-id="cdbad-114">Der Name der zu erstellende ASR-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="cdbad-114">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="cdbad-115">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="cdbad-115">-PrimaryNetwork</span></span>
<span data-ttu-id="cdbad-116">Gibt das primäre Netzwerkobjekt für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="cdbad-116">Specifies the primary network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdbad-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="cdbad-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="cdbad-118">Gibt die Azure-Wiederherstellungs-ID für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="cdbad-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdbad-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="cdbad-119">-RecoveryNetwork</span></span>
<span data-ttu-id="cdbad-120">Gibt das Wiederherstellungs Netzwerkobjekt für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="cdbad-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdbad-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cdbad-121">-Confirm</span></span>
<span data-ttu-id="cdbad-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cdbad-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdbad-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdbad-123">-WhatIf</span></span>
<span data-ttu-id="cdbad-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cdbad-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cdbad-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cdbad-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdbad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdbad-126">CommonParameters</span></span>
<span data-ttu-id="cdbad-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdbad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdbad-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdbad-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdbad-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cdbad-129">INPUTS</span></span>

### <span data-ttu-id="cdbad-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="cdbad-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="cdbad-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cdbad-131">OUTPUTS</span></span>

### <span data-ttu-id="cdbad-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="cdbad-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cdbad-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="cdbad-133">NOTES</span></span>

## <span data-ttu-id="cdbad-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cdbad-134">RELATED LINKS</span></span>

[<span data-ttu-id="cdbad-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cdbad-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="cdbad-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cdbad-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
