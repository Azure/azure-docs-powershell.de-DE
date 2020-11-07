---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a358e38dcba9c0f7fb4bae0c1b1af28845a3851b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659848"
---
# <span data-ttu-id="f3d96-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f3d96-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="f3d96-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3d96-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d96-103">Löscht die angegebene ASR-Replikationsrichtlinie aus dem Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="f3d96-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="f3d96-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3d96-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3d96-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3d96-105">DESCRIPTION</span></span>
<span data-ttu-id="f3d96-106">Das Cmdlet " **Remove-AzRecoveryServicesAsrPolicy** " hat die angegebene Replikationsrichtlinie aus dem Vault für Wiederherstellungsdienste gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f3d96-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="f3d96-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3d96-107">EXAMPLES</span></span>

### <span data-ttu-id="f3d96-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f3d96-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="f3d96-109">Startet das Löschen der angegebenen Replikationsrichtlinie und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f3d96-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f3d96-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3d96-110">PARAMETERS</span></span>

### <span data-ttu-id="f3d96-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d96-111">-DefaultProfile</span></span>
<span data-ttu-id="f3d96-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3d96-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f3d96-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f3d96-113">-InputObject</span></span>
<span data-ttu-id="f3d96-114">Das Eingabeobjekt für das Cmdlet: das ASR-Replikationsrichtlinien Objekt, das der zu löschenden Replikationsrichtlinie entspricht.</span><span class="sxs-lookup"><span data-stu-id="f3d96-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="f3d96-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f3d96-115">-Confirm</span></span>
<span data-ttu-id="f3d96-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f3d96-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3d96-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3d96-117">-WhatIf</span></span>
<span data-ttu-id="f3d96-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f3d96-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3d96-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3d96-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3d96-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d96-120">CommonParameters</span></span>
<span data-ttu-id="f3d96-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3d96-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d96-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3d96-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d96-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3d96-123">INPUTS</span></span>

### <span data-ttu-id="f3d96-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="f3d96-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="f3d96-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3d96-125">OUTPUTS</span></span>

### <span data-ttu-id="f3d96-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f3d96-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f3d96-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3d96-127">NOTES</span></span>

## <span data-ttu-id="f3d96-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3d96-128">RELATED LINKS</span></span>

[<span data-ttu-id="f3d96-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f3d96-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="f3d96-130">Neu – AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f3d96-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
