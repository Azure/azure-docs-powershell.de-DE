---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 09e6cbbbae30d1a2e43d8292573f4bf45d9db461
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165708"
---
# <span data-ttu-id="582be-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="582be-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="582be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="582be-102">SYNOPSIS</span></span>
<span data-ttu-id="582be-103">Aktualisiert die angegebene Azure Site Recovery-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="582be-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="582be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="582be-104">SYNTAX</span></span>

### <span data-ttu-id="582be-105">ByNetworkObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="582be-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="582be-106">ById</span><span class="sxs-lookup"><span data-stu-id="582be-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="582be-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="582be-107">DESCRIPTION</span></span>
<span data-ttu-id="582be-108">Das Cmdlet **Update-AzRecoveryServicesAsrNetworkMapping** aktualisiert die angegebene Azure Site Recovery-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="582be-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="582be-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="582be-109">EXAMPLES</span></span>

### <span data-ttu-id="582be-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="582be-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="582be-111">Startet den Update-Netzwerk Zuordnungsvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="582be-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="582be-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="582be-112">PARAMETERS</span></span>

### <span data-ttu-id="582be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="582be-113">-DefaultProfile</span></span>
<span data-ttu-id="582be-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="582be-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="582be-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="582be-115">-InputObject</span></span>
<span data-ttu-id="582be-116">Eingabeobjekt: gibt das ASR-Netzwerk Zuordnungsobjekt an, das der ASR-Netzwerkzuordnung entspricht, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="582be-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="582be-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="582be-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="582be-118">Gibt die Azure-Wiederherstellungs-ID für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="582be-118">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="582be-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="582be-119">-RecoveryNetwork</span></span>
<span data-ttu-id="582be-120">Gibt das Wiederherstellungs Netzwerkobjekt für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="582be-120">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="582be-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="582be-121">-Confirm</span></span>
<span data-ttu-id="582be-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="582be-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="582be-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="582be-123">-WhatIf</span></span>
<span data-ttu-id="582be-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="582be-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="582be-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="582be-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="582be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="582be-126">CommonParameters</span></span>
<span data-ttu-id="582be-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="582be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="582be-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="582be-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="582be-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="582be-129">INPUTS</span></span>

### <span data-ttu-id="582be-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="582be-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="582be-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="582be-131">OUTPUTS</span></span>

### <span data-ttu-id="582be-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="582be-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="582be-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="582be-133">NOTES</span></span>

## <span data-ttu-id="582be-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="582be-134">RELATED LINKS</span></span>
