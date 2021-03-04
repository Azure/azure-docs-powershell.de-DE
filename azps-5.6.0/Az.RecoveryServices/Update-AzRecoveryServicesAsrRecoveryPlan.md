---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b0780e4fb82a3e58e70f3a0bd64b5211ad07fd42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938496"
---
# <span data-ttu-id="c6cd6-101">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c6cd6-101">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="c6cd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="c6cd6-103">Aktualisiert den Inhalt eines Azure -Wiederherstellungsplans.</span><span class="sxs-lookup"><span data-stu-id="c6cd6-103">Updates the contents of an Azure Site recovery plan.</span></span>

## <span data-ttu-id="c6cd6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6cd6-104">SYNTAX</span></span>

### <span data-ttu-id="c6cd6-105">ByRPObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="c6cd6-105">ByRPObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6cd6-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="c6cd6-106">ByRPFile</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6cd6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6cd6-107">DESCRIPTION</span></span>
<span data-ttu-id="c6cd6-108">Das **Cmdlet Update-AzRecoveryServicesAsrRecoveryPlan** aktualisiert den Inhalt eines Wiederherstellungsplans mithilfe des Inhalts des angegebenen ASR-Wiederherstellungsplanobjekts oder der Jsondatei für die ASR-Wiederherstellungsplandefinition.</span><span class="sxs-lookup"><span data-stu-id="c6cd6-108">The **Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="c6cd6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c6cd6-109">EXAMPLES</span></span>

### <span data-ttu-id="c6cd6-110">Beispiel 1: Aktualisieren eines Wiederherstellungsplans</span><span class="sxs-lookup"><span data-stu-id="c6cd6-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="c6cd6-111">Starten Sie den Vorgang zum Aktualisieren eines Wiederherstellungsplans mithilfe des Inhalts des angegebenen ASR-Wiederherstellungsplanobjekts und gibt den ZUM Nachverfolgen des Vorgangs verwendeten ASR-Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="c6cd6-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c6cd6-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c6cd6-112">PARAMETERS</span></span>

### <span data-ttu-id="c6cd6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6cd6-113">-DefaultProfile</span></span>
<span data-ttu-id="c6cd6-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6cd6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c6cd6-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6cd6-115">-InputObject</span></span>
<span data-ttu-id="c6cd6-116">Eingabeobjekt für das Cmdlet: Gibt ein ASR-Wiederherstellungsplanobjekt an, dessen Inhalt zum Aktualisieren des vom -Objekt bezeichneten Wiederherstellungsplans verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6cd6-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6cd6-117">-Path</span><span class="sxs-lookup"><span data-stu-id="c6cd6-117">-Path</span></span>
<span data-ttu-id="c6cd6-118">Gibt den Pfad der Jsondatei für die Wiederherstellungsplandefinition an, die zum Aktualisieren des Wiederherstellungsplans verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6cd6-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6cd6-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c6cd6-119">-Confirm</span></span>
<span data-ttu-id="c6cd6-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6cd6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6cd6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6cd6-121">-WhatIf</span></span>
<span data-ttu-id="c6cd6-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6cd6-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6cd6-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6cd6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6cd6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6cd6-124">CommonParameters</span></span>
<span data-ttu-id="c6cd6-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6cd6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6cd6-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6cd6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6cd6-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c6cd6-127">INPUTS</span></span>

### <span data-ttu-id="c6cd6-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c6cd6-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="c6cd6-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c6cd6-129">OUTPUTS</span></span>

### <span data-ttu-id="c6cd6-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="c6cd6-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c6cd6-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c6cd6-131">NOTES</span></span>

## <span data-ttu-id="c6cd6-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c6cd6-132">RELATED LINKS</span></span>

[<span data-ttu-id="c6cd6-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c6cd6-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="c6cd6-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c6cd6-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="c6cd6-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c6cd6-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)
