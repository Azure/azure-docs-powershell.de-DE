---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 6ff0031c5bb8571c69287968f984565daf58b530
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156505"
---
# <span data-ttu-id="192c3-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="192c3-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="192c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="192c3-102">SYNOPSIS</span></span>
<span data-ttu-id="192c3-103">Löscht die angegebene ASR-Replikationsrichtlinie aus dem Recovery Services-Tresor.</span><span class="sxs-lookup"><span data-stu-id="192c3-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="192c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="192c3-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="192c3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="192c3-105">DESCRIPTION</span></span>
<span data-ttu-id="192c3-106">Das **Cmdlet "Remove-AzRecoveryServicesAsrPolicy"** hat die angegebene Replikationsrichtlinie aus dem Tresor für Wiederherstellungsdienste gelöscht.</span><span class="sxs-lookup"><span data-stu-id="192c3-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="192c3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="192c3-107">EXAMPLES</span></span>

### <span data-ttu-id="192c3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="192c3-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="192c3-109">Startet das Löschen der angegebenen Replikationsrichtlinie und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="192c3-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="192c3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="192c3-110">PARAMETERS</span></span>

### <span data-ttu-id="192c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="192c3-111">-DefaultProfile</span></span>
<span data-ttu-id="192c3-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="192c3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="192c3-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="192c3-113">-InputObject</span></span>
<span data-ttu-id="192c3-114">Das Eingabeobjekt für das Cmdlet: Das ASR-Replikationsrichtlinienobjekt, das der zu löschende Replikationsrichtlinie entspricht.</span><span class="sxs-lookup"><span data-stu-id="192c3-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="192c3-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="192c3-115">-Confirm</span></span>
<span data-ttu-id="192c3-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="192c3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="192c3-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="192c3-117">-WhatIf</span></span>
<span data-ttu-id="192c3-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="192c3-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="192c3-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="192c3-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="192c3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="192c3-120">CommonParameters</span></span>
<span data-ttu-id="192c3-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="192c3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="192c3-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="192c3-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="192c3-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="192c3-123">INPUTS</span></span>

### <span data-ttu-id="192c3-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="192c3-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="192c3-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="192c3-125">OUTPUTS</span></span>

### <span data-ttu-id="192c3-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="192c3-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="192c3-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="192c3-127">NOTES</span></span>

## <span data-ttu-id="192c3-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="192c3-128">RELATED LINKS</span></span>

[<span data-ttu-id="192c3-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="192c3-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="192c3-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="192c3-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
