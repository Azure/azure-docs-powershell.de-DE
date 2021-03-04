---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 6041973d4bab91310ed213d461cf97db9cc5e720
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940016"
---
# <span data-ttu-id="dd583-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="dd583-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="dd583-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd583-102">SYNOPSIS</span></span>
<span data-ttu-id="dd583-103">Aktualisiert die angegebene Azure-Websitewiederherstellungsnetzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="dd583-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="dd583-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd583-104">SYNTAX</span></span>

### <span data-ttu-id="dd583-105">ByNetworkObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd583-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd583-106">ById</span><span class="sxs-lookup"><span data-stu-id="dd583-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd583-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd583-107">DESCRIPTION</span></span>
<span data-ttu-id="dd583-108">Das **Cmdlet Update-AzRecoveryServicesAsrNetworkMapping** aktualisiert die angegebene Azure Site Recovery-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="dd583-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="dd583-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dd583-109">EXAMPLES</span></span>

### <span data-ttu-id="dd583-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dd583-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="dd583-111">Startet den Aktualisierungsnetzwerkzuordnungsvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd583-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="dd583-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dd583-112">PARAMETERS</span></span>

### <span data-ttu-id="dd583-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd583-113">-DefaultProfile</span></span>
<span data-ttu-id="dd583-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd583-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="dd583-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd583-115">-InputObject</span></span>
<span data-ttu-id="dd583-116">Eingabeobjekt: Gibt das ASR-Netzwerkzuordnungsobjekt an, das der zu aktualisierenden ASR-Netzwerkzuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="dd583-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="dd583-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="dd583-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="dd583-118">Gibt die Wiederherstellungs-Azure-Netzwerk-ID für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="dd583-118">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="dd583-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="dd583-119">-RecoveryNetwork</span></span>
<span data-ttu-id="dd583-120">Gibt das Wiederherstellungsnetzwerkobjekt für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="dd583-120">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="dd583-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd583-121">-Confirm</span></span>
<span data-ttu-id="dd583-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd583-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd583-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd583-123">-WhatIf</span></span>
<span data-ttu-id="dd583-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd583-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd583-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd583-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd583-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd583-126">CommonParameters</span></span>
<span data-ttu-id="dd583-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd583-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd583-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd583-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd583-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dd583-129">INPUTS</span></span>

### <span data-ttu-id="dd583-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="dd583-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="dd583-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dd583-131">OUTPUTS</span></span>

### <span data-ttu-id="dd583-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="dd583-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dd583-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dd583-133">NOTES</span></span>

## <span data-ttu-id="dd583-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dd583-134">RELATED LINKS</span></span>
