---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: be521545111667493c5b0e268013ffa4464ed3a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476645"
---
# <span data-ttu-id="afcaa-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="afcaa-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="afcaa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="afcaa-102">SYNOPSIS</span></span>
<span data-ttu-id="afcaa-103">Aktualisiert die angegebene Azure Site Recovery-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="afcaa-103">Updates the specified azure site recovery network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afcaa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="afcaa-104">SYNTAX</span></span>

### <span data-ttu-id="afcaa-105">ByNetworkObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="afcaa-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afcaa-106">ById</span><span class="sxs-lookup"><span data-stu-id="afcaa-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afcaa-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="afcaa-107">DESCRIPTION</span></span>
<span data-ttu-id="afcaa-108">Das Cmdlet **Update-AzureRmRecoveryServicesAsrNetworkMapping** aktualisiert die angegebene Azure Site Recovery-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="afcaa-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="afcaa-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="afcaa-109">EXAMPLES</span></span>

### <span data-ttu-id="afcaa-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="afcaa-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="afcaa-111">Startet den Update-Netzwerk Zuordnungsvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="afcaa-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="afcaa-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="afcaa-112">PARAMETERS</span></span>

### <span data-ttu-id="afcaa-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="afcaa-113">-Confirm</span></span>
<span data-ttu-id="afcaa-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="afcaa-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afcaa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afcaa-115">-DefaultProfile</span></span>
<span data-ttu-id="afcaa-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="afcaa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="afcaa-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="afcaa-117">-InputObject</span></span>
<span data-ttu-id="afcaa-118">Eingabeobjekt: gibt das ASR-Netzwerk Zuordnungsobjekt an, das der ASR-Netzwerkzuordnung entspricht, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="afcaa-118">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="afcaa-119">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="afcaa-119">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="afcaa-120">Gibt die Azure-Wiederherstellungs-ID für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="afcaa-120">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="afcaa-121">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="afcaa-121">-RecoveryNetwork</span></span>
<span data-ttu-id="afcaa-122">Gibt das Wiederherstellungs Netzwerkobjekt für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="afcaa-122">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="afcaa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afcaa-123">-WhatIf</span></span>
<span data-ttu-id="afcaa-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="afcaa-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afcaa-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="afcaa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afcaa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afcaa-126">CommonParameters</span></span>
<span data-ttu-id="afcaa-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afcaa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afcaa-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afcaa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afcaa-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="afcaa-129">INPUTS</span></span>

### <span data-ttu-id="afcaa-130">Keine</span><span class="sxs-lookup"><span data-stu-id="afcaa-130">None</span></span>

## <span data-ttu-id="afcaa-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="afcaa-131">OUTPUTS</span></span>

### <span data-ttu-id="afcaa-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="afcaa-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="afcaa-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="afcaa-133">NOTES</span></span>

## <span data-ttu-id="afcaa-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="afcaa-134">RELATED LINKS</span></span>
