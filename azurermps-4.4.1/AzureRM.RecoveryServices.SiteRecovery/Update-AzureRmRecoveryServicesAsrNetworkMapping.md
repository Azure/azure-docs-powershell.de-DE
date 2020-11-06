---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dd17eef73ab07d662a10177ffb68776aa4ec6016
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501669"
---
# <span data-ttu-id="fe459-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fe459-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="fe459-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fe459-102">SYNOPSIS</span></span>
<span data-ttu-id="fe459-103">Aktualisiert die angegebene ASR-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="fe459-103">Updates the specified ASR network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe459-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe459-104">SYNTAX</span></span>

### <span data-ttu-id="fe459-105">ByNetworkObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe459-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe459-106">ById</span><span class="sxs-lookup"><span data-stu-id="fe459-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe459-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe459-107">DESCRIPTION</span></span>
<span data-ttu-id="fe459-108">Das Cmdlet **Update-AzureRmRecoveryServicesAsrNetworkMapping** aktualisiert die angegebene Azure Site Recovery-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="fe459-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="fe459-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe459-109">EXAMPLES</span></span>

### <span data-ttu-id="fe459-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fe459-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="fe459-111">Startet den Update-Netzwerk Zuordnungsvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe459-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="fe459-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe459-112">PARAMETERS</span></span>

### <span data-ttu-id="fe459-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fe459-113">-InputObject</span></span>
<span data-ttu-id="fe459-114">Eingabeobjekt: gibt das ASR-Netzwerk Zuordnungsobjekt an, das der ASR-Netzwerkzuordnung entspricht, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe459-114">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated</span></span> 

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe459-115">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="fe459-115">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="fe459-116">Gibt die Azure-Wiederherstellungs-ID für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="fe459-116">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe459-117">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="fe459-117">-RecoveryNetwork</span></span>
<span data-ttu-id="fe459-118">Gibt das Wiederherstellungs Netzwerkobjekt für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="fe459-118">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByNetworkObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe459-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fe459-119">-Confirm</span></span>
<span data-ttu-id="fe459-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe459-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe459-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe459-121">-WhatIf</span></span>
<span data-ttu-id="fe459-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe459-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe459-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe459-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe459-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe459-124">CommonParameters</span></span>
<span data-ttu-id="fe459-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe459-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe459-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe459-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe459-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fe459-127">INPUTS</span></span>

### <span data-ttu-id="fe459-128">Keine</span><span class="sxs-lookup"><span data-stu-id="fe459-128">None</span></span>

## <span data-ttu-id="fe459-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fe459-129">OUTPUTS</span></span>

### <span data-ttu-id="fe459-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fe459-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fe459-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="fe459-131">NOTES</span></span>

## <span data-ttu-id="fe459-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fe459-132">RELATED LINKS</span></span>

