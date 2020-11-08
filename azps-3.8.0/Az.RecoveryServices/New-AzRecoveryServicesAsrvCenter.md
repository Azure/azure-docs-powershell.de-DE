---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 696c5812a4b8eece62261208c501727aa48c2262
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997387"
---
# <span data-ttu-id="f760e-101">New-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="f760e-101">New-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="f760e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f760e-102">SYNOPSIS</span></span>
<span data-ttu-id="f760e-103">Fügt einen vCenter Server hinzu, um geschützte Elemente zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="f760e-103">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="f760e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f760e-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount> -Port <Int32>
 -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f760e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f760e-105">DESCRIPTION</span></span>
<span data-ttu-id="f760e-106">Mit dem Cmdlet **New-AzRecoveryServicesAsrvCenter** wird ein vCenter Server hinzugefügt, in dem die geschützten Elemente erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="f760e-106">The **New-AzRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="f760e-107">Mit diesem Cmdlet wird der vCenter Server für die Ermittlung mit dem Konfigurationsserver registriert.</span><span class="sxs-lookup"><span data-stu-id="f760e-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="f760e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f760e-108">EXAMPLES</span></span>

### <span data-ttu-id="f760e-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f760e-109">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="f760e-110">Fügt einen vCenter Server hinzu, um geschützte Elemente zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="f760e-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="f760e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f760e-111">PARAMETERS</span></span>

### <span data-ttu-id="f760e-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="f760e-112">-Account</span></span>
<span data-ttu-id="f760e-113">Konto für Benutzeranmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="f760e-113">User login credential Account.</span></span>

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

### <span data-ttu-id="f760e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f760e-114">-DefaultProfile</span></span>
<span data-ttu-id="f760e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f760e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f760e-116">-Stoff</span><span class="sxs-lookup"><span data-stu-id="f760e-116">-Fabric</span></span>
<span data-ttu-id="f760e-117">ASR-Fabric, die dem Konfigurationsserver entspricht.</span><span class="sxs-lookup"><span data-stu-id="f760e-117">ASR fabric corresponding to the Configuration server.</span></span>

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

### <span data-ttu-id="f760e-118">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="f760e-118">-IpOrHostName</span></span>
<span data-ttu-id="f760e-119">IPv4-Adresse oder FQDN des vCenter-Servers.</span><span class="sxs-lookup"><span data-stu-id="f760e-119">IPv4 address or FQDN of the vCenter server.</span></span>

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

### <span data-ttu-id="f760e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f760e-120">-Name</span></span>
<span data-ttu-id="f760e-121">Ein Anzeigename für den vCenter Server.</span><span class="sxs-lookup"><span data-stu-id="f760e-121">A friendly name for the vCenter server.</span></span>

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

### <span data-ttu-id="f760e-122">-Port</span><span class="sxs-lookup"><span data-stu-id="f760e-122">-Port</span></span>
<span data-ttu-id="f760e-123">Der TCP-Port auf dem vCenter Server, der für die Erkennung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f760e-123">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="f760e-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f760e-124">-Confirm</span></span>
<span data-ttu-id="f760e-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f760e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f760e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f760e-126">-WhatIf</span></span>
<span data-ttu-id="f760e-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f760e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f760e-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f760e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f760e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f760e-129">CommonParameters</span></span>
<span data-ttu-id="f760e-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f760e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f760e-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f760e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f760e-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f760e-132">INPUTS</span></span>

### <span data-ttu-id="f760e-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="f760e-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="f760e-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f760e-134">OUTPUTS</span></span>

### <span data-ttu-id="f760e-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f760e-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f760e-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="f760e-136">NOTES</span></span>

## <span data-ttu-id="f760e-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f760e-137">RELATED LINKS</span></span>
