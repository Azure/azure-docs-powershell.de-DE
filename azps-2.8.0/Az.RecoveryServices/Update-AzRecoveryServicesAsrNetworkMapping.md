---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 32412127388e233af303cc29de8ecf66304a0bf3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825176"
---
# <span data-ttu-id="a7e04-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a7e04-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="a7e04-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7e04-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e04-103">Aktualisiert die angegebene Azure Site Recovery-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="a7e04-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="a7e04-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7e04-104">SYNTAX</span></span>

### <span data-ttu-id="a7e04-105">ByNetworkObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="a7e04-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7e04-106">ById</span><span class="sxs-lookup"><span data-stu-id="a7e04-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7e04-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7e04-107">DESCRIPTION</span></span>
<span data-ttu-id="a7e04-108">Das Cmdlet **Update-AzRecoveryServicesAsrNetworkMapping** aktualisiert die angegebene Azure Site Recovery-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="a7e04-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="a7e04-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7e04-109">EXAMPLES</span></span>

### <span data-ttu-id="a7e04-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a7e04-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="a7e04-111">Startet den Update-Netzwerk Zuordnungsvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a7e04-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a7e04-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7e04-112">PARAMETERS</span></span>

### <span data-ttu-id="a7e04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e04-113">-DefaultProfile</span></span>
<span data-ttu-id="a7e04-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a7e04-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a7e04-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a7e04-115">-InputObject</span></span>
<span data-ttu-id="a7e04-116">Eingabeobjekt: gibt das ASR-Netzwerk Zuordnungsobjekt an, das der ASR-Netzwerkzuordnung entspricht, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7e04-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7e04-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="a7e04-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="a7e04-118">Gibt die Azure-Wiederherstellungs-ID für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="a7e04-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e04-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="a7e04-119">-RecoveryNetwork</span></span>
<span data-ttu-id="a7e04-120">Gibt das Wiederherstellungs Netzwerkobjekt für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="a7e04-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e04-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a7e04-121">-Confirm</span></span>
<span data-ttu-id="a7e04-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7e04-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7e04-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7e04-123">-WhatIf</span></span>
<span data-ttu-id="a7e04-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7e04-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7e04-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7e04-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7e04-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e04-126">CommonParameters</span></span>
<span data-ttu-id="a7e04-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7e04-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e04-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7e04-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e04-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7e04-129">INPUTS</span></span>

### <span data-ttu-id="a7e04-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a7e04-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="a7e04-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7e04-131">OUTPUTS</span></span>

### <span data-ttu-id="a7e04-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a7e04-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a7e04-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7e04-133">NOTES</span></span>

## <span data-ttu-id="a7e04-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7e04-134">RELATED LINKS</span></span>
