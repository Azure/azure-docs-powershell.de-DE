---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 8973c3606c7c29c254650b3412275c1dfd7bf761
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502505"
---
# <span data-ttu-id="f8f5b-101">New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f8f5b-101">New-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="f8f5b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8f5b-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f5b-103">Hinzufügen (ermitteln) eines physikalischen Servers zur Liste der geschützten Elemente</span><span class="sxs-lookup"><span data-stu-id="f8f5b-103">Add(Discover) a physical server to the list of protectable items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8f5b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8f5b-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 -FriendlyName <String> -IPAddress <String> -OSType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8f5b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8f5b-105">DESCRIPTION</span></span>
<span data-ttu-id="f8f5b-106">Das **New-AzureRmRecoveryServicesAsrProtectableItem** fügt ein neues geschütztes Element zur Liste der ermittelten geschützten Elemente in einem Schutzcontainer innerhalb eines ASR-Fabrics hinzu (gilt nur für den VMware Fabric-Typ).</span><span class="sxs-lookup"><span data-stu-id="f8f5b-106">The **New-AzureRmRecoveryServicesAsrProtectableItem** adds a new protectable item to the list of discovered protectable items in a protection container within an ASR fabric (applicable only for the VMware fabric type).</span></span>

## <span data-ttu-id="f8f5b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8f5b-107">EXAMPLES</span></span>

### <span data-ttu-id="f8f5b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8f5b-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectableItem ProtectionContainer $pc -Name $name -IPAddress $ipaddresss -OSType $OsType
```

<span data-ttu-id="f8f5b-109">Hinzufügen oder entdecken des neuen Azure Recovery Service-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f8f5b-109">Add or Discover new Azure Recovery Service ProtectableItem.</span></span>

## <span data-ttu-id="f8f5b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8f5b-110">PARAMETERS</span></span>

### <span data-ttu-id="f8f5b-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8f5b-111">-Confirm</span></span>
<span data-ttu-id="f8f5b-112">Zur Bestätigung bestätigen, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8f5b-112">Prompt for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8f5b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8f5b-113">-DefaultProfile</span></span>
<span data-ttu-id="f8f5b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8f5b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8f5b-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f8f5b-115">-FriendlyName</span></span>
<span data-ttu-id="f8f5b-116">Anzeigename für das zu schützende Element.</span><span class="sxs-lookup"><span data-stu-id="f8f5b-116">Friendly name for the protectable item.</span></span>

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

### <span data-ttu-id="f8f5b-117">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="f8f5b-117">-IPAddress</span></span>
<span data-ttu-id="f8f5b-118">Die IP-Adresse des geschützten Elements.</span><span class="sxs-lookup"><span data-stu-id="f8f5b-118">IP address of the protectable item.</span></span>

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

### <span data-ttu-id="f8f5b-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="f8f5b-119">-OSType</span></span>
<span data-ttu-id="f8f5b-120">Betriebssystemtyp (Windows/Linux) des geschützten Elements.</span><span class="sxs-lookup"><span data-stu-id="f8f5b-120">Operating System type (Windows/Linux) of the protectable item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f5b-121">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f8f5b-121">-ProtectionContainer</span></span>
<span data-ttu-id="f8f5b-122">ASR-Schutzcontainer Objekt, dem das zu schützende Element hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8f5b-122">ASR Protection container object to which the protectable item should be added.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8f5b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8f5b-123">-WhatIf</span></span>
<span data-ttu-id="f8f5b-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8f5b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8f5b-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8f5b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8f5b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f5b-126">CommonParameters</span></span>
<span data-ttu-id="f8f5b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8f5b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f5b-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8f5b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f5b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8f5b-129">INPUTS</span></span>

### <span data-ttu-id="f8f5b-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f8f5b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="f8f5b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8f5b-131">OUTPUTS</span></span>

### <span data-ttu-id="f8f5b-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f8f5b-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f8f5b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8f5b-133">NOTES</span></span>

## <span data-ttu-id="f8f5b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8f5b-134">RELATED LINKS</span></span>
