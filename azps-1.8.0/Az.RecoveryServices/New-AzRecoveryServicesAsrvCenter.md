---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 98bc2dfde30357e7f6a3db62ec550a2a0c173bb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659864"
---
# <span data-ttu-id="8cdcc-101">New-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="8cdcc-101">New-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="8cdcc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8cdcc-102">SYNOPSIS</span></span>
<span data-ttu-id="8cdcc-103">Fügt einen vCenter Server hinzu, um geschützte Elemente zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="8cdcc-103">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="8cdcc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cdcc-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount> -Port <Int32>
 -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cdcc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cdcc-105">DESCRIPTION</span></span>
<span data-ttu-id="8cdcc-106">Mit dem Cmdlet **New-AzRecoveryServicesAsrvCenter** wird ein vCenter Server hinzugefügt, in dem die geschützten Elemente erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="8cdcc-106">The **New-AzRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="8cdcc-107">Mit diesem Cmdlet wird der vCenter Server für die Ermittlung mit dem Konfigurationsserver registriert.</span><span class="sxs-lookup"><span data-stu-id="8cdcc-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="8cdcc-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8cdcc-108">EXAMPLES</span></span>

### <span data-ttu-id="8cdcc-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8cdcc-109">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="8cdcc-110">Fügt einen vCenter Server hinzu, um geschützte Elemente zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="8cdcc-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="8cdcc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cdcc-111">PARAMETERS</span></span>

### <span data-ttu-id="8cdcc-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="8cdcc-112">-Account</span></span>
<span data-ttu-id="8cdcc-113">Benutzer-Login-creadential-Konto.</span><span class="sxs-lookup"><span data-stu-id="8cdcc-113">User login creadential Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdcc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cdcc-114">-DefaultProfile</span></span>
<span data-ttu-id="8cdcc-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8cdcc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cdcc-116">-Stoff</span><span class="sxs-lookup"><span data-stu-id="8cdcc-116">-Fabric</span></span>
<span data-ttu-id="8cdcc-117">ASR-Fabric, die dem Konfigurationsserver entspricht.</span><span class="sxs-lookup"><span data-stu-id="8cdcc-117">ASR fabric corresponding to the Configuration server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdcc-118">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="8cdcc-118">-IpOrHostName</span></span>
<span data-ttu-id="8cdcc-119">IPv4-Adresse oder FQDN des vCenter-Servers.</span><span class="sxs-lookup"><span data-stu-id="8cdcc-119">IPv4 address or FQDN of the vCenter server.</span></span>

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

### <span data-ttu-id="8cdcc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8cdcc-120">-Name</span></span>
<span data-ttu-id="8cdcc-121">Ein Anzeigename für den vCenter Server.</span><span class="sxs-lookup"><span data-stu-id="8cdcc-121">A friendly name for the vCenter server.</span></span>

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

### <span data-ttu-id="8cdcc-122">-Port</span><span class="sxs-lookup"><span data-stu-id="8cdcc-122">-Port</span></span>
<span data-ttu-id="8cdcc-123">Der TCP-Port auf dem vCenter Server, der für die Erkennung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8cdcc-123">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdcc-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8cdcc-124">-Confirm</span></span>
<span data-ttu-id="8cdcc-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8cdcc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cdcc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cdcc-126">-WhatIf</span></span>
<span data-ttu-id="8cdcc-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8cdcc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cdcc-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cdcc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cdcc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cdcc-129">CommonParameters</span></span>
<span data-ttu-id="8cdcc-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cdcc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cdcc-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cdcc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cdcc-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8cdcc-132">INPUTS</span></span>

### <span data-ttu-id="8cdcc-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="8cdcc-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="8cdcc-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8cdcc-134">OUTPUTS</span></span>

### <span data-ttu-id="8cdcc-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8cdcc-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8cdcc-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="8cdcc-136">NOTES</span></span>

## <span data-ttu-id="8cdcc-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8cdcc-137">RELATED LINKS</span></span>
