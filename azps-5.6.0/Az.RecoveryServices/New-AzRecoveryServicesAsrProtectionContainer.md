---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 22ade5e749909683ff2de93065ccf458ab2ec73f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920971"
---
# <span data-ttu-id="8c2dc-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8c2dc-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="8c2dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c2dc-102">SYNOPSIS</span></span>
<span data-ttu-id="8c2dc-103">Erstellt einen Azure Site Recovery Protection-Container innerhalb der angegebenen Fabric.</span><span class="sxs-lookup"><span data-stu-id="8c2dc-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="8c2dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c2dc-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c2dc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c2dc-105">DESCRIPTION</span></span>
<span data-ttu-id="8c2dc-106">Das New-AzRecoveryServicesAsrProtectionContainer erstellt einen Schutzcontainer unter dem angegebenen Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="8c2dc-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="8c2dc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8c2dc-107">EXAMPLES</span></span>

### <span data-ttu-id="8c2dc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8c2dc-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="8c2dc-109">Startet die Erstellung des Schutzcontainers mit den angegebenen Parametern und gibt den ZUM Nachverfolgen des Vorgangs verwendeten ASR-Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="8c2dc-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8c2dc-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8c2dc-110">PARAMETERS</span></span>

### <span data-ttu-id="8c2dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c2dc-111">-DefaultProfile</span></span>
<span data-ttu-id="8c2dc-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c2dc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c2dc-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c2dc-113">-InputObject</span></span>
<span data-ttu-id="8c2dc-114">Erstellt den Replikationsschutzcontainer im angegebenen Eingabeobjekt (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="8c2dc-114">Creates the replication protection container in specified input Object (Azure Fabric).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c2dc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8c2dc-115">-Name</span></span>
<span data-ttu-id="8c2dc-116">Name des Schutzcontainers.</span><span class="sxs-lookup"><span data-stu-id="8c2dc-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="8c2dc-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8c2dc-117">-Confirm</span></span>
<span data-ttu-id="8c2dc-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c2dc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c2dc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c2dc-119">-WhatIf</span></span>
<span data-ttu-id="8c2dc-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c2dc-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c2dc-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c2dc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c2dc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c2dc-122">CommonParameters</span></span>
<span data-ttu-id="8c2dc-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c2dc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c2dc-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c2dc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c2dc-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8c2dc-125">INPUTS</span></span>

### <span data-ttu-id="8c2dc-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="8c2dc-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="8c2dc-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8c2dc-127">OUTPUTS</span></span>

### <span data-ttu-id="8c2dc-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="8c2dc-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8c2dc-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8c2dc-129">NOTES</span></span>

## <span data-ttu-id="8c2dc-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8c2dc-130">RELATED LINKS</span></span>
