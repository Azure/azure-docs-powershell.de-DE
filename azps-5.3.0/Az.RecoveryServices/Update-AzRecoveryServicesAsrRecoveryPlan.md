---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 99c91f24bcc81ee6d6971b74779dfd116b90fdef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460867"
---
# <span data-ttu-id="6b92c-101">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6b92c-101">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="6b92c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b92c-102">SYNOPSIS</span></span>
<span data-ttu-id="6b92c-103">Aktualisiert den Inhalt eines Azure-Websitewiederherstellungsplans.</span><span class="sxs-lookup"><span data-stu-id="6b92c-103">Updates the contents of an Azure Site recovery plan.</span></span>

## <span data-ttu-id="6b92c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b92c-104">SYNTAX</span></span>

### <span data-ttu-id="6b92c-105">ByRPObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b92c-105">ByRPObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b92c-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="6b92c-106">ByRPFile</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b92c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b92c-107">DESCRIPTION</span></span>
<span data-ttu-id="6b92c-108">Das **Cmdlet "Update-AzRecoveryServicesAsrRecoveryPlan"** aktualisiert den Inhalt eines Wiederherstellungsplans mithilfe der Inhalte des angegebenen ASR-Wiederherstellungsplanobjekts oder der JSON-Datei mit der ASR-Wiederherstellungsplandefinition.</span><span class="sxs-lookup"><span data-stu-id="6b92c-108">The **Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="6b92c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6b92c-109">EXAMPLES</span></span>

### <span data-ttu-id="6b92c-110">Beispiel 1: Aktualisieren eines Wiederherstellungsplans</span><span class="sxs-lookup"><span data-stu-id="6b92c-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="6b92c-111">Starten Sie den Vorgang zum Aktualisieren eines Wiederherstellungsplans mithilfe des Inhalts des angegebenen ASR-Wiederherstellungsplanobjekts, und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="6b92c-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6b92c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b92c-112">PARAMETERS</span></span>

### <span data-ttu-id="6b92c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b92c-113">-DefaultProfile</span></span>
<span data-ttu-id="6b92c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b92c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6b92c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b92c-115">-InputObject</span></span>
<span data-ttu-id="6b92c-116">Eingabeobjekt für das Cmdlet: Gibt ein ASR-Wiederherstellungsplanobjekt an, dessen Inhalte zum Aktualisieren des Wiederherstellungsplans verwendet werden, auf den das Objekt verwiesen hat.</span><span class="sxs-lookup"><span data-stu-id="6b92c-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

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

### <span data-ttu-id="6b92c-117">-Path</span><span class="sxs-lookup"><span data-stu-id="6b92c-117">-Path</span></span>
<span data-ttu-id="6b92c-118">Gibt den Pfad der JSON-Datei mit der Wiederherstellungsplandefinition an, die zum Aktualisieren des Wiederherstellungsplans verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b92c-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

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

### <span data-ttu-id="6b92c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b92c-119">-Confirm</span></span>
<span data-ttu-id="6b92c-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b92c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b92c-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6b92c-121">-WhatIf</span></span>
<span data-ttu-id="6b92c-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b92c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b92c-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b92c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b92c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b92c-124">CommonParameters</span></span>
<span data-ttu-id="6b92c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b92c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b92c-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b92c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b92c-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6b92c-127">INPUTS</span></span>

### <span data-ttu-id="6b92c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6b92c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="6b92c-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6b92c-129">OUTPUTS</span></span>

### <span data-ttu-id="6b92c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="6b92c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6b92c-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6b92c-131">NOTES</span></span>

## <span data-ttu-id="6b92c-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6b92c-132">RELATED LINKS</span></span>

[<span data-ttu-id="6b92c-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6b92c-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6b92c-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6b92c-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6b92c-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6b92c-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)
