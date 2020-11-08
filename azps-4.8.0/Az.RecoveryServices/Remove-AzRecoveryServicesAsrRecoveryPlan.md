---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 138fd84684fda149d66be85a0fabfbe4a2df0e52
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174454"
---
# <span data-ttu-id="87599-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="87599-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="87599-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87599-102">SYNOPSIS</span></span>
<span data-ttu-id="87599-103">Löscht den angegebenen ASR-Wiederherstellungsplan aus dem Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="87599-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="87599-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87599-104">SYNTAX</span></span>

### <span data-ttu-id="87599-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="87599-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87599-106">ByName</span><span class="sxs-lookup"><span data-stu-id="87599-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87599-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87599-107">DESCRIPTION</span></span>
<span data-ttu-id="87599-108">Das Cmdlet **Remove-AzRecoveryServicesAsrRecoveryPlan** löscht den angegebenen Wiederherstellungsplan aus dem Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="87599-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="87599-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87599-109">EXAMPLES</span></span>

### <span data-ttu-id="87599-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="87599-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="87599-111">Startet den Löschvorgang des angegebenen Wiederherstellungsplans und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="87599-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="87599-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="87599-112">PARAMETERS</span></span>

### <span data-ttu-id="87599-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87599-113">-DefaultProfile</span></span>
<span data-ttu-id="87599-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="87599-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="87599-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="87599-115">-InputObject</span></span>
<span data-ttu-id="87599-116">Das Eingabeobjekt für das Cmdlet: das ASR-Wiederherstellungsplan Objekt, das dem Wiederherstellungsplan entspricht, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="87599-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="87599-117">-Name</span><span class="sxs-lookup"><span data-stu-id="87599-117">-Name</span></span>
<span data-ttu-id="87599-118">Gibt den Namen des Wiederherstellungsplans an, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="87599-118">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="87599-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="87599-119">-Confirm</span></span>
<span data-ttu-id="87599-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87599-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87599-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87599-121">-WhatIf</span></span>
<span data-ttu-id="87599-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87599-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87599-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87599-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87599-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87599-124">CommonParameters</span></span>
<span data-ttu-id="87599-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87599-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87599-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87599-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87599-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87599-127">INPUTS</span></span>

### <span data-ttu-id="87599-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="87599-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="87599-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87599-129">OUTPUTS</span></span>

### <span data-ttu-id="87599-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="87599-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="87599-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="87599-131">NOTES</span></span>

## <span data-ttu-id="87599-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87599-132">RELATED LINKS</span></span>

[<span data-ttu-id="87599-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="87599-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="87599-134">Neu – AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="87599-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="87599-135">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="87599-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


