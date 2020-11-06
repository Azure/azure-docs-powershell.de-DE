---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 1d298a543071c879e2279734247febba00b8da21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476665"
---
# <span data-ttu-id="f47a5-101">New-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="f47a5-101">New-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="f47a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f47a5-102">SYNOPSIS</span></span>
<span data-ttu-id="f47a5-103">Fügt einen vCenter Server hinzu, um geschützte Elemente zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="f47a5-103">Adds a vCenter server to discover protectable items from.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f47a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f47a5-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount>
 -Port <Int32> -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f47a5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f47a5-105">DESCRIPTION</span></span>
<span data-ttu-id="f47a5-106">Mit dem Cmdlet **New-AzureRmRecoveryServicesAsrvCenter** wird ein vCenter Server hinzugefügt, in dem die geschützten Elemente erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="f47a5-106">The **New-AzureRmRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="f47a5-107">Mit diesem Cmdlet wird der vCenter Server für die Ermittlung mit dem Konfigurationsserver registriert.</span><span class="sxs-lookup"><span data-stu-id="f47a5-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="f47a5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f47a5-108">EXAMPLES</span></span>

### <span data-ttu-id="f47a5-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f47a5-109">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="f47a5-110">Fügt einen vCenter Server hinzu, um geschützte Elemente zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="f47a5-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="f47a5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f47a5-111">PARAMETERS</span></span>

### <span data-ttu-id="f47a5-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="f47a5-112">-Account</span></span>
<span data-ttu-id="f47a5-113">Benutzer-Login-creadential-Konto.</span><span class="sxs-lookup"><span data-stu-id="f47a5-113">User login creadential Account.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f47a5-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f47a5-114">-Confirm</span></span>
<span data-ttu-id="f47a5-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f47a5-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f47a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f47a5-116">-DefaultProfile</span></span>
<span data-ttu-id="f47a5-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f47a5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f47a5-118">-Stoff</span><span class="sxs-lookup"><span data-stu-id="f47a5-118">-Fabric</span></span>
<span data-ttu-id="f47a5-119">ASR-Fabric, die dem Konfigurationsserver entspricht.</span><span class="sxs-lookup"><span data-stu-id="f47a5-119">ASR fabric corresponding to the Configuration server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f47a5-120">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="f47a5-120">-IpOrHostName</span></span>
<span data-ttu-id="f47a5-121">IPv4-Adresse oder FQDN des vCenter-Servers.</span><span class="sxs-lookup"><span data-stu-id="f47a5-121">IPv4 address or FQDN of the vCenter server.</span></span>

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

### <span data-ttu-id="f47a5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f47a5-122">-Name</span></span>
<span data-ttu-id="f47a5-123">Ein Anzeigename für den vCenter Server.</span><span class="sxs-lookup"><span data-stu-id="f47a5-123">A friendly name for the vCenter server.</span></span>

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

### <span data-ttu-id="f47a5-124">-Port</span><span class="sxs-lookup"><span data-stu-id="f47a5-124">-Port</span></span>
<span data-ttu-id="f47a5-125">Der TCP-Port auf dem vCenter Server, der für die Erkennung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f47a5-125">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f47a5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f47a5-126">-WhatIf</span></span>
<span data-ttu-id="f47a5-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f47a5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f47a5-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f47a5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f47a5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f47a5-129">CommonParameters</span></span>
<span data-ttu-id="f47a5-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f47a5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f47a5-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f47a5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f47a5-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f47a5-132">INPUTS</span></span>

### <span data-ttu-id="f47a5-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="f47a5-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="f47a5-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f47a5-134">OUTPUTS</span></span>

### <span data-ttu-id="f47a5-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f47a5-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f47a5-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="f47a5-136">NOTES</span></span>

## <span data-ttu-id="f47a5-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f47a5-137">RELATED LINKS</span></span>
