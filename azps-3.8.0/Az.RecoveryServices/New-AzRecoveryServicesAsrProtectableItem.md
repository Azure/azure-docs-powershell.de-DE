---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 5fa9ca0cd11213a2d44f56850eec77ecb8020311
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004903"
---
# <span data-ttu-id="4e6b1-101">New-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4e6b1-101">New-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="4e6b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e6b1-102">SYNOPSIS</span></span>
<span data-ttu-id="4e6b1-103">Hinzufügen (ermitteln) eines physikalischen Servers zur Liste der geschützten Elemente</span><span class="sxs-lookup"><span data-stu-id="4e6b1-103">Add(Discover) a physical server to the list of protectable items.</span></span>

## <span data-ttu-id="4e6b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e6b1-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer> -FriendlyName <String>
 -IPAddress <String> -OSType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e6b1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e6b1-105">DESCRIPTION</span></span>
<span data-ttu-id="4e6b1-106">Das **New-AzRecoveryServicesAsrProtectableItem** fügt ein neues geschütztes Element zur Liste der ermittelten geschützten Elemente in einem Schutzcontainer innerhalb eines ASR-Fabrics hinzu (gilt nur für den VMware Fabric-Typ).</span><span class="sxs-lookup"><span data-stu-id="4e6b1-106">The **New-AzRecoveryServicesAsrProtectableItem** adds a new protectable item to the list of discovered protectable items in a protection container within an ASR fabric (applicable only for the VMware fabric type).</span></span>

## <span data-ttu-id="4e6b1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e6b1-107">EXAMPLES</span></span>

### <span data-ttu-id="4e6b1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4e6b1-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $pc -Name $name -IPAddress $ipaddresss -OSType $OsType
```

<span data-ttu-id="4e6b1-109">Hinzufügen oder entdecken des neuen Azure Recovery Service-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4e6b1-109">Add or Discover new Azure Recovery Service ProtectableItem.</span></span>

## <span data-ttu-id="4e6b1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e6b1-110">PARAMETERS</span></span>

### <span data-ttu-id="4e6b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e6b1-111">-DefaultProfile</span></span>
<span data-ttu-id="4e6b1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e6b1-113">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4e6b1-113">-FriendlyName</span></span>
<span data-ttu-id="4e6b1-114">Anzeigename für das zu schützende Element.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-114">Friendly name for the protectable item.</span></span>

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

### <span data-ttu-id="4e6b1-115">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="4e6b1-115">-IPAddress</span></span>
<span data-ttu-id="4e6b1-116">Die IP-Adresse des geschützten Elements.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-116">IP address of the protectable item.</span></span>

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

### <span data-ttu-id="4e6b1-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="4e6b1-117">-OSType</span></span>
<span data-ttu-id="4e6b1-118">Betriebssystemtyp (Windows/Linux) des geschützten Elements.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-118">Operating System type (Windows/Linux) of the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6b1-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4e6b1-119">-ProtectionContainer</span></span>
<span data-ttu-id="4e6b1-120">ASR-Schutzcontainer Objekt, dem das zu schützende Element hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-120">ASR Protection container object to which the protectable item should be added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e6b1-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4e6b1-121">-Confirm</span></span>
<span data-ttu-id="4e6b1-122">Zur Bestätigung bestätigen, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-122">Prompt for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e6b1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e6b1-123">-WhatIf</span></span>
<span data-ttu-id="4e6b1-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e6b1-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e6b1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e6b1-126">CommonParameters</span></span>
<span data-ttu-id="4e6b1-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e6b1-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e6b1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e6b1-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e6b1-129">INPUTS</span></span>

### <span data-ttu-id="4e6b1-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4e6b1-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="4e6b1-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e6b1-131">OUTPUTS</span></span>

### <span data-ttu-id="4e6b1-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4e6b1-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4e6b1-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e6b1-133">NOTES</span></span>

## <span data-ttu-id="4e6b1-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e6b1-134">RELATED LINKS</span></span>
