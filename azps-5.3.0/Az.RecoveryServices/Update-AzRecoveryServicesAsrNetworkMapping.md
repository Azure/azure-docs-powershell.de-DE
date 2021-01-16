---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 09e6cbbbae30d1a2e43d8292573f4bf45d9db461
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460868"
---
# <span data-ttu-id="226b2-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="226b2-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="226b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="226b2-102">SYNOPSIS</span></span>
<span data-ttu-id="226b2-103">Aktualisiert die angegebene Netzwerkzuordnung für die Azure-Websitewiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="226b2-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="226b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="226b2-104">SYNTAX</span></span>

### <span data-ttu-id="226b2-105">ByNetworkObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="226b2-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="226b2-106">ById</span><span class="sxs-lookup"><span data-stu-id="226b2-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="226b2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="226b2-107">DESCRIPTION</span></span>
<span data-ttu-id="226b2-108">Das **Cmdlet "Update-AzRecoveryServicesAsrNetworkMapping"** aktualisiert die angegebene Azure Site Recovery-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="226b2-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="226b2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="226b2-109">EXAMPLES</span></span>

### <span data-ttu-id="226b2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="226b2-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="226b2-111">Startet den Netzwerkzuordnungsvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="226b2-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="226b2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="226b2-112">PARAMETERS</span></span>

### <span data-ttu-id="226b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="226b2-113">-DefaultProfile</span></span>
<span data-ttu-id="226b2-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="226b2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="226b2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="226b2-115">-InputObject</span></span>
<span data-ttu-id="226b2-116">Eingabeobjekt: Gibt das ASR-Netzwerkzuordnungsobjekt an, das der zu aktualisierenden ASR-Netzwerkzuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="226b2-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="226b2-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="226b2-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="226b2-118">Gibt die Azure-Netzwerk-ID der Wiederherstellung für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="226b2-118">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="226b2-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="226b2-119">-RecoveryNetwork</span></span>
<span data-ttu-id="226b2-120">Gibt das Wiederherstellungsnetzwerkobjekt für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="226b2-120">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="226b2-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="226b2-121">-Confirm</span></span>
<span data-ttu-id="226b2-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="226b2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="226b2-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="226b2-123">-WhatIf</span></span>
<span data-ttu-id="226b2-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="226b2-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="226b2-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="226b2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="226b2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="226b2-126">CommonParameters</span></span>
<span data-ttu-id="226b2-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="226b2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="226b2-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="226b2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="226b2-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="226b2-129">INPUTS</span></span>

### <span data-ttu-id="226b2-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="226b2-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="226b2-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="226b2-131">OUTPUTS</span></span>

### <span data-ttu-id="226b2-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="226b2-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="226b2-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="226b2-133">NOTES</span></span>

## <span data-ttu-id="226b2-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="226b2-134">RELATED LINKS</span></span>
