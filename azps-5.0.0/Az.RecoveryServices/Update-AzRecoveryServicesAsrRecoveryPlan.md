---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 99c91f24bcc81ee6d6971b74779dfd116b90fdef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179375"
---
# <span data-ttu-id="6e8a7-101">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6e8a7-101">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="6e8a7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e8a7-102">SYNOPSIS</span></span>
<span data-ttu-id="6e8a7-103">Aktualisiert den Inhalt eines Azure Site Recovery-Plans.</span><span class="sxs-lookup"><span data-stu-id="6e8a7-103">Updates the contents of an Azure Site recovery plan.</span></span>

## <span data-ttu-id="6e8a7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e8a7-104">SYNTAX</span></span>

### <span data-ttu-id="6e8a7-105">ByRPObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="6e8a7-105">ByRPObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e8a7-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="6e8a7-106">ByRPFile</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e8a7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e8a7-107">DESCRIPTION</span></span>
<span data-ttu-id="6e8a7-108">Das Cmdlet **Update-AzRecoveryServicesAsrRecoveryPlan** aktualisiert den Inhalt eines Wiederherstellungsplans unter Verwendung des Inhalts des angegebenen ASR-Wiederherstellungsplan Objekts oder der JSON-Datei für die ASR-Wiederherstellungsplan Definition.</span><span class="sxs-lookup"><span data-stu-id="6e8a7-108">The **Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="6e8a7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e8a7-109">EXAMPLES</span></span>

### <span data-ttu-id="6e8a7-110">Beispiel 1: Aktualisieren eines Wiederherstellungsplans</span><span class="sxs-lookup"><span data-stu-id="6e8a7-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="6e8a7-111">Starten Sie den Vorgang zum Aktualisieren eines Wiederherstellungsplans mithilfe des Inhalts des angegebenen ASR-Wiederherstellungsplan Objekts, und geben Sie den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6e8a7-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6e8a7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e8a7-112">PARAMETERS</span></span>

### <span data-ttu-id="6e8a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e8a7-113">-DefaultProfile</span></span>
<span data-ttu-id="6e8a7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6e8a7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6e8a7-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6e8a7-115">-InputObject</span></span>
<span data-ttu-id="6e8a7-116">Eingabeobjekt für das Cmdlet: gibt ein ASR-Wiederherstellungsplan-Objekt an, dessen Inhalt zum Aktualisieren des Wiederherstellungsplans verwendet wird, auf den das Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="6e8a7-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

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

### <span data-ttu-id="6e8a7-117">-Path</span><span class="sxs-lookup"><span data-stu-id="6e8a7-117">-Path</span></span>
<span data-ttu-id="6e8a7-118">Gibt den Pfad der JSON-Datei für die Wiederherstellungsplan Definition an, mit der der Wiederherstellungsplan aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6e8a7-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

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

### <span data-ttu-id="6e8a7-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6e8a7-119">-Confirm</span></span>
<span data-ttu-id="6e8a7-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e8a7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e8a7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e8a7-121">-WhatIf</span></span>
<span data-ttu-id="6e8a7-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e8a7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e8a7-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e8a7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e8a7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e8a7-124">CommonParameters</span></span>
<span data-ttu-id="6e8a7-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e8a7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e8a7-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e8a7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e8a7-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e8a7-127">INPUTS</span></span>

### <span data-ttu-id="6e8a7-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6e8a7-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="6e8a7-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e8a7-129">OUTPUTS</span></span>

### <span data-ttu-id="6e8a7-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6e8a7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6e8a7-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e8a7-131">NOTES</span></span>

## <span data-ttu-id="6e8a7-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e8a7-132">RELATED LINKS</span></span>

[<span data-ttu-id="6e8a7-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6e8a7-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6e8a7-134">Neu – AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6e8a7-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6e8a7-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6e8a7-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)
