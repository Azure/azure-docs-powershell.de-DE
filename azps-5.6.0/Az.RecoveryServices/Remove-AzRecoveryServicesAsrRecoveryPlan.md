---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 96c50c812dcb73c92dc3704e576bfc45fbf21bba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919235"
---
# <span data-ttu-id="94424-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="94424-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="94424-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94424-102">SYNOPSIS</span></span>
<span data-ttu-id="94424-103">Löscht den angegebenen ASR-Wiederherstellungsplan aus dem Recovery Services-Tresor.</span><span class="sxs-lookup"><span data-stu-id="94424-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="94424-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94424-104">SYNTAX</span></span>

### <span data-ttu-id="94424-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="94424-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94424-106">ByName</span><span class="sxs-lookup"><span data-stu-id="94424-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94424-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94424-107">DESCRIPTION</span></span>
<span data-ttu-id="94424-108">Das **Cmdlet Remove-AzRecoveryServicesAsrRecoveryPlan** löscht den angegebenen Wiederherstellungsplan aus dem Recovery Services-Tresor.</span><span class="sxs-lookup"><span data-stu-id="94424-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="94424-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="94424-109">EXAMPLES</span></span>

### <span data-ttu-id="94424-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="94424-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="94424-111">Startet das Löschen des angegebenen Wiederherstellungsplans und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="94424-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="94424-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="94424-112">PARAMETERS</span></span>

### <span data-ttu-id="94424-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94424-113">-DefaultProfile</span></span>
<span data-ttu-id="94424-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94424-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="94424-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94424-115">-InputObject</span></span>
<span data-ttu-id="94424-116">Das Eingabeobjekt für das Cmdlet: Das ASR-Wiederherstellungsplanobjekt, das dem zu löschende Wiederherstellungsplan entspricht.</span><span class="sxs-lookup"><span data-stu-id="94424-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94424-117">-Name</span><span class="sxs-lookup"><span data-stu-id="94424-117">-Name</span></span>
<span data-ttu-id="94424-118">Gibt den Namen des wie zu löschenden Wiederherstellungsplans an.</span><span class="sxs-lookup"><span data-stu-id="94424-118">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94424-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="94424-119">-Confirm</span></span>
<span data-ttu-id="94424-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="94424-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94424-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94424-121">-WhatIf</span></span>
<span data-ttu-id="94424-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94424-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94424-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94424-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94424-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94424-124">CommonParameters</span></span>
<span data-ttu-id="94424-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94424-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94424-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94424-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94424-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="94424-127">INPUTS</span></span>

### <span data-ttu-id="94424-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="94424-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="94424-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="94424-129">OUTPUTS</span></span>

### <span data-ttu-id="94424-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="94424-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="94424-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="94424-131">NOTES</span></span>

## <span data-ttu-id="94424-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="94424-132">RELATED LINKS</span></span>

[<span data-ttu-id="94424-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="94424-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="94424-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="94424-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="94424-135">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="94424-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


